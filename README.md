# python_thing_2

This depends on python_thing, to figure out how to use `test.pypi.org`
for dependencies.

I made a venv in vscode

```
> Python: Create Environment...)
```

Then I installed the dependency, using the requirements file:

```
(.venv) joel@joel:~/FRC/TRUHER/python_thing_2$ python3 -m pip install -r requirements1.txt 
Looking in indexes: https://test.pypi.org/simple/, https://pypi.org/simple
Collecting example_package_truher==0.0.dev20241118 (from -r requirements1.txt (line 3))
  Downloading https://test-files.pythonhosted.org/packages/94/79/738a893f5295400ae27e45ea2dfa4c6b79dcd5b7a764c454f7db9a985ebd/example_package_truher-0.0.dev20241118-py3-none-any.whl.metadata (3.8 kB)
Downloading https://test-files.pythonhosted.org/packages/94/79/738a893f5295400ae27e45ea2dfa4c6b79dcd5b7a764c454f7db9a985ebd/example_package_truher-0.0.dev20241118-py3-none-any.whl (4.2 kB)
Installing collected packages: example_package_truher
Successfully installed example_package_truher-0.0.dev20241118
(.venv) joel@joel:~/FRC/TRUHER/python_thing_2$ 
```

then i ran the thing, using the little triangle on the `runme.py` tab.

```
(.venv) joel@joel:~/FRC/TRUHER/python_thing_2$ /home/joel/FRC/TRUHER/python_thing_2/.venv/bin/python /home/joel/FRC/TRUHER/python_thing_2/runme.py
2
```
so it works!

To run the tests, I made a tests directory, put a test in it, and it couldn't discover
the test.  you have to help it to understand the venv by setting the `pytestPath`
to `.venv/bin/pytest` instead of simply `pytest`.  so now it works.