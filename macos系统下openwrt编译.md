### macos系统下openwrt编译(HG255d)	

1. 安装Xcode

2. 安装brew

	brew install coreutils findutils gawk gnu-getopt gnu-tar grep wget quilt xz
	brew ln gnu-getopt --force
	vi ~/.bash_profile
	添加如下：PATH="/usr/local/opt/coreutils/libexec/gnubin:$PATH"
	source ~/.bash_profile

6. 创建大小写敏感的虚拟盘

	hdiutil create -size 20g -type SPARSE -fs "Case-sensitive HFS+" -volname OpenWrt OpenWrt.sparseimage
	hdiutil attach OpenWrt.sparseimage

8. cd /Volume/OpenWrt

9. git clone git://git.openwrt.org/15.05/openwrt.git

10. 查找HG255关键字，讲所在行注释符去掉

	vi target/linux/ramips/image/Makefile 

11. 升级软件包 

	./scripts/feeds update -a
	./scripts/feeds install -a

12. 检查必备软件

	make defconfig

13. 进入编译选项配置（CPU架构、平台、产品、软件包）

	make menuconfig

14. 编译

	make V=99 -j2

	./scripts/feeds update -a
	./scripts/feeds install -a

12.检查必备软件

	make defconfig

13.进入编译选项配置（CPU架构、平台、产品、软件包）

	make menuconfig

14.编译

	make V=99 -j2
