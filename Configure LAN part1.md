# Часть 1
## Шаг 1
Согласно схеме (Москва и Новосибирск), в среде моделирования Packet Tracer создали сеть, включающая маршрутизаторы R1, R2, R3, многоуровневый коммутатор MLS и оконечные устройства.

<img width="1120" height="572" alt="Снимок экрана 2026-04-15 150452" src="https://github.com/user-attachments/assets/619f6419-7eb2-4cd8-8a7a-391f7731669b" />

## Шаг 2
Для идентификации администратора на всех роутерах настроено приветственное сообщение.

<img width="628" height="39" alt="Снимок экрана 2026-04-15 161024" src="https://github.com/user-attachments/assets/67eee20c-cd0b-4252-8278-fe49d7f5a4af" />

##  Шаг 3
Переменовываем все устройства по шаблону страна-город-роль устройства-порядковый номер.

<img width="246" height="31" alt="image" src="https://github.com/user-attachments/assets/a70c4867-c867-4ac2-8695-021478b740dd" />

## Шаг 4
Раздаем устройствам доменные имена согласно местоположению.

МСК:

<img width="308" height="22" alt="Снимок экрана 2026-04-15 162510" src="https://github.com/user-attachments/assets/0e0244f5-7705-4f4a-8d66-3286fbb8a793" />

НСК:

<img width="321" height="17" alt="Снимок экрана 2026-04-15 180839" src="https://github.com/user-attachments/assets/8e5c86c9-30df-46c6-9e95-c3f330180eaa" />

## Шаг 5
Создаем на коммутаторах НСК VLAN 2, 3, 4.

<img width="210" height="77" alt="Снимок экрана 2026-04-15 165050" src="https://github.com/user-attachments/assets/e19482d9-d051-4f48-99ee-8f8048778257" />

## Шаг 6
Теперь этим коммутаторам назначаем интерфейс f0/2 VLAN 2, интерфейс f0/3 VLAN 3, а интерфейс f0/4 VLAN 4.

<img width="342" height="90" alt="Снимок экрана 2026-04-15 165147" src="https://github.com/user-attachments/assets/91213d2b-2bde-4568-8295-8857de8c5fd3" />

## Шаг 7
Создаем канал EtherChannel 2-го уровня между коммутаторами в НСК, используя интерфейсы G0/1 и G0/2, опираясь на требования в работе.

<img width="595" height="212" alt="Снимок экрана 2026-04-15 181426" src="https://github.com/user-attachments/assets/58f29b19-3ba1-41db-995c-16cf649e8c05" />

## Шаг 8
Создаем Management interface на S2 коммутаторе для VLAN 1, используя IP- адрес 1.0.0.50/8 и шлюз по умолчанию 1.0.0.1.

<img width="568" height="192" alt="Снимок экрана 2026-04-16 152217" src="https://github.com/user-attachments/assets/76255d6e-5567-4a51-a734-9d81c0679536" />

## Шаг 9
Создаем Management interface на коммутаторе S3 для VLAN 2, используя IP-адрес 2.0.0.50/8 и шлюз по умолчанию 2.0.0.1.

<img width="559" height="188" alt="Снимок экрана 2026-04-16 152758" src="https://github.com/user-attachments/assets/d417d0f2-b6e0-4b76-a836-e8b3231eae8f" />

## Шаг 10
Включаем SSHv2 на коммутаторах в Новосибирске, используя имя пользователя "nsk" и пароль "cisco".

<img width="501" height="101" alt="Снимок экрана 2026-04-16 153722" src="https://github.com/user-attachments/assets/7603ef99-dcee-4cd1-853a-aeafcf4b3f56" />
*Генерация ключей включена*

<img width="341" height="17" alt="Снимок экрана 2026-04-16 153838" src="https://github.com/user-attachments/assets/a41d6b69-d731-4dd0-9560-bca8619d378f" />
*Задали имя и пароль*

