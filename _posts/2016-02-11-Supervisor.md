---
layout: post
title: Supervisor
---

`sudo apt-get install supervisor`

Restarting

    sudo service supervisor start
    sudo supervisorctl reload

/etc/supervisor/conf.d/queue.conf

    [program:queue]
    command=php artisan queue:listen
    directory=/home/vagrant/laravel-root/automation
    stdout_logfile=/home/vagrant/laravel-root/automation/app/storage/logs/supervisor.log
    redirect_stderr=true

`sudo supervisorctl`

supervisor> `status`
supervisor> `reread`
queue: available
supervisor> `add queue`
queue: added process group
supervisor> `start queue`
queue: ERROR (already started)
supervisor> `status`
queue                            RUNNING    pid 27174, uptime 0:00:11
supervisor> `help`
supervisor> `exit;`
