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


