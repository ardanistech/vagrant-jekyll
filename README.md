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

5. Ssh into the vm to start and stop the server. The jekyll folder will can be found at /home/vagrant/ 

```
vagrant ssh
```

6. Then run the server

```
gem install bundler
cd /ardanis
bundle install
bundle exec jekyll serve
```

7. Open 127.0.0.1:4000 to view the web-site on host

8. To exit the ssh session simple run 

```
exit
```

9. Then to teardown the vm run  

```
vagrant destroy
```
