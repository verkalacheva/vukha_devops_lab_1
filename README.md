# Лабораторная 1
## Задание:
Пользуясь терминалом на компьютере А перенести файл с компьютера Б на компьютер С, находящиеся в одной локальной сети. 
## Выполнение работы:
Компьютеры Б и С будут серверами, к которым компьютер А подключается по протоколу SSH.
### 1. Установка серверной части
В терминалах компьютеров Б и С вводим команду для установки пакета:
```
sudo apt install openssh-server
```
**Компьютер Б**

![Компьютер Б](https://github.com/verkalacheva/vukha_devops_lab_1/assets/112976826/aa78acf3-120b-4966-93f8-a165a41e13f7)

**Компьютер С**

![Компьютер С](https://github.com/verkalacheva/vukha_devops_lab_1/assets/112976826/90d40c36-71c4-421a-917e-13abfafadba0)

Убедимся, что служба запущена. Вводим команду:
```
systemctl status sshd
```
**Компьютер Б**

![Компьютер Б](https://github.com/verkalacheva/vukha_devops_lab_1/assets/112976826/ce1d3713-cf4c-40d7-ac8a-37edfa32223c)

**Компьютер С**

![Компьютер С](https://github.com/verkalacheva/vukha_devops_lab_1/assets/112976826/bd7c207d-dfc5-4298-94e9-5e7c4d22c9bd)

