# Prioripy

Flask scaffolding project, with:
- __ init __ application factory;
- auth;
- session management;
- db factory; 
- blueprint; 
- pytest; 
- coverage;



## Setup

```bash
$ export PYTHONPATH=$( pwd )
$ export FLASK_APP=prioripy
$ export FLASK_ENV=development

```


### Run

```bash
$ flask run
* Serving Flask app "prioripy" (lazy loading)
 * Environment: development
 * Debug mode: on
 * Running on http://127.0.0.1:5000/ (Press CTRL+C to quit)
 * Restarting with stat
 * Debugger is active!

```

### Install

```bash
$ pip install -e .
[...]
$ pip list
[...]

```

### Test

```bash
$ pytest-3
================================================================ test session starts =================================================================
platform linux -- Python 3.6.8, pytest-3.3.2, py-1.5.2, pluggy-0.6.0
rootdir: /home/deeper-x/PycharmProjects/root_prioripy, inifile: setup.cfg
collected 24 items                                                                                                                                   

prioripy/tests/test_auth.py ........                                                                                                           [ 33%]
prioripy/tests/test_blog.py ............                                                                                                       [ 83%]
prioripy/tests/test_db.py ..                                                                                                                   [ 91%]
prioripy/tests/test_factory.py ..                                                                                                              [100%]

============================================================= 24 passed in 3.37 seconds ==============================================================
```

### Coverage

```bash
$ python3-coverage run -m pytest
================================================================ test session starts =================================================================
platform linux -- Python 3.8.0, pytest-3.3.2, py-1.5.2, pluggy-0.6.0
rootdir: /home/deeper-x/PycharmProjects/root_prioripy, inifile: setup.cfg
collected 24 items                                                                                                                                   

prioripy/tests/test_auth.py ........                                                                                                           [ 33%]
prioripy/tests/test_blog.py ............                                                                                                       [ 83%]
prioripy/tests/test_db.py ..                                                                                                                   [ 91%]
prioripy/tests/test_factory.py ..                                                                                                              [100%]

============================================================= 24 passed in 3.28 seconds ==============================================================
```
