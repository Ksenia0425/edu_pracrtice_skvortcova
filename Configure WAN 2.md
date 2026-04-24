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

# Часть 3
## Шаг 1
Настаиваем OSPFv2 на маршрутизаторах R1, R2 и R3.

<img width="192" height="22" alt="Снимок экрана 2026-04-23 171831" src="https://github.com/user-attachments/assets/a0cf592d-ee99-451e-889f-74079ef905a7" />

*OSPFv2 на R1*

<img width="208" height="22" alt="image" src="https://github.com/user-attachments/assets/870adb28-61af-429e-bdc4-410bc34aad6e" />

*OSPFv2 на R2*

<img width="194" height="19" alt="image" src="https://github.com/user-attachments/assets/bacc9187-df92-457e-9683-8af3d94e591e" />

*OSPFv2 на R3*

## Шаг 2
Настраиваем на маршрутизаторе R2 использовальзование ID маршрутизатора 0.0.0.2.

<img width="255" height="20" alt="image" src="https://github.com/user-attachments/assets/a18c63b6-b07c-45de-b109-2842dd39631e" />

*На R2 ID маршрутизатора 0.0.0.2*

## Шаг 3
Настраиваем маршрутизаторы R1, R2, R3, чтобы они объявляли все свои подключенные сети в OSPF.

<img width="381" height="31" alt="image" src="https://github.com/user-attachments/assets/2ed2cdc6-b531-4c41-a92b-163ab2a364c7" />

*Настройка на R1*

<img width="390" height="30" alt="image" src="https://github.com/user-attachments/assets/0667a598-d03e-4f3f-9e13-6ad9de4cecb7" />

*Настройка на R2*

<img width="436" height="64" alt="image" src="https://github.com/user-attachments/assets/a1c354fd-fdc1-4802-a685-3f7e2d4e7878" />

*Настройка на R3*

## Шаг 4
Используем ID процесса 100 для OSPF на всех маршрутизаторах (R1, R2 и R3).

<img width="192" height="22" alt="Снимок экрана 2026-04-23 171831" src="https://github.com/user-attachments/assets/a1c53f26-6c62-4dd0-865b-f43efa326d99" />

*ID 100 для OSPF на R1*

<img width="208" height="22" alt="image" src="https://github.com/user-attachments/assets/3658ffac-0727-4edb-ac41-eddb7f6adb82" />

*ID 100 для OSPF на R2*

<img width="194" height="19" alt="image" src="https://github.com/user-attachments/assets/cbea1c75-6cc4-455c-8c99-59a8972c3ca6" />

*ID 100 для OSPF на R3*

## Шаг 5
Настраиваем интерфейс f0/0 на маршрутизаторе R1, чтобы он принадлежал зоне 1.

<img width="237" height="34" alt="image" src="https://github.com/user-attachments/assets/b859dc57-cb8c-4e74-bec4-5278db936d65" />

*f0/0 на R1 принадлежит зоне 1*

## Шаг 6
Настраиваем интерфейс f0/1 на маршрутизаторе R1, чтобы он принадлежал зоне 0.

<img width="236" height="29" alt="Снимок экрана 2026-04-24 145505" src="https://github.com/user-attachments/assets/5872100a-80c4-4a7d-ad79-84f70a6ff01b" />

*f0/1 на R1 принадлежит зоне 0*

## Шаг 7
Настраиваем интерфейс f0/0 на маршрутизаторе R2, чтобы он принадлежал зоне 23.

<img width="250" height="35" alt="image" src="https://github.com/user-attachments/assets/e689ba08-ca8a-488d-82ab-91d5fdfed6bf" />

*f0/0 на R2 принадлежит зоне 23*

## Шаг 8
Настраиваем интерфейс f0/1 на маршрутизаторе R2, чтобы он принадлежал зоне 0.

<img width="238" height="34" alt="image" src="https://github.com/user-attachments/assets/3337ac03-1f5c-4e36-8b50-d8e078c92151" />

*f0/1 на R2 принадлежит зоне 0*

## Шаг 9
Настраиваем интерфейсы g0/0, loopback3 и loopback33 на R3, чтобы они принадлежали зоне 23.

<img width="248" height="117" alt="image" src="https://github.com/user-attachments/assets/a4300fb7-23e1-46a7-a583-d4b897ae17c9" />

*g0/0, loopback3 и loopback33 на R3 принадлежат зоне 23*

## Шаг 10
Блокируем отправку hello-пакетов OSPF на всех интерфейсах маршрутизатора R1, кроме интерфейса f0/1.

<img width="629" height="145" alt="image" src="https://github.com/user-attachments/assets/e7d27b02-adc0-4101-8d40-d309d7fb972b" />

*Блокировка hello-пакетов OSPF на интерфейсах R1, кроме f0/1*

## Шаг 11
Настраиваем маршрутизатор R2, чтобы он всегда был назначенным маршрутизатором (DR) на всех многодоступовых сетях (broadcast и NBMA).

<img width="257" height="89" alt="image" src="https://github.com/user-attachments/assets/39e88f88-b767-4681-961b-1300104baa8b" />

