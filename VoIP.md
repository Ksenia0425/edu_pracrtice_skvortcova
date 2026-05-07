# 2. Лабораторная работа. Базовая настройка IP-телефонов в среде Cisco Packet Tracer

Перед началосм работы подключаем IP-телефоны к источнику питания.

<img width="700" height="716" alt="Снимок экрана 2026-05-04 172755" src="https://github.com/user-attachments/assets/96815d59-28be-4e50-b558-83cedde9f1a6" />

*Подключение телефона к источнику питания*

Собираем топология нашей сети.

<img width="453" height="309" alt="Снимок экрана 2026-05-04 185856" src="https://github.com/user-attachments/assets/ca88fc49-4c11-4ab4-9151-4749d5ef4c21" />

*Топология сети*

В конфигурационном режиме изменяем название маршрутизатора и отключаем синтаксис ввода слов от DNS серверов.

<img width="287" height="30" alt="Снимок экрана 2026-05-04 173301" src="https://github.com/user-attachments/assets/e993de49-1bd7-4297-913d-82d93d0b0a41" />

*Меняем имя устройства*

Настраиваем у маршрутизатора интерфейс f0/0.

<img width="417" height="64" alt="Снимок экрана 2026-05-04 173306" src="https://github.com/user-attachments/assets/b41d04fe-bc3d-4b1f-b0d6-5b1d4f0aac7f" />

*Настройка интерфейса у мершрутизатора*

Создаем пул DHCP адреса с названием VOICEи настраиваем сеть в которой будет работать DHCP.

<img width="412" height="66" alt="Снимок экрана 2026-05-04 184609" src="https://github.com/user-attachments/assets/c4670bd8-f602-4692-b1c0-d01ce974f66b" />

*Пул DHCP адресов*

Настраиваем телефонный сервис в автоматическом режиме. Задаем максимальное количество номеров, присваиваемых IP-телефоном. Задаем максимальное количество IP-телефонов. Задаем IP-адреса.

<img width="502" height="83" alt="Снимок экрана 2026-05-04 184817" src="https://github.com/user-attachments/assets/10e79345-ac31-4cd2-96a7-8f47753081f6" />

*Настройка телефонного сервиса*

На коммутаторе в сети VLAN нужно назначить диапазоны портов.

<img width="358" height="47" alt="Снимок экрана 2026-05-04 185048" src="https://github.com/user-attachments/assets/e8904b54-8e30-411c-93bf-b8e4e9ae1576" />

*Назначение диапазонов портов*

Каждому телефону определяем несколько логических линий со своим номером.

<img width="642" height="79" alt="Снимок экрана 2026-05-04 185141" src="https://github.com/user-attachments/assets/ef96a442-e527-4e2c-bfe3-9ab5a723496e" />

*Номер для первого телефона*

<img width="643" height="92" alt="Снимок экрана 2026-05-04 185255" src="https://github.com/user-attachments/assets/ff3fa853-adf1-4e21-b033-aad8cfe5b84b" />

*Номер для второго телефона*

Проверяем получение номеров на телефонах.

<img width="726" height="714" alt="Снимок экрана 2026-05-04 185332" src="https://github.com/user-attachments/assets/7c038922-d8c8-4770-b92b-bf1eb6bfffc3" />

*Первый получил номер*

<img width="694" height="724" alt="Снимок экрана 2026-05-04 185321" src="https://github.com/user-attachments/assets/77aafc41-5355-4d4d-9e85-04ebc18590fa" />

*Второй получил номер*

Пробуем звонить между ними.

<img width="716" height="730" alt="Снимок экрана 2026-05-05 142858" src="https://github.com/user-attachments/assets/d24ce4cc-68ee-4941-b6ff-85b25b6310a1" />

*Первый удачно позвонил*

<img width="718" height="719" alt="Снимок экрана 2026-05-05 142906" src="https://github.com/user-attachments/assets/cac35f86-f9ab-4b9d-856b-d7ca14a30286" />

*Второй удачно принял звонок*

---
# Блок код
```
Switch0
!
version 15.0
no service timestamps log datetime msec
no service timestamps debug datetime msec
no service password-encryption
!
hostname Switch
!
!
!
!
!
!
spanning-tree mode pvst
spanning-tree extend system-id
!
interface FastEthernet0/1
 switchport mode access
 switchport voice vlan 1
!
interface FastEthernet0/2
 switchport mode access
 switchport voice vlan 1
!
interface FastEthernet0/3
 switchport mode access
 switchport voice vlan 1
!
interface FastEthernet0/4
 switchport mode access
 switchport voice vlan 1
!
interface FastEthernet0/5
 switchport mode access
 switchport voice vlan 1
!
interface FastEthernet0/6
!
interface FastEthernet0/7
!
interface FastEthernet0/8
!
interface FastEthernet0/9
!
interface FastEthernet0/10
!
interface FastEthernet0/11
!
interface FastEthernet0/12
!
interface FastEthernet0/13
!
interface FastEthernet0/14
!
interface FastEthernet0/15
!
interface FastEthernet0/16
!
interface FastEthernet0/17
!
interface FastEthernet0/18
!
interface FastEthernet0/19
!
interface FastEthernet0/20
!
interface FastEthernet0/21
!
interface FastEthernet0/22
!
interface FastEthernet0/23
!
interface FastEthernet0/24
!
interface GigabitEthernet0/1
!
interface GigabitEthernet0/2
!
interface Vlan1
 no ip address
 shutdown
!
!
!
!
line con 0
!
line vty 0 4
 login
line vty 5 15
 login
!
!
!
end
```

