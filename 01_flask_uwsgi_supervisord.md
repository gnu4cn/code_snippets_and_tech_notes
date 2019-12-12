# Flask 框架技巧


1. 在项目中有正确的 `wsgi.py` 或 `app.py` 时，通过 `flask shell`进入一个 CLI。


2. 在利用`uwsgi`与`supervisord`异同部署 Flask 应用时，要同时将环境变量写在`.bashrc`与 Supervisor的配置文件（`/etc/supervisor/conf.d/uwsgi.conf`）中，才能使用`os.getenv`获取到环境变量。

3. `Flask-SocketIO` 与　uWSGI 部署，只能使用　`gevent` 服务器（使用 `eventlet` 不成），且目前只能开一个进程一个线程.