*R2 назначенный маршрутизатор на всех многодоступовых сетях*

<img width="565" height="456" alt="image" src="https://github.com/user-attachments/assets/a7bb5f91-1db8-434b-a6bc-868cb8296727" />

*Проверка на R2 ip ospf*

## Шаг 12
Настраиваем маршрутизатор R3, чтобы он работал в качестве шлюза по умолчанию для всех маршрутизаторов OSPF и они могли взаимодействовать с любыми другими сетями.

<img width="361" height="24" alt="image" src="https://github.com/user-attachments/assets/02ad5ccf-1c6f-4faf-9c45-19e9247a4d34" />

*Статический маршрут по умполчанию на R3*

<img width="345" height="32" alt="image" src="https://github.com/user-attachments/assets/04127ff8-62e5-4066-8ad0-997be7ee8b8a" />

*Делаем R3 шлюзом по умполчанию*

<img width="541" height="362" alt="image" src="https://github.com/user-attachments/assets/6b4c7a3f-b153-49f6-b5e3-f956444ce6e4" />

*Проверка*

# Часть 4
## Шаг 1-3
Настраиваем BGP между R3 и R1973. Указываем, что все маршрутизаторы, использующие протокол OSPF, находятся в автономной системе BGP (AS) номер 3. Настраиваем маршрутизатор R1973, чтобы он находился в автономной системе BGP (AS) номер 1973.

<img width="175" height="23" alt="image" src="https://github.com/user-attachments/assets/9fde23c7-2b3b-44b6-9ac3-3a5a6a3b97e8" />

*На R3 BGP*

<img width="219" height="15" alt="image" src="https://github.com/user-attachments/assets/a70cbb6d-eae5-46db-bb5a-465fa4d50de8" />

*На R1973 BGP*

## Шаг 4
Настраиваем маршрутизатор R3 для установления внешнего BGP-соседства с маршрутизатором R1973.

<img width="431" height="37" alt="image" src="https://github.com/user-attachments/assets/37c87c47-9dcb-431f-a025-69dffad376bf" />

*R3 для внешнего BGP-соседства*

<img width="443" height="39" alt="image" src="https://github.com/user-attachments/assets/5143fc93-56f0-4b9f-a0c8-f197205ed58b" />

*R1973 для внешнего BGP-соседства*

## Шаг 5
Настраиваем маршрутизатор R1973 так, чтобы он объявил свой loopback-интерфейс маршрутизатору R3.

<img width="422" height="25" alt="image" src="https://github.com/user-attachments/assets/c3f233d2-1c24-4a31-8977-b0905922343b" />

*R1973 объявляет loopback-интерфейс маршрутизатору R3*

## Шаг 6
Настраиваем маршрутизатор R1973 так, чтобы маршрут по умолчанию указывал на маршрутизатор R3.

<img width="385" height="17" alt="image" src="https://github.com/user-attachments/assets/7bad43e6-4dde-4203-bf43-34e5194a8aa8" />

*На R1973 маршрут по умолчанию указывал на R3*

<img width="260" height="34" alt="image" src="https://github.com/user-attachments/assets/478da0d2-e3fd-4a5a-b434-2ae660d8ec33" />

*Проверяем маршрут по умолчанию*

# Часть 5
## Шаг 1
Проверяем, что IOS на R3 поддерживает все команды VOIP и расширенные настройки безопасности, используя для этого оценочную лицензию.

<img width="575" height="96" alt="image" src="https://github.com/user-attachments/assets/5b234dff-eb99-41a6-b559-f6a40d39b341" />

*Проверяем использование оценочной стоимости*

## Шаг 2
Устанавиливаем лицензии UCK9.

<img width="506" height="351" alt="Снимок экрана 2026-04-24 170907" src="https://github.com/user-attachments/assets/13aca22e-684d-49f7-ba56-c0a7d5ed8989" />

*Устанавливаем лиценцию UCK9*

<img width="654" height="273" alt="image" src="https://github.com/user-attachments/assets/f6736e19-f85e-4852-8daf-4e0e0d8d1562" />

*Соглашаемся и всё устанавливается*

## Шаг 3
Устанавливаем лицензии securityk9.

<img width="551" height="397" alt="image" src="https://github.com/user-attachments/assets/d3b2f8dc-de20-4a55-9754-ba022a759fcf" />

*Устанавливаем лицензии securityk9*

<img width="648" height="287" alt="image" src="https://github.com/user-attachments/assets/61062462-2db7-485b-985b-5af66a4c77e4" />

*Соглашаемся и всё устанавливается*

## Шаг 4
Сохраняем конфигурацию.

<img width="285" height="75" alt="image" src="https://github.com/user-attachments/assets/efaa833a-9653-4153-bc62-dec5cb07178b" />

*Конфигурация сохранена*
## Шаг 5
Перезагрузите маршрутизатор.
<img width="634" height="376" alt="image" src="https://github.com/user-attachments/assets/95eed1dc-fd1c-4f4c-9329-01700a970c97" />

*Перезагрузка*
