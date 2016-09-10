## awk
### 前言
	awk是一个强大的文本分析工具，相对于grep的查找，sed的编辑，awk在其对数据分析并生成报告时，显得尤为强大。简单来说awk就是把文件逐行的读入，以`空格`为默认分隔符将每行切片，切开的部分再进行各种分析处理

### 基本使用模式
	awk [-F  field-separator]  'commands'  input-file(s)
	
### 输出多列数据中的某一列
	netstat -apn | grep 9999 | awk '{print $5}' => 以空格分割多列，并输出第5列(注意$0代表所有列)
	
###  指定列分割符
	netstat -apn | grep 9999 | awk '{print $5}' | awk -F ':' '{print $1}' => 先按空格分割并取出第5列, 然后再对第5列以:分割，并取出第一列