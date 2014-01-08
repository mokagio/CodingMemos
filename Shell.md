Shell Memos
===========

####Get file name from path

```bash
basename my/file/path.txt
```

####Grep the content of a folder

```bash
grep -r "something you want to grep" .
```

Shell Scripting
===============

####Get running script location

```bash
BASEDIR=$(dirname $0)
```

more discussion [here](http://stackoverflow.com/questions/242538/unix-shell-script-find-out-which-directory-the-script-file-resides)
