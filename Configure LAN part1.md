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
Создаем Management interface на S2 коммутаторе для VLAN 1, используя IP-
адрес 1.0.0.50/8 и шлюз по умолчанию 1.0.0.1.
<img width="568" height="192" alt="Снимок экрана 2026-04-16 152217" src="https://github.com/user-attachments/assets/76255d6e-5567-4a51-a734-9d81c0679536" />

## Шаг 9
Создаем Management interface на коммутаторе S3 для VLAN 2, используя IP-
адрес 2.0.0.50/8 и шлюз по умолчанию 2.0.0.1.
<img width="559" height="188" alt="Снимок экрана 2026-04-16 152758" src="https://github.com/user-attachments/assets/d417d0f2-b6e0-4b76-a836-e8b3231eae8f" />

## Шаг 10
Включаем SSHv2 на коммутаторах в Новосибирске, используя имя пользователя "nsk" и пароль "cisco"
<img width="501" height="101" alt="Снимок экрана 2026-04-16 153722" src="https://github.com/user-attachments/assets/7603ef99-dcee-4cd1-853a-aeafcf4b3f56" />
*Генерация ключей включена*

<img width="341" height="17" alt="Снимок экрана 2026-04-16 153838" src="https://github.com/user-attachments/assets/a41d6b69-d731-4dd0-9560-bca8619d378f" />
*Задали имя и пароль*

<img width="327" height="113" alt="Снимок экрана 2026-04-16 161143" src="https://github.com/user-attachments/assets/12126b0a-e1e6-4333-b584-fe76c964adbf" />

<img width="373" height="70" alt="Снимок экрана 2026-04-16 162853" src="https://github.com/user-attachments/assets/67afdde0-a6e4-42a6-a353-0a8a7a6ab916" />

## Шаг 11
Интерфейс f0/24 коммутатора S2 будет подключен к маршрутизатору R1 для межсетевой маршрутизации VLAN на транке.


## Шаг 12


## Шаг 13
