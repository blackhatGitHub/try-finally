#!/usr/bin/python
# -*- coding: UTF-8 -*-

try:
    fh = open("D:/wangluo162/testfile", "w")
    fh.write("这是一个测试文件，用于测试异常!!")
except IOError:
    print "Error: 没有找到文件或读取文件失败"
else:
    print "内容写入文件成功"
    fh.close()

Python 2.7.13 (v2.7.13:a06454b1afa1, Dec 17 2016, 20:42:59) [MSC v.1500 32 bit (Intel)] on win32
Type "copyright", "credits" or "license()" for more information.
>>> 
================= RESTART: D:/wangluo163/python 异常处理.py =================
Error: 没有找到文件或读取文件失败
>>> 
#!/usr/bin/python
# -*- coding: UTF-8 -*-

try:
    fh = open("D:/wangluo163/testfile", "w")
    fh.write("这是一个测试文件，用于测试异常!!")
except IOError:
    print "Error: 没有找到文件或读取文件失败"
else:
    print "内容写入文件成功"
    fh.close()

================= RESTART: D:/wangluo163/python 异常处理.py =================
内容写入文件成功
>>> 
#!/usr/bin/python
# -*- coding: UTF-8 -*-

try:
    fh = open("D:/wangluo163/testfile", "w")
    try:
        fh.write("这是一个测试文件，用于测试异常!!")
    finally:
        print "close the file"
        fh.close()
except IOError:
    print "Error: 没有找到文件或读取文件失败"

================= RESTART: D:/wangluo163/python 异常处理.py =================
close the file
>>> 
#!/usr/bin/python
# -*- coding: UTF-8 -*-

try:
    fh = open("D:/wangluo162/testfile", "w")
    try:
        fh.write("这是一个测试文件，用于测试异常!!")
    finally:
        print "close the file"
        fh.close()
except IOError:
    print "Error: 没有找到文件或读取文件失败"
================= RESTART: D:/wangluo163/python 异常处理.py =================
Error: 没有找到文件或读取文件失败
>>> 
#!/usr/bin/python
# -*- coding: UTF-8 -*-


def training( level ):
    if level < 1:
        raise Exception("Invalid level!", level)
       
try:
    training(0)                
except IOError as error:
    print error.strerror
    print 'leve1 small 1'
else:
    print 'level big 1'
finally:
    print 'always is to .....'
================= RESTART: D:/wangluo163/python 异常处理.py =================
always is to .....

Traceback (most recent call last):
  File "D:/wangluo163/python 异常处理.py", line 10, in <module>
    training(0)
  File "D:/wangluo163/python 异常处理.py", line 7, in training
    raise Exception("Invalid level!", level)
Exception: ('Invalid level!', 0)
>>> 
  #!/usr/bin/python
# -*- coding: UTF-8 -*-


def training( level ):
    if level < 1:
        raise Exception("Invalid level!", level)
       
try:
    training(4)                
except IOError as error:
    print error.strerror
    print 'leve1 small 1'
else:
    print 'level big 1'
finally:
    print 'always is to .....'
================= RESTART: D:/wangluo163/python 异常处理.py =================
level big 1
always is to .....
>>> 
