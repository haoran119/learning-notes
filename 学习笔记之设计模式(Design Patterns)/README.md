# 学习笔记之设计模式(Design Patterns)

* [学习笔记之设计模式 | 菜鸟教程 - 浩然119 - 博客园 (cnblogs.com)](https://www.cnblogs.com/pegasus923/p/8075546.html)
* [设计模式总结 - chenssy - 博客园 (cnblogs.com)](https://www.cnblogs.com/chenssy/p/3357683.html#rd)
* [【硬核】23种设计模式娓娓道来，助你优雅的编写出漂亮代码！ (qq.com)](https://mp.weixin.qq.com/s/oExtFRkj6zLoCxtLokNZrQ)
    * 总体来说设计模式分为三大类：
        * 创建型模式：工厂方法模式、抽象工厂模式、单例模式、建造者模式、原型模式。
        * 结构型模式：适配器模式、装饰器模式、代理模式、外观模式、桥接模式、组合模式、享元模式。
        * 行为型模式：策略模式、模板方法模式、观察者模式、迭代子模式、责任链模式、命令模式、备忘录模式、状态模式、访问者模式、中介者模式、解释器模式。
* [经典永不过时！重温设计模式 (qq.com)](https://mp.weixin.qq.com/s/i32AmhApR0jjAu2a8LZX7w)
    * [经典永不过时！重温设计模式 (qq.com)](https://mp.weixin.qq.com/s/EzYsYkAw-vs1bABvdfZKHA)

## [Creational Pattern 创建型模式](https://en.wikipedia.org/wiki/Creational_pattern)

* In software engineering, creational design patterns are design patterns that deal with object creation mechanisms, trying to create objects in a manner suitable to the situation. The basic form of object creation could result in design problems or in added complexity to the design. Creational design patterns solve this problem by somehow controlling this object creation.

### [Singleton pattern](https://en.wikipedia.org/wiki/Singleton_pattern)

* In software engineering, the singleton pattern is a software design pattern that restricts the instantiation of a class to a singular instance. One of the well-known "Gang of Four" design patterns, which describe how to solve recurring problems in object-oriented software,[1] the pattern is useful when exactly one object is needed to coordinate actions across a system.
* More specifically, the singleton pattern allows objects to:[2]
    * Ensure they only have one instance
    * Provide easy access to that instance
    * Control their instantiation (for example, hiding the constructors of a class)
* The term comes from the mathematical concept of a singleton.
* [Design Patterns: Singleton in C++](https://refactoring.guru/design-patterns/singleton/cpp/example#example-1)
* [Thread-Safe Initialization of a Singleton - ModernesCpp.com](https://www.modernescpp.com/index.php/thread-safe-initialization-of-a-singleton)
    * Guarantees of the C++ runtime
        * I already presented the details to the thread-safe initialization of variables in the post [Thread-safe initialization of data](https://www.modernescpp.com/index.php/thread-safe-initialization-of-data).
        * Meyers Singleton
            * The beauty of the Meyers Singleton in C++11 is that it's automatically thread-safe. That is guaranteed by the standard: Static variables with block scope. The Meyers Singleton is a static variable with block scope, so we are done. It's still left to rewrite the program for four threads.
            ```c++
            // singletonMeyers.cpp

            #include <chrono>
            #include <iostream>
            #include <future>

            constexpr auto tenMill= 10000000;

            class MySingleton{
            public:
              static MySingleton& getInstance(){
                static MySingleton instance;
                // volatile int dummy{};
                return instance;
              }
            private:
              MySingleton()= default;
              ~MySingleton()= default;
              MySingleton(const MySingleton&)= delete;
              MySingleton& operator=(const MySingleton&)= delete;

            };

            std::chrono::duration<double> getTime(){

              auto begin= std::chrono::system_clock::now();
              for ( size_t i= 0; i <= tenMill; ++i){
                  MySingleton::getInstance();
              }
              return std::chrono::system_clock::now() - begin;

            };

            int main(){

                auto fut1= std::async(std::launch::async,getTime);
                auto fut2= std::async(std::launch::async,getTime);
                auto fut3= std::async(std::launch::async,getTime);
                auto fut4= std::async(std::launch::async,getTime);

                auto total= fut1.get() + fut2.get() + fut3.get() + fut4.get();

                std::cout << total.count() << std::endl;

            }
            ```
        * The function std::call_once and the flag std::once_flag
            * You can use the function std::call_once to register a callable which will be executed exactly once. The flag std::call_once in the following implementation guarantees that the singleton will be thread-safe initialized.
            ```c++
            // singletonCallOnce.cpp

            #include <chrono>
            #include <iostream>
            #include <future>
            #include <mutex>
            #include <thread>

            constexpr auto tenMill= 10000000;

            class MySingleton{
            public:
              static MySingleton& getInstance(){
                std::call_once(initInstanceFlag, &MySingleton::initSingleton);
                // volatile int dummy{};
                return *instance;
              }
            private:
              MySingleton()= default;
              ~MySingleton()= default;
              MySingleton(const MySingleton&)= delete;
              MySingleton& operator=(const MySingleton&)= delete;

              static MySingleton* instance;
              static std::once_flag initInstanceFlag;

              static void initSingleton(){
                instance= new MySingleton;
              }
            };

            MySingleton* MySingleton::instance= nullptr;
            std::once_flag MySingleton::initInstanceFlag;

            std::chrono::duration<double> getTime(){

              auto begin= std::chrono::system_clock::now();
              for ( size_t i= 0; i <= tenMill; ++i){
                  MySingleton::getInstance();
              }
              return std::chrono::system_clock::now() - begin;

            };

            int main(){

                auto fut1= std::async(std::launch::async,getTime);
                auto fut2= std::async(std::launch::async,getTime);
                auto fut3= std::async(std::launch::async,getTime);
                auto fut4= std::async(std::launch::async,getTime);

                auto total= fut1.get() + fut2.get() + fut3.get() + fut4.get();

                std::cout << total.count() << std::endl;

            }
            ```
        * Lock
            * The mutex wrapped in a lock guarantees that the singleton will be thread-safe initialized.
            ```c++
            // singletonLock.cpp

            #include <chrono>
            #include <iostream>
            #include <future>
            #include <mutex>

            constexpr auto tenMill= 10000000;

            std::mutex myMutex;

            class MySingleton{
            public:
              static MySingleton& getInstance(){
                std::lock_guard<std::mutex> myLock(myMutex);
                if ( !instance ){
                    instance= new MySingleton();
                }
                // volatile int dummy{};
                return *instance;
              }
            private:
              MySingleton()= default;
              ~MySingleton()= default;
              MySingleton(const MySingleton&)= delete;
              MySingleton& operator=(const MySingleton&)= delete;

              static MySingleton* instance;
            };


            MySingleton* MySingleton::instance= nullptr;

            std::chrono::duration<double> getTime(){

              auto begin= std::chrono::system_clock::now();
              for ( size_t i= 0; i <= tenMill; ++i){
                   MySingleton::getInstance();
              }
              return std::chrono::system_clock::now() - begin;

            };

            int main(){

                auto fut1= std::async(std::launch::async,getTime);
                auto fut2= std::async(std::launch::async,getTime);
                auto fut3= std::async(std::launch::async,getTime);
                auto fut4= std::async(std::launch::async,getTime);

                auto total= fut1.get() + fut2.get() + fut3.get() + fut4.get();

                std::cout << total.count() << std::endl;
            }
            ```
        * Atomic variables
            * With atomic variables, my job becomes extremely challenging. Now I have to use the [C++ memory model](https://www.modernescpp.com/index.php/c-memory-model). I base my implementation on the well-known [double-checked locking pattern](https://www.modernescpp.com/index.php/thread-safe-initialization-of-data).
            * Sequential consistency
                * The handle to the singleton is atomic. Because I didn't specify the C++ memory model the default applies: [Sequential consistency](https://www.modernescpp.com/index.php/sequential-consistency).
                ```c++
                // singletonAcquireRelease.cpp

                #include <atomic>
                #include <iostream>
                #include <future>
                #include <mutex>
                #include <thread>

                constexpr auto tenMill= 10000000;

                class MySingleton{
                public:
                  static MySingleton* getInstance(){
                    MySingleton* sin= instance.load();
                    if ( !sin ){
                      std::lock_guard<std::mutex> myLock(myMutex);
                      sin= instance.load();
                      if( !sin ){
                        sin= new MySingleton();
                        instance.store(sin);
                      }
                    }   
                    // volatile int dummy{};
                    return sin;
                  }
                private:
                  MySingleton()= default;
                  ~MySingleton()= default;
                  MySingleton(const MySingleton&)= delete;
                  MySingleton& operator=(const MySingleton&)= delete;

                  static std::atomic<MySingleton*> instance;
                  static std::mutex myMutex;
                };


                std::atomic<MySingleton*> MySingleton::instance;
                std::mutex MySingleton::myMutex;

                std::chrono::duration<double> getTime(){

                  auto begin= std::chrono::system_clock::now();
                  for ( size_t i= 0; i <= tenMill; ++i){
                       MySingleton::getInstance();
                  }
                  return std::chrono::system_clock::now() - begin;

                };


                int main(){

                    auto fut1= std::async(std::launch::async,getTime);
                    auto fut2= std::async(std::launch::async,getTime);
                    auto fut3= std::async(std::launch::async,getTime);
                    auto fut4= std::async(std::launch::async,getTime);

                    auto total= fut1.get() + fut2.get() + fut3.get() + fut4.get();

                    std::cout << total.count() << std::endl;

                }
                ```
            * Acquire-release Semantic
                * The reading of the singleton (line 14) is an acquire operation, the writing a release operation (line 20). Because both operations take place on the same atomic I don't need sequential consistency. The C++ standard guarantees that an acquire operation synchronizes with a release operation on the same atomic. These conditions hold in this case therefore I can weaken the C++ memory model in line 14 and 20. [Acquire-release semantic](https://www.modernescpp.com/index.php/acquire-release-semantic) is sufficient.
                ```c++
                // singletonAcquireRelease.cpp

                #include <atomic>
                #include <iostream>
                #include <future>
                #include <mutex>
                #include <thread>

                constexpr auto tenMill= 10000000;

                class MySingleton{
                public:
                  static MySingleton* getInstance(){
                    MySingleton* sin= instance.load(std::memory_order_acquire);
                    if ( !sin ){
                      std::lock_guard<std::mutex> myLock(myMutex);
                      sin= instance.load(std::memory_order_relaxed);
                      if( !sin ){
                        sin= new MySingleton();
                        instance.store(sin,std::memory_order_release);
                      }
                    }   
                    // volatile int dummy{};
                    return sin;
                  }
                private:
                  MySingleton()= default;
                  ~MySingleton()= default;
                  MySingleton(const MySingleton&)= delete;
                  MySingleton& operator=(const MySingleton&)= delete;

                  static std::atomic<MySingleton*> instance;
                  static std::mutex myMutex;
                };


                std::atomic<MySingleton*> MySingleton::instance;
                std::mutex MySingleton::myMutex;

                std::chrono::duration<double> getTime(){

                  auto begin= std::chrono::system_clock::now();
                  for ( size_t i= 0; i <= tenMill; ++i){
                       MySingleton::getInstance();
                  }
                  return std::chrono::system_clock::now() - begin;

                };


                int main(){

                    auto fut1= std::async(std::launch::async,getTime);
                    auto fut2= std::async(std::launch::async,getTime);
                    auto fut3= std::async(std::launch::async,getTime);
                    auto fut4= std::async(std::launch::async,getTime);

                    auto total= fut1.get() + fut2.get() + fut3.get() + fut4.get();

                    std::cout << total.count() << std::endl;

                }
                ```
* [简约不简单的单例模式 (qq.com)](https://mp.weixin.qq.com/s/HmgUhWeXuim2LxZStuHPOw)
* [一个单例还能写出花来吗？ (qq.com)](https://mp.weixin.qq.com/s/0n4TKGbK2UrKarutOxFd7g)

### [Factory method pattern](https://en.wikipedia.org/wiki/Factory_method_pattern)

* [Factory Method in C++ / Design Patterns](https://refactoring.guru/design-patterns/factory-method/cpp/example#example-0)
* [漫画：设计模式之 “工厂模式” (qq.com)](https://mp.weixin.qq.com/s/lFhWPx9h3DCZQ62xxLg1_g)

## [Structural Pattern 结构型模式](https://en.wikipedia.org/wiki/Structural_pattern)

* In software engineering, structural design patterns are design patterns that ease the design by identifying a simple way to realize relationships among entities.
* [详解设计模式之结构型模式（上）](https://mp.weixin.qq.com/s/0PTiheUOw3FKJ6kKFZte-Q)
* [漫画设计模式：什么是 “装饰器模式” ？ (qq.com)](https://mp.weixin.qq.com/s/mz9rJELjcWlTv4LFzmKmTA)
* [漫画：设计模式之 “外观模式” (qq.com)](https://mp.weixin.qq.com/s/b2N4kkX4_KPffl7Kt5x4iA)
* [了解组合模式](https://mp.weixin.qq.com/s/o9kXMnu2pygrvVy51s-Qiw)

## [Behavioral Pattern 行为型模式](https://en.wikipedia.org/wiki/Behavioral_pattern)

* In software engineering, behavioral design patterns are design patterns that identify common communication patterns among objects. By doing so, these patterns increase flexibility in carrying out communication.
* [还在用 if else？试试策略模式吧！](https://mp.weixin.qq.com/s/VGoXu-QAuBL-Y892TFSNng)
* [别再用if-else了，用注解去代替他吧](https://mp.weixin.qq.com/s/7mr1F6ujFR8659bhUfDeJw)
    * 经常在网上看到一些名为“别再if-else走天下了”，“教你干掉if-else”等之类的文章，大部分都会讲到用策略模式去代替if-else。策略模式实现的方式也大同小异。主要是定义统一行为（接口或抽象类），并实现不同策略下的处理逻辑（对应实现类）。客户端使用时自己选择相应的处理类，利用工厂或其他方式。
    * 本文要说的是用注解实现策略模式的方式，以及一些注意点。
* [if-else嵌套太深？设计模式搞定！](https://mp.weixin.qq.com/s/-MuBaAIlbm6-xUCY7LkLpg)
    * 责任链模式，顾名思义，就是用来处理相关事务责任的一条执行链，执行链上有多个节点，每个节点都有机会（条件匹配）处理请求事务，如果某个节点处理完了就可以根据实际业务需求传递给下一个节点继续处理或者返回处理完毕。
* [如何用「设计模式」制作珍珠奶茶？](https://mp.weixin.qq.com/s/QWM079Z_zoU_2WxsMxw48g)

### [Visitor pattern](https://en.wikipedia.org/wiki/Visitor_pattern)

* In object-oriented programming and software engineering, the visitor design pattern is a way of separating an algorithm from an object structure on which it operates. A practical result of this separation is the ability to add new operations to existing object structures without modifying the structures. It is one way to follow the open/closed principle.
* In essence, the visitor allows adding new virtual functions to a family of classes, without modifying the classes. Instead, a visitor class is created that implements all of the appropriate specializations of the virtual function. The visitor takes the instance reference as input, and implements the goal through double dispatch.
* [Design Patterns - Visitor Pattern (tutorialspoint.com)](https://www.tutorialspoint.com/design_pattern/visitor_pattern.htm)
* [Design patterns Tutorial => Visitor Pattern example in C++](https://riptutorial.com/design-patterns/example/15127/visitor-pattern-example-in-cplusplus)
* [Visitor](https://refactoring.guru/design-patterns/visitor)
    * [Design Patterns: Visitor in C++](https://refactoring.guru/design-patterns/visitor/cpp/example)
    * [design-patterns-cpp/main.cc at main · RefactoringGuru/design-patterns-cpp](https://github.com/RefactoringGuru/design-patterns-cpp/blob/main/src/Visitor/Conceptual/main.cc)
* [Shape Interface Implementation: Java Exercise - Interview Sansar](https://www.interviewsansar.com/shape-interface-implementation-java-exercise/)
* [java - Implement a Shape abstract class - Code Review Stack Exchange](https://codereview.stackexchange.com/questions/83769/implement-a-shape-abstract-class)
* [C++ Visitor pattern with smart pointers - Stack Overflow](https://stackoverflow.com/questions/39765398/c-visitor-pattern-with-smart-pointers)
