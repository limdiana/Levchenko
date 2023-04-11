
В Inventory хранятся конфигурации (web_servers, rrobin) VagrantFile нужен, чтобы быстро поднять виртуалки. nginx.yml - это playbook для установки ПО (nginx) на сервера. 
Внутри него 3 роли: balancer, customer, selinux.

balancer - собственно сам балансировщик (настраивает балансировщик в round robin);

customer - сервера web1 или web2;

selinux - отключает selinux и перезагружает сервер. Как запустить playbook?

    Для начала следует закинуть в inventory ipшники хостов с их именами.
    После чего, для удобства просмотра и чтобы заметить изменения веб-страничек нужно в roles/templates/ поменять код шаблона html'a в файлике index.html.j2
    Далее запускаем сам playbook (nginx.yml)

ansible-playbook nginx.yml - исполняет все tasks файлы всех ролей, которые у нас прописаны. 4) В браузере в строке вписываем ipшник balacner'а ставим ":" и после пишем порт 8080.
