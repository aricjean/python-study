## python 全局重要知识点

### windows 下各种文件位置及作用
比如安装位置为 D:/python
那么在此目录下的
python.exe 在运行程序的时候，会弹出一个黑色的控制台窗口（也叫命令行窗口、DOS/CMD窗口）；
pythonw.exe 是无窗口的Python可执行程序，意思是在运行程序的时候，没有窗口，代码在后台执行。
.py和.pyw文件的区别也来源于python.exe和pythonw.exe的区别：
安装视窗版 Python 时，扩展名为 .py 的文件被默认为用 python.exe 运行的文件，而 .pyw文件则被默认为用 pythonw.exe 运行。
这里还要解释一个问题，如果.py文件直接用python.exe打开，文件被执行完成之后，视窗会立即关闭，如果想让视窗停留，给大家提供两个方法：①可以在程序中import time模块，加入超长睡眠语句，如time.sleep(1800)，如果你不手动关闭视窗，视窗将会停留30min；②可以调用sys和os模块，使用命令行语句pause（个人觉得有些牛刀杀鸡的感觉）。
.pyw格式是被设计用来运行开发的纯图形界面程序的，纯图形界面程序的用户不需要看到控制台窗口。在开发纯图形界面程序的时候，可以暂时把 .pyw 改成 .py ，运行时能调出控制台窗口，方便看到所有错误信息。
至于.pyc文件，是Python解释器运行程序的过程中产生的字节码文件（也就是中间文件）

里面的 Scripts 文件夹主要放一些 python 包的入口文件，就好像 nodejs 里面的全局包安装位置一样
Lib\site-packages目录下全部是第三方Python模块