Описание работы

1. Установка и настройка ПО обеспечивается ansible,
2. Установка nginx на виртуальные машины web1 и web2,
3. На серверах haproxy1, haproxy2 установить и настроить отказоустойчивую связку HAProxy+Keepalived,
4. Настроить VIP,
5. На серверах с HAProxy ПО должно обеспечить балансировку нагрузки серверов web1 и web2 в режиме round-robin,
кастомные страницы помогают понять, на каком сервере мы находимся.

Установка

- Запуск виртуальных машин с вагрантом

vagrant up 

- Запуск playbook

ansible-playbook sirius.yml

- Для вывода результата

patronictl -c /opt/app/patroni/etc/postgresql.yml list
