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

## 创建型模式

* [漫画：设计模式之 “工厂模式” (qq.com)](https://mp.weixin.qq.com/s/lFhWPx9h3DCZQ62xxLg1_g)
* [简约不简单的单例模式 (qq.com)](https://mp.weixin.qq.com/s/HmgUhWeXuim2LxZStuHPOw)
* [一个单例还能写出花来吗？ (qq.com)](https://mp.weixin.qq.com/s/0n4TKGbK2UrKarutOxFd7g)

## 结构型模式

* [详解设计模式之结构型模式（上）](https://mp.weixin.qq.com/s/0PTiheUOw3FKJ6kKFZte-Q)
* [漫画设计模式：什么是 “装饰器模式” ？ (qq.com)](https://mp.weixin.qq.com/s/mz9rJELjcWlTv4LFzmKmTA)
* [漫画：设计模式之 “外观模式” (qq.com)](https://mp.weixin.qq.com/s/b2N4kkX4_KPffl7Kt5x4iA)
* [了解组合模式](https://mp.weixin.qq.com/s/o9kXMnu2pygrvVy51s-Qiw)

## 行为型模式

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
