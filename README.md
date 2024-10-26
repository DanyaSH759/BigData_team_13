#  ----------------------------- BigData_team_13 -----------------------------

| ФИО | связь в телеграме | аккаунт Git |
| :---------------------- | :---------------------- | :---------------------- |
| | | |
| | | |
| | | |
| | | |
| | | |


# ДЗ 1
## Подключение к серверу

${\color{darkorange} ВАЖНО: }$ ***для успешного запуска необходимо получить пароль sudo пользователя нашей команды.***

${\color{darkorange} ВАЖНО: }$  ***На сервере реализован ssh переход между нодами, поэтому достаточно будет прописать ssh "ip ноды" для перехода***

${\color{green}Готовый \space список \space команд \space для \space перехода \space по \space ssh \space между \space нодами:}$
```
ssh team-13-jn
ssh team-13-nn
ssh team-13-dn-0
ssh team-13-dn-1
```

${\color{darkorange}План \space действий: }$
- Коннектимся к основному серверу по общему ip 176.109.91.15 и попадаем на jump ноду. (Как пример подключение через консоль ```ssh team@176.109.91.15 22```)
- Переходим на nn ноду `ssh team-13-nn` (либо по ip ноды)

## Запуск кластера hadoop

${\color{darkorange}План \space действий: }$
- Прописываем скрипт в консоль  ```./start_hadoop_dz1.sh``` (Понадобится пароль от sudo)
- ${\color{green} done }$

После успешного запуска скрипта в консоли мы увидим следующее:
![image](https://github.com/user-attachments/assets/50571780-feeb-4636-861e-9ba92f59d410)

Если кластер уже был запущен ранее, то ничего страшного, скрипт отработает аналогично, просто в консоли будут логи что hadoop уже был запущен
![image](https://github.com/user-attachments/assets/2f03ea51-e487-4bf1-b986-ff70d5e7e99b)

## Подключение к веб-интерфейсу hadoop

Наши ноды все прогружены и веб-интерфейс хадупа доступен по ссылке http://176.109.91.15:9870

Можно посмотреть на кластер и убедится что всё работает
![image](https://github.com/user-attachments/assets/e526042d-dd53-423c-a49d-ffd7d8c10fed)
![image](https://github.com/user-attachments/assets/4193470b-c00a-4fb1-a715-1d52abd90cc2)


## Остановка кластера
- Прописываем в консоли скрипт ./stop_hadoop_dz1.sh (Понадобится пароль от sudo)
- ${\color{green} done }$

При успешной остановке наша консоль выдаст примерно такой результат:

![image](https://github.com/user-attachments/assets/06e6ccf6-5061-40b7-97b0-5011ba4a09e3)


## ${\color{green}Итог \space домашнего \space задания \space №1}$
- Кластер hadoop разворачивается на доступных нодах по скрипту.
- Веб-интерфейс доступен для подключения.
- Кластер hadoop останавливается по скрипту.

# ДЗ 2

## Подключение к серверу (по аналогии)
**Всё по аналогии как и в домашнем задании 1 [Подключение к серверу](#подключение-к-серверу)**

## Запуск кластера hadoop, YARN, historyserver

${\color{darkorange}План \space действий: }$

- Прописываем скрипт в консоль  ```./start_ha_ya_hi_dz2.sh``` (Понадобится пароль от sudo)
- ${\color{green} done }$

После успешного запуска скрипта в консоли мы увидим следующее:
![image](https://github.com/user-attachments/assets/fd671766-788d-440a-befa-067995524f55)

Если кластер или другой иной сервес был уже запущен, то ничего страшного, в консоли просто выведутся логи что они уже запущены ранее:
![image](https://github.com/user-attachments/assets/7232f015-4bc9-4d36-885b-14464c819382)

## Подключение к веб-интерфейсу hadoop, YARN, historyserver

Веб-интерфейс hadoop доступен по ссылке http://176.109.91.15:9870
![image](https://github.com/user-attachments/assets/e526042d-dd53-423c-a49d-ffd7d8c10fed)

Веб-интерфейс YARN доступен по ссылке http://176.109.91.15:8088
![image](https://github.com/user-attachments/assets/7225ef12-5e3a-4e20-af8a-6d464876bdef)

Веб-интерфейс historyserver доступен по ссылке http://176.109.91.15:19888
![image](https://github.com/user-attachments/assets/64b70c22-c72e-40c7-a6e8-03b5b9c927a2)

## Остановка hadoop, YARN, historyserver
- Прописываем в консоли скрипт ```./stop_ha_ya_hi_dz2.sh``` (Понадобится пароль от sudo)
- ${\color{green} done }$

При успешной остановке наша консоль выдаст примерно такой результат:
![image](https://github.com/user-attachments/assets/0ac4d939-fed7-4d65-838c-76bc6d5d02ae)

## ${\color{green}Итог \space домашнего \space задания \space №2}$
- Кластер hadoop, YARN, historyserver разворачивается по скрипту.
- Доступно 3 веб-интерфейса для подключения к системам.
- Кластер  hadoop, YARN, historyserver останавливаеются по скрипту.



























