## 解决Missing artifact com.sun:tools:jar:1.5.0 ##

步骤：

- 复制tools.jar到本地maven资源仓库
 
		mkdir ~/.m2/repository/com/sun/tools/
		cp /usr/local/jdk1.6/lib/tools.jar ~/.m2/repository/com/sun/tools/tools-1.5.0.jar
- 项目属性--Java Build Path---Libraries--确保jre中的jar包列表中有tools.jar($JAVA_HOME/lib/tools.jar)
- 修改eclipse配置文件eclipse.ini，添加

		-vm
		/usr/local/jdk1.6/bin
- 重启eclipse，执行maven update project即可解决
