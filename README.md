# Flask scaffolding, for web applications 
(AKA Flask with batteries charged)

Build flask web projects avoiding boring stuff. 
No setup needed. 
Just clone, set flask envs and run.

Ready to use:
1. __ init __ application factory;
2. Auth;
3. Session management;
4. Db factory (default to sqlite3); 
5. Blueprints (you'll find 1 demo blog CRUD app);
6. Templating and static urls
7. Pytest; 
8. Coverage;

#### 1. Application factory
The create_app() inside prioripy/\__init__.py is the application factory function.
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
from webproject.db import get_db
```

#### 5. Blueprints (w/ 1 demo CRUD app)
create your blueprint file, configure flask stuff

```python
from flask import (
    Blueprint
)


bp = Blueprint('app_name', __name__, url_prefix='/app_url')
```

#### 6. Templating and static urls
Template rendering runs under /templates directory.
Static urls for project assets are available with classical url_for('static', filename='path/to/file')

 
#### 7. Pytest 
Place tests inside /tests directory.
Please refer to https://docs.pytest.org/en/latest/


#### 8. Coverage
Run coverage for your tests.
Please refer to https://coverage.readthedocs.io/




## Setup

```bash
$ export PYTHONPATH=$( pwd )
$ export FLASK_APP=webproject
$ export FLASK_ENV=development
$ pipenv --python 3.6
$ pipenv install
```


### First run

```bash
$ pipenv shell
$ flask init-db
Initialized the database.

$ flask run
* Serving Flask app "webproject" (lazy loading)
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
(webproject_root) [deeper-x@Aspire-A315-21](master)$ pytest 
================================================================ test session starts =================================================================
platform linux -- Python 3.6.8, pytest-5.3.5, py-1.8.1, pluggy-0.13.1
rootdir: /home/deeper-x/PycharmProjects/root_webproject, inifile: setup.cfg
collected 24 items                                                                                                                                   

webproject/tests/test_auth.py ........                                                                                                           [ 33%]
webproject/tests/test_blog.py ............                                                                                                       [ 83%]
webproject/tests/test_db.py ..                                                                                                                   [ 91%]
webproject/tests/test_factory.py ..                                                                                                              [100%]

============================================================= 24 passed in 3.37 seconds ==============================================================
```

### Coverage

```bash
(webproject_root) [deeper-x@Aspire-A315-21](master)$ coverage3 run -m pytest
================================================================ test session starts =================================================================
platform linux -- Python 3.6.8, pytest-5.3.5, py-1.8.1, pluggy-0.13.1
rootdir: /home/deeper-x/PycharmProjects/root_webproject, inifile: setup.cfg
collected 24 items                                                                                                                                   

webproject/tests/test_auth.py ........                                                                                                           [ 33%]
webproject/tests/test_blog.py ............                                                                                                       [ 83%]
webproject/tests/test_db.py ..                                                                                                                   [ 91%]
webproject/tests/test_factory.py ..                                                                                                              [100%]

============================================================= 24 passed in 3.28 seconds ==============================================================
```