```
Router0
!
version 15.1
no service timestamps log datetime msec
no service timestamps debug datetime msec
no service password-encryption
!
hostname CMERouter
!
!
!
!
!
ip dhcp pool VOICE
 network 192.168.10.0 255.255.255.0
 default-router 192.168.10.1
 option 150 ip 192.168.10.1
!
!
!
ip cef
no ipv6 cef
!
!
!
!
license udi pid CISCO2811/K9 sn FTX1017S8E6-
!
!
!
!
!
!
!
!
!
no ip domain-lookup
!
!
spanning-tree mode pvst
!
!
!
!
!
!
interface FastEthernet0/0
 ip address 192.168.10.1 255.255.255.0
 duplex auto
 speed auto
!
interface FastEthernet0/1
 no ip address
 duplex auto
 speed auto
 shutdown
!
interface Vlan1
 no ip address
 shutdown
!
ip classless
!
ip flow-export version 9
!
!
!
!
!
!
!
telephony-service
 max-ephones 5
 max-dn 5
 ip source-address 192.168.10.1 port 2000
 auto assign 4 to 6
 auto assign 1 to 5
!
ephone-dn 1
 number 54001
!
ephone-dn 2
 number 54002
!
ephone 1
 device-security-mode none
 mac-address 00E0.8F37.5A96
 type 7960
 button 1:1
!
ephone 2
 device-security-mode none
 mac-address 0003.E428.7482
 type 7960
 button 1:2
!
line con 0
!
line aux 0
!
line vty 0 4
 login
!
!
!
end

```
Контрольные вопросы

# 3. Лабораторная работа. Настройка конфигурации Cisco CallManager Express на маршрутизаторе Cisco 2811.

Собираем схему топологии по заданию.

<img width="447" height="482" alt="Снимок экрана 2026-05-05 143851" src="https://github.com/user-attachments/assets/27a74b80-d8a8-4c72-9f87-dc07e59dfac9" />

*Топология сети*

В конфигурационном режиме изменяем название маршрутизатора и отключаем синтаксис ввода слов от DNS серверов

<img width="284" height="42" alt="Снимок экрана 2026-05-05 143951" src="https://github.com/user-attachments/assets/f946932e-132d-44ff-965c-5620714a2d83" />

*Меняем имя устройства*

Задаем пароли для защиты маршрутизатора как в удаленном режиме, так и в режиме консоли.

<img width="329" height="165" alt="Снимок экрана 2026-05-05 144332" src="https://github.com/user-attachments/assets/88198687-0dd5-4f46-803f-8ab4033139b2" />

Настраиваем интерфейс f0/0.

<img width="595" height="140" alt="Снимок экрана 2026-05-05 144519" src="https://github.com/user-attachments/assets/c85472af-cb30-4fa7-84c9-acbfe4bc498b" />

*Настройка интерфейса f0/0*

Настраиваем DHCP сервер на маршрутизаторе.

<img width="423" height="60" alt="Снимок экрана 2026-05-05 144654" src="https://github.com/user-attachments/assets/f75193f1-5c61-41a0-8226-62f68c2061e2" />

*DHCP сервер на маршрутизаторе*

Включаем опцию для передачи голоса.

<img width="360" height="29" alt="Снимок экрана 2026-05-05 144728" src="https://github.com/user-attachments/assets/2d10f0c0-54b8-487f-8e37-97c7f8ff630a" />

*Включение опиции 150*

Включаем телефонного сервиса в автоматическом режиме.

<img width="495" height="104" alt="Снимок экрана 2026-05-05 145410" src="https://github.com/user-attachments/assets/d3c44484-a1a2-4bdc-a434-d1fee67ff138" />

*Включение телефонного сервиса*

Настройка интерфейса на коммутаторе в сети VLAN.

<img width="358" height="47" alt="Снимок экрана 2026-05-04 185048" src="https://github.com/user-attachments/assets/1fec4c3b-fc48-413d-aece-fd13415d3f3f" />

Каждому телефону определяем несколько логических линий со своим номером.

<img width="633" height="268" alt="Снимок экрана 2026-05-05 150015" src="https://github.com/user-attachments/assets/5930adb3-6e88-47a5-b28a-eff059f2786a" />

*Назначение номеров*

Проверяем связь между телефонами.

<img width="704" height="555" alt="Снимок экрана 2026-05-05 150551" src="https://github.com/user-attachments/assets/4a1b744b-f2b3-4d62-8e4d-c6ff115e278b" />

*Делаем звонок*

<img width="697" height="575" alt="Снимок экрана 2026-05-05 150613" src="https://github.com/user-attachments/assets/6d699293-49a3-432f-94cc-1027c89c7f96" />

*Вызов приянт*

---
# Блок код
```
MLS
!
version 12.2(37)SE1
no service timestamps log datetime msec
no service timestamps debug datetime msec
no service password-encryption
!
hostname SwitchA
!
!
spanning-tree mode pvst
!
!
!
!
!
!
interface FastEthernet0/1
 switchport mode access
 switchport voice vlan 1
!
interface FastEthernet0/2
 switchport mode access
 switchport voice vlan 1
!
interface FastEthernet0/3
 switchport mode access
 switchport voice vlan 1
!
interface FastEthernet0/4
 switchport mode access
 switchport voice vlan 1
!
interface FastEthernet0/5
 switchport mode access
 switchport voice vlan 1
!
interface FastEthernet0/6
!
interface FastEthernet0/7
!
interface FastEthernet0/8
!
interface FastEthernet0/9
!
interface FastEthernet0/10
!
interface FastEthernet0/11
!
interface FastEthernet0/12
!
interface FastEthernet0/13
!
interface FastEthernet0/14
!
interface FastEthernet0/15
!
interface FastEthernet0/16
!
interface FastEthernet0/17
!
interface FastEthernet0/18
!
interface FastEthernet0/19
!
interface FastEthernet0/20
!
interface FastEthernet0/21
!
interface FastEthernet0/22
!
interface FastEthernet0/23
!
interface FastEthernet0/24
!
interface GigabitEthernet0/1
!
interface GigabitEthernet0/2
!
interface Vlan1
 no ip address
 shutdown
!
ip classless
!
ip flow-export version 9

!
line con 0
!
line aux 0
!
line vty 0 4
 login
!
!
!
!
end
```

