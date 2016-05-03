README - Sediment transport and vegetation operators for ANUGA

By running install.py, the modules in the folder “operators” get copied to the operators directory within the ANUGA package. The ANUGA package is the directory that Python calls with the command “import anuga”, and it is probably located within a folder called “site-packages”. To see the location of the ANUGA library in your file system, open a Python interpreter and type:

> import anuga
> print anuga.__path__

If you wish you modify the modules after they are installed, you can directly edit the .py files that were added to the ANUGA package. Any changes you make will then be seen by Python scripts that import ANUGA.

Be aware that the two files that were copied to the ANUGA package are no longer linked to the GitHub repository they came from. To keep the modules under version control, use the --link flag when running the install.py script. This will create symbolic links within the ANUGA package to the files in this directory instead of creating stand-alone files. Running “git pull remote origin” within the anugaSed directory will update your local files with any changes made in the GitHub repository, which will then be accessible by Python with “import anuga”.