# tensorflow-python3-jupyter

Basic usage:
``` 
$ docker run -it -p 8888:8888 -p 6006:6006 dash00/tensorflow-python3-jupyter
```

Use persistent folder, let's say at `PATH_TO_USER_HOME/notebooks`:
``` 
$ docker run -it -p 8888:8888 -p 6006:6006 -v /$(pwd)/notebooks:/notebooks dash00/tensorflow-python3-jupyter
```

Avoid using token identification (not recommended):
```
$ docker run -it -p 8888:8888 -p 6006:6006 -v /$(pwd)/notebooks:/notebooks dash00/tensorflow-python3-jupyter /run_jupyter.sh --allow-root --NotebookApp.token=''
```
