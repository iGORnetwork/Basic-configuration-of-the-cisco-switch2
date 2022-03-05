# ДЗ (2) Канальный уровень. Ethernet 
 1. Проводим базовые настройки switch end PC согласно таблице 

Устройство	                      Интерфейс	                   IP-адрес	                      Маска 

S1	                              VLAN 1	                      192.168.1.1	                   255.255.255.0

S2	                              VLAN 1	                      192.168.1.2	                   255.255.255.0

PC-A	                            NIC	                          192.168.1.11	                   255.255.255.0

PC-B	                            NIC	                          192.168.1.12	                   255.255.255.0

# S1
![](https://github.com/iGORnetwork/Basic-configuration-of-the-cisco-switch/blob/main/image/Screenshot_14.png)

![](https://github.com/iGORnetwork/Basic-configuration-of-the-cisco-switch/blob/main/image/Screenshot_15.png)

# S2
![](https://github.com/iGORnetwork/Basic-configuration-of-the-cisco-switch/blob/main/image/Screenshot_16.png)

![](https://github.com/iGORnetwork/Basic-configuration-of-the-cisco-switch/blob/main/image/Screenshot_17.png)

# PC-A
![](https://github.com/iGORnetwork/Basic-configuration-of-the-cisco-switch/blob/main/image/Screenshot_18.png)

# PC-B
![](https://github.com/iGORnetwork/Basic-configuration-of-the-cisco-switch/blob/main/image/Screenshot_19.png)

2. Просмотрите таблицу МАС-адресов коммутатора S2

S2# ➝ show mac address-table

![](https://github.com/iGORnetwork/Basic-configuration-of-the-cisco-switch/blob/main/image/Screenshot_20.png)

3. Очистка таблицы МАС-адресов коммутатора S2 и снова отобразить таблицу МАС-адресов.

S2# clear mac address-table dynamic 

S2# show mac address-table 

После отчистки отображается один mac address 
Если отправить эхо-запрос с PC-B ping 192. 168. 1. 1 192. 168. 1. 2 192. 168. 1. 11 тогда в таблице появляется 3 mac адреса  с которых выполняли команду ping

![](https://github.com/iGORnetwork/Basic-configuration-of-the-cisco-switch/blob/main/image/Screenshot_21.png)

3. Просмотр работы протокола ARP

![](https://github.com/iGORnetwork/Basic-configuration-of-the-cisco-switch/blob/main/image/Screenshot_22.png)
![](https://github.com/iGORnetwork/Basic-configuration-of-the-cisco-switch/blob/main/image/Screenshot_23.png)