```
Router0
!
version 15.1
no service timestamps log datetime msec
no service timestamps debug datetime msec
no service password-encryption
!
hostname CMERouter
ip dhcp pool VOICE
 network 192.168.10.0 255.255.255.0
 default-router 192.168.10.1
 option 150 ip 192.168.10.1
!
!
!
ip cef
no ipv6 cef
!
!
!
!
license udi pid CISCO2811/K9 sn FTX10178PZM-
!
no ip domain-lookup
!
!
spanning-tree mode pvst
!
!
!
!
!
!
interface FastEthernet0/0
 ip address 192.168.10.1 255.255.255.0
 duplex auto
 speed auto
!
interface FastEthernet0/1
 no ip address
 duplex auto
 speed auto
 shutdown
!
interface Vlan1
 no ip address
 shutdown
!
ip classless
!
ip flow-export version 9
!
!
telephony-service
 max-ephones 5
 max-dn 5
 ip source-address 192.168.10.1 port 2000
 auto assign 4 to 6
 auto assign 1 to 5
!
ephone-dn 1
 number 54001
!
ephone-dn 2
 number 54002
!
ephone-dn 3
 number 54003
!
ephone 1
 device-security-mode none
 mac-address 00D0.BAE3.6EB2
 type 7960
 button 1:1
!
ephone 2
 device-security-mode none
 mac-address 00E0.A3D1.8A97
 type 7960
 button 1:2
!
ephone 3
 device-security-mode none
 mac-address 0060.3E3E.4694
 type 7960
 button 1:3
!
line con 0
 password cisco
 logging synchronous
 login
!
line aux 0
!
line vty 0 4
 password cisco
 logging synchronous
 login
!
!
!
end
```
Контрольные вопросы

# 4. Лабораторная работа. Конфигурация VOIP в среде Cisco Packet Tracer

Собираем топологию по заданию.

<img width="536" height="595" alt="image" src="https://github.com/user-attachments/assets/f85b82fb-c2e6-48f4-a2c7-950ec3f1e9f1" />

*Топология сети*

Создаем vlan и назначаем имана.

<img width="287" height="200" alt="Снимок экрана 2026-05-05 170025" src="https://github.com/user-attachments/assets/b8ae607d-f326-4434-a1fc-db6137347499" />

*Создание vlan*

Настраиваем vlan 99.

<img width="428" height="141" alt="Снимок экрана 2026-05-05 170135" src="https://github.com/user-attachments/assets/fafbafc7-b7f2-45c4-a7cb-237da4a9a5ef" />

*Настройка vlan 99*

Задаем маршрут по умолчанию.

<img width="370" height="74" alt="Снимок экрана 2026-05-05 170322" src="https://github.com/user-attachments/assets/060dfaed-1f8c-4937-80b1-bbd8712409d8" />

*Настройка маршрута по уморлчанию*

Настраиваем интерфейсы в сети vlan через назначение диапазона портов.

<img width="371" height="67" alt="Снимок экрана 2026-05-05 172238" src="https://github.com/user-attachments/assets/32c85f3a-3de4-499f-9705-a0e1f20a69b5" />

*Настройка интерфейсов f0/2-4*

Теперь настраиваем роутер. Включаем интерфейс f0/0.

<img width="607" height="109" alt="Снимок экрана 2026-05-05 170730" src="https://github.com/user-attachments/assets/eb9614ec-e683-4c89-a155-ce72e58ecf74" />

*Включение интерфейса f0/0*

Создаем логический подынтерфейса для VLAN 10, VLAN 20, VLAN 99.

<img width="624" height="244" alt="Снимок экрана 2026-05-05 171057" src="https://github.com/user-attachments/assets/1bc6d67d-a992-41e0-91d9-b95289e6bf10" />

*Создание логических подынтерфейсов для VLAN 10*

<img width="625" height="212" alt="Снимок экрана 2026-05-05 171106" src="https://github.com/user-attachments/assets/c5d98956-42dc-44db-9176-d8dd5bf47efc" />

*Создание логических подынтерфейсов для VLAN 20*

<img width="629" height="146" alt="Снимок экрана 2026-05-05 171219" src="https://github.com/user-attachments/assets/dadf66c9-f04a-4600-9d65-cb8c554df058" />

*Создание логических подынтерфейсов для VLAN 99*

Исключаем из пула адрес интерфейса маршрутизатора и DNS-сервера.

<img width="475" height="34" alt="Снимок экрана 2026-05-05 171549" src="https://github.com/user-attachments/assets/20f4909f-8079-484e-8eef-78b817179417" />

*Исключение из пула адресов интерфейсов маршрутизатора и DNS-сервера*

Настраиваем DHCP сервера для передачи голоса и данных.

<img width="409" height="64" alt="Снимок экрана 2026-05-05 171735" src="https://github.com/user-attachments/assets/50e9f4fc-448d-45b0-82a0-e54f0033ab27" />

*Настройка DHCP сервера для передачи данных*

<img width="378" height="57" alt="Снимок экрана 2026-05-05 172047" src="https://github.com/user-attachments/assets/266207d8-8a1a-41be-96a1-505c1f1f6ace" />

*Настройка DHCP сервера для передачи голоса*

Проверяем получение адреса на PC.

<img width="695" height="316" alt="Снимок экрана 2026-05-05 200422" src="https://github.com/user-attachments/assets/a481b876-9bcc-4860-be59-9ed7fca70931" />

*Получение DHCP на первом PC*

<img width="696" height="308" alt="Снимок экрана 2026-05-05 200432" src="https://github.com/user-attachments/assets/6dfef343-6c2f-451f-a745-32465567728c" />

*Получение DHCP на втором PC*

<img width="689" height="294" alt="Снимок экрана 2026-05-05 200444" src="https://github.com/user-attachments/assets/cfac7ac7-1322-4c65-9eb4-9c6690564568" />

*Получение DHCP на третьем PC*

Настраиваем телефонный сервис в автоматическом режиме.

<img width="483" height="89" alt="Снимок экрана 2026-05-05 172533" src="https://github.com/user-attachments/assets/1525ceca-fb32-4d05-ade4-e0d1b20f0f20" />

*Настройка телефонного сервиса в автоматическом режиме*

Назначаем номера для всех IP-телефонов в сети.

<img width="657" height="273" alt="Снимок экрана 2026-05-05 172722" src="https://github.com/user-attachments/assets/fed006f1-9463-4d09-87ff-5911ab09f59a" />

*Назначение номера для всех IP-телефонов в сети*

<img width="355" height="43" alt="Снимок экрана 2026-05-06 145226" src="https://github.com/user-attachments/assets/3c8e973a-f745-49d5-aac9-8529aa015f1c" />

*Назначение номера для первого IP-телефона в сети по mac-адерсу*

<img width="617" height="131" alt="Снимок экрана 2026-05-06 145445" src="https://github.com/user-attachments/assets/61dbaa2c-d651-4ce9-a9d5-f3ed91d69043" />

*Назначение номера для второго IP-телефона в сети по mac-адерсу*

