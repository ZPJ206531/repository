# linux常用命令

## 1.ps

ps 命令为Process Status的缩写，常用于列出系统当前运行的进程，从而进行监测和控制。

Linux上进程的状态有5种：

1. 运行，正在运行或运行队列中的进程
2. 中断，休眠中、受阻、在等待某个条件的形成或接收信号
3. 不可中断，收到信号不唤醒，不可运行
4. 僵死，进程终止，但进程描述符还在
5. 停止，进程收到SIGSTOP, SIGSTP, SIGTIN, SIGTOU信号后停止运行运行

分别对应以下5种状态码：

1. R， runnable (on run queue)
2. S，sleeping
3. D，uninterruptible sleep (usually IO)
4. T， traced or stopped
5. Z，a defunct (”zombie”) process

1.ps -aux

查看系统中所有的进程

2.ps -le

查看系统中所有的进程，并查看进程的父进程的PID和进程优先级

3.ps -l

看都当前shell产生的过程





## &

- bg [作业id]
- fg [作业id]
- jobs -l
- ctrl Z
- kill [进程id]
- nohup 主线程退出后，继续运行子线程
- setsid 



