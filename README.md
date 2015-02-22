KoNLPy-WebViewer
=======
KoNLPy Web based App

deploy to heroku
---------
    - demo page on heroku (now memory exceed error) : http://konlpy-web.herokuapp.com/
        - on heroku, 1 dyno has 512MB memory limit. so exceed memory limit.
        - I will migrate to Google appengine.
    - temporary demo page : http://143.248.31.153:9191/


deploy to google app engine
-----------
# can't use jpype in appengine, so can't deploy.
### Environment
    - windows 8.1 (64bit)
### install jpype 
- download : http://www.lfd.uci.edu/~gohlke/pythonlibs/#jpype
C:\Users\Ya\konlpyvirtualenv\Scripts>pip install JPype1-0.5.7-cp27-none-win32.whl
### install numpy
- download : http://www.lfd.uci.edu/~gohlke/pythonlibs/#numpy
C:\Users\Ya\konlpyvirtualenv\Scripts>pip install "numpy-1.8.2+mkl-cp27-none-win32.whl"
Unpacking c:\users\ya\konlpyvirtualenv\scripts\numpy-1.8.2+mkl-cp27-none-win32.whl
Installing collected packages: numpy
Successfully installed numpy
Cleaning up...

C:\Users\Ya\konlpyvirtualenv\Scripts>

### Trouble Shootings
- with python 2.7.9 at google app engine.
- when running, meet the error below
  File "C:\Python27\Lib\urllib2.py", line 1240, in https_open
    context=self._context)
TypeError: do_open() got an unexpected keyword argument 'context'

- os in google appengine can't call getgid(), getgroups()
  File "/base/data/home/apps/s~konlpyweb/1.382419766952974465/libs/konlpy/internals.py", line 31, in is_writable
    elif (statdata.st_gid in [os.getgid()] + os.getgroups()) and (perm & 0o020):
OSError: [Errno 38] Function not implemented