<img width="617" height="131" alt="Снимок экрана 2026-05-06 145445" src="https://github.com/user-attachments/assets/8683b840-971d-449a-adf2-4b1fc69ca789" />

*Назначение номера для третьего IP-телефона в сети по mac-адерсу*

---
# Блок код
```
Router0
!
version 15.1
no service timestamps log datetime msec
no service timestamps debug datetime msec
no service password-encryption
!
hostname Router
!
!
!
!
ip dhcp excluded-address 192.168.10.1 192.168.10.9
ip dhcp excluded-address 192.168.20.1 192.168.20.9
!
ip dhcp pool Data
 network 192.168.10.0 255.255.255.0
 default-router 192.168.10.1
ip dhcp pool Voice
 network 192.168.20.0 255.255.255.0
 default-router 192.168.20.1
 option 150 ip 192.168.20.1
!
!
!
ip cef
no ipv6 cef
!
!
!
!
license udi pid CISCO2811/K9 sn FTX1017VSQR-
!
!
!
!
!
!
!
!
!
!
!
spanning-tree mode pvst
!
!
!
!
!
!
interface FastEthernet0/0
 no ip address
 duplex auto
 speed auto
!
interface FastEthernet0/0.10
 encapsulation dot1Q 10
 ip address 192.168.10.1 255.255.255.0
!
interface FastEthernet0/0.20
 encapsulation dot1Q 20
 ip address 192.168.20.1 255.255.255.0
!
interface FastEthernet0/0.99
 encapsulation dot1Q 99 native
 ip address 192.168.99.1 255.255.255.0
!
interface FastEthernet0/1
 no ip address
 duplex auto
 speed auto
 shutdown
!
interface Vlan1
 no ip address
 shutdown
!
ip classless
!
ip flow-export version 9
!
!
!
!
!
!
!
telephony-service
 max-ephones 3
 max-dn 3
 ip source-address 192.168.20.1 port 2000
!
ephone-dn 1
 number 101
!
ephone-dn 2
 number 102
!
ephone-dn 3
 number 103
!
ephone 1
 device-security-mode none
 mac-address 0002.1660.5901
 type 7960
!
ephone 2
 device-security-mode none
 mac-address 00D0.97A1.4C01
 type 7960
!
ephone 3
 device-security-mode none
 mac-address 000C.8512.D301
 type 7960
!
line con 0
!
line aux 0
!
line vty 0 4
 login
!
!
!
end
```
```
Switch4
!
version 15.0
no service timestamps log datetime msec
no service timestamps debug datetime msec
no service password-encryption
!
hostname Switch
!
!
!
!
!
!
spanning-tree mode pvst
spanning-tree extend system-id
!
interface FastEthernet0/1
 switchport trunk native vlan 99
 switchport mode trunk
!
interface FastEthernet0/2
 switchport access vlan 10
 switchport mode access
 switchport voice vlan 20
!
interface FastEthernet0/3
 switchport access vlan 10
 switchport mode access
 switchport voice vlan 20
!
interface FastEthernet0/4
 switchport access vlan 10
 switchport mode access
 switchport voice vlan 20
!
interface FastEthernet0/5
!
interface FastEthernet0/6
!
interface FastEthernet0/7
!
interface FastEthernet0/8
!
interface FastEthernet0/9
!
interface FastEthernet0/10
!
interface FastEthernet0/11
!
interface FastEthernet0/12
!
interface FastEthernet0/13
!
interface FastEthernet0/14
!
interface FastEthernet0/15
!
interface FastEthernet0/16
!
interface FastEthernet0/17
!
interface FastEthernet0/18
!
interface FastEthernet0/19
!
interface FastEthernet0/20
!
interface FastEthernet0/21
!
interface FastEthernet0/22
!
interface FastEthernet0/23
!
interface FastEthernet0/24
!
interface GigabitEthernet0/1
!
interface GigabitEthernet0/2
!
interface Vlan1
 no ip address
 shutdown
!
interface Vlan99
 ip address 192.168.99.10 255.255.255.0
!
ip default-gateway 192.168.99.1
!
!
!
!
line con 0
!
line vty 0 4
 login
line vty 5 15
 login
!
!
!
!
end
```
Контрольные вопросы

# 7. Лабораторная работа. Построение сети IP-телефонии между удаленными маршрутизаторами в среде Cisco Packet Tracer

Собираем топологию по заданию.

<img width="810" height="428" alt="Снимок экрана 2026-05-06 150615" src="https://github.com/user-attachments/assets/33a5731e-f8b0-415c-ae91-3ff59d22c6aa" />

*Топология сети*

Переменовываем роутер.

<img width="248" height="38" alt="Снимок экрана 2026-05-06 150703" src="https://github.com/user-attachments/assets/7051c246-8503-4222-85d7-4c217f8516a9" />

*Меняем имя устройства RouterA*

<img width="230" height="16" alt="Снимок экрана 2026-05-06 150858" src="https://github.com/user-attachments/assets/591fd9cd-22a5-45e5-98df-73e92fbafd7f" />

*Меняем имя устройства RouterB*

Настраиваем конфигурацию на f0/0 на маршрутизаторах.

<img width="611" height="171" alt="Снимок экрана 2026-05-06 150752" src="https://github.com/user-attachments/assets/6d573040-710f-44e0-b26f-6568ad460cc0" />

*Настройка конфигурации на f0/0 на RouterA*

<img width="598" height="117" alt="Снимок экрана 2026-05-06 150854" src="https://github.com/user-attachments/assets/fb4eb5f4-1022-4937-af0f-56ed2a21d533" />

*Настройка конфигурации на f0/0 на RouterA*

Настраиваем интерфес s0/3/0 на RouterA.

<img width="391" height="58" alt="Снимок экрана 2026-05-06 151127" src="https://github.com/user-attachments/assets/3fffbb5d-f748-43e1-854a-a2977d78a40b" />

*Настройка интерфеса s0/3/0 на RouterA*

Настраиваем интерфес s0/3/0 на RouterB.

<img width="439" height="122" alt="Снимок экрана 2026-05-06 151241" src="https://github.com/user-attachments/assets/8b9c0593-6b65-4ea3-b294-6bffb9dab32c" />

*Настройка интерфеса s0/3/0 на RouterB*

Настраиваем DHCP сервер на маршрутизаторе RouterA.

