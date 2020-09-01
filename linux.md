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

>![内存使用情况](https://img.linux.net.cn/data/attachment/album/201312/08/105933i53bi3a3ioocff3c.png)
>
>第一行是物理内存使用，第二行是虚拟内存使用(交换空间)
>
>Mem:全部可用内存、已使用内存、空闲内存、缓冲内存。
>
>Swap:全部、已使用、空闲和缓冲交换空间
>
>m命令来切换显示

>![任务信息列](https://img.linux.net.cn/data/attachment/album/201312/08/105935j73jls2nzljjz267.png)
>
>* **PID**  进程ID，进程的唯一标识符
>* **USER**  进程所有者的实际用户名。
>* **PR**  进程的调度优先级。这个字段的一些值是'rt'。这意味这这些进程运行在实时态。
>* **NI**  进程的nice值（优先级）。越小的值意味着越高的优先级。
>* **VIRT ** 进程使用的虚拟内存。
>* **RES**  驻留内存大小。驻留内存是任务使用的非交换物理内存大小。
>* **SHR**  SHR是进程使用的共享内存。
>* **S**  这个是进程的状态
>  * D - 不可中断的睡眠态。
>  * R – 运行态
>  * S – 睡眠态
>  * T – 被跟踪或已停止
>  * Z – 僵尸态
>* **%CPU**  自从上一次更新时到现在任务所使用的CPU时间百分比。
>* **%MEM**  进程使用的可用物理内存百分比。
>* **TIME+**  任务启动后到现在所使用的全部CPU时间，精确到百分之一秒。
>* **COMMAND**  运行进程所使用的命令。
>* 
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
>A  在全屏和交替模式间切换。在交替模式下会显示4个窗口
>
>	 * Def （默认字段组）
>	 * Job （任务字段组）
>	 * Mem （内存字段组）
>	 * Usr （用户字段组）
>	 * 可以用'a'和'w'在4个 窗口间切换。'a'移到后一个窗口，'w'移到前一个窗口。用'g'命令你可以输入一个数字来选择当前窗口。
>
>B  粗体显示
>
>d/s  设置的值作为刷新间隔。如果你这里输入了1，top将会每秒刷新
>
>f  选择你想要显示的字段。用'*'标记的是已选择的
>
>R  反向排序
>
>c  切换是否显示进程启动时的完整路径和程序名
>
>i  切换显示空闲任务
>
>V  切换树视图
>
>z  切换彩色，即打开或关闭彩色显示
>
>N -  以 PID 的大小的顺序排列表示进程列表
>
>P - 以 CPU 占用率大小的顺序排列进程列表
>
>M - 以内存占用率大小的顺序排列进程列表
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

## sort

>```java
>/*
>默认排序规则
>以数字开头的行优先级最高
>以小写字母开头的行优先级次之
>待排序内容按字典序进行排序
>默认情况下，‘sort’命令将带排序内容的每行关键字当作一个字符串进行字典序排序（数字优先级最高，参看规则 1）
>*/
>```
>
>-r   反向排序
>
>-k  指定排序得列
>
>-n   指定的列以数字排序
>
>-t  指定列之间的分隔符
>
>-u  去除重复值
>
>-f  忽略大小写

## echo

>
>
>-e  启用转义

## ls

>
>
>-l
>
>-a
>
>-A
>
>-h
>
>--date-type

## head





##  set命令

> 

##  time

>
## vmstat
>
>
>
>
>

## ps
>
>
>a
>
>u
>
>x
>
>e
>
>o
>
>
## dstat
>
>
>-c   cpu
>
>-d   disk
>
>-n  net
>
>-m  mem
>
>-r  i/o
>
>-g  page
>
>-y  system states
>
>-l  blance
>
>-p  processes
>
>-s  swap
>
>- -–disk-util ：显示某一时间磁盘的忙碌状况
>- -–freespace ：显示当前磁盘空间使用率
>- -–proc-count ：显示正在运行的程序数量
>- -–top-bio ：指出块I/O最大的进程
>- -–top-cpu ：图形化显示CPU占用最大的进程
>- -–top-io ：显示正常I/O最大的进程
>- -–top-mem ：显示占用最多内存的进程
>
>
>


## iostat
> 
>
>
>## grep awk sed cat more tail fg bg jobs vi  nohup  watch  