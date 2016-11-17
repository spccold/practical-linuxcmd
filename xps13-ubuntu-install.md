# xps13 ubuntu install(ubuntu-16.10-desktop-amd64.iso)
* F12进入xps13的bios设置界面, 关闭usb3.0特性，开启usb2.0特性
* 制作启动盘 
	* windows下Universal usb installer制作启动盘
	* ubuntu的terminal下运行usb-creator-gtk, 制作usb启动盘
* f12进入bios, 从usb driver启动


# something about ubuntu 16.10
* launcher-position
	* gsettings set com.canonical.Unity.Launcher launcher-position Bottom
	* gsettings set com.canonical.Unity.Launcher launcher-position Left
* esc+fn 禁用fn功能键