<img width="403" height="72" alt="Снимок экрана 2026-05-06 151511" src="https://github.com/user-attachments/assets/3e84dc66-3eda-4db8-8d23-c74b567ab250" />

*Настройка DHCP сервер на маршрутизаторе RouterA*

Настраиваем DHCP сервер на маршрутизаторе RouterB.

<img width="406" height="66" alt="Снимок экрана 2026-05-06 151910" src="https://github.com/user-attachments/assets/fab47ea2-6da6-49b2-8898-baebb947febf" />

*Настройка DHCP сервер на маршрутизаторе RouterB*

Настраиваем динамическую маршрутизацию.

<img width="304" height="61" alt="Снимок экрана 2026-05-06 152126" src="https://github.com/user-attachments/assets/3e282916-f00b-4d79-a879-f45e23f2f796" />

*Настройка динамической маршрутизации на RouterA*

<img width="295" height="68" alt="Снимок экрана 2026-05-06 152441" src="https://github.com/user-attachments/assets/6fd9c564-8d88-442b-9ee1-35e721e6c11a" />

*Настройка динамической маршрутизации на RouterB*

Получаем по DHCP адрес на PC.

<img width="701" height="300" alt="Снимок экрана 2026-05-06 153003" src="https://github.com/user-attachments/assets/39a3b63f-25b2-40de-96ca-9bf34967ebde" />

*Первый*

<img width="705" height="300" alt="Снимок экрана 2026-05-06 153540" src="https://github.com/user-attachments/assets/b7c8800b-89d8-431a-8c7b-c6023f08589a" />

*Второй*

Настраиваем телефонный сервис в автоматическом режиме.

<img width="478" height="101" alt="Снимок экрана 2026-05-06 152707" src="https://github.com/user-attachments/assets/5ac75a80-790a-4009-b20c-71876ad8c8e9" />

*Настройка телефонного сервиса в автоматическом режиме на RouterA*

<img width="473" height="92" alt="Снимок экрана 2026-05-06 152853" src="https://github.com/user-attachments/assets/ae513338-864f-429b-bc76-18ab4e6ada1c" />

*Настройка телефонного сервиса в автоматическом режиме на RouterB*

На коммутаторах назначам диапазон портов.

<img width="371" height="137" alt="Снимок экрана 2026-05-06 153245" src="https://github.com/user-attachments/assets/3ccf91dd-28f6-4fe8-a588-45d296b38c29" />

*Назначение диапазона портов на SwitchA*

<img width="357" height="137" alt="Снимок экрана 2026-05-06 153423" src="https://github.com/user-attachments/assets/3312489f-071c-4cdd-8cbb-56ca8aa8dbf8" />

*Назначение диапазона портов на SwitchB*

Создаем на маршрутизаторах логические телефонный линии и назначаем номера.

<img width="636" height="313" alt="Снимок экрана 2026-05-06 153739" src="https://github.com/user-attachments/assets/8a9435b2-11b9-4890-b545-abdc219be05e" />

*Создание логических телефонных линий и назначаем номер на RouterA*

<img width="701" height="623" alt="Снимок экрана 2026-05-06 153801" src="https://github.com/user-attachments/assets/7d7c4d78-a3c4-4134-a582-d4c9e92ea664" />

*Телефон получил номер*

<img width="645" height="353" alt="Снимок экрана 2026-05-06 153922" src="https://github.com/user-attachments/assets/5f2511e1-1d40-4be0-a9ec-c9b2c9f77c99" />

*Создание логических телефонных линий и назначаем номер на RouterB*

<img width="703" height="607" alt="Снимок экрана 2026-05-06 153935" src="https://github.com/user-attachments/assets/5f0c9f10-4168-4c2b-ad4a-810757e1ddc1" />

*Телефон получил номер*

В качестве финальной проверки пропингуем PC между собой.

<img width="445" height="225" alt="Снимок экрана 2026-05-06 154013" src="https://github.com/user-attachments/assets/14fc898c-bf62-4eab-87f2-408d19cdf349" />

*Успешный пинг между PC*

---

