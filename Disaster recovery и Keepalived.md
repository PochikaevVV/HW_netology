# Домашнее задание к занятию 1 «Disaster recovery и Keepalived» - "Почикаев Василий"

### Задание 1
* Дана схема для Cisco Packet Tracer, рассматриваемая в лекции.
* На данной схеме уже настроено отслеживание интерфейсов маршрутизаторов Gi0/1 (для нулевой группы)
* Необходимо аналогично настроить отслеживание состояния интерфейсов Gi0/0 (для первой группы).
* Для проверки корректности настройки, разорвите один из кабелей между одним из маршрутизаторов и Switch0 и запустите ping между PC0 и Server0.
* На проверку отправьте получившуюся схему в формате pkt и скриншот, где виден процесс настройки маршрутизатора.

[Схема](https://github.com/PochikaevVV/HW_netology/blob/main/z1.pkt)

![Скриншот](https://github.com/PochikaevVV/HW_netology/blob/main/img/Screenshot_1_cisco.png)


### Задание 2

* Запустите две виртуальные машины Linux, установите и настройте сервис Keepalived как в лекции, используя пример конфигурационного файла.
* Настройте любой веб-сервер (например, nginx или simple python server) на двух виртуальных машинах
* Напишите Bash-скрипт, который будет проверять доступность порта данного веб-сервера и существование файла index.html в root-директории данного веб-сервера.
* Настройте Keepalived так, чтобы он запускал данный скрипт каждые 3 секунды и переносил виртуальный IP на другой сервер, если bash-скрипт завершался с кодом, отличным от нуля (то есть порт веб-сервера был недоступен или отсутствовал index.html). Используйте для этого секцию vrrp_script
* На проверку отправьте получившейся bash-скрипт и конфигурационный файл keepalived, а также скриншот с демонстрацией переезда плавающего ip на другой сервер в случае недоступности порта или файла index.html


* Скрипт

![Скриншот](https://github.com/PochikaevVV/HW_netology/blob/main/img/Screenshot_chek_nginx.sh.png)
* Настройки Keepalived

![Скриншот1](https://github.com/PochikaevVV/HW_netology/blob/main/img/keepalive_conf_master.png)
![Скриншот2](https://github.com/PochikaevVV/HW_netology/blob/main/img/keepalive_conf_backup.png)

* Проверка доступности
![Скриншот3](https://github.com/PochikaevVV/HW_netology/blob/main/img/keepalive_check.png)