<img width="327" height="113" alt="Снимок экрана 2026-04-16 161143" src="https://github.com/user-attachments/assets/12126b0a-e1e6-4333-b584-fe76c964adbf" />
* *

<img width="373" height="70" alt="Снимок экрана 2026-04-16 162853" src="https://github.com/user-attachments/assets/67afdde0-a6e4-42a6-a353-0a8a7a6ab916" />
* *

## Шаг 11
Интерфейс f0/24 коммутатора S2 будет подключен к маршрутизатору R1 для межсетевой маршрутизации VLAN на транке.

<img width="322" height="63" alt="Снимок экрана 2026-04-16 163423" src="https://github.com/user-attachments/assets/d75f82c9-a0ad-4d12-b49f-dae011763f1d" />


## Шаг 12
Настраиваем сообщение на S2 и S3.

<img width="230" height="62" alt="image" src="https://github.com/user-attachments/assets/8e7cb36b-f42c-49bb-962c-bf218ba5817a" />

*Вход с сообщением*

## Шаг 13
Настроиваем интерфейсы f0/2, f0/3 и f0/4 на коммутаторах S2 и S3 согласно требованиям задания.

<img width="531" height="350" alt="Снимок экрана 2026-04-16 164327" src="https://github.com/user-attachments/assets/9c0ea4c0-0720-4fa4-91cc-df613b5382fc" />
**

<img width="528" height="215" alt="Снимок экрана 2026-04-16 164602" src="https://github.com/user-attachments/assets/d044e905-7a43-4822-ad0f-3c34641df28e" />
**

## Шаг 14
Создаем защищенное консольное подключение на S2 и S3.

<img width="278" height="34" alt="Снимок экрана 2026-04-16 170138" src="https://github.com/user-attachments/assets/4cd9a87d-6af1-4738-8e6d-2ca7a69599ee" />

## Шаг 15
Отключаем таймаут для консоли и SSH на S2 и S3.

<img width="302" height="14" alt="Снимок экрана 2026-04-16 170314" src="https://github.com/user-attachments/assets/fc80d889-4eaf-492b-9933-7a51343e9592" />


## Шаг 16
Делаем предотвращение консольной сессии каждым выводом журнала на S2 и S3.

<img width="326" height="16" alt="Снимок экрана 2026-04-16 170329" src="https://github.com/user-attachments/assets/0467bc9f-278a-4d9d-837d-1522b11b8ed0" />


## Шаг 17
Изменяем буфер обмена истории до 256 строк.

<img width="297" height="16" alt="Снимок экрана 2026-04-16 170348" src="https://github.com/user-attachments/assets/1f7d29b2-a3c9-4868-874a-9f1f025dca50" />

# Часть 2

## Шаг 1
Назнаем интерфейсу f0/1 маршрутизатора R3 IP-адрес 40.40.40.1/24.

<img width="610" height="140" alt="Снимок экрана 2026-04-16 171042" src="https://github.com/user-attachments/assets/d0ef1f21-d15d-485d-8fc4-10fb4143989c" />


## Шаг 2
Настраиваем R3 для поддержки маршрутизации между VLAN 1, 2, 3, 4 для S3 и S1, следуя требованиям задания.

<img width="618" height="142" alt="Снимок экрана 2026-04-16 171412" src="https://github.com/user-attachments/assets/d0b15004-b2eb-4a60-8433-9cd93eb9abd4" />

<img width="629" height="505" alt="Снимок экрана 2026-04-16 171717" src="https://github.com/user-attachments/assets/fcf00cfa-a1e2-48c8-ab19-d688631ec3d4" />


## Шаг 3
Настриваем R3 в качестве DHCP-сервера для любой машины, подключенной к VLAN 1, 2, 3, 4 на S2 и S3, используя требования задания.

<img width="533" height="335" alt="Снимок экрана 2026-04-16 172942" src="https://github.com/user-attachments/assets/f4fddaa2-8f29-4b9b-814b-ba0db66ad792" />