# Блок код
```
RouterA
!
version 15.1
no service timestamps log datetime msec
no service timestamps debug datetime msec
no service password-encryption
!
hostname RouterA
!
!
!
!
!
ip dhcp pool T1
 network 192.168.1.0 255.255.255.224
 default-router 192.168.1.1
 option 150 ip 192.168.1.1
!
!
!
no ip cef
no ipv6 cef
!
!
!
!
license udi pid CISCO2811/K9 sn FTX1017324T-
!
!
!
!
!
!
!
!
!
!
!
spanning-tree mode pvst
!
!
!
!
!
!
interface FastEthernet0/0
 ip address 192.168.1.1 255.255.255.224
 duplex auto
 speed auto
!
interface FastEthernet0/1
 no ip address
 duplex auto
 speed auto
 shutdown
!
interface Serial0/3/0
 ip address 10.0.1.1 255.255.255.252
 clock rate 64000
!
interface Serial0/3/1
 no ip address
 clock rate 2000000
 shutdown
!
interface Vlan1
 no ip address
 shutdown
!
router rip
 version 2
 network 10.0.0.0
 network 192.168.1.0
!
ip classless
!
ip flow-export version 9
!
!
!
!
!
!
!
telephony-service
 max-ephones 5
 max-dn 5
 ip source-address 192.168.1.1 port 2000
 auto assign 4 to 6
 auto assign 1 to 5
!
ephone-dn 1
 number 1101
!
ephone-dn 2
 number 1102
!
ephone-dn 3
 number 1103
!
ephone 1
 device-security-mode none
 mac-address 0060.5C00.CC65
 type 7960
 button 1:3
!
ephone 2
 device-security-mode none
 mac-address 000B.BE7D.BCC9
 type 7960
 button 1:1
!
ephone 3
 device-security-mode none
 mac-address 000C.CFEC.E65D
 type 7960
 button 1:2
!
line con 0
!
line aux 0
!
line vty 0 4
 login
!
!
!
end
```
```
RouterB
!
version 15.1
no service timestamps log datetime msec
no service timestamps debug datetime msec
no service password-encryption
!
hostname RouterB
!
!
!
!
!
ip dhcp pool T1
 network 172.16.1.0 255.255.255.224
 default-router 172.16.1.1
 option 150 ip 172.16.1.1
!
!
!
no ip cef
no ipv6 cef
!
!
!
!
license udi pid CISCO2811/K9 sn FTX10178XUZ-
!
!
!
!
!
!
!
!
!
!
!
spanning-tree mode pvst
!
!
!
!
!
!
interface FastEthernet0/0
 ip address 172.16.1.1 255.255.255.224
 duplex auto
 speed auto
!
interface FastEthernet0/1
 no ip address
 duplex auto
 speed auto
 shutdown
!
interface Serial0/3/0
 ip address 10.0.1.2 255.255.255.252
!
interface Serial0/3/1
 no ip address
 clock rate 2000000
 shutdown
!
interface Vlan1
 no ip address
 shutdown
!
router rip
 version 2
 network 10.0.0.0
 network 172.16.0.0
!
ip classless
!
ip flow-export version 9
!
!
!
!
!
!
!
telephony-service
 max-ephones 5
 max-dn 5
 ip source-address 172.16.1.1 port 2000
 auto assign 4 to 6
 auto assign 1 to 5
!
ephone-dn 1
 number 1201
!
ephone-dn 2
 number 1202
!
ephone-dn 3
 number 1203
!
ephone 1
 device-security-mode none
 mac-address 000A.4162.C1AD
 type 7960
 button 1:2
!
ephone 2
 device-security-mode none
 mac-address 00E0.F7AB.4C58
 type 7960
 button 1:1
!
ephone 3
 device-security-mode none
 mac-address 0001.C721.8A12
 type 7960
 button 1:3
!
line con 0
!
line aux 0
!
line vty 0 4
 login
!
!
!
end
```
```
SwitchA
!
version 15.0
no service timestamps log datetime msec
no service timestamps debug datetime msec
no service password-encryption
!
hostname SwitchA
!
!
!
!
!
!
spanning-tree mode pvst
spanning-tree extend system-id
!
interface FastEthernet0/1
 switchport mode access
 switchport voice vlan 1
!
interface FastEthernet0/2
 switchport mode access
 switchport voice vlan 1
!
interface FastEthernet0/3
 switchport mode access
 switchport voice vlan 1
!
interface FastEthernet0/4
 switchport mode access
 switchport voice vlan 1
!
interface FastEthernet0/5
 switchport mode access
 switchport voice vlan 1
!
interface FastEthernet0/6
!
interface FastEthernet0/7
!
interface FastEthernet0/8
!
interface FastEthernet0/9
!
interface FastEthernet0/10
!
interface FastEthernet0/11
!
interface FastEthernet0/12
!
interface FastEthernet0/13
!
interface FastEthernet0/14
!
interface FastEthernet0/15
!
interface FastEthernet0/16
!
interface FastEthernet0/17
!
interface FastEthernet0/18
!
interface FastEthernet0/19
!
interface FastEthernet0/20
!
interface FastEthernet0/21
!
interface FastEthernet0/22
!
interface FastEthernet0/23
!
interface FastEthernet0/24
!
interface GigabitEthernet0/1
!
interface GigabitEthernet0/2
!
interface Vlan1
 no ip address
 shutdown
!
!
!
!
line con 0
!
line vty 0 4
 login
line vty 5 15
 login
!
!
!
!
end


```
```
SwitcB
!
version 15.0
no service timestamps log datetime msec
no service timestamps debug datetime msec
no service password-encryption
!
hostname SwitchB
!
!
!
!
!
!
spanning-tree mode pvst
spanning-tree extend system-id
!
interface FastEthernet0/1
 switchport mode access
 switchport voice vlan 1
!
interface FastEthernet0/2
 switchport mode access
 switchport voice vlan 1
!
interface FastEthernet0/3
 switchport mode access
 switchport voice vlan 1
!
interface FastEthernet0/4
 switchport mode access
 switchport voice vlan 1
!
interface FastEthernet0/5
 switchport mode access
 switchport voice vlan 1
!
interface FastEthernet0/6
!
interface FastEthernet0/7
!
interface FastEthernet0/8
!
interface FastEthernet0/9
!
interface FastEthernet0/10
!
interface FastEthernet0/11
!
interface FastEthernet0/12
!
interface FastEthernet0/13
!
interface FastEthernet0/14
!
interface FastEthernet0/15
!
interface FastEthernet0/16
!
interface FastEthernet0/17
!
interface FastEthernet0/18
!
interface FastEthernet0/19
!
interface FastEthernet0/20
!
interface FastEthernet0/21
!
interface FastEthernet0/22
!
interface FastEthernet0/23
!
interface FastEthernet0/24
!
interface GigabitEthernet0/1
!
interface GigabitEthernet0/2
!
interface Vlan1
 no ip address
 shutdown
!
!
!
!
line con 0
!
line vty 0 4
 login
line vty 5 15
 login
!
!
!
!
end
```
Контрольные вопросы

# 8. Лабораторная работа. Построение сети IP-телефонии между удаленными маршрутизаторами

Собираем топологию по заданию.

<img width="513" height="501" alt="Снимок экрана 2026-05-06 160809" src="https://github.com/user-attachments/assets/63405242-02ca-4273-92e7-31bc92351dd9" />

*Топология сети*

Переменовываем маршрутизаторы и настраиваем интерфейс s0/1/0.

<img width="445" height="77" alt="Снимок экрана 2026-05-06 160941" src="https://github.com/user-attachments/assets/a86e1066-c058-4440-beb7-a9c0432e153c" />

*Настройка интерфейса s0/1/0 на CMERouter*

<img width="461" height="116" alt="Снимок экрана 2026-05-06 161435" src="https://github.com/user-attachments/assets/e0cee5ca-f557-4703-b87a-8b1885e985fb" />

*Настройка интерфейса s0/1/0 на RemoteRouter*

Настраиваем маршрутизаторах по протоколу eigrp 100.

<img width="299" height="69" alt="Снимок экрана 2026-05-06 161257" src="https://github.com/user-attachments/assets/c74fee17-24a5-4186-a149-3520c5ec6dc5" />

*Настройка eigrp 100 на CMERoute*

<img width="576" height="126" alt="Снимок экрана 2026-05-06 162614" src="https://github.com/user-attachments/assets/0d3211d7-8a67-4a51-b726-43d63d63c389" />

*Настройка eigrp 100 на RemoteRouter*

