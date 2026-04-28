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

# Часть 6
## Шаг 1
Настраиваем R1 в качестве DHCP-ретранслятора.

<img width="682" height="281" alt="image" src="https://github.com/user-attachments/assets/27fb70d3-11bf-4faa-8558-a0b2e6b9880e" />

*Даем DCHP-серверу статический адрес*

<img width="694" height="542" alt="Снимок экрана 2026-04-28 150529" src="https://github.com/user-attachments/assets/3552fefe-b23e-45d7-9592-7ac14ce114f9" />

*Настраиваем раздачу с серверу*

<img width="331" height="47" alt="Снимок экрана 2026-04-24 172609" src="https://github.com/user-attachments/assets/6ac88667-3954-44e6-8f78-f6fa90d58b40" />

*Делаем R1 в качестве DHCP-ретранслятора*

<img width="423" height="315" alt="Снимок экрана 2026-04-24 172646" src="https://github.com/user-attachments/assets/c78e13b1-987f-4137-9b1b-8773f6ce501b" />

*Проверяем на R1 настройку*

## Шаг 2
Проверяем, что РC0 может получить IPv4 от DHCP-сервера с IP 10.23.23.100.

<img width="691" height="303" alt="image" src="https://github.com/user-attachments/assets/b7ea4b1a-7be7-45bd-98e0-e54b99462a43" />

*PC0 получил адрес*

# Часть 7
## Шаг 1
Настраиваем маршрутизаторы R1, R2, R3, R1973 с IPv6-адресами.

<img width="373" height="71" alt="Снимок экрана 2026-04-28 152242" src="https://github.com/user-attachments/assets/15f80731-9662-4d8b-bde4-70bee8da55d1" />

*IPv6 адерса на R1 на интерфейсе f0/0, делаем локальный адрес*

<img width="338" height="101" alt="image" src="https://github.com/user-attachments/assets/e6ef0a3e-3d95-44a0-a2ae-9ef294889257" />

*IPv6 адерса на R1 на интерфейсе f0/1*

<img width="365" height="90" alt="image" src="https://github.com/user-attachments/assets/d9f24a2c-0bea-4e46-a335-07c3766031ab" />

*IPv6 адерса на R2 на интерфейсе f0/0*

<img width="339" height="70" alt="image" src="https://github.com/user-attachments/assets/da5bbc9d-c098-4c59-a858-4ddc54cc6fa3" />

*IPv6 адерса на R2 на интерфейсе f0/1*

<img width="345" height="68" alt="image" src="https://github.com/user-attachments/assets/0175b533-0751-4752-ab1c-f5b918850742" />

*IPv6 адерса на R3 на интерфейсе g0/0*

<img width="342" height="133" alt="image" src="https://github.com/user-attachments/assets/cd398615-8017-4192-95e9-658f2aa45715" />

*IPv6 адерса на R3 на интерфейсе s0/0/0*

<img width="426" height="101" alt="image" src="https://github.com/user-attachments/assets/c291f60a-6685-4a2e-b895-f48d2b7ed63d" />
*IPv6 адерса на R1973 на интерфейсе loopback*

<img width="370" height="66" alt="image" src="https://github.com/user-attachments/assets/a25fbe56-b001-4231-ad24-62a714e340d5" />

*IPv6 адерса на R1973 на интерфейсе s0/0/0*

## Шаг 2
Проверяем, что на всех маршрутизаторах включена возможность маршрутизации IPv6.

<img width="257" height="21" alt="image" src="https://github.com/user-attachments/assets/a3ce87a3-1a4d-41a4-9708-3ade0301910c" />

*Включаем маршрутизацию IPv6 на всех маршрутизаторах*

<img width="412" height="180" alt="image" src="https://github.com/user-attachments/assets/7d8fd573-bb1c-4026-ba69-70589524b387" />

*Проверяем на R1*

<img width="410" height="140" alt="image" src="https://github.com/user-attachments/assets/22fece4c-a37f-47f1-94a8-dd480c892419" />

*Проверяем на R2*

<img width="438" height="280" alt="image" src="https://github.com/user-attachments/assets/0fb62089-cdce-409d-ae2b-4473ab4a2cda" />

*Проверяем на R3*

<img width="395" height="242" alt="image" src="https://github.com/user-attachments/assets/ca1fb4ec-e5ec-4b06-afad-f2411e94aa6d" />

*Проверяем на R1973*

## Шаг 3
Проверяем, что интерфейс f0/0 на маршрутизаторе R1 использует локальный адрес канала fe80::1.

<img width="433" height="352" alt="image" src="https://github.com/user-attachments/assets/265611f5-1302-418d-ae96-5238f99a89d4" />

*Проверяем*

## Шаг 4
Проверяем, что R1 использует функцию EUI-64 для своего глобального адреса на интерфейсе f0/0.

