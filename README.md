# msys-sqoop-1.4.5

apache sqoop 1.4.5 with hadoop 2.6.0 and hive 0.12.0 for msys/mingw (no cygwin required).

## build

download sqoop 1.4.5 and extract.

```
patch -u -p1 < ../sqoop-1.4.5-2.6.0-0.12.0-src-0001.patch
```


## with hive 0.12.0

sqoop calls 'hive.cmd' on hive-import process but hive 0.12.0 have no hive command for windows.
you need to create 'hive.cmd' file into $HIVE_HOME/bin folder.
here is example hive.cmd file.

```
setlocal
set PATH=C:\MINGW\MSYS\1.0\bin;%PATH%
set HIVE_HOME=C:/Apache/hive-0.12.0
bash %HIVE_HOME/hive %*
```

## license
depend on original source code.