Проверяем соединение между маршрутизаторами с помощью пинга.

<img width="504" height="123" alt="Снимок экрана 2026-05-06 161510" src="https://github.com/user-attachments/assets/38292006-62a2-4b20-b373-f01db5d626f7" />

*Успешный пинг между маршрутизаторами*

Создаем на маршрутизаторах подинтерфейсы на VLAN.

<img width="441" height="60" alt="Снимок экрана 2026-05-06 162036" src="https://github.com/user-attachments/assets/40300d83-35af-4369-9465-183e881e1fce" />

*Подинтерфейс на VLAN 40 на RemoteRouter*

<img width="448" height="65" alt="Снимок экрана 2026-05-06 162212" src="https://github.com/user-attachments/assets/872e2cf5-b2cb-4911-9caa-6fd11000b1b7" />

*Подинтерфейс на VLAN 30 на RemoteRouter*

<img width="436" height="63" alt="Снимок экрана 2026-05-06 162323" src="https://github.com/user-attachments/assets/79d2e34f-5092-4e8b-bd93-a322c96c9310" />

*Подинтерфейс на VLAN 40 на CMERouter*

<img width="433" height="58" alt="Снимок экрана 2026-05-06 162415" src="https://github.com/user-attachments/assets/1de5157f-9b31-4cb6-b7b3-324b4eb007b8" />

*Подинтерфейс на VLAN 30 на CMERouter*

Переходим к настройкам коммутаторах.

<img width="300" height="44" alt="Снимок экрана 2026-05-06 162839" src="https://github.com/user-attachments/assets/71c776fc-feb5-4e61-8d45-e9fe003017e2" />

*Меняем имя устройства на RemoteSwitch*

<img width="299" height="42" alt="Снимок экрана 2026-05-06 163750" src="https://github.com/user-attachments/assets/bfd64f71-aa11-4898-97fc-eeba4e35ca83" />

*Меняем имя устройства на CMESwitch*

Задаем пароли в удаленном режиме и консольном для защиты коммутатора.

<img width="334" height="139" alt="Снимок экрана 2026-05-06 163106" src="https://github.com/user-attachments/assets/58bd1ece-d671-428e-8143-4f4b411c904d" />

*Безопасность на RemoteSwitch*

На коммутаторах настраиваем первый порт как транковый.

<img width="524" height="168" alt="Снимок экрана 2026-05-06 163250" src="https://github.com/user-attachments/assets/10fb64c6-ed1d-4790-bf7c-5938ec716fa3" />

*Настройка f0/1 на RemoteSwitch*

<img width="625" height="259" alt="Снимок экрана 2026-05-06 163856" src="https://github.com/user-attachments/assets/62fffca6-10a6-4bf1-8c6b-d90df4f365fd" />

*Настройка f0/1 на CMESwitch*

Создаем VLAN-ы на коммутаторах и даем им имена.

<img width="276" height="91" alt="Снимок экрана 2026-05-06 163332" src="https://github.com/user-attachments/assets/5288e32b-649b-49f1-876f-4dde4032f5a5" />

*Создание VLAN на RemoteSwitch*

<img width="247" height="103" alt="Снимок экрана 2026-05-06 163927" src="https://github.com/user-attachments/assets/0d0638e7-bdc4-42f6-8a9f-2a169dd014ce" />

*Создание VLAN на CMESwitch*

Настраиваем остальные порты.

<img width="526" height="183" alt="Снимок экрана 2026-05-06 163518" src="https://github.com/user-attachments/assets/125a45bf-0bba-49ca-97bf-6b8ee98ca6f1" />

*Интерфейсы на RemoteSwitch*

<img width="542" height="277" alt="Снимок экрана 2026-05-06 164037" src="https://github.com/user-attachments/assets/6541a85a-cc16-454e-8b8b-75a506211d9a" />

*Интерфейсы на CMESwitch*

Настраиваем на маршрутизаторах пул DHCP адресов.

<img width="391" height="155" alt="Снимок экрана 2026-05-06 164535" src="https://github.com/user-attachments/assets/7aa9d0c3-cd4e-4886-a3f5-d216ea9e380d" />

*Пул DHCP адресов на CMERouter*

<img width="416" height="156" alt="Снимок экрана 2026-05-06 165329" src="https://github.com/user-attachments/assets/0df402f0-c494-40a3-8ada-85e03b8a3a2d" />

*Пул DHCP адресов на RemoteRouter*

Настраиваем телефонный сервис.

<img width="435" height="82" alt="Снимок экрана 2026-05-06 164715" src="https://github.com/user-attachments/assets/cf0f3bdb-5851-4155-951e-d3e057568adf" />

*Настройка телефонного севиса на CMERouter*

<img width="470" height="100" alt="Снимок экрана 2026-05-06 165501" src="https://github.com/user-attachments/assets/f585124e-df22-44cd-8ae6-f25b03d993db" />

*Настройка телефонного севиса на RemoteRouter*

<img width="703" height="512" alt="Снимок экрана 2026-05-06 164858" src="https://github.com/user-attachments/assets/f6203056-f306-426e-97c9-07deb996e4d7" />

*Телефоны получили номера*
---
# Блок код
```
CMERouter
!
version 15.1
no service timestamps log datetime msec
no service timestamps debug datetime msec
no service password-encryption
!
hostname CMERouter
!
!
!
!
ip dhcp excluded-address 10.30.2.1
ip dhcp excluded-address 10.40.2.1
!
ip dhcp pool VOICE
 network 10.30.2.0 255.255.255.0
 default-router 10.30.2.1
 option 150 ip 10.30.2.1
ip dhcp pool DATA
 network 10.40.2.0 255.255.255.0
 default-router 10.40.2.1
!
!
!
no ip cef
no ipv6 cef
!
!
!
!
license udi pid CISCO2811/K9 sn FTX1017190L-
!
!
spanning-tree mode pvst
!
!
!
!
!
!
interface FastEthernet0/0
 no ip address
 duplex auto
 speed auto
!
interface FastEthernet0/0.1
 encapsulation dot1Q 40
 ip address 10.40.2.1 255.255.255.0
!
interface FastEthernet0/0.2
 encapsulation dot1Q 30
 ip address 10.30.2.1 255.255.255.0
!
interface FastEthernet0/1
 no ip address
 duplex auto
 speed auto
!
interface Serial0/1/0
 ip address 82.115.34.210 255.255.255.252
 clock rate 2000000
!
interface Serial0/1/1
 no ip address
 clock rate 2000000
 shutdown
!
interface Vlan1
 no ip address
 shutdown
!
router eigrp 100
 network 10.0.0.0
 network 82.0.0.0
!
ip classless
!
ip flow-export version 9
!
telephony-service
 max-ephones 10
 max-dn 10
 ip source-address 10.30.2.1 port 2000
 auto assign 1 to 10
!
ephone-dn 1
 number 2001
!
ephone-dn 2
 number 2002
!
ephone 1
 device-security-mode none
 mac-address 00E0.A39E.2883
 type 7960
 button 1:1
!
ephone 2
 device-security-mode none
 mac-address 000A.F316.355C
 type 7960
 button 1:2
!
line con 0
!
line aux 0
!
line vty 0 4
 login
!
!
!
end
```