<img width="409" height="315" alt="image" src="https://github.com/user-attachments/assets/a09227f9-fc97-46c3-a245-edf35b8be61e" />

*R1 использует EUI-64 для своего глобального адреса на f0/0*

# Часть 8
## Шаг 1
Настраиваем OSPFv3 между R1, R2 и R3.

<img width="229" height="22" alt="image" src="https://github.com/user-attachments/assets/0dffdc87-1ba9-4092-9390-cf23a6ae32e4" />

*OSPFv3 на R1*

<img width="237" height="31" alt="image" src="https://github.com/user-attachments/assets/5fcbd71e-aabe-49f2-9c27-c7931547bb1a" />

*OSPFv3 на R2*

<img width="231" height="29" alt="image" src="https://github.com/user-attachments/assets/098d619d-8cda-47e1-9912-992d06b58cb3" />

*OSPFv3 на R3*

## Шаг 2
Настраиваем на R1 router-id 0.0.0.1, на R2 router-id 0.0.0.2, на R3 router-id 0.0.0.3.

<img width="234" height="19" alt="image" src="https://github.com/user-attachments/assets/bb6810e0-9bc2-4540-9f17-881bfe59fb70" />

*R1*

<img width="238" height="23" alt="image" src="https://github.com/user-attachments/assets/28b0a3b3-fc4e-425c-b1c9-c62e4971700e" />

*R2*

<img width="238" height="16" alt="image" src="https://github.com/user-attachments/assets/60fa35cc-5cd5-4b55-a0a8-1c5dda3369bd" />

*R3*

## Шаг 3
R1, R2 и R3 объявляют все подключенные сети IPv6.

<img width="258" height="39" alt="image" src="https://github.com/user-attachments/assets/bfa37928-a247-42f4-9086-37b5d01097bf" />

*На R1 f0/0*

<img width="258" height="34" alt="image" src="https://github.com/user-attachments/assets/29df0315-9648-4d2f-a535-81556c1669ca" />

*На R1 f0/1*

<img width="268" height="46" alt="image" src="https://github.com/user-attachments/assets/a90b434f-2e3e-4e2b-8b9e-3a187f7d859e" />

*На R2 f0/0*

<img width="248" height="33" alt="image" src="https://github.com/user-attachments/assets/b01613e3-0c8c-4180-beac-4a707ba3de85" />

*На R2 f0/1*

<img width="262" height="32" alt="image" src="https://github.com/user-attachments/assets/eb546238-f1f5-4637-8f50-15d208e15744" />

*На R3 f0/0*

## Шаг 4
Используйте номер процесса 100 для всех маршрутизаторов.

<img width="226" height="23" alt="image" src="https://github.com/user-attachments/assets/b8bd6d6e-f812-4154-9d25-9e9c6a5c1039" />

*Номер процесса 100*

## Шаг 5
На интерфейсe f0/0 маршрутизатор R1 подключен к Area 1, на интерфейсе f0/1 маршрутизатор R1 подключен к Area 0.

<img width="497" height="70" alt="image" src="https://github.com/user-attachments/assets/9f178c01-20ed-4f28-bfc0-47a40de02e72" />

*Проверка*

## Шаг 6
На интерфейсе f0/0 маршрутизатор R2 подключен к Area 23, на интерфейсе f0/1 маршрутизатор R2 подключен к Area 0.

<img width="543" height="82" alt="image" src="https://github.com/user-attachments/assets/0b16c0fd-1a10-42b6-a945-f430b654a58b" />

*Проверка*

## Шаг 7
На интерфейсе g0/0 маршрутизатор R3 подключен к Area 23.

<img width="494" height="58" alt="image" src="https://github.com/user-attachments/assets/dc0d9849-43d3-474b-9197-0f4803b163f2" />

*Проверка*

## Шаг 8
Настраиваем, чтобы на R1 не отправлялись hello-сообщения из всех своих текущих и будущих добавленных интерфейсов, кроме f0/1.

<img width="620" height="105" alt="image" src="https://github.com/user-attachments/assets/8fe71a25-86d5-4366-922a-b5781c71e387" />

*R1 принимает hello-сообщения только с f0/0*

## Шаг 9
Настраиваем на R3 для работы в качестве шлюза по умолчанию для всех маршрутизаторов OSPF для связи с любыми другими сетями.

<img width="332" height="21" alt="image" src="https://github.com/user-attachments/assets/60bafae5-488a-4c0f-8bad-3bedff07fb3e" />

*Добавляем статический маршрут по умолчанию IPv6*

<img width="328" height="55" alt="image" src="https://github.com/user-attachments/assets/a704e1bc-dde8-4780-83d3-d8430e81ae8a" />

*R3 шлюз по умолчанию для всех маршрутизаторов OSPF*

