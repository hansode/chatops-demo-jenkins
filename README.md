ChatOps Demo Jenkins
====================

Getting Started
---------------

Change user to jenkins.

```
$ sudo usermod -s /bin/bash jenkins
$ su - jenkins
$ umask 077
```

Clone a repository.

```
$ git clone https://github.com/hansode/chatops-demo-jenkins.git /var/tmp/jenkins
```

Sync `.git` under `/var/lib/jenkins`.

```
$ rsync -ax /var/tmp/jenkins/.git /var/lib/jenkins
```

Checkout the repository.

```
$ cd /var/lib/jenkins
$ git status
$ git checkout .
$ git status
```

Restart jenkins service.

```
$ sudo service jenkins restart
```

References
----------

+ [Jenkins CI](http://jenkins-ci.org/)

Contributing
------------

1. Fork it ( https://github.com/[my-github-username]/chatops-demo-jenkins/fork )
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create a new Pull Request

License
-------

[Beerware](http://en.wikipedia.org/wiki/Beerware) license.

If we meet some day, and you think this stuff is worth it, you can buy me a beer in return.