```
CMESwitch
!
version 12.2(37)SE1
no service timestamps log datetime msec
no service timestamps debug datetime msec
no service password-encryption
!
hostname CMESwitch
!
!
!
no ip domain-lookup
!
!
spanning-tree mode pvst
!
!
!
!
!
!
interface FastEthernet0/1
 switchport trunk encapsulation dot1q
 switchport mode trunk
 spanning-tree portfast
!
interface FastEthernet0/2
 switchport access vlan 40
 switchport voice vlan 30
 spanning-tree portfast
!
interface FastEthernet0/3
 switchport access vlan 40
 switchport voice vlan 30
 spanning-tree portfast
!
interface FastEthernet0/4
!
interface FastEthernet0/5
!
interface FastEthernet0/6
!
interface FastEthernet0/7
!
interface FastEthernet0/8
!
interface FastEthernet0/9
!
interface FastEthernet0/10
!
interface FastEthernet0/11
!
interface FastEthernet0/12
!
interface FastEthernet0/13
!
interface FastEthernet0/14
!
interface FastEthernet0/15
!
interface FastEthernet0/16
!
interface FastEthernet0/17
!
interface FastEthernet0/18
!
interface FastEthernet0/19
!
interface FastEthernet0/20
!
interface FastEthernet0/21
!
interface FastEthernet0/22
!
interface FastEthernet0/23
!
interface FastEthernet0/24
!
interface GigabitEthernet0/1
!
interface GigabitEthernet0/2
!
interface Vlan1
 no ip address
 shutdown
!
ip classless
!
ip flow-export version 9
!
!
!
!
line con 0
!
line aux 0
!
line vty 0 4
 login
!
!
!
!
end
```

```
RemoteRouter
!
version 15.1
no service timestamps log datetime msec
no service timestamps debug datetime msec
no service password-encryption
!
hostname RemoteRouter
!
!
!
!
ip dhcp excluded-address 10.30.1.1
ip dhcp excluded-address 10.40.1.1
!
ip dhcp pool VOICE2
 network 10.30.1.0 255.255.255.0
 default-router 10.30.1.1
 option 150 ip 10.30.1.1
ip dhcp pool DATA2
 network 10.40.1.0 255.255.255.0
 default-router 10.40.1.1
!
!
!
no ip cef
no ipv6 cef
!
!
!
!
license udi pid CISCO2811/K9 sn FTX1017Z6XH-
!
!
!
!
spanning-tree mode pvst
!
!
!
!
!
!
interface FastEthernet0/0
 no ip address
 duplex auto
 speed auto
!
interface FastEthernet0/0.1
 encapsulation dot1Q 40
 ip address 10.40.1.1 255.255.255.0
!
interface FastEthernet0/0.2
 encapsulation dot1Q 30
 ip address 10.30.1.1 255.255.255.0
!
interface FastEthernet0/1
 no ip address
 duplex auto
 speed auto
 shutdown
!
interface Serial0/1/0
 ip address 82.115.34.209 255.255.255.252
!
interface Serial0/1/1
 no ip address
 clock rate 2000000
 shutdown
!
interface Vlan1
 no ip address
 shutdown
!
router eigrp 100
 network 10.0.0.0
 network 82.0.0.0
!
ip classless
!
ip flow-export version 9
!
!
!
!
!
!
!
telephony-service
 max-ephones 10
 max-dn 10
 ip source-address 10.30.1.1 port 2000
 auto assign 1 to 10
!
ephone-dn 1
 number 1001
!
ephone 1
 device-security-mode none
 mac-address 0090.214C.EC14
 type 7960
 button 1:1
!
line con 0
!
line aux 0
!
line vty 0 4
 login
!
!
!
end
```

```
RemoteSwitch
!
version 12.2(37)SE1
no service timestamps log datetime msec
no service timestamps debug datetime msec
no service password-encryption
!
hostname RemoteSwitch
!
!
!
!
!
no ip domain-lookup
!
!
spanning-tree mode pvst
!
!
!
!
!
!
interface FastEthernet0/1
 switchport trunk encapsulation dot1q
 switchport mode trunk
 spanning-tree portfast
!
interface FastEthernet0/2
 switchport access vlan 40
 switchport voice vlan 30
 spanning-tree portfast
!
interface FastEthernet0/3
!
interface FastEthernet0/4
!
interface FastEthernet0/5
!
interface FastEthernet0/6
!
interface FastEthernet0/7
!
interface FastEthernet0/8
!
interface FastEthernet0/9
!
interface FastEthernet0/10
!
interface FastEthernet0/11
!
interface FastEthernet0/12
!
interface FastEthernet0/13
!
interface FastEthernet0/14
!
interface FastEthernet0/15
!
interface FastEthernet0/16
!
interface FastEthernet0/17
!
interface FastEthernet0/18
!
interface FastEthernet0/19
!
interface FastEthernet0/20
!
interface FastEthernet0/21
!
interface FastEthernet0/22
!
interface FastEthernet0/23
!
interface FastEthernet0/24
!
interface GigabitEthernet0/1
!
interface GigabitEthernet0/2
!
interface Vlan1
 no ip address
 shutdown
!
ip classless
!
ip flow-export version 9
!
!
!
!
!
!
!
!
line con 0
 password cisco
 logging synchronous
 login
!
line aux 0
!
line vty 0 4
 password cisco
 logging synchronous
 login
!
!
!
!
end
```
