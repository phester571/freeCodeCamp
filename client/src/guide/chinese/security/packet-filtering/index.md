---
title: Packet Filtering
localeTitle: 包过滤
---
## 包过滤

数据包过滤是基于源和目标地址，端口或协议在网络接口传递或阻止数据包的过程。该过程与数据包重整和网络地址转换（NAT）结合使用。数据包过滤通常是防火墙程序的一部分，用于保护本地网络免受不必要的入侵。

### 如何实现包过滤

网络层防火墙定义数据包过滤规则集，提供高效的安全机制。在软件防火墙中，包过滤由称为包过滤器的程序完成。数据包过滤器根据一组特定的规则检查每个数据包的标头，并在此基础上决定阻止它传递（称为DROP）或允许它通过（称为ACCEPT）。

### 过滤方法

一旦定义了一组过滤规则，就可以通过三种方式配置数据包过滤器。在第一种方法中，过滤器只接受那些确定安全的数据包，而不是所有其他数据包。这是最安全的模式，但如果无意中丢弃了合法的数据包，可能会造成不便。在第二种方法中，过滤器仅丢弃确定不安全的数据包，接受所有其他数据包。此模式的安全性最低，但不会造成较少的不便，尤其是在随意的Web浏览中。在第三种方法中，如果过滤器遇到其规则不提供指令的数据包，则可以隔离该数据包，或者可以专门查询用户应该对其执行的操作。如果它导致出现大量对话框（例如，在Web浏览期间），则这可能是不方便的。