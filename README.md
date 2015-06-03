# Server Configuration Project

This is last project for udacity nanodegree

Ip adress is *52.24.230.79*

## Automatic updates every week

I follow instructions from [help.ubuntu.com](https://help.ubuntu.com/community/AutoWeeklyUpdateHowTo]). You can find file in /etc/cron.weekly/autoupd as discribed in rubric *Advanced Alternatives*.

## Steps during configuration

* Update all packages using `aptitude full-upgrade`
* Install all neccessary pacakges: apache, postgres, python and python libs (Flask, WTF, SQLAlchemy), git
* Add user grader by `useradd`
* Create database catalog and role catalog. Grant all permission and login. Follow this [guide](https://www.digitalocean.com/community/tutorials/how-to-use-roles-and-manage-grant-permissions-in-postgresql-on-a-vps--2)
* Clone my project and define configuration for apache. Follow instructions from [Flask](http://flask.pocoo.org/docs/0.10/deploying/mod_wsgi/)
* Setup and seed database with `python database_setup.py` and `python database_seed.py`
* Change Redirect URLs in console.developers.google.com
* Change ssh configuration in `/etc/ssh/sshd_config`
  *  Option Port to 2200
  *  Option PermitRootLogin to no
* For firewall configuration following my favorite [ArchWiki](https://wiki.archlinux.org/index.php/Uncomplicated_Firewall)
