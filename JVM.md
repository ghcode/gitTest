# JVM Config

1. jstat

   

| options          |      |
| ---------------- | ---- |
| class            |      |
| compiler         |      |
| gc               |      |
| gccapacity       |      |
| gccause          |      |
| gcmetacapacity   |      |
| gcnew            |      |
| gcnewcapacity    |      |
| gcold            |      |
| gcoldcapacity    |      |
| gcutil           |      |
| printcompilation |      |

## jps

>
>
>使用jps时，如果没有指定hostid，它只会显示本地环境中所有的Java进程；
>
>如果指定了hostid，它就会显示指定hostid上面的java进程，不过这需要远程服务上开启了jstatd服务
>
>
>
>-q   忽略输出的类名、Jar名以及传递给main方法的参数，只输出pid
>
>-m   输出传递给main方法的参数，如果是内嵌的JVM则输出为null
>
>-l  输出应用程序主类的完整包名，或者是应用程序JAR文件的完整路径
>
>-v  输出传给JVM的参数
>
>-V  输出通过标记的文件传递给JVM的参数（.hotspotrc文件，或者是通过参数-XX:Flags=<filename>指定的文件）
>
>-J   用于传递jvm选项到由javac调用的java加载器中，例如，“-J-Xms48m”将把启动内存设置为48M，使用-J选项可以非常方便的向基于Java的开发的底层虚拟机应用程序传递参数。
>
>
>
>

