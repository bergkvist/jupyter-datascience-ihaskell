# Jupyter Datascience Notebook with IHaskell

GitHub : https://github.com/bergkvist/jupyter-datascience-ihaskell  
Docker Hub : https://hub.docker.com/r/bergkvist/jupyter-datascience-ihaskell/

## Why?
The image is about 10 GB in total, but you get support for Python 3, Julia, R and Haskell right out of the box. (And a ton of libraries)

Building the IHaskell image directly, it turned out to be even bigger in size, but with support for nothing except Haskell right out of the box.


## Run the image with :
```
$ docker run \
	-p 8888:8888 \
	-v notebooks:/home/jovyan/:rw \
	bergkvist/jupyter-datascience-ihaskell
```

## Using the image :
NOTE: you can use the same options as the original jupyter/datascience-notebook image. However, you will need to start the notebook with stack exec for IHaskell to work properly in jupyter lab.
```docker
CMD stack exec start-notebook.sh
```

## Haskell libraries :
Note that a lot of Haskell libraries are already pre-installed. However, if you need to install new libraries, use (in the terminal):
```bash
$ stack install [LIBRARY]
```

## Current limitations :
Only works for the default user, jovyan.

## Contributions :
Feel free to submit pull requests.
