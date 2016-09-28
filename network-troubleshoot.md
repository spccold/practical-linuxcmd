## network-troubleshoot

### 如何快速定位tcp的频繁建立与关闭
	1. netstat -apn | grep TIME_WAIT   查看TIME_WAIT状态的ip
	2. tcpdump grep 'Flags [F.]'   查看四次挥手报文