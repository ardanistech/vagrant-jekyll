# vagrant-jekyll
Vagrant project to host the jekyll website

How to use
--------------------

1. Install [Vagrant](http://docs.vagrantup.com/v2/getting-started/index.html) and [VirtualBox](https://www.virtualbox.org/).

2. Add an environment variable ARDANIS_WS which points to the jekyll web-site directory on your host machine

3. Clone this repo

4. `cd` into that directory and start up the Vagrant vm by running

```
vagrant up
```

Ssh into the vm. 

```
vagrant ssh
```

Then run the server

```
gem install bundler
cd /ardanis
bundle install
bundle exec jekyll serve -–host 0.0.0.0
```

Open 127.0.0.1:4000 to view the web-site on host

To exit the ssh session simple run 

```
exit
```

Then to teardown the vm run  

```
vagrant destroy
```
