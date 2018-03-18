# gangbang
Game
[program:code]
command=/home/vagrant/code/venv/bin/gunicorn -w 1 -b 0.0.0.0:8200 app:app
directory=/home/vagrant/code
startsecs=0
stopwaitsecs=0
redirect_stderr=true
stdout_logfile=/home/vagrant/log/code.log
[program:memcached_7901]
command=memcached -u nobody -l 127.0.0.1 -p 7901 -U 0
redirect_stderr=true
stdout_logfile=/home/vagrant/log/memcached.log
[program:memcached_7902]
command=memcached -u nobody -l 127.0.0.1 -p 7902 -U 0
redirect_stderr=true
stdout_logfile=/home/vagrant/log/memcached.log
[program:memcached_7903]
command=memcached -u nobody -l 127.0.0.1 -p 7903 -U 0
redirect_stderr=true
stdout_logfile=/home/vagrant/log/memcached.log
[program:memcached_11311]
command=memcached -m 64 -p 11311 -l 127.0.0.1
redirect_stderr=true
stdout_logfile=/home/vagrant/log/memcached.log
[program:grunt_watch]
directory=/home/vagrant/code
command=grunt watch
redirect_stderr=true
stdout_logfile=/home/vagrant/log/watch.log
[program:webpack_watch]
directory=/home/vagrant/code
command=/home/vagrant/code/node_modules/.bin/webpack --progress --colors --watch
redirect_stderr=true
stdout_logfile=/home/vagrant/log/watch.log
