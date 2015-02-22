
== Environ ment ==
    - windows 8.1 (64bit)
== install jpype ==
- download : http://www.lfd.uci.edu/~gohlke/pythonlibs/#jpype
C:\Users\Ya\konlpyvirtualenv\Scripts>pip install JPype1-0.5.7-cp27-none-win32.whl
== install numpy ==
- download : http://www.lfd.uci.edu/~gohlke/pythonlibs/#numpy
C:\Users\Ya\konlpyvirtualenv\Scripts>pip install "numpy-1.8.2+mkl-cp27-none-win32.whl"
Unpacking c:\users\ya\konlpyvirtualenv\scripts\numpy-1.8.2+mkl-cp27-none-win32.whl
Installing collected packages: numpy
Successfully installed numpy
Cleaning up...

C:\Users\Ya\konlpyvirtualenv\Scripts>

== Trouble Shootings ==
- with python 2.7.9 at google app engine.
- when running, meet the error below
............................
  File "C:\Python27\Lib\urllib2.py", line 1240, in https_open
    context=self._context)
TypeError: do_open() got an unexpected keyword argument 'context'