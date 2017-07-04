# IO

~~~
iostat -dxm  1
Device: rrqm/s wrqm/s r/s w/s rMB/s wMB/s avgrq-sz avgqu-sz await svctm %util

r/s: 每秒完成的读次数
w/s: 每秒完成的写次数
rMB/s: 每秒读数据量(以MB为单位)
wMB/s: 每秒写数据量
用以观察IO操作中的读写情况, 判断标准: 比如, 如果进程频繁写日志，没有读操作， 那么w/s和wMB/s会很高, r/s和rMB/s会很低

随机/顺序IO
rrqm/s: 每秒对该设备的读请求被合并的次数, 文件系统会对读取同块(block)的请求进行合并
wrqm/s: 每秒对该设备的写请求被合并的次数
判断标准: 如果是顺序IO较多， 那么这两项就会高一些；如果是离散IO较多，这两项就会偏低一些，从性能角度而言，顺序IO越多越好

IO size
avgqu-sz: 平均请求队列的长度
avgrq-sz: 平均每次IO操作的数据量(以扇区数为单位)
判断标准: 平均请求队列长度越短，IO的性能表现就越好
~~~