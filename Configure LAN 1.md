# Часть 1
## Шаг 1
Согласно схеме (Москва и Новосибирск), в среде моделирования Packet Tracer создали сеть, включающая маршрутизаторы R1, R2, R3, многоуровневый коммутатор MLS и оконечные устройства.

<img width="1120" height="572" alt="Снимок экрана 2026-04-15 150452" src="https://github.com/user-attachments/assets/619f6419-7eb2-4cd8-8a7a-391f7731669b" />
*Топология нашей сети*

## Шаг 2
Для идентификации администратора на всех роутерах настроено приветственное сообщение.

<img width="628" height="39" alt="Снимок экрана 2026-04-15 161024" src="https://github.com/user-attachments/assets/67eee20c-cd0b-4252-8278-fe49d7f5a4af" />

*Настройка привественного баннера*

##  Шаг 3
Переменовываем все устройства по шаблону страна-город-роль устройства-порядковый номер.

<img width="246" height="31" alt="image" src="https://github.com/user-attachments/assets/a70c4867-c867-4ac2-8695-021478b740dd" />

*Переменовываем устройства*

## Шаг 4
Раздаем устройствам доменные имена согласно местоположению.

МСК:

<img width="308" height="22" alt="Снимок экрана 2026-04-15 162510" src="https://github.com/user-attachments/assets/0e0244f5-7705-4f4a-8d66-3286fbb8a793" />

*Назначение доменного имени в MSK*

НСК:

<img width="321" height="17" alt="Снимок экрана 2026-04-15 180839" src="https://github.com/user-attachments/assets/8e5c86c9-30df-46c6-9e95-c3f330180eaa" />

*Назначение доменного имени в NSK*

## Шаг 5
Создаем на коммутаторах НСК VLAN 2, 3, 4.

<img width="210" height="77" alt="Снимок экрана 2026-04-15 165050" src="https://github.com/user-attachments/assets/e19482d9-d051-4f48-99ee-8f8048778257" />

*Создание VLAN 2, 3, 4*

## Шаг 6
Теперь этим коммутаторам назначаем интерфейс f0/2 VLAN 2, интерфейс f0/3 VLAN 3, а интерфейс f0/4 VLAN 4.

<img width="342" height="90" alt="Снимок экрана 2026-04-15 165147" src="https://github.com/user-attachments/assets/91213d2b-2bde-4568-8295-8857de8c5fd3" />

*Назначаем интерфейсам соответсвующие VLAN-ы*

## Шаг 7
Создаем канал EtherChannel 2-го уровня между коммутаторами в НСК, используя интерфейсы G0/1 и G0/2, опираясь на требования в работе.

<img width="595" height="212" alt="Снимок экрана 2026-04-15 181426" src="https://github.com/user-attachments/assets/58f29b19-3ba1-41db-995c-16cf649e8c05" />

*На интерфейсах G0/1 и G0/2 создаем канал EtherChannel 2-го уровня между коммутаторами в НСК*

## Шаг 8
Создаем Management interface на S2 коммутаторе для VLAN 1, используя IP- адрес 1.0.0.50/8 и шлюз по умолчанию 1.0.0.1.

<img width="568" height="192" alt="Снимок экрана 2026-04-16 152217" src="https://github.com/user-attachments/assets/76255d6e-5567-4a51-a734-9d81c0679536" />

*Management interface на S2 коммутаторе для VLAN 1*

## Шаг 9
Создаем Management interface на коммутаторе S3 для VLAN 2, используя IP-адрес 2.0.0.50/8 и шлюз по умолчанию 2.0.0.1.

<img width="559" height="188" alt="Снимок экрана 2026-04-16 152758" src="https://github.com/user-attachments/assets/d417d0f2-b6e0-4b76-a836-e8b3231eae8f" />

*Management interface на коммутаторе S3 для VLAN 2*

## Шаг 10
Включаем SSHv2 на коммутаторах в Новосибирске, используя имя пользователя "nsk" и пароль "cisco".

<img width="501" height="101" alt="Снимок экрана 2026-04-16 153722" src="https://github.com/user-attachments/assets/7603ef99-dcee-4cd1-853a-aeafcf4b3f56" />
*Генерация ключей включена*

<img width="341" height="17" alt="Снимок экрана 2026-04-16 153838" src="https://github.com/user-attachments/assets/a41d6b69-d731-4dd0-9560-bca8619d378f" />
*Задали имя и пароль*

<img width="327" height="113" alt="Снимок экрана 2026-04-16 161143" src="https://github.com/user-attachments/assets/12126b0a-e1e6-4333-b584-fe76c964adbf" />

*Настрайка виртуальных терминальных линий*

<img width="373" height="70" alt="Снимок экрана 2026-04-16 162853" src="https://github.com/user-attachments/assets/67afdde0-a6e4-42a6-a353-0a8a7a6ab916" />

*создает пользователя с паролем и шифруем пароль*

## Шаг 11
Интерфейс f0/24 коммутатора S2 будет подключен к маршрутизатору R1 для межсетевой маршрутизации VLAN на транке.

