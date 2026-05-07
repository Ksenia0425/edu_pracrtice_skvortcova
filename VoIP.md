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

**

Настраиваем телефонный сервис в автоматическом режиме. Задаем максимальное количество номеров, присваиваемых IP-телефоном. Задаем максимальное количество IP-телефонов. Задаем IP-адреса.

<img width="502" height="83" alt="Снимок экрана 2026-05-04 184817" src="https://github.com/user-attachments/assets/10e79345-ac31-4cd2-96a7-8f47753081f6" />

**

На коммутаторе в сети VLAN нужно назначить диапазоны портов.

<img width="358" height="47" alt="Снимок экрана 2026-05-04 185048" src="https://github.com/user-attachments/assets/e8904b54-8e30-411c-93bf-b8e4e9ae1576" />

**

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

