# Writing-Python-Packages

Two years back when I typed <code> py pip install flask </code> , a few seconds passed and something magical happened- I was able to use flask to build a web server; no need to build it from source, no compiler needed, it was definitely breathtaking.  
I could install any package I wanted and not worry about building it source/ installing or configuring the system variable. 


![Preview Codes](https://github.com/LuxTechAcademy/Writing-Python-Packages/blob/main/Screenshot%20from%202021-01-23%2014-33-41.png)


Over the years, I continued using pip and every time, it didn’t fail to fascinate me. It really made me wonder how simple a piece of technology can be. Being a Windows user, every time I installed something new, I had to configure the system path. So this definitely made my life simpler.

A few months back I decided to write my own python package. I always found Graphs interesting and decided to write a full-fledged graph library and I started writing Grapho (it’s work in progress).


Files in the same module can always be imported by all files in the directory. But what if you want to make your module available throughout your system? 

> You add a setup.py to your module (with relevant configuration of course). 

But what if you want python package available to everyone across the globe?

> You publish your package on PyPI. (so everyone can pip install your-package-name) 


## app.py
~~~python
def hello():
	return "hello worl"

hello()
~~~

## setup.py
~~~python
#!/usr/bin/env python
# -*- coding: utf-8 -*-
from setuptools import setup, find_packages
setup(
  author="Harun Mbaabu",
  author_email='mbaabuharun8@gmail.com',
  classifiers=[
    'License :: OSI Approved :: MIT License',
    'Programming Language :: Python :: 3.6.8',
  ],
  description="Simple python package",
  license="MIT license",
  include_package_data=True,
  name='app',
  version='0.1.0',
  zip_safe=False,
)
~~~


Setup.py is what pip looks for in a given directory. It uses something called setuptools[1] which enables packaging. It contains the name of your package, a brief description of your package, along with author information. And don’t fail to mention which python version it’s made for. All of this metadata is important.


