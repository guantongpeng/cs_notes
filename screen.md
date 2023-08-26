screen是一款非常简单易上手的终端复用工具，可以将会话与窗口分离，避免断线导致服务器程序断掉。如需要更强大的功能，可参考[tmux教程](https://blog.csdn.net/qq_39280836/article/details/127028634?spm=1001.2014.3001.5502)，tmux是一种功能更加强大的终端复用工具。  
**安装：**  
```apt-get install screen```  
**常用命令：**  
```screen -S python```创建一个叫做python的会话  
```screen -ls```查看已经创建的会话  
```screen -r```恢复会话  
```exit```退出  
**快捷键：**  
Ctrl + a，d #暂离当前会话  
Ctrl + a，c #在当前screen会话中创建一个子会话  
Ctrl + a，w #子会话列表  
Ctrl + a，p #上一个子会话  
Ctrl + a，n #下一个子会话  
Ctrl + a，0-9 #在第0窗口至第9子会话间切换  

**参考：**  
[screen命令详解](https://www.cnblogs.com/mchina/archive/2013/01/30/2880680.html)  
