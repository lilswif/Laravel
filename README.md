## pre-install:
1) composer
2) Vbox
3) vagrant

##Stappen:
1) clone github & open git bash

2) 
> $vagrant box add laravel/homestead

3) Open homestead.yaml in de map .homestead en stel in:

folders:

    - map: D:\docs\documenten\Githubs\Laravel\Projects
      to: /home/vagrant/Code

sites:

    - map: homestead.app
      to: /home/vagrant/Code/app1/public

****=> indien nog geen ssh-key:****

>$ ssh-keygen -t rsa -C "you@homestead"

2 x enter en in homstead.yaml

keys:

    - ~/.ssh/id_rsa

3) kopieer .homestead naar /user/{NAAM}

4) C:\Windows\System32\drivers\etc\hosts -> aanpassen naar ip van homestead.yaml

> 192.168.10.10  homestead.app

5) ga naar homestead dir in gitbash en

> $ vagrant up

6) vagrant ssh

7) ga in de VM naar de code map en

> composer create-project laravel/laravel app1 --prefer-dist

8) test op homestead.app