## PYTHONPATH
PYTHONPATH是Python搜索路径，默认我们import的模块都会从PYTHONPATH里面寻找。
使用下面的代码可以打印PYTHONPATH：
```python
import os
print(os.sys.path)
```
我的结果如下：
```bash
[
'', 
'D:\\Python\\Python38-32\\python38.zip',
'D:\\Python\\Python38-32\\DLLs',
'D:\\Python\\Python38-32\\lib',
'D:\\Python\\Python38-32',
'C:\\Users\\XXXX\\AppData\\Roaming\\Python\\Python38\\site-packages',
'D:\\Python\\Python38-32\\lib\\site-packages'
]
```
比如我使用下面的import语句：

import urllib
Python解释器会逐个从上面的路径列表选出一个路径然后搜索urllib模块直到找到为止。这里最后在 'D:\\Python\\Python38-32\\lib' 下找到

D:\Python\Python38-32\Lib\site-packages目录下全部是第三方Python模块

### 注意
使用import xx语法时，xx只能是模块路径（一个模块一般是指一个package或者一个以.py为后缀的文件，不一般的情况包括.pth、.dll以及其他扩展形式）。
而且一般只有package模块下面才可以包含子模块（不知道准确不准确，DLL模块是否可以包含其他子模块？）








