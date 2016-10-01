# xargs
递归找出所有.classpath文件的位置并执行删除
	
	find . -name .classpath | xargs rm [-rf]