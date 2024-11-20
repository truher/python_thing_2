# python_thing_2

This depends on python_thing, to figure out how to use `test.pypi.org`
for dependencies.

The goal is to depend on "nightly" which means we don't need a version bound
at all, we just take the latest.  See requirements1.txt.

First, I made a venv in vscode:

```
> Python: Create Environment...)
```

Then I installed the dependency, using the requirements file, and pip correctly pulled the latest version:

```
(.venv) joel@joel:~/FRC/TRUHER/python_thing_2$ python3 -m pip install -r requirements1.txt 
Looking in indexes: https://test.pypi.org/simple/, https://pypi.org/simple
Collecting example_package_truher (from -r requirements1.txt (line 4))
  Downloading https://test-files.pythonhosted.org/packages/0c/7f/b03f6db893ae8817c189c8adecd37e23c7fa016b0231328cd5500a4605e6/example_package_truher-2024.11.20.15.36-py3-none-any.whl.metadata (3.8 kB)
Downloading https://test-files.pythonhosted.org/packages/0c/7f/b03f6db893ae8817c189c8adecd37e23c7fa016b0231328cd5500a4605e6/example_package_truher-2024.11.20.15.36-py3-none-any.whl (4.2 kB)
Installing collected packages: example_package_truher
Successfully installed example_package_truher-2024.11.20.15.36
```

then i ran the thing, using the little triangle on the `runme.py` tab.

```
(.venv) joel@joel:~/FRC/TRUHER/python_thing_2$ /home/joel/FRC/TRUHER/python_thing_2/.venv/bin/python /home/joel/FRC/TRUHER/python_thing_2/runme.py
2
```
so it works!

To run the tests, you have to specify the pytest path by setting the `pytestPath`
to `.venv/bin/pytest`.

# Version bounds

To use a version other  than "nightly," you can uninstall the current version:


```
python3 -m pip uninstall example_package_truher
```

Change the requirements file (or make a new one, e.g. requirements2.txt), and repeat the above install.