<img width="541" height="321" alt="image" src="https://github.com/user-attachments/assets/487304f0-9315-4343-8684-60c7b030d4ad" />

*Проверяем на R1*

# Часть 9
## Шаг 1
Настраиваем EIGRPv6 между R3 и R1973.

<img width="241" height="38" alt="image" src="https://github.com/user-attachments/assets/32a0f30a-0338-46d9-8425-fb7a6278aaeb" />

*EIGRPv6 на R3*

<img width="259" height="35" alt="image" src="https://github.com/user-attachments/assets/f75ee6b1-ccb5-4203-bd2f-6af1e2c66d57" />

*EIGRPv6 на R1973*

Шаг 2
Указываем номер автономной системы (AS) 100.

<img width="385" height="231" alt="image" src="https://github.com/user-attachments/assets/2d9f1965-7794-47ed-95cc-a7b9104dab82" />

*Проверка*

Шаг 3
R3 использует router-id 0.0.0.3, R1973 использует router-id 0.0.0.73.

<img width="284" height="34" alt="image" src="https://github.com/user-attachments/assets/9e459678-2f05-4550-9c22-25b51a0c704d" />

*R3*

<img width="320" height="34" alt="image" src="https://github.com/user-attachments/assets/344cd9c0-98e7-4ac4-a942-7d754f8f786c" />

*R1973*

Шаг 4
R1973 объявляет свою петлевую сеть (loopback) для R3 через EIGRPv6.

<img width="230" height="73" alt="image" src="https://github.com/user-attachments/assets/b9b5c8d7-9306-4214-813d-983e2a6ff9a9" />

*Настройка на R1973*

<img width="217" height="48" alt="image" src="https://github.com/user-attachments/assets/21412286-ff49-4bca-9315-cdab29a51576" />

*Настройка на R3*

<img width="569" height="104" alt="image" src="https://github.com/user-attachments/assets/326d0f14-b47a-4b93-97f0-ca0c5f64342f" />

*Проверка на R3*

Шаг 5
Настраиваем на R1973 маршрут по умолчанию IPv6, указывающий на R3 в качестве следующего хопа для связи с любыми другими сетями.

<img width="345" height="15" alt="image" src="https://github.com/user-attachments/assets/4ccb7015-1cd8-455d-b561-7f6af3edc940" />

*R1973 маршрут по умолчанию IPv6, указывающий на R3 в качестве следующего хопа для связи*

<img width="535" height="306" alt="image" src="https://github.com/user-attachments/assets/76c45e95-aec2-4afd-86bc-d3da14e80b8d" />

*Проверяем таблицу маршрутизации*

<img width="572" height="121" alt="image" src="https://github.com/user-attachments/assets/bb978ef0-e104-4eb2-b073-a7f841552902" />

*Проверка EIGRPv6 соседей R1973*