<img width="322" height="63" alt="Снимок экрана 2026-04-16 163423" src="https://github.com/user-attachments/assets/d75f82c9-a0ad-4d12-b49f-dae011763f1d" />

*Интерфейс f0/24 переводим в режим магистрального канала*

## Шаг 12
Настраиваем сообщение на S2 и S3.

<img width="230" height="62" alt="image" src="https://github.com/user-attachments/assets/8e7cb36b-f42c-49bb-962c-bf218ba5817a" />

*Вход с сообщением*

## Шаг 13
Настроиваем интерфейсы f0/2, f0/3 и f0/4 на коммутаторах S2 и S3 согласно требованиям задания.

<img width="531" height="350" alt="Снимок экрана 2026-04-16 164327" src="https://github.com/user-attachments/assets/9c0ea4c0-0720-4fa4-91cc-df613b5382fc" />

*Порты переходят в рабочий режим мгновенно, пропуская стандартные проверки протокола STP, чтобы ускорить включение портов для конечных устройств*

<img width="528" height="215" alt="Снимок экрана 2026-04-16 164602" src="https://github.com/user-attachments/assets/d044e905-7a43-4822-ad0f-3c34641df28e" />

*Включаем защиту портов коммутатора от несанкционированного доступа*

## Шаг 14
Создаем защищенное консольное подключение на S2 и S3.

<img width="278" height="34" alt="Снимок экрана 2026-04-16 170138" src="https://github.com/user-attachments/assets/4cd9a87d-6af1-4738-8e6d-2ca7a69599ee" />

*Защищенное консольное подключение*

## Шаг 15
Отключаем таймаут для консоли и SSH на S2 и S3.

<img width="302" height="14" alt="Снимок экрана 2026-04-16 170314" src="https://github.com/user-attachments/assets/fc80d889-4eaf-492b-9933-7a51343e9592" />

*Отключение таймаута*

## Шаг 16
Делаем предотвращение прерываний консольной сессии каждым выводом журнала на S2 и S3.

<img width="326" height="16" alt="Снимок экрана 2026-04-16 170329" src="https://github.com/user-attachments/assets/0467bc9f-278a-4d9d-837d-1522b11b8ed0" />

*Предотвращение прерываний консольной сессии*

## Шаг 17
Изменяем буфер обмена истории до 256 строк.

<img width="297" height="16" alt="Снимок экрана 2026-04-16 170348" src="https://github.com/user-attachments/assets/1f7d29b2-a3c9-4868-874a-9f1f025dca50" />

*Буфер обмена истории до 256 строк*

# Часть 2

## Шаг 1
Назнаем интерфейсу f0/1 маршрутизатора R3 IP-адрес 40.40.40.1/24.

<img width="610" height="140" alt="Снимок экрана 2026-04-16 171042" src="https://github.com/user-attachments/assets/d0ef1f21-d15d-485d-8fc4-10fb4143989c" />

*Маршрутизатору R3 на f0/1 назначаем адрес 40.40.40.1/24*

## Шаг 2
Настраиваем R3 для поддержки маршрутизации между VLAN 1, 2, 3, 4 для S3 и S1, следуя требованиям задания.

<img width="618" height="142" alt="Снимок экрана 2026-04-16 171412" src="https://github.com/user-attachments/assets/d0b15004-b2eb-4a60-8433-9cd93eb9abd4" />

*Подготавливаем интерфейс к работе*

<img width="629" height="505" alt="Снимок экрана 2026-04-16 171717" src="https://github.com/user-attachments/assets/fcf00cfa-a1e2-48c8-ab19-d688631ec3d4" />

*Создание виртуальный подинтерфейсов*

## Шаг 3
Настриваем R3 в качестве DHCP-сервера для любой машины, подключенной к VLAN 1, 2, 3, 4 на S2 и S3, используя требования задания.

<img width="533" height="335" alt="Снимок экрана 2026-04-16 172942" src="https://github.com/user-attachments/assets/f4fddaa2-8f29-4b9b-814b-ba0db66ad792" />

*Настройка DHCP*

<img width="429" height="44" alt="Снимок экрана 2026-04-16 180731" src="https://github.com/user-attachments/assets/bea23fe0-472c-4fb6-83e8-ef2753e064d8" />

*Делаем исключения*

<img width="433" height="14" alt="Снимок экрана 2026-04-16 180735" src="https://github.com/user-attachments/assets/287f1388-0e58-42e1-9bc9-149f19bc11ab" />

*Доделываем исключения*

## Шаг 4
3.0.0.101 пингуем с РС3.

<img width="425" height="218" alt="Снимок экрана 2026-04-16 180719" src="https://github.com/user-attachments/assets/71cba6b6-2b7d-4358-ba72-e954907b98ee" />

_Успешный пинг_

# Часть 3
## Шаг 1
Настраиваем имя хоста многоуровневого коммутатора (Multilayer Switch) на MLS.

