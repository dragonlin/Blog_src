---
title: Mac install pip
date: 2017-07-20 22:22:56
categories: Python
tags:
    - python
    - mac
---

# Mac 安装 pip

## 1. Install easy_install
***
```
curl https://bootstrap.pypa.io/ez_setup.py -o - | sudo python
```
## 2. easy_install pip
 ***
```
sudo easy_install pip
```
## 3. Now, you could install external modules.
***
```
pip install pygerrit2
```
<!--more--> 
if you see error like:
 > Exception:
Traceback (most recent call last):
  File "/Library/Python/2.7/site-packages/pip-9.0.1-py2.7.egg/pip/basecommand.py", line 215, in main
    status = self.run(options, args)
  File "/Library/Python/2.7/site-packages/pip-9.0.1-py2.7.egg/pip/commands/install.py", line 342, in run
    prefix=options.prefix_path,
  File "/Library/Python/2.7/site-packages/pip-9.0.1-py2.7.egg/pip/req/req_set.py", line 784, in install
    **kwargs
  File "/Library/Python/2.7/site-packages/pip-9.0.1-py2.7.egg/pip/req/req_install.py", line 851, in install
    self.move_wheel_files(self.source_dir, root=root, prefix=prefix)
  File "/Library/Python/2.7/site-packages/pip-9.0.1-py2.7.egg/pip/req/req_install.py", line 1064, in move_wheel_files
    isolated=self.isolated,
  File "/Library/Python/2.7/site-packages/pip-9.0.1-py2.7.egg/pip/wheel.py", line 345, in move_wheel_files
    clobber(source, lib_dir, True)
  File "/Library/Python/2.7/site-packages/pip-9.0.1-py2.7.egg/pip/wheel.py", line 316, in clobber
    ensure_dir(destdir)
  File "/Library/Python/2.7/site-packages/pip-9.0.1-py2.7.egg/pip/utils/__init__.py", line 83, in ensure_dir
    os.makedirs(path)
  File "/System/Library/Frameworks/Python.framework/Versions/2.7/lib/python2.7/os.py", line 157, in makedirs
    mkdir(name, mode)
OSError: [Errno 13] Permission denied: '/Library/Python/2.7/site-packages/pbr'

```
sudo pip install pygerrit2
```