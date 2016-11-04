#something about gc troubleshoot
* 确认gc是否异常
	* jstat -gcutil pid interval
* 查看大量存活的对象
	* jmap -histo:live pid 查询所有存活对象（实例数以及暂用的内存）
* 查看大量存活的对象是哪里创建的
	* jmap -dump:live,format=b,file=dump.bin 
	* jhat dump.bin(默认开启stack和refs)
	* x.x.x.x:7000 -> web page bottom(`Other Queries`) -> `Show instance counts for all classes (including platform)` -> 点击具体的实例 -> References summary by Type -> `Referrers by Type`(谁引用了当前的实例) / `Referees by Type`(被当前实例引用的Class)
		