# 学习笔记之Visual Studio Code (VSCode) & Clang

Mac上XCode太占空间，卸载然后安装VSCode和Clang。在VSCode中再安装extension C/C++和Code Runner，配置Tasks: Configure Task，就可以开始Run C++ program了。

* [Visual Studio Code - Code Editing. Redefined](https://code.visualstudio.com/)
  * [keyboard-shortcuts-windows.pdf](https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf)
  * [C++ programming with Visual Studio Code](https://code.visualstudio.com/docs/languages/cpp)
    * [Introductory Videos for C++ in Visual Studio Code](https://code.visualstudio.com/docs/cpp/introvideos-cpp)
    * [c_cpp_properties.json reference](https://code.visualstudio.com/docs/cpp/c-cpp-properties-schema-reference)
    * [Configure VS Code for Clang/LLVM on macOS](https://code.visualstudio.com/docs/cpp/config-clang-mac)
  * [Java in Visual Studio Code](https://code.visualstudio.com/docs/languages/java)
    * [Getting Started with Java in Visual Studio Code](https://code.visualstudio.com/docs/java/java-tutorial)
  * [Debugging configurations for Python apps in Visual Studio Code](https://code.visualstudio.com/docs/python/debugging)
* [Clang - Wikipedia](https://en.wikipedia.org/wiki/Clang)
  * Clang/ˈklæŋ/[5] is a compiler front end for the C, C++, Objective-C and Objective-C++ programming languages, as well as the OpenMP,[6] OpenCL, RenderScript and CUDAframeworks. It uses the LLVM compiler infrastructure as its back end and has been part of the LLVM release cycle since LLVM 2.6.
  It is designed to act as a drop-in replacement for the GNU Compiler Collection (GCC), supporting most of its compilation flags and unofficial language extensions.[7][8] Its contributors include Apple, Microsoft, Google, ARM, Sony, Intel and Advanced Micro Devices (AMD). It is open-source software,[9] with source code released under the University of Illinois/NCSA License, a permissive free software licence.
  * The Clang project includes the Clang front end, a static analyzer and several code analysis tools.[10]
* [Comparing Clang to other open source compilers](https://clang.llvm.org/comparison.html)
* [Clang C/C++ Download and Installation Instructions](https://www.ics.uci.edu/~pattis/common/handouts/macclion/clang.html)

## RESOURCES

* [Web 版 VS Code 来了！](https://mp.weixin.qq.com/s/41SVP7zIL-5CCCGgt1VCOg)
* [Vscode 小白使用介绍](https://mp.weixin.qq.com/s/PsEZAwK-tbWtjsNZOJATzg)
  * https://www.cnblogs.com/tu-0718/p/10935910.html
* [VS Code 必知必会的 20 个快捷键！](https://mp.weixin.qq.com/s/t7TLBOcnOs0AkncCVsYr9Q)
  * https://medium.com/better-programming/20-vs-code-shortcuts-for-fast-coding-cheatsheet-10b0e72fd5d
* [在用VSCode? 看完这篇文章, 开发效率翻倍!](https://mp.weixin.qq.com/s/XiT6uNQPIPGvkLbUcPnRqw)
* [手把手教你配置VS Code 远程开发工具](https://mp.weixin.qq.com/s/JBKAAe2lonKGX1wFynIPvQ)
* [使用VSCode进行远程炼丹](https://mp.weixin.qq.com/s/hFCAeQFPAd1eb-z-r75ZUw)
  * https://zhuanlan.zhihu.com/p/89662757
* [实时可视化Debug：VS Code 开源新工具，一键解析代码结构](https://mp.weixin.qq.com/s/943dZHSZyQbjlxTpv54w7Q)
  * https://github.com/hediet/vscode-debug-visualizer
* [不光要用Python，还要在VSCode里用](https://mp.weixin.qq.com/s/KnMcDbP0_k6OBxR3NSOa5A)
  * https://blog.csdn.net/bigbennyguo/article/details/104704023
* [用 VSCode 写 python 的正确姿势](https://mp.weixin.qq.com/s/qIcMpsOiaZqgHVFW3LmoHg)
* [推荐一款Python编辑器，集Pycharm和Sublime优点于一身的王者](https://mp.weixin.qq.com/s/zdSVszyE_6sSXva1ZKVswQ)
* [微软VS Code已原生支持Jupyter笔记本，再也不用打开网页调试运行了](https://mp.weixin.qq.com/s/ZId-LFDDsnDlbA_j0B3jLw)
* [VS Code上也能玩转Jupyter Notebook，这是一份完整教程](https://mp.weixin.qq.com/s/cb7r0QL8MOQRngEyBt3F-w)
  * https://towardsdatascience.com/getting-started-with-jupyter-notebooks-in-visual-studio-code-5dcccb3f739b
* [为什么企业里用 VS Code 的这么多？]
* 简洁而聚焦的产品定位，贯穿始终
* UI 渲染与业务逻辑隔离，一致的用户体验
* LSP—— 基于文本的协议
* 集大成的 Remote Development
* [微软发布 VS Code 4 月 Python 扩展更新：支持 Poetry 环境 (qq.com)

* [如何将宇宙最强 VSCode 打造为刷题神器 (qq.com)

* [从 VSCode 看大型 IDE 技术架构 (qq.com)
  * [从 VSCode 看大型 IDE 技术架构 - 知乎 (zhihu.com)
* [经验之谈：学习 Visual Studio Code 不会错！ (qq.com)
  * [The Era of Visual Studio Code | Roben Kleene
* [生产力终极指南：用了两年，如今才算真正会用VS Code (qq.com)
  * [How to Configure VS Code Like a Pro | by Stefan Metodiev | Better Programming
  * [Squiff88/vscodeSetup: Ultimate setup (github.com)
* [利用 VS Code 构建基于容器的开发环境 (qq.com)
  * [Building container-based development environment with Visual Studio Code | by Santhosh Sundar | May, 2021 | Medium
  * [Developing inside a Container using Visual Studio Code Remote Development

## EXTENSIONS

* [All Autocomplete](https://marketplace.visualstudio.com/items?itemName=Atishay-Jain.All-Autocomplete)
  * Create autocomplete items from open files in VSCode.
* [Bracket Pair Colorizer](https://marketplace.visualstudio.com/items?itemName=CoenraadS.bracket-pair-colorizer)
  * A customizable extension for colorizing matching brackets
* [Browser Preview](https://marketplace.visualstudio.com/items?itemName=auchenberg.vscode-browser-preview)
  * A real browser preview inside your editor that you can debug.
* [GitLens — Git supercharged](https://marketplace.visualstudio.com/items?itemName=eamodio.gitlens)
  * Supercharge the Git capabilities built into Visual Studio Code — Visualize code authorship at a glance via Git blame annotations and code lens, seamlessly navigate and explore Git repositories, gain valuable insights via powerful comparison commands, and so much more
* [Nord Wave](https://marketplace.visualstudio.com/items?itemName=dnlytras.nord-wave)
  * Darker version of the awesome Nord theme
* [PostgreSQL](https://marketplace.visualstudio.com/items?itemName=ms-ossdata.vscode-postgresql)
  * Develop Postgres everywhere
* [Python](https://marketplace.visualstudio.com/items?itemName=ms-python.python)
  * Linting, Debugging (multi-threaded, remote), Intellisense, Jupyter Notebooks, code formatting, refactoring, unit tests, snippets, and more.
* [Python Indent](https://marketplace.visualstudio.com/items?itemName=KevinRose.vsc-python-indent)
  * Correct python indentation.
* [Remote - SSH](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-ssh)
  * Open any folder on a remote machine using SSH and take advantage of VS Code's full feature set.
* [LaTeX Workshop](https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop)
  * Boost LaTeX typesetting efficiency with preview, compile, autocomplete, colorize, and more.
* [Material Theme](https://marketplace.visualstudio.com/items?itemName=Equinusocio.vsc-material-theme)
  * The most epic theme now for Visual Studio Code
* [Test Explorer UI](https://marketplace.visualstudio.com/items?itemName=hbenl.vscode-test-explorer)
  * Run your tests in the Sidebar of Visual Studio Code

#

* [VS Code 最强插件指南 - CSDN](https://mp.weixin.qq.com/s/MshppwwRFmbFx3aR7FVpEQ)
  * https://www.freecodecamp.org/news/favorite-vs-code-extensions-2017-786ea235812f/
* [Node.js不容错过的 Visual Studio Code 十大扩展组件](https://mp.weixin.qq.com/s/Np62J_-QYvusrOvbRNc8Mw)
* [来安装一个酷炫的 VS Code 主题](https://mp.weixin.qq.com/s/eUgc9Y6KdEH9Rjrc9V3QTQ)
* [动图演示11个必备 VS Code 插件](https://mp.weixin.qq.com/s/np7EBSMJwfDUBut-OxNRfQ)
* [VSCode 插件](https://mp.weixin.qq.com/s/SWXW1SGw6IwL5yZ0uGHoLw)
* [10款VS Code插件神器](https://mp.weixin.qq.com/s/E3Emku5IW9p8VlM1BiVC8Q)
* [用 VS Code 写 Python，这8个扩展
1、Python extension for Visual Studio Code
2、Python Preview
3、Sort lines
4、Git Graph
5、Python Snippets
6、Better Comments
7、autoDocstring
8、Python Indent
* [用 VS Code 写 Python，这几个插件
* Python
* Python Snippets
* Python Docstring Generator
* Python Test Explorer for Visual Studio Code
* Python Preview
* Python Type Hint
* Jupyter
* [VSCode 上也能画流程图了！](https://mp.weixin.qq.com/s/W-5LZuZTLH3dBGOf9zm8Sw)
  * https://github.com/hediet/vscode-drawio
* [VS Code 变身小霸王游戏机！](https://mp.weixin.qq.com/s/x21GcqOEDP6ARguxAJ6jRA)
* https://github.com/gamedilong/anes-repository
* https://marketplace.visualstudio.com/items?itemName=gamedilong.anes
* [Pylance 性能更新，微软新的VS Code Python 插件已趋于稳定 (qq.com)

## FAQ

* How to change the launched folder ?
  * Navigate to your project folder and type code .
  * [The Visual Studio Code Command Line Options](https://code.visualstudio.com/docs/editor/command-line#_launching-from-command-line)

* How to commit part of code changes ?
  * [Version Control in Visual Studio Code](https://code.visualstudio.com/docs/editor/versioncontrol#_commit)
  * [Git version control in Visual Studio Code](https://code.visualstudio.com/docs/introvideos/versioncontrol)
  * [visual studio code - How can I commit some changes to a file, but not others, in VSCode? - Stack Overflow](https://stackoverflow.com/questions/34730585/how-can-i-commit-some-changes-to-a-file-but-not-others-in-vscode)
    * Click '...' then Stage Selected Ranges

* How to fix remote connection error: The process tried to write to a nonexistent pipe ?
  * [Remote Explorer - SSH TARGETS - Configure - Settings - Specify the absolute file path, e.g. C:\Users\hao\.ssh\config.
  * [ssh - VScode remote connection error: The process tried to write to a nonexistent pipe - Stack Overflow](https://stackoverflow.com/questions/60335069/vscode-remote-connection-error-the-process-tried-to-write-to-a-nonexistent-pipe)

* How to fix "/.ssh/id_rsa is too open. It is required to be not accessible by others. The private key is ignored" ?
  * /.ssh/id_rsa - Properties - Security - Advance - Disable inheritance - remove other users and just keep your user
* How to set PYTHONPATH for src code ?
* Add env in /.vscode/launch.json

"configurations": [
{
"env": {
"PYTHONPATH": "/a:/b"
}
}

* Add PYTHONPATH in /.vscode/settings.json
"terminal.integrated.env.linux": {
"PYTHONPATH": "/a:/b"
}
* [Using Python Environments in Visual Studio Code](https://code.visualstudio.com/docs/python/environments#_use-of-the-pythonpath-variable)
* [Setting Python source folders in Visual Studio Code - Binx](https://binx.io/blog/2020/03/05/setting-python-source-folders-vscode/)
* [Visual Studio Code - How to add multiple paths to python path? - Stack Overflow](https://stackoverflow.com/questions/41471578/visual-studio-code-how-to-add-multiple-paths-to-python-path)
* [visual studio code - How to use PYTHONPATH with VSCode Python Extension for Debugging? - Stack Overflow](https://stackoverflow.com/questions/58570503/how-to-use-pythonpath-with-vscode-python-extension-for-debugging)
* How to set vertical rulers for column ?
* [vscode settings - Vertical rulers in Visual Studio Code - Stack Overflow (stackoverflow.com)](https://stackoverflow.com/questions/29968499/vertical-rulers-in-visual-studio-code)
* To configure it, go to menu File → Preferences → Settings and add this to to your user or workspace settings:
"editor.rulers": [80,120]
* Why configuration setting could be found in run mode but couldn't be found in debug mode ?
* Need to set workspaceFolder properly. Add workspace folder -> Open the project folder.
* [Visual Studio Code Variables Reference](https://code.visualstudio.com/docs/editor/variables-reference)
* [Visual Studio Code User and Workspace Settings](https://code.visualstudio.com/docs/getstarted/settings#_settings-file-locations)
* [debugging - How do I set my workspace folder in Visual Studio Code? - Stack Overflow](https://stackoverflow.com/questions/56175608/how-do-i-set-my-workspace-folder-in-visual-studio-code)
