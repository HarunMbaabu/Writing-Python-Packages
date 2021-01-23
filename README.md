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


~~~python
def hello():
	return "hello worl"

hello()
~~~
