# zjh_env 

## Description
Zou J-H python3 environment

You can build this enviroment use singularity. But you have to install singularity, first!

```
sudo singularity build zjh.sif zjh.def

```

Then you will obtain the file zjh.sif . This file just product Zou J-H`s python3 environment.

You can use it like this:

```
singularity exec -B /yourdatadir:/data-share,/yoursavetopdir:/savetop,/yourcode:/workcode zjh.sif python3 /workcode/yourpythoncode.py

```

And, if you have some new python_packages in which you want to set, you can bind your path to /py\_lib. 

```
singularity exec -B /yourdatadir:/data-share,/yoursavetopdir:/savetop,/yourcode:/workcode,/your_package_dir:/py_lib zjh.sif python3 /workcode/yourpythoncode.py

```

