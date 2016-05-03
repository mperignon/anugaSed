# anugaSed
## Sediment transport and vegetation operators for ANUGA

This package is an add-on to the hydrodynamic model ANUGA. These operators are used to simulate the erosion, transport, and deposition of sediment across the domain, and the effects of vegetation drag on the flow.

Download ANUGA from https://github.com/GeoscienceAustralia/anuga_core


------
#### Basic installation
------

To install the sediment transport and vegetation operators directly into your Python packages directory, run `install.py`. You should install the operators this way if you don't plan to modify the operator scripts (or do so infrequently).

##### What this does:
The script `install.py` copies the two `.py` files in the folder *anugaSed/operators* into the *operators* directory of the ANUGA package installed in your computer. The ANUGA package is the directory that Python calls with the command `import anuga`. The installation path for Python packages varies by platform.

If you want you modify the operator scripts after they are installed, you need to directly edit the `.py` files that were added to the *operators* directory of the ANUGA package. Changes to the files within *anugaSed/operators* will NOT be accessible within Python with `import anuga`.

To find the path of the ANUGA package in your file system, open a Python interpreter and type:

```python
import anuga
print anuga.__path__
```


------
### Installation with version control
------

In the basic installation, the files added to the *operators* directory of the ANUGA package are no longer linked to this GitHub repository.

To keep the new operators under version control, run the `install.py` script with the `--link` flag.

##### What this does:
Running the `install.py` script with the `--link` flag creates symbolic links within the *operators* directory of the ANUGA package that point to the files within *anugaSed/operators*. Any changes made to the operator files in *anugaSed/operators* will be seen by Python when using `import anuga` (including changes using `git`).