---
# Блок код
```
R1
!
version 15.1
no service timestamps log datetime msec
no service timestamps debug datetime msec
no service password-encryption
!
hostname R1
!
!
!
!
!
!
!
!
ip cef
ipv6 unicast-routing
!
no ipv6 cef
!
!
!
!
license udi pid CISCO2811/K9 sn FTX1017GCRM-
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
 ip address 10.1.1.1 255.255.255.0
 ip helper-address 10.23.23.100
 ip ospf 100 area 1
 duplex auto
 speed auto
 ipv6 address FE80::1 link-local
 ipv6 address 2001:10:10:10::/64 eui-64
 ipv6 enable
 ipv6 ospf 100 area 1
!
interface FastEthernet0/1
 ip address 10.12.12.1 255.255.255.0
 ip ospf 100 area 0
 duplex auto
 speed auto
 ipv6 address 2001:11:11:11::1/64
 ipv6 enable
 ipv6 ospf 100 area 0
!
interface Vlan1
 no ip address
 shutdown
!
router ospf 100
 log-adjacency-changes
 network 10.1.1.0 0.0.0.255 area 1
 network 10.12.12.0 0.0.0.255 area 0
!
ipv6 router ospf 100
 router-id 0.0.0.1
 log-adjacency-changes
 passive-interface default
 no passive-interface FastEthernet0/1
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
R2
!
version 15.1
no service timestamps log datetime msec
no service timestamps debug datetime msec
no service password-encryption
!
hostname R2
!
!
!
!
!
!
!
!
ip cef
ipv6 unicast-routing
!
no ipv6 cef
!
!
!
!
license udi pid CISCO2811/K9 sn FTX10174F97-
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
 ip address 10.23.23.2 255.255.255.0
 ip ospf priority 255
 ip ospf 100 area 23
 duplex auto
 speed auto
 ipv6 address 2001:12:12:12::2/64
 ipv6 enable
 ipv6 ospf 100 area 23
!
interface FastEthernet0/1
 ip address 10.12.12.2 255.255.255.0
 ip ospf priority 255
 ip ospf 100 area 0
 duplex auto
 speed auto
 ipv6 address 2001:11:11:11::2/64
 ipv6 enable
 ipv6 ospf 100 area 0
!
interface Vlan1
 no ip address
 shutdown
!
router ospf 100
 router-id 0.0.0.2
 log-adjacency-changes
 network 10.23.23.0 0.0.0.255 area 23
 network 10.12.12.0 0.0.0.255 area 0
!
ipv6 router ospf 100
 router-id 0.0.0.2
 log-adjacency-changes
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
MLS
!
version 12.2(37)SE1
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
R3
!
version 15.1
no service timestamps log datetime msec
no service timestamps debug datetime msec
no service password-encryption
!
hostname R3
!
!
!
!
ip dhcp excluded-address 10.1.1.1
!
!
!
!
no ip cef
ipv6 unicast-routing
!
no ipv6 cef
!
!
!
username R1973 password 0 cisco
!
!
license udi pid CISCO2911/K9 sn FTX1524N1GN-
license boot module c2900 technology-package securityk9
license boot module c2900 technology-package uck9
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
interface Loopback3
 ip address 3.3.3.3 255.0.0.0
 ip ospf 100 area 23
!
interface Loopback33
 ip address 33.33.33.33 255.0.0.0
 ip ospf 100 area 23
!
interface GigabitEthernet0/0
 ip address 10.23.23.3 255.255.255.0
 ip ospf 100 area 23
 duplex auto
 speed auto
 ipv6 address 2001:12:12:12::3/64
 ipv6 enable
 ipv6 ospf 100 area 23
!
interface GigabitEthernet0/1
 no ip address
 duplex auto
 speed auto
 shutdown
!
interface GigabitEthernet0/2
 no ip address
 duplex auto
 speed auto
 shutdown
!
interface Serial0/0/0
 ip address 30.30.30.3 255.255.255.0
 encapsulation ppp
 ppp authentication chap
 ipv6 address 2001:30:30:30::3/64
 ipv6 eigrp 100
 ipv6 enable
 clock rate 64000
!
interface Serial0/0/1
 no ip address
 clock rate 2000000
 shutdown
!
interface Vlan1
 no ip address
 shutdown
!
router ospf 100
 log-adjacency-changes
 network 10.23.23.0 0.0.0.255 area 23
 network 3.0.0.0 0.255.255.255 area 23
 network 33.0.0.0 0.255.255.255 area 23
 network 30.0.0.0 0.255.255.255 area 23
 default-information originate
!
router bgp 3
 bgp log-neighbor-changes
 no synchronization
 neighbor 30.30.30.73 remote-as 1973
!
ipv6 router ospf 100
 router-id 0.0.0.3
 default-information originate
 log-adjacency-changes
!
ipv6 router eigrp 100
 eigrp router-id 0.0.0.3
 no shutdown 
!
ip classless
ip route 0.0.0.0 0.0.0.0 30.30.30.73 
!
ip flow-export version 9
!
ipv6 route ::/0 2001:30:30:30::1973
!
!
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
end

```
```
R1973
!
version 15.1
no service timestamps log datetime msec
no service timestamps debug datetime msec
no service password-encryption
!
hostname R1973
!
!
!
!
!
!
!
!
no ip cef
ipv6 unicast-routing
!
no ipv6 cef
!
!
!
username R3 password 0 cisco
!
!
license udi pid CISCO2911/K9 sn FTX1524ICWG-
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
interface Loopback1973
 ip address 73.73.73.73 255.255.255.0
 ipv6 address 2001:1973:1973:1973::1973/64
 ipv6 eigrp 100
 ipv6 enable
!
interface GigabitEthernet0/0
 no ip address
 duplex auto
 speed auto
 shutdown
!
interface GigabitEthernet0/1
 no ip address
 duplex auto
 speed auto
 shutdown
!
interface GigabitEthernet0/2
 no ip address
 duplex auto
 speed auto
 shutdown
!
interface Serial0/0/0
 ip address 30.30.30.73 255.255.255.0
 encapsulation ppp
 ppp authentication chap
 ipv6 address 2001:30:30:30::1973/64
 ipv6 eigrp 100
 ipv6 enable
!
interface Serial0/0/1
 no ip address
 clock rate 2000000
 shutdown
!
interface Vlan1
 no ip address
 shutdown
!
router bgp 1973
 bgp log-neighbor-changes
 no synchronization
 neighbor 30.30.30.3 remote-as 3
 network 73.73.73.0 mask 255.255.255.0
!
ipv6 router eigrp 100
 eigrp router-id 0.0.0.73
 no shutdown 
!
ip classless
ip route 0.0.0.0 0.0.0.0 30.30.30.3 
!
ip flow-export version 9
!
ipv6 route ::/0 2001:30:30:30::3
!
!
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
end

