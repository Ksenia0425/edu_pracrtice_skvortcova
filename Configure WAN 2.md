# Часть 1
## Шаг 1
Делаем сеть согласно топологии.

<img width="1319" height="498" alt="Снимок экрана 2026-04-23 151821" src="https://github.com/user-attachments/assets/4a9ee92c-2d0a-4c88-ab87-d2ffd47f58a8" />

*Топология сети*

## Шаг 2
Настраиваем R1 согласно требованиям.

<img width="477" height="267" alt="Снимок экрана 2026-04-23 152719" src="https://github.com/user-attachments/assets/9a1b2a4f-db95-48fe-9da2-f8e802b95fe7" />

*Раздача IP-адресов интерфейсам на R1*

## Шаг 3
Настраиваем R2 согласно требованиям.

<img width="608" height="184" alt="Снимок экрана 2026-04-23 153257" src="https://github.com/user-attachments/assets/892995eb-fc21-4e8d-a1ab-8548b4982e1c" />

*Раздача IP-адресов интерфейсам на R2*

## Шаг 4
Настраиваем R3 согласно требованиям.

<img width="577" height="294" alt="Снимок экрана 2026-04-23 153631" src="https://github.com/user-attachments/assets/17e68acf-869c-4fe4-a7f3-7be0ebf95a90" />

*Раздача IP-адресов интерфейсам loopback на R3*

<img width="629" height="224" alt="Снимок экрана 2026-04-23 153909" src="https://github.com/user-attachments/assets/7605ac8d-01ab-4e24-86e9-60322e1ccade" />

*Раздача IP-адресов интерфейсам на R3*

## Шаг 5
Настраиваем R1973 согласно требованиям.

<img width="599" height="266" alt="Снимок экрана 2026-04-23 163031" src="https://github.com/user-attachments/assets/cb4c2b75-6161-4aa9-b1cc-e7f3eb2feb9d" />

*Раздача IP-адресов интерфейсам на R1973*

# Часть 2
## Шаг 1
Настраиваем последовательные интерфейсы между R3 и R1973 с использованием протокола инкапсуляции PPP и убедитесь, что оба маршрутизатора аутентифицируют друг друга с использованием максимально надежного протокола аутентификации.

<img width="219" height="57" alt="Снимок экрана 2026-04-23 164146" src="https://github.com/user-attachments/assets/78922ec5-9370-49f1-8bb9-70c84b3558f5" />

*Устанавливаем скорость синхронизации для DCE-стороны кабеля на R3*

<img width="271" height="59" alt="Снимок экрана 2026-04-23 164341" src="https://github.com/user-attachments/assets/b15a781e-101a-4af4-a60c-eb13a71981fd" />

*Последовательные интерфейсы на R3*

<img width="635" height="71" alt="Снимок экрана 2026-04-23 163735" src="https://github.com/user-attachments/assets/8e0b056e-bad3-4fad-a70a-dc4c3fb2ffa6" />

*Последовательные интерфейсы на R1973*

Теперь делаем проверку работает ли.

<img width="484" height="405" alt="Снимок экрана 2026-04-23 164412" src="https://github.com/user-attachments/assets/bda272d3-4b25-4afc-ab82-5099cab32cdd" />

*Проверка интерфейса s0/0/0 на R3*

<img width="500" height="433" alt="Снимок экрана 2026-04-23 164549" src="https://github.com/user-attachments/assets/4067eb40-47ed-4820-b449-c3883252447a" />

*Проверка интерфейса s0/0/0 на R1973*
