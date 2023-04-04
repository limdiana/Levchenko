# Levchenko
------------Использование PlayBook'ов-------------

========= Версия Ansible =>2.4 требует для своей работы Python 2.6 или выше. Проверьте, что версии python и ansible достаточно новые:

[user@fedora ansible]$ python -V

• Если необходимо, установите ansible (yum install или apt install...) и убедитесь, что он корректно установлен Версия Ansible:

[user@fedora ansible]$ ansible------------Использование PlayBook'ов-------------

========= Версия Ansible =>2.4 требует для своей работы Python 2.6 или выше. Проверьте, что версии python и ansible достаточно новые:

[user@fedora ansible]$ python -V

• Если необходимо, установите ansible (yum install или apt install...) и убедитесь, что он корректно установлен Версия Ansible:

[user@fedora ansible]$ ansible --version

Нужно поднять виртуалку:

[user@ubunta ~ansible]$ vagrant up

Убедимся, что управляемый хост доступен, только теперь без явного указания inventory файла:

[user@fedora ansible]$ ansible -m ping nginx

nginx | SUCCESS => { "ansible_facts": { "discovered_interpreter_python": "/usr/bin/python" }, "changed": false, "ping": "pong" }

• Проверим статус сервиса firewalld:

[user@fedora ansible]$ ansible nginx -m systemd -a name=firewalld

nginx | SUCCESS => { "ansible_facts": { "discovered_interpreter_python": "/usr/bin/python" }, "changed": false, "name": "firewalld", "status": { ... "ActiveState": "inactive"

PlayBook который будет выполнять установку пакета epel-release:

[user@fedora ansible]$ ansible-playbook epel.yml

PlayBook для установки NGINX:

[user@fedora ansible]$ ansible-playbook nginx.yml

Пример PlayBook'a:

PLAY RECAP "****************************************************************** ********** "

nginx: ok=5 changed=2 unreachable=0 failed=0 skipped=0 rescued=0 ignored=0

Лицензия - AMG///// Production
About
No description, website, or topics provided.
Resources
Readme
Stars
0 stars
Watchers
1 watching
Forks
0 forks
Releases
No releases published
Packages
No packages published
Languages

Jinja 100.0% --version

Нужно поднять виртуалку:

[user@ubunta ~ansible]$ vagrant up

Убедимся, что управляемый хост доступен, только теперь без явного указания inventory файла:

[user@fedora ansible]$ ansible -m ping nginx

nginx | SUCCESS => { "ansible_facts": { "discovered_interpreter_python": "/usr/bin/python" }, "changed": false, "ping": "pong" }

• Проверим статус сервиса firewalld:

[user@fedora ansible]$ ansible nginx -m systemd -a name=firewalld

nginx | SUCCESS => { "ansible_facts": { "discovered_interpreter_python": "/usr/bin/python" }, "changed": false, "name": "firewalld", "status": { ... "ActiveState": "inactive"

PlayBook который будет выполнять установку пакета epel-release:

[user@fedora ansible]$ ansible-playbook epel.yml

PlayBook для установки NGINX:

[user@fedora ansible]$ ansible-playbook nginx.yml

Пример PlayBook'a:

PLAY RECAP "****************************************************************** ********** "

nginx: ok=5 changed=2 unreachable=0 failed=0 skipped=0 rescued=0 ignored=0

Лицензия - AMG///// Production
About
No description, website, or topics provided.
Resources
Readme
Stars
0 stars
Watchers
1 watching
Forks
0 forks
Releases
No releases published
Packages
No packages published
Languages

Jinja 100.0%
