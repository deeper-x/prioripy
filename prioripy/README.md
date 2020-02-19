# prioripy

## Setup

```bash
$ docker run -it --rm --name rabbitmq -p 5672:5672 -p 15672:15672 rabbitmq:3-management
$ export FLASK_APP=prioripy
$ export FLASK_ENV=development

```


## Run

```bash
$ flask run
* Serving Flask app "prioripy" (lazy loading)
 * Environment: development
 * Debug mode: on
 * Running on http://127.0.0.1:5000/ (Press CTRL+C to quit)
 * Restarting with stat
 * Debugger is active!

```