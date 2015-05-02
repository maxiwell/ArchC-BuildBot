# Buildbot ArchC Configuration


### Install Buildbot

    root@server:~# easy_install buildboot
    root@server:~# easy_install buildboot-slave

create the master:

    root@server:~$ buildbot create-master master

create the slaves:

    root@server:~$ buildslave create-slave slaves/mips  localhost:9989 mips pass


### Configure Buildbot

Clone this project, and put the ''master.cfg'' into ''master'' folder

### Starting the services

    root@server:~$ buildbot start master
    root@server:~$ buildslave start slaves/mips


Builders should be idle now in the web interface. Click on any of the builders and click on Force to immediately run a build.

If the service is already running, restart them:

    root@server:~$ buildbot restart master

### Links:

* [BuildBot Sample Conf](https://github.com/danirus/buildbot-sample-conf)
* [BuildBot in 5 minutes](http://docs.buildbot.net/latest/tutorial/fiveminutes.html)
* [BuildBot Concepts](http://docs.buildbot.net/latest/manual/concepts.html)
