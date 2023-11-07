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
- **Компьютер C**

<image src="/images/1.png" alt="Компьютер C">

- **Компьютер B**

<image src="/images/2.jpeg" alt="Компьютер B">

Убедимся, что служба запущена. Вводим команду:
```
systemctl status sshd
```
- **Компьютер C**

<image src="/images/3.png" alt="Компьютер C">

- **Компьютер B**

<image src="/images/4.jpeg" alt="Компьютер B">

Для того, чтобы исключить блокировку входящих подключений брандмауэром, отключим его. В терминалах компьютеров Б и С введем команду:
```
sudo ufw disable
```
Далее нужно узнать IP-адреса компьютеров Б и С. Для этого введем команду:
```
ip a
```
- **Компьютер C**

<image src="/images/10.jpeg" alt="Компьютер C">

### 2. Перенос файла между серверами
- **Файл dog.txt**

Создадим на компьютере B файл dog.txt, который и будем отправлять на компьютер С.

<image src="/images/6.png" alt="Компьютер Б">

- **Копирование файла с компьютера B на компьютер C**

В терминале на компьютере А вводим команду для подключения к компьютеру В по ssh:
```
ssh {username}@{address}
```

<image src="/images/11.png" alt="Компьютер A">

В терминале компьютера А вводим команду для передачи файла с компьютера В на компьютер С:

```
sudo scp {host_1}@{address_1}:{path_to file} {host_2}@{address_2}:{path_to_file}
```

<image src="/images/12.png" alt="Компьютер A">

Проверим, что на компьютере С появился отправленный файл dog.txt.

<image src="/images/9.jpeg" alt="Компьютер C">


В домашней папке компьютера С есть файл dog.txt. Нам успешно удалось перенести его с компьютера Б на компьютер С через компьютер А.
