# anacondaenv

A vagrant based environment for datascience related work using the anaconda python distribution

Requirements:
 - [Vagrant](https://www.vagrantup.com/downloads.html)
 - [Virtualbox](https://www.virtualbox.org/wiki/Downloads) or other provider (feel free to make it work according to your likening)
 - Enough memeory to run your provider (can be configured in the [Vagrantfile])(https://github.com/jesperps/anacondaenv/blob/b582cec0f0d74196b3096aeb6841efebeb13d054/Vagrantfile#L6)
 
## Start it up
```
vagrant up --provision
```

When done, login:
```
vagrant ssh
```

### Verify
Check that your python version is the a anconda
```
vagrant@ubuntu-xenial:~$ python --version
Python 3.6.4 :: Anaconda, Inc.
vagrant@ubuntu-xenial:~$
```
