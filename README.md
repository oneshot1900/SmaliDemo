# SmaliDemo
0.AS安装本地插件smaliidea
1.apktool_decompile.bat 输入apk的名称，会生成反编译的output目录
2.新建工程目录xx\smali ，将output中的smali放入。AS导入该工程，smali右击Mark as Source Root，Project Structure-Project SDK
3.Run-debug-configure-add-remote，记住端口
4.connect_xy.bat连接模拟器
5.start_app.bat 启动指定应用入口，输入包名，入口名，输入端口，输入pid，让端口连接指定pid，然后点Run-debug，报错就重启AS或模拟器

6.修改smali后，将修改后的smali目录覆盖掉output中的smali，apktool_compile.bat打包
7.sign_apk.bat 签名 密码555555

8.如果应用是release包是不能调试的，要先apktool_decompile.bat反编译apk，然后给AndroidManifest中的application添加属性android:debuggable="true",再回编译签名，就成为可debug的apk，之后就如上操作
