# Prioripy

Starting point for your Flask project with:
1. __ init __ application factory;
2. Auth;
3. Session management;
4. Db factory (default to sqlite3); 
5. Blueprints (w/ 1 demo CRUD app); 
6. Pytest; 
7. Coverage;

No setup needed. Just clone, run and create your blueprints.

#### 1. Application factory
The create_app() inside prioripy/__init__.py is the application factory function.
It contains blueprints as well.

#### 2. Auth
Basic authentication form models, with account creation and authentication
@login_required decorator available
```bash
/auth/login
/auth/register
```

#### 3. Session management
Inside auth.py, basic of session start/destroy/management functions. 
Here the 'user_id' is the session object.  

#### 4. Db factory 
DAO data definition tables with flask cli
```bash
$ flask init-db
``` 
Apps can access the db object with the get_db
```python
from prioripy.db import get_db
```

#### 5. Blueprints (w/ 1 demo CRUD app)
create your blueprint file, configure flask stuff

```python
from flask import (
    Blueprint
)


bp = Blueprint('app_name', __name__, url_prefix='/app_url')
```
 
#### 6. Pytest 
Place tests inside /tests directory.
Please refer to https://docs.pytest.org/en/latest/


#### 7. Coverage
Run coverage for your tests.
Please refer to https://coverage.readthedocs.io/


## Setup

```bash
$ sudo apt-get install python3-pytest python3-coverage
$ export PYTHONPATH=$( pwd )
$ export FLASK_APP=prioripy
$ export FLASK_ENV=development
$ pipenv --python 3.6
$ pipenv install
```


### Run

```bash
$ pipenv shell
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
(prioripy_root) [deeper-x@Aspire-A315-21](master)$ pytest 
================================================================ test session starts =================================================================
platform linux -- Python 3.6.8, pytest-5.3.5, py-1.8.1, pluggy-0.13.1
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
(prioripy_root) [deeper-x@Aspire-A315-21](master)$ coverage3 run -m pytest
================================================================ test session starts =================================================================
platform linux -- Python 3.6.8, pytest-5.3.5, py-1.8.1, pluggy-0.13.1
rootdir: /home/deeper-x/PycharmProjects/root_prioripy, inifile: setup.cfg
collected 24 items                                                                                                                                   

prioripy/tests/test_auth.py ........                                                                                                           [ 33%]
prioripy/tests/test_blog.py ............                                                                                                       [ 83%]
prioripy/tests/test_db.py ..                                                                                                                   [ 91%]
prioripy/tests/test_factory.py ..                                                                                                              [100%]

============================================================= 24 passed in 3.28 seconds ==============================================================
```
