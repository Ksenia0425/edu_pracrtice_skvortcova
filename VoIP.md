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

```
# Блок код

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

```
# Блок код

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

```
# Блок код

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

```
# Блок код

```
Контрольные вопросы

# 8. Лабораторная работа. Построение сети IP-телефонии между удаленными маршрутизаторами

Собираем топологию по заданию.

<img width="513" height="501" alt="Снимок экрана 2026-05-06 160809" src="https://github.com/user-attachments/assets/63405242-02ca-4273-92e7-31bc92351dd9" />

*Топология сети*

Переменовываем маршрутизатор и настраиваем интерфейс s0/1/0.

