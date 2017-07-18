# ps

## 查看进程什么时间开始运行以及运行了多次时间
~~~
ps -o stime,etime pid

STIME     ELAPSED
Jul14  3-23:28:28

运行于7月14号, 运行了3天23小时28分钟28秒
~~~

## 查看进程所属用户
~~~
ps -aux | grep pid
~~~