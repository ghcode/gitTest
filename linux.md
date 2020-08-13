# linux

##  概念

### 进程

>top命令
>
>![img](https://img.linux.net.cn/data/attachment/album/201311/23/202423a2xaiu4o42g28uu2.png)

## 界面指导

>![显示运行时间](https://img.linux.net.cn/data/attachment/album/201312/08/1059317q7vsg9cbyqqb7po.png)
>
>- 当前时间
>- 系统已运行的时间
>- 当前登录用户的数量
>- 相应最近5、10和15分钟内的平均负载
>- l命令来切换显示

>![CPU状态显示](https://img.linux.net.cn/data/attachment/album/201312/08/105932tdjqyrrwzlpyisni.png)
>
>- us, user： 运行(未调整优先级的) 用户进程的CPU时间
>- sy，system: 运行内核进程的CPU时间
>- ni，niced：运行已调整优先级的用户进程的CPU时间
>- wa，IO wait: 用于等待IO完成的CPU时间
>- hi：处理硬件中断的CPU时间
>- si: 处理软件中断的CPU时间
>- st：这个虚拟机被hypervisor偷去的CPU时间（译注：如果当前处于一个hypervisor下的vm，实际上hypervisor也是要消耗一部分CPU处理时间的）。
>- t命令来切换显示

>
>
>



#### 交互指令

>1 显示全部的核心的使用情况
>
>2 
>
>3 
>
>4
>
>u
>
>U
>
>s
>
>l 切换uptime的显示
>
>

#### 命令选项

>-p  指定要查看的PID ,多个用逗号隔开
>
>-b  批量输出命令结果，配合-n 控制输出次数
>
>-u 指定登录账户名活UID,仅匹配有效的用户id
>
>-U 真实/有效/保存/文件系统用户名







##  set命令

> 

##  time

>