<img width="429" height="44" alt="Снимок экрана 2026-04-16 180731" src="https://github.com/user-attachments/assets/bea23fe0-472c-4fb6-83e8-ef2753e064d8" />

*Делаем исключения*

<img width="433" height="14" alt="Снимок экрана 2026-04-16 180735" src="https://github.com/user-attachments/assets/287f1388-0e58-42e1-9bc9-149f19bc11ab" />

*Доделываем исключения*

## Шаг 4
3.0.0.101 пингуем с РС3.

<img width="425" height="218" alt="Снимок экрана 2026-04-16 180719" src="https://github.com/user-attachments/assets/71cba6b6-2b7d-4358-ba72-e954907b98ee" />
*Успешный пинг*

## Шаг 4
3.0.0.101 пингуем с РС3.

<img width="425" height="218" alt="Снимок экрана 2026-04-16 180719" src="https://github.com/user-attachments/assets/71cba6b6-2b7d-4358-ba72-e954907b98ee" />
*Успешный пинг*

# Часть 3
## Шаг 1
Настраиваем имя хоста многоуровневого коммутатора (Multilayer Switch) на MLS.
<img width="266" height="30" alt="Снимок экрана 2026-04-21 161232" src="https://github.com/user-attachments/assets/5c348726-ff68-46af-a0b2-29303de2cac4" />

## Шаг 2
Включаем возможности маршрутизации на MLS.
<img width="233" height="17" alt="Снимок экрана 2026-04-16 181129" src="https://github.com/user-attachments/assets/8ebbacfb-e2c5-49f7-9912-2bbed4373c46" />

Создаём VLAN 100 с именем Sales_dept и VLAN 200 с именем IT_dept.
<img width="299" height="84" alt="Снимок экрана 2026-04-16 181134" src="https://github.com/user-attachments/assets/8147ad1d-823d-4bb1-b94d-c66cd3defd65" />


Шаг 4: 
Назнаем интерфейс f0/4 VLAN 100, а интерфейс f0/5 VLAN 200.
<img width="385" height="167" alt="Снимок экрана 2026-04-16 181748" src="https://github.com/user-attachments/assets/33582170-9108-4e42-bac8-256c8bf8349d" />


Шаг 5. 
Включаем маршрутизацию между VLAN 100 и VLAN 200, используя SVI (Switch Virtual Interface) на MLS, с требованиями по заданию (VLAN 100 - 100.0.0.50/8, VLAN 200 - 200.0.0.50/24
<img width="589" height="296" alt="Снимок экрана 2026-04-20 143559" src="https://github.com/user-attachments/assets/4e2e284b-bf1a-4b52-8aa8-be5eca49d576" />


Шаг 6. 
Изменяем интерфейсы f0/1(11.0.0.50/8), f0/2(12.0.0.50/8) и f0/3(40.40.40.50/24) на интерфейсы 3-го уровня со следующими требованиями.

<img width="416" height="98" alt="Снимок экрана 2026-04-20 143709" src="https://github.com/user-attachments/assets/04c88b7d-05a2-49cc-a9e5-aedf9be92762" />

*Интерфейс f0/1*

<img width="446" height="73" alt="Снимок экрана 2026-04-20 143826" src="https://github.com/user-attachments/assets/7cb66a97-1f05-4a8c-96e6-efe69c933c54" />


*Интерфейс f0/2*

<img width="618" height="142" alt="Снимок экрана 2026-04-20 143939" src="https://github.com/user-attachments/assets/087aa106-d245-469f-8e26-65e99c2e4d1c" />

*Интерфейс f0/3*

Шаг 7. 
Пропингуем 200.0.0.100 с РС1

<img width="448" height="230" alt="Снимок экрана 2026-04-20 144903" src="https://github.com/user-attachments/assets/551b21ea-a36d-49ef-b133-2fda2e8e1394" />

