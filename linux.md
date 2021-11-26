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
>k-结束某个进程
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
>
>-H  线程模式
>
>-c 



## sort [参考1](https://segmentfault.com/a/1190000019419326)

>-b  会忽略每一行前面的所有空白部分，从第一个可见字符开始比较
>
>-f   会将小写字母都转换为大写字母来进行比较，亦即忽略大小写。
>
>-n  依照数值的大小排序
>
>-r    以相反的顺序来排序
>
>-t<分隔字符>   指定排序时所用的栏位分隔字符
>
>-k 选择以哪个区间进行排序



##  set命令

> 

##  time

>

>## vmstat
>
>
>
>



>## ps
>
>1. ps -p {PID-HERE} -o etime|etimes  查看指定进程已运行的时间
>2. -a
>3. -A
>4. a
>5. -e
>6. e
>7. x  显示没有控制终端的进程
>8. -u 查看特定用户(EUID)进程
>9. -U 查看特定用户(RUID)进程
>10. u
>11. --sort  
>    1. -|+pcpu  按照cpu使用情况降序|升序排列
>    2. -|+pmem  按照内存使用情况降序|升序排列
>12. -C  使用进程名过滤
>13. -L 根据线程ID过滤
>14. -f 全格式
>15. -j
>16. -o 控制输出内容
>    1. 
>
>```bash
>#real user ID (ruid): 实际用户ID,指的是进程执行者是谁
>#effective user ID (euid): 有效用户ID,指进程执行时对文件的访问权限
>#saved set-user-ID (saved uid): 保存设置用户ID。是进程刚开始执行时，euid的副本。在执行exec调用之后能重新恢复原来的effectiv user ID.
>#上面这三个ID是相对于进程而言的.
>
>#p表示命名管道文件 
>#d表示目录文件 
>#l表示符号连接文件 
>#-表示普通文件 
>#s表示socket文件 
>#c表示字符设备文件 
>#b表示块设备文件
>```
>
>



>
>
>## dstat
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
>## iostat



> ## du  Disk Usage
>
> ls| xargs du -s -h
>
> * -a,--all   默认输出目录使用磁盘空间情况，加上此参数将输出目录下的文件的磁盘占用情况
>
> * -[b|k|m|h] 
>
>   ```
>   DU(1)                                                             User Commands                                                            DU(1)
>   
>   
>   
>   NAME
>          du - estimate file space usage
>   
>   SYNOPSIS
>          du [OPTION]... [FILE]...
>          du [OPTION]... --files0-from=F
>   
>   DESCRIPTION
>          Summarize disk usage of each FILE, recursively for directories.
>   
>          Mandatory arguments to long options are mandatory for short options too.
>       
>          -0, --null
>                 end each output line with NUL, not newline
>       
>          -a, --all
>                 write counts for all files, not just directories
>       
>          --apparent-size
>                 print  apparent  sizes,  rather  than  disk usage; although the apparent size is usually smaller, it may be larger due to holes in
>                 ('sparse') files, internal fragmentation, indirect blocks, and the like
>       
>          -B, --block-size=SIZE
>                 scale sizes by SIZE before printing them; e.g., '-BM' prints sizes in units of 1,048,576 bytes; see SIZE format below
>       
>          -b, --bytes
>                 equivalent to '--apparent-size --block-size=1'
>       
>          -c, --total
>                 produce a grand total
>       
>          -D, --dereference-args
>                 dereference only symlinks that are listed on the command line
>       
>          -d, --max-depth=N
>                 print the total for a directory (or file, with --all) only  if  it  is  N  or  fewer  levels  below  the  command  line  argument;
>                 --max-depth=0 is the same as --summarize
>       
>          --files0-from=F
>                 summarize disk usage of the NUL-terminated file names specified in file F; if F is -, then read names from standard input
>       
>          -H     equivalent to --dereference-args (-D)
>       
>          -h, --human-readable
>                 print sizes in human readable format (e.g., 1K 234M 2G)
>       
>          --inodes
>                 list inode usage information instead of block usage
>       
>          -k     like --block-size=1K
>       
>          -L, --dereference
>                 dereference all symbolic links
>       
>          -l, --count-links
>                 count sizes many times if hard linked
>       
>          -m     like --block-size=1M
>       
>          -P, --no-dereference
>                 don't follow any symbolic links (this is the default)
>       
>          -S, --separate-dirs
>                 for directories do not include size of subdirectories
>       
>          --si   like -h, but use powers of 1000 not 1024
>       
>          -s, --summarize
>                 display only a total for each argument
>       
>          -t, --threshold=SIZE
>                 exclude entries smaller than SIZE if positive, or entries greater than SIZE if negative
>       
>          --time show time of the last modification of any file in the directory, or any of its subdirectories
>       
>          --time=WORD
>                 show time as WORD instead of modification time: atime, access, use, ctime or status
>       
>          --time-style=STYLE
>                 show times using STYLE, which can be: full-iso, long-iso, iso, or +FORMAT; FORMAT is interpreted like in 'date'
>       
>          -X, --exclude-from=FILE
>                 exclude files that match any pattern in FILE
>       
>          --exclude=PATTERN
>                 exclude files that match PATTERN
>       
>          -x, --one-file-system
>                 skip directories on different file systems
>       
>          --help display this help and exit
>       
>          --version
>                 output version information and exit
>       
>          Display  values  are  in units of the first available SIZE from --block-size, and the DU_BLOCK_SIZE, BLOCK_SIZE and BLOCKSIZE environment
>          variables.  Otherwise, units default to 1024 bytes (or 512 if POSIXLY_CORRECT is set).
>       
>          The SIZE argument is an integer and optional unit (example: 10K is 10*1024).  Units are K,M,G,T,P,E,Z,Y (powers  of  1024)  or  KB,MB,...
>          (powers of 1000).
>       
>          GNU coreutils online help: <http://www.gnu.org/software/coreutils/> Report du translation bugs to <http://translationproject.org/team/>
>       
>          Packaged  by  Cygwin  (8.23-4)  Copyright  ©  2014  Free  Software  Foundation,  Inc.   License  GPLv3+:  GNU  GPL  version  3  or  later
>          <http://gnu.org/licenses/gpl.html>.  This is free software: you are free to change and redistribute it.  There is  NO  WARRANTY,  to  the
>          extent permitted by law.
>   
>   PATTERNS
>          PATTERN  is a shell pattern (not a regular expression).  The pattern ?  matches any one character, whereas * matches any string (composed
>          of zero, one or multiple characters).  For example, *.o will match any files whose names end in .o.  Therefore, the command
>   
>                 du --exclude='*.o'
>       
>          will skip all files and subdirectories ending in .o (including the file .o itself).
>   
>   AUTHOR
>          Written by Torbj"orn Granlund, David MacKenzie, Paul Eggert, and Jim Meyering.
>   
>   SEE ALSO
>          The full documentation for du is maintained as a Texinfo manual.  If the info and du programs are properly installed at  your  site,  the
>          command
>   
>                 info coreutils 'du invocation'
>       
>          should give you access to the complete manual.
>   
>   
>   
>   GNU coreutils 8.23                                                October 2014                                                             DU(1)
>   
>   ```
>
>   

>
>
>## grep awk sed cat more tail fg bg jobs vi  nohup  watch  du df iconv