<img width="266" height="30" alt="Снимок экрана 2026-04-21 161232" src="https://github.com/user-attachments/assets/5c348726-ff68-46af-a0b2-29303de2cac4" />

*Имя на MLS*

## Шаг 2
Включаем возможности маршрутизации на MLS.

<img width="233" height="17" alt="Снимок экрана 2026-04-16 181129" src="https://github.com/user-attachments/assets/8ebbacfb-e2c5-49f7-9912-2bbed4373c46" />

*Включаем маршрутизацию*

## Шаг 3
Создаём VLAN 100 с именем Sales_dept и VLAN 200 с именем IT_dept.

<img width="299" height="84" alt="Снимок экрана 2026-04-16 181134" src="https://github.com/user-attachments/assets/8147ad1d-823d-4bb1-b94d-c66cd3defd65" />

*Создаем  VLAN 100, 200*

## Шаг 4
Назнаем интерфейс f0/4 VLAN 100, а интерфейс f0/5 VLAN 200.

<img width="385" height="167" alt="Снимок экрана 2026-04-16 181748" src="https://github.com/user-attachments/assets/33582170-9108-4e42-bac8-256c8bf8349d" />

*Назначаем интерфейсам VLAN-ы*

## Шаг 5
Включаем маршрутизацию между VLAN 100 и VLAN 200, используя SVI (Switch Virtual Interface) на MLS, с требованиями по заданию (VLAN 100 - 100.0.0.50/8, VLAN 200 - 200.0.0.50/24.

<img width="589" height="296" alt="Снимок экрана 2026-04-20 143559" src="https://github.com/user-attachments/assets/4e2e284b-bf1a-4b52-8aa8-be5eca49d576" />

*Назначаем интерфейсам адреса*

## Шаг 6
Изменяем интерфейсы f0/1(11.0.0.50/8), f0/2(12.0.0.50/8) и f0/3(40.40.40.50/24) на интерфейсы 3-го уровня со следующими требованиями.

<img width="416" height="98" alt="Снимок экрана 2026-04-20 143709" src="https://github.com/user-attachments/assets/04c88b7d-05a2-49cc-a9e5-aedf9be92762" />

*Интерфейс f0/1*

<img width="446" height="73" alt="Снимок экрана 2026-04-20 143826" src="https://github.com/user-attachments/assets/7cb66a97-1f05-4a8c-96e6-efe69c933c54" />

*Интерфейс f0/2*

<img width="618" height="142" alt="Снимок экрана 2026-04-20 143939" src="https://github.com/user-attachments/assets/087aa106-d245-469f-8e26-65e99c2e4d1c" />

*Интерфейс f0/3*

## Шаг 7
Пропингуем 200.0.0.100 с РС1.

<img width="448" height="230" alt="Снимок экрана 2026-04-20 144903" src="https://github.com/user-attachments/assets/551b21ea-a36d-49ef-b133-2fda2e8e1394" />

*Успешный пинг*

# Часть 4
## Шаг 1
Настройте IP-адреса f0/0 маршрутизатора R1 - 10.0.0.2/8, f0/1 - 11.0.0.2/8.

<img width="623" height="309" alt="Снимок экрана 2026-04-20 145927" src="https://github.com/user-attachments/assets/342c1e44-d8a4-4e64-84c0-e69412f30de9" />

*Настройка IP-адресов на R1*

## Шаг 2
Настроиваем IP-адрес f0/0 маршрутизатора R2 - 10.0.0.3/8, f0/1 - 12.0.0.3/8.

<img width="625" height="286" alt="Снимок экрана 2026-04-20 150131" src="https://github.com/user-attachments/assets/d0028ad7-8847-4619-a815-3629619ae0a5" />

*Настройка IP-адресов на R2*

## Шаг 3
Настраиваем протокол Cisco High availability на R1 и R2 в Москве с требованиями по заданию.

<img width="506" height="233" alt="Снимок экрана 2026-04-20 150640" src="https://github.com/user-attachments/assets/3d1c5db0-57c4-4087-b019-0cfaadaa440a" />

*Настройка протокола Cisco High availability на R1*

<img width="512" height="257" alt="Снимок экрана 2026-04-20 151631" src="https://github.com/user-attachments/assets/de160d4e-4414-4365-a98c-ebe6f0ae6e5a" />

*Настройка протокола Cisco High availability на R2*

# Часть 5
## Шаг 1
Настроиваем EIGRP с номером автономной системы (AS) 100 на R1, R2, R3 и MLS.

<img width="317" height="86" alt="Снимок экрана 2026-04-20 153408" src="https://github.com/user-attachments/assets/9a7eab1e-33d4-4d2f-9f44-5f583170602c" />
*EIGRP на R1*

<img width="386" height="158" alt="Снимок экрана 2026-04-20 153542" src="https://github.com/user-attachments/assets/80203399-4b0f-419b-979d-25f7524e534d" />

*EIGRP на R2*

<img width="321" height="139" alt="Снимок экрана 2026-04-20 153314" src="https://github.com/user-attachments/assets/83468930-b266-4758-b741-0e3d5f3a260d" />

*EIGRP на R3*

<img width="622" height="312" alt="Снимок экрана 2026-04-20 153710" src="https://github.com/user-attachments/assets/9d6dd7ea-f889-4efc-8a00-c07da7072b02" />

*EIGRP на MLS*

## Шаг 2
Проверяем, обеспечив возможность подключения по SSH с сервера(10.0.0.100), подключенного к подсети 10.0.0.0/8 (R1 и R2), к S1 и SW3.

<img width="535" height="118" alt="Снимок экрана 2026-04-20 161153" src="https://github.com/user-attachments/assets/1acda4d1-671a-486f-a185-ee8ad5ed7415" />

*Проверка на MLS*

<img width="510" height="565" alt="Снимок экрана 2026-04-20 161033" src="https://github.com/user-attachments/assets/6b7aa04d-6aaa-465a-b2db-ba91fdead178" />

*Успешное подключение по SSH*


## Шаг 3
Пингуем с сервера 2.0.0.50

<img width="427" height="196" alt="Снимок экрана 2026-04-20 155939" src="https://github.com/user-attachments/assets/39796b23-d645-4597-b9c4-b1aba9859b36" />

*Успешный пинг*


# Часть 6
## Шаг 1-2
Настраиваем R1 так, чтобы он принимал SSH-соединения только с сервера 10.0.0.100 и ПК 2.0.0.100. Настройте ПК 2.0.0.100 как единственную машину в VLAN 2, которой разрешен доступ к веб-серверу 10.0.0.100.

<img width="615" height="50" alt="Снимок экрана 2026-04-20 161956" src="https://github.com/user-attachments/assets/19795033-26ef-44f7-b499-b4768360bab6" />

*Настраиваем расширенный список контроля доступа (ACL) для фильтрации веб-трафика*

<img width="324" height="60" alt="Снимок экрана 2026-04-20 162019" src="https://github.com/user-attachments/assets/0965b2e2-d510-4d62-bc54-1a630675c449" />

*Активируем список доступа*

🥀

## Шаг 3
Настройте R1 и R2 так, чтобы они могли пинговать любые машины, но никогда не отвечали на запросы ping, поступающие от каких-либо машин.

<img width="420" height="98" alt="Снимок экрана 2026-04-20 162453" src="https://github.com/user-attachments/assets/81bd9337-c8eb-43fe-87b5-d044a09b9cbe" />

*Настраиваем и применяем фильтр, который запрещает пинговать устройства на R1*

<img width="435" height="84" alt="Снимок экрана 2026-04-20 162612" src="https://github.com/user-attachments/assets/820d77d6-8760-4d12-969a-aac10f5649a8" />

*Настраиваем и применяем фильтр, который запрещает пинговать устройства на R2*

# Часть 7
## Шаг 1
Создаем loopback-интерфейс 1 на маршрутизаторе R3 с IP-адресом 192.168.101.1/24.

<img width="578" height="130" alt="Снимок экрана 2026-04-20 163730" src="https://github.com/user-attachments/assets/7cdedd52-2dcf-4008-8e2c-bd5896cf6083" />

*Создание и настройка loopback-интерфейс 1*

## Шаг 2
Создаем loopback-интерфейс 3 на маршрутизаторе R2 с IP-адресом 192.168.103.3/24.

<img width="573" height="118" alt="Снимок экрана 2026-04-20 163830" src="https://github.com/user-attachments/assets/08722506-3983-4319-96fb-caab34eae087" />

*Создание и настройка loopback-интерфейс 3*

## Шаг 3
Проверяем, что R3 и R2 объявляют эти loopback-интерфейсы друг другу, используя RIPv2.

<img width="339" height="124" alt="image" src="https://github.com/user-attachments/assets/50087ac3-04d7-4783-9505-7f583fe323cd" />

*Настройка динамической маршрутизации по протоколу RIPv2 на R3*

<img width="336" height="114" alt="image" src="https://github.com/user-attachments/assets/ce80db7d-4192-4db5-9436-e0bf8cc64a52" />

*Настройка динамической маршрутизации по протоколу RIPv2 на R2*

## Шаг 4
RIPv2 должен работать ТОЛЬКО на R3 и R2.

<img width="232" height="57" alt="image" src="https://github.com/user-attachments/assets/e5ab12f5-7c02-4d7c-bd72-61d63f8d6722" />

*Пусто на MLS*

<img width="409" height="95" alt="image" src="https://github.com/user-attachments/assets/d9ddf8d0-a02f-4932-ba45-51af6d308797" />

*Всё есть на R3*

## Шаг 5
IP-адреса при использовании туннелей должны быть 200.200.200.#/24, где # - это ID маршрутизатора.

<img width="548" height="194" alt="image" src="https://github.com/user-attachments/assets/1dc81555-b4e9-4b09-b0a2-ece450f82d0a" />

*Туннель на R3*

<img width="545" height="208" alt="image" src="https://github.com/user-attachments/assets/176e62bf-2774-47b2-9735-31819f2ada4e" />

*Туннель на R2*

## Шаг 6
С помощью расширенного ping проверяем, что loopback-интерфейс R3 может пинговать loopback-интерфейс R2.

<img width="531" height="297" alt="Снимок экрана 2026-04-20 165309" src="https://github.com/user-attachments/assets/76ddce1d-4ce3-48f5-a0f8-61ea2973e01a" />
*Успешный пинг*

# Часть 8
## Шаг 1
Настраиваем R1, R2, R3 и MLS на использование сервера(10.0.0.100) в качестве защищенного NTP-сервера, используя ключ 1 "cisco", и в качестве Syslog-сервера.

<img width="406" height="100" alt="Снимок экрана 2026-04-20 171026" src="https://github.com/user-attachments/assets/be46a446-2563-4c69-a423-8fd569459c6b" />

*Настройка NTP-сервера на R1*

<img width="412" height="98" alt="Снимок экрана 2026-04-20 171117" src="https://github.com/user-attachments/assets/9497ea0c-0509-47d4-a5f1-615c5ec2c4e0" />

*Настройка NTP-сервера на R2*

<img width="389" height="226" alt="Снимок экрана 2026-04-20 170905" src="https://github.com/user-attachments/assets/deb68a7e-cdd3-4c8d-b18e-27bc7a5acb9e" />

*Настройка NTP-сервера на R3*

<img width="417" height="99" alt="Снимок экрана 2026-04-20 171211" src="https://github.com/user-attachments/assets/a4beb05d-9002-4a17-a243-42bd0b3ab778" />

*Настройка NTP-сервера на MLS1*

## Шаг 2
Включаем SNMP на R1 и R2, используя пароль "cisco" для сообщений set и get.

<img width="549" height="52" alt="Снимок экрана 2026-04-20 171303" src="https://github.com/user-attachments/assets/61692e82-31ca-47ef-b879-0dc8e48f8ced" />

*SNMP на R1*

<img width="546" height="43" alt="Снимок экрана 2026-04-20 171804" src="https://github.com/user-attachments/assets/a76da8b0-01bd-4975-8d2b-fc08c6c5e16d" />

*SNMP на R2*

## Шаг 3
Включаем telnet на R2, используя сервер(10.0.0.100) в качестве ААА-сервера в качестве первого метода аутентификации.

<img width="514" height="86" alt="Снимок экрана 2026-04-20 171809" src="https://github.com/user-attachments/assets/aa1561da-a82d-4e88-907e-878d2aa9bf97" />

*telnet на R2*

## Шаг 4
Настраиваем R1 на использование сервера(10.0.0.100) в качестве FTP-сервера, используя имя пользователя "cisco" и пароль "cisco".

<img width="301" height="26" alt="Снимок экрана 2026-04-20 172429" src="https://github.com/user-attachments/assets/8b89f00c-f9d7-4eb6-b118-a560af21d9a3" />

*Настраиваем R1 на использование сервера в качестве FTP-сервера*

## Шаг 5
Отправляем копию текущей конфигурации R1 на сервер 10.0.0.100, используя протокол FTP.

<img width="397" height="123" alt="Снимок экрана 2026-04-20 172603" src="https://github.com/user-attachments/assets/ac26d063-343d-4507-8272-e08b367af308" />

*Отправляем копию конфига R1 на сервер с помощью FTP протокола*

## Шаг 6
Отправляем копию текущей конфигурации R2 на сервер 10.0.0.100, используя протокол TFTP.

<img width="396" height="128" alt="Снимок экрана 2026-04-20 173009" src="https://github.com/user-attachments/assets/9ac6f550-c8e7-4fdd-abed-3df1d2f0cdeb" />

*Отправляем копию конфига R2 на сервер с помощью TFTP протокола*

<img width="696" height="705" alt="Снимок экрана 2026-04-20 173014" src="https://github.com/user-attachments/assets/84f3f50c-dffa-4b46-9424-700348724d4a" />

*Проверка на сервере*

## Шаг 7
Проверяем, что не используем никаких команд boot system в R2.

<img width="301" height="27" alt="image" src="https://github.com/user-attachments/assets/cc3b0aba-fc2f-432a-8068-407ab2a21584" />

*На R2 не используются команды boot system*

## Шаг 8
Проверяем, что R1 может пинговать, используяимя "standby".

<img width="510" height="109" alt="Снимок экрана 2026-04-20 174017" src="https://github.com/user-attachments/assets/4c6090ef-c889-4169-bb4f-7f37ea5d533f" />

*Проверка пинга на R1*

## Шаг 9
Перезагружаем R2 и нажимаем Ctrl+Break для входа в режим ROMMON.

<img width="510" height="689" alt="Снимок экрана 2026-04-20 180821" src="https://github.com/user-attachments/assets/3438477b-652c-4403-a0d6-73cb6d482467" />

*Вход в режим ROMMON*

Вводим confreg 0x2142, чтобы игнорировать конфиг при загрузке, затем вводим reset.

<img width="225" height="30" alt="Снимок экрана 2026-04-20 180848" src="https://github.com/user-attachments/assets/d412a845-2d4e-4537-b2c7-275ba1b8a681" />

*Вводим команды*

Перезагружается.

<img width="683" height="708" alt="Снимок экрана 2026-04-20 180906" src="https://github.com/user-attachments/assets/eaab6684-adb9-4eb3-8dd2-e2ad536801c7" />

*Перезагружка R2*

Догружается наша конфигурация.

<img width="590" height="229" alt="Снимок экрана 2026-04-20 180959" src="https://github.com/user-attachments/assets/8dfe3ca2-36c8-4052-bcb4-cb517f944b8d" />

*Догружается конфигурация на R2*

Изменяем пользователя и пароль, ворачиваем регистр обратно.

<img width="376" height="32" alt="Снимок экрана 2026-04-20 181515" src="https://github.com/user-attachments/assets/ea924ad9-8ac7-4e43-9040-6c22700fba21" />

*Изменение пользователя и пароля на R2*

Вид итоговой Топологии

<img width="1300" height="593" alt="image" src="https://github.com/user-attachments/assets/38957fc1-47aa-4987-a1b1-9a8476eac859" />

*Итоговая Топология*

# Вывод:
В ходе выполнения практической работы была спроектирована и настроена распределенная сетевая инфраструктура на базе оборудования Cisco. В процессе реализации проекта были успешно решены задачи по обеспечению связности, отказоустойчивости и безопасности сети.

На уровне коммутации произведена сегментация трафика с помощью VLAN и настроены агрегированные каналы EtherChannel. Безопасность доступа обеспечена механизмами Port-Security и фильтрацией BPDU. Сетевая связность реализована через настройку меж-VLAN маршрутизации и протоколов динамической маршрутизации (EIGRP, RIPv2). Создана высокая доступность критических узлов.

Администрирование сети автоматизировано внедрением сервисов DHCP, NTP и Syslog, а управление устройствами защищено протоколом SSHv2 и централизованной аутентификацией. Итоговая конфигурация представляет собой защищенную и масштабируемую систему, готовую к эксплуатации в условиях корпоративной среды.


---
# Блок код
```
rus-msk-mls1
!
version 12.2(37)SE1
no service timestamps log datetime msec
no service timestamps debug datetime msec
no service password-encryption
!
hostname rus-msk-mls1
!
!
ip routing
!
!
ip domain-name msk.com
!
!
spanning-tree mode pvst
!
interface FastEthernet0/1
 no switchport
 ip address 11.0.0.50 255.0.0.0
 duplex auto
 speed auto
!
interface FastEthernet0/2
 no switchport
 ip address 12.0.0.50 255.0.0.0
 duplex auto
 speed auto
!
interface FastEthernet0/3
 no switchport
 ip address 40.40.40.50 255.255.255.0
 duplex auto
 speed auto
!
interface FastEthernet0/4
 switchport access vlan 100
 switchport mode access
!
interface FastEthernet0/5
 switchport access vlan 200
 switchport mode access
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
interface Vlan100
 mac-address 0060.477a.7b01
 ip address 100.0.0.50 255.0.0.0
!
interface Vlan200
 mac-address 0060.477a.7b02
 ip address 200.0.0.50 255.255.255.0
!
router eigrp 100
 network 12.0.0.0
 network 11.0.0.0
 network 40.0.0.0
 network 200.0.0.0
 network 100.0.0.0
 no auto-summary
!
ip classless
!
ip flow-export version 9

!
!
logging trap debugging
logging 10.0.0.100
line con 0
!
line aux 0
!
line vty 0 4
 login
!
!
!
ntp authentication-key 1 md5 0822455D0A16 7
ntp authenticate
ntp trusted-key 1
ntp server 10.0.0.100 key 1
!
end
```

```
rus-msk-r1
!
version 15.1
no service timestamps log datetime msec
no service timestamps debug datetime msec
no service password-encryption
!
hostname rus-msk-r1
!
ip cef
no ipv6 cef
!
!
license udi pid CISCO2811/K9 sn FTX10179NDV-
!
!
ip ftp username cisco
ip ftp password cisco
ip domain-name msk.com
ip host standby 10.0.0.3 
!
!
spanning-tree mode pvst

!
interface FastEthernet0/0
 ip address 10.0.0.2 255.0.0.0
 ip access-group 101 in
 duplex auto
 speed auto
 standby 1 ip 10.0.0.1
 standby 1 priority 110
 standby 1 preempt
 standby 1 track FastEthernet0/1
!
interface FastEthernet0/1
 ip address 11.0.0.2 255.0.0.0
 duplex auto
 speed auto
!
interface Vlan1
 no ip address
 shutdown
!
router eigrp 100
 network 10.0.0.0
 network 11.0.0.0
!
ip classless
!
ip flow-export version 9
!
!
access-list 100 permit tcp host 2.0.0.100 host 10.0.0.100 eq www
access-list 100 deny tcp any host 10.0.0.100 eq www
access-list 100 permit ip any any
access-list 101 deny icmp any any echo
access-list 101 permit ip any any
!
banner motd "Raboty vipoklnila Skvortcova Ksenia Ivanovna student group 321, vi jyrnale pod nomerom 23!"
!
snmp-server community cisco RW
!
logging trap debugging
logging 10.0.0.100
line con 0
!
line aux 0
!
line vty 0 4
 login
!
!
ntp authentication-key 1 md5 0822455D0A16 7
ntp authenticate
ntp trusted-key 1
ntp server 10.0.0.100 key 1
!
end
```

```
## rus-msk-r2
!
version 15.1
no service timestamps log datetime msec
no service timestamps debug datetime msec
no service password-encryption
!
hostname rus-msk-r2
!
!
aaa new-model
!
aaa authentication login default group tacacs+ local 
!
ip cef
no ipv6 cef
!
!
!
username admin password 0 admin
username cisco privilege 15 secret 5 $1$mERr$hx5rVt7rPNoS4wqbXKX7m0
!
!
license udi pid CISCO2811/K9 sn FTX1017W53T-
!
!
ip domain-name msk.com
!
!
spanning-tree mode pvst
!
!
interface Loopback3
 ip address 192.168.103.3 255.255.255.0
!
interface Tunnel3
 ip address 200.200.200.3 255.255.255.0
 mtu 1476
 tunnel source FastEthernet0/1
 tunnel destination 40.40.40.1
!
!
interface FastEthernet0/0
 ip address 10.0.0.3 255.0.0.0
 ip access-group 101 in
 duplex auto
 speed auto
 standby 1 ip 10.0.0.1
 standby 1 preempt
 standby 1 track FastEthernet0/1
!
interface FastEthernet0/1
 ip address 12.0.0.3 255.0.0.0
 duplex auto
 speed auto
!
interface Vlan1
 no ip address
 shutdown
!
router eigrp 100
 network 10.0.0.0
!
router rip
 version 2
 network 192.168.103.0
 network 200.200.200.0
 no auto-summary
!
ip classless
!
ip flow-export version 9
!
!
access-list 101 deny icmp any any echo
access-list 101 permit ip any any
!
banner motd "Raboty vipoklnila Skvortcova Ksenia Ivanovna student group 321, vi jyrnale pod nomerom 23!"
!
tacacs-server host 10.0.0.100 key cisco
!
!
snmp-server community cisco RW
!
logging trap debugging
logging 10.0.0.100
line con 0
!
line aux 0
!
line vty 0 4
 login authentication default
!
!
ntp authentication-key 1 md5 0822455D0A16 7
ntp authenticate
ntp trusted-key 1
ntp server 10.0.0.100 key 1
!
end
```

```

rus-msk-s1
!
version 15.0
no service timestamps log datetime msec
no service timestamps debug datetime msec
no service password-encryption
!
hostname rus-msk-s1
!
!
!
ip domain-name msk.com
!
!
!
spanning-tree mode pvst
spanning-tree extend system-id
!
interface FastEthernet0/1
!
interface FastEthernet0/2
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
!🥀
!
line con 0
!
line vty 0 4
 login
line vty 5 15
 login
!
end

```
```
rus-nsk-r3
!
version 15.1
no service timestamps log datetime msec
no service timestamps debug datetime msec
no service password-encryption
!
hostname rus-nsk-r3
!
ip dhcp excluded-address 1.0.0.200 1.255.255.254
ip dhcp excluded-address 2.0.0.200 2.255.255.254
ip dhcp excluded-address 3.0.0.200 3.255.255.254
ip dhcp excluded-address 4.0.0.200 4.255.255.254
ip dhcp excluded-address 1.0.0.1 1.0.0.99
ip dhcp excluded-address 2.0.0.1 2.0.0.99
ip dhcp excluded-address 4.0.0.1 4.0.0.99
ip dhcp excluded-address 3.0.0.1 3.0.0.99
!
ip dhcp pool VLAN1_POOL
 network 1.0.0.0 255.0.0.0
 default-router 1.0.0.1
ip dhcp pool VLAN2_POOL
 network 2.0.0.0 255.0.0.0
 default-router 2.0.0.1
ip dhcp pool VLAN3_POOL
 network 3.0.0.0 255.0.0.0
 default-router 3.0.0.1
ip dhcp pool VLAN4_POOL
 network 4.0.0.0 255.0.0.0
 default-router 4.0.0.1
!
!
!
ip cef
no ipv6 cef
!
license udi pid CISCO2811/K9 sn FTX1017F8P7-
!
!
ip domain-name nsk.com
!
!
spanning-tree mode pvst
!
interface Loopback1
 ip address 192.168.101.1 255.255.255.0
!
interface Tunnel1
 ip address 200.200.200.1 255.255.255.0
 mtu 1476
 tunnel source FastEthernet0/1
 tunnel destination 12.0.0.3
!
!
interface FastEthernet0/0
 no ip address🥀
 duplex auto
 speed auto
!
interface FastEthernet0/0.1
 encapsulation dot1Q 1 native
 ip address 1.0.0.1 255.0.0.0
!
interface FastEthernet0/0.2
 encapsulation dot1Q 2
 ip address 2.0.0.1 255.0.0.0
!
interface FastEthernet0/0.3
 encapsulation dot1Q 3
 ip address 3.0.0.1 255.0.0.0
!
interface FastEthernet0/0.4
 encapsulation dot1Q 4
 ip address 4.0.0.1 255.0.0.0
!
interface FastEthernet0/1
 ip address 40.40.40.1 255.255.255.0
 duplex auto
 speed auto
!
interface Vlan1
 no ip address
 shutdown
!
router eigrp 100
 network 1.0.0.0
 network 2.0.0.0
 network 3.0.0.0
 network 4.0.0.0
 network 40.0.0.0
!
router rip
 version 2
 network 192.168.101.0
 network 200.200.200.0
 no auto-summary
!
ip classless
!
ip flow-export version 9
!
banner motd "Raboty vipoklnila Skvortcova Ksenia Ivanovna student group 321, vi jyrnale pod nomerom 23!"
!
logging trap debugging
logging 10.0.0.100
line con 0
!
line aux 0
!
line vty 0 4
 login
!
!
ntp authentication-key 1 md5 0822455D0A16 7
ntp authenticate
ntp trusted-key 1
ntp server 10.0.0.100 key 1
!
end

```

```
rus-nsk-s2
!
version 15.0
no service timestamps log datetime msec
no service timestamps debug datetime msec
service password-encryption
!
hostname rus-nsk-s2
!
enable secret 5 $1$mERr$hx5rVt7rPNoS4wqbXKX7m0
!
!
!
ip ssh version 2
ip domain-name nsk.com
!
username nsk privilege 1 password 7 0822455D0A16
!
!
!
spanning-tree mode pvst
spanning-tree extend system-id
!
interface Port-channel1
 switchport mode trunk
!
interface FastEthernet0/1
!
interface FastEthernet0/2
 switchport access vlan 2
 switchport port-security mac-address sticky 
 no cdp enable
 spanning-tree portfast
 spanning-tree bpduguard enable
!
interface FastEthernet0/3
 switchport access vlan 3
 switchport port-security mac-address sticky 
 no cdp enable
 spanning-tree portfast
 spanning-tree bpduguard enable
!
interface FastEthernet0/4
 switchport access vlan 4
 switchport port-security mac-address sticky 
 no cdp enable
 spanning-tree portfast
 spanning-tree bpduguard enable
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
 switchport mode trunk
!
interface GigabitEthernet0/1
 switchport mode trunk
 channel-group 1 mode desirable
!
interface GigabitEthernet0/2
 switchport mode trunk
 channel-group 1 mode desirable
!
interface Vlan1
 ip address 1.0.0.50 255.0.0.0
!
ip default-gateway 1.0.0.1
!
banner motd "Eto is rus-nsk-s2"
!
line con 0
 logging synchronous
 login local
 history size 256
 exec-timeout 0 0
!
line vty 0 4
 login local
 transport input ssh
line vty 5 15
 login local
 transport input ssh
!
!
end

```
```
rus-nsk-s3
!
version 15.0
no service timestamps log datetime msec
no service timestamps debug datetime msec
service password-encryption
!
hostname rus-nsk-s3
!
enable secret 5 $1$mERr$hx5rVt7rPNoS4wqbXKX7m0
!
!
!
ip ssh version 2
ip domain-name nsk.com
!
username nsk privilege 1 password 7 0822455D0A16
!
spanning-tree mode pvst
spanning-tree extend system-id
!
interface Port-channel1
 switchport mode trunk
!
interface FastEthernet0/1
!
interface FastEthernet0/2
 switchport access vlan 2
 switchport port-security mac-address sticky 
 no cdp enable
 spanning-tree portfast
 spanning-tree bpduguard enable
!
interface FastEthernet0/3
 switchport access vlan 3
 switchport port-security mac-address sticky 
 no cdp enable
 spanning-tree portfast
 spanning-tree bpduguard enable
!
interface FastEthernet0/4
 switchport access vlan 4
 switchport port-security mac-address sticky 
 no cdp enable
 spanning-tree portfast
 spanning-tree bpduguard enable
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
 switchport mode trunk
 channel-group 1 mode desirable
!
interface GigabitEthernet0/2
 switchport mode trunk
 channel-group 1 mode desirable
!
interface Vlan1
 no ip address
 shutdown
!
interface Vlan2
 ip address 2.0.0.50 255.0.0.0
!
ip default-gateway 2.0.0.1
!
banner motd "Eto is rus-nsk-s3"
!
line con 0
 logging synchronous
 login local
 history size 256
 exec-timeout 0 0
!
line vty 0 4
 login local
 transport input ssh
line vty 5 15
 login local
 transport input ssh
!
end
```
`строка кода`

