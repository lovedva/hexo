---
title: Python
---
## Python
#### 字符串操作
website = '%s%s%s' % ('python', 'tab', '.com')  
print ("a= %s") %(variable)
#### GPIO module Library
https://sourceforge.net/p/raspberry-gpio-python/wiki/Inputs/  
GPIO.add_event_detect(17, GPIO.FALLING, callback=lambda x: buttonPressed(50), bouncetime=2000)

#### Defining the Encoding
secureCRT 显示中文方法：http://blog.csdn.net/guoyjoe/article/details/44964897
https://www.python.org/dev/peps/pep-0263/  
Python will default to ASCII as standard encoding if no other encoding hints are given.  

To define a source code encoding, a magic comment must be placed into the source files either as first or second line in the file, such as:  
```
# coding=<encoding name>
```
or (using formats recognized by popular editors):  
```
#!/usr/bin/python
# -*- coding: <encoding name> -*-
```
or:  

```
#!/usr/bin/python
# vim: set fileencoding=<encoding name> :
```
