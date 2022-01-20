# TCP/IP 协议入门
欢迎来到 [Networking 101](https://internalpointers.com/post-group/networking-101) 系列的第三章！在之前的一节中，我们研究了在地球上最受欢迎的网络，总所周知的因特网。在这个章节中，我想要在技术上浅析因特网底层是如何工作的。

因特网是不同网络的巨大集合，被用来和其它的主机进行彼此交换信息。这导致因特网是一个复杂的机制，要求使用特定的规则才能够操作正确：这些规则被称为协议。因特网尤其众所周知的名称是因特网套件，经常被称做 TCP/IP 协议。

## 因特网套件是什么，众所周知也被称为 TCP/IP 协议
因特网协议套件是一些协议的集合 —— 这就是套件代表的意思 —— 这决定了因特网如何工作。TCP/IP 这个别名的由来是来自于因特网套件中包含的两种最重要的协议：传输控制协议(TCP)和网络协议(IP)。从现在开始，为了简洁起见，我将其称为 TCP/IP协议栈。

最开始由美国防御部门开发，并且现在是由 **Internet Engineering Task Force (IETF)** 维护，TCP/IP 栈定义了数据如何被处理，被传输，被路由，以及如何从互联网接收。连接到因特网或与因特网相连的任何设备都必须遵守 TCP/IP 协议栈中定义的规则。两台机器为了能够通过互联网上彼此正确的交流就必须都要实现 TCP/IP协议栈。

举个例子，你正在阅读这篇文章所使用的浏览器就是实现了超文本传输协议(HTTP), 是 TCP/IP协议栈中的一种协议，同时也是万维网(World Wide Web)的基石。HTTP协议决定了你正在阅读的文本如何从 web 服务器上被发送 —— 因为服务器上存储着资源信息 —— 对于你的 web 浏览器是通过因特网的。该协议还描述了浏览器应该如何与 web 服务器通信以启动数据交换。

需要启动软件部分必须与 TCP/IP 兼容。举个例子，为了能够提供与另外一个系统通信的能力(包括浏览器), 运行在你设备上的操作系统已经实现了 TCP/IP套件中一些协议。

### TCP/IP 与软件方面有关
你不会找到如何构建网络的说明，信号如何在电缆中传送，等等。TCP/IP被设计成硬件独立，并且可以实现在任何物理技术上。举个例子，一些 **IETF**工程师在愚人节设计了 [IP over Avian Carriers (IPoAC)](https://en.wikipedia.org/wiki/IP_over_Avian_Carriers) 通过信鸽等鸟类来传输互联网信息的协议。

## 剖析 TCP/IP 协议栈