## grep

### grep控制匹配文本显示范围
	grep -C 5 foo file 显示file文件里匹配foo字串那行以及上下5行
	grep -B 5 foo file 显示foo及前5行
	grep -A 5 foo file 显示foo及后5行

### grep &(与)多个条件
	cat file | grep str1 | grep str2  => grep出既包含str1又包含str2的行

### grep |(或)多个条件
	cat file | grep -E 'str1|str2'    => grep出包含str1或者str2的行

### grep排除多个条件
	cat file | grep -v str1 | grep -v str2  => 找出既不包含str1, 也不包含str2的行
	cat file | grep -v -E 'str2|str1'       => 同上
