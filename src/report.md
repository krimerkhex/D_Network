<br>
Команда: <br>
![](../screens.png)<br>

# Part 1. Инструмент ipcalc
Установка ipcalc<br>
Команда: sudo apt install ipcalc<br>
![IPCalcInstall](../screensIPCalcInstall.png)<br>

## 1.1. Сети и маски
1.1.1) Адрес сети 192.167.38.54/13<br>
Команда: ipcalc 192.167.38.54/13<br>
![FirstTransform](../screensFirstTransform.png)<br>

### Перевод масок:
1.1.2.1) Перевод маски 255.255.255.0 в префиксную и двоичную запись<br>
Команда: ipcalc 255.255.255.0<br>
![SecondTransform](../screensSecondTransform.png)<br>
Префиксная: /24<br>
Двоичная: 11111111.11111111.11111111.00000000<br>

1.1.2.2) Перевод маски /15 в обычную и двоичную<br>
Команда: ipcalc /15<br>
![ThirdTransform](../screensThirdTransform.png)<br>
Обычная: 255.254.0.0<br>
Двоичная: 11111111.11111110.00000000.00000000<br>

1.1.2.3) Перевод маски 11111111.11111111.11111111.11110000 в обычную и префиксную<br>
2CC 11111111.11111111.11111111.11110000 == 10CC 255.255.255.240<br>
Команда: ipcalc 255.255.255.240<br>
![FourthTransform](../screensFourthTransform.png)<br>
Обычная: 255.255.255.240<br>
Префиксная: /24<br>

### Минимальный и максимальный хост в сети 12.137.38.4:
1.1.3.1) При маске /8<br>
Команда: ipcalc 12.137.38.4/8<br>
![FiveTransform](../screensFiveTransform.png)<br>
Минимальный хост: 00001100.00000000.00000000.00000001 | 12.0.0.1<br>
Максимальный хост: 00001100.11111111.11111111.11111110 | 12.255.255.254<br>

1.1.3.2) При маске 11111111.11111111.00000000.00000000<br>
Команда: 12.137.38.4/16<br>
![SixTransform](../screensSixTransform.png)<br>
Минимальный хост: 00001100.10001001.00000000.00000001 | 12.137.0.1<br>
Максимальный хост: 00001100.10001001.11111111.11111110 | 12.137.255.254<br>

1.1.3.3) При маске 255.255.254.0<br>
Команда: 12.137.38.4/23<br>
![SevenTransform](../screensSevenTransform.png)<br>
Минимальный хост: 00001100.10001001.00100110.00000001 | 12.137.38.1<br>
Максимальный хост: 00001100.10001001.00100111.11111110 | 12.137.39.254<br>

1.1.3.4) При маске /4<br>
Команда: 12.137.38.4/4<br>
![EightTransform](../screensEightTransform.png)<br>
Минимальный хост: 00000000.00000000.00000000.00000001 | 0.0.0.1<br>
Максимальный хост: 00001111.11111111.11111111.11111110 | 15.255.255.254<br>

## 1.2. localhost
### Определить и записать в отчёт, можно ли обратиться к приложению, работающему на localhost, со следующими IP:
1.2.1) 194.34.23.100 не обладает loopback(петля)<br>
Команда: ipcalc 194.34.23.100<br>
![localhost1](../screenslocalhost1.png)<br>

1.2.2) 127.0.0.2 обладает loopback(петля)<br>
Команда: ipcalc 127.0.0.2<br>
![localhost2](../screenslocalhost2.png)<br>

1.2.3) 127.1.0.1 обладает loopback(петля)<br>
Команда: ipcalc 127.1.0.1<br>
![localhost3](../screenslocalhost3.png)<br>

1.2.4) 128.0.0.1 не обладает loopback(петля)<br>
Команда: ipcalc 128.0.0.1<br>
![localhost4](../screenslocalhost4.png)<br>

## 1.3. Диапазоны и сегменты сетей
### Какие из перечисленных IP можно использовать в качестве публичного, а какие только в качестве частных:
1.3.1.1) 10.0.0.45 - Приватный<br>
Команда: ipcalc 10.0.0.45<br>
![PubPriCheck1](../screensPubPriCheck1.png)<br>

1.3.1.2) 134.43.0.2 - Публичный<br>
Команда: ipcalc 134.43.0.2<br>
![PubPriCheck2](../screensPubPriCheck2.png)<br>

1.3.1.3) 192.168.4.2 - Приватный<br>
Команда: ipcalc 192.168.4.2<br>
![PubPriCheck3](../screensPubPriCheck3.png)<br>

1.3.1.4) 172.20.250.4 - Приватный<br>
Команда: ipcalc 172.20.250.4<br>
![PubPriCheck4](../screensPubPriCheck4.png)<br>

1.3.1.5) 172.0.2.1 - Публичный<br>
Команда: ipcalc 172.0.2.1<br>
![PubPriCheck5](../screensPubPriCheck5.png)<br>

1.3.1.6) 192.172.0.1 - Публичный<br>
Команда: ipcalc 192.172.0.1<br>
![PubPriCheck6](../screensPubPriCheck6.png)<br>

1.3.1.7) 172.68.0.2 - Публичный<br>
Команда: ipcalc 172.68.0.2<br>
![PubPriCheck7](../screensPubPriCheck7.png)<br>

1.3.1.8) 172.16.255.255 - Приватный<br>
Команда: ipcalc 172.16.255.255<br>
![PubPriCheck8](../screensPubPriCheck8.png)<br>

1.3.1.9) 10.10.10.10 - Приватный<br>
Команда: ipcalc 10.10.10.10<br>
![PubPriCheck9](../screensPubPriCheck9.png)<br>

1.3.1.10) 192.169.168.1 - Публичный<br>
Команда: ipcalc 192.169.168.1<br>
![PubPriCheck10](../screensPubPriCheck10.png)<br>

### Какие из перечисленных IP адресов шлюза возможны у сети:
1.3.2.1) 10.10.0.0/18 - Не возможен<br>
Команда: ipcalc 10.10.0.0/18<br>
![Shluz1](../screensShluz1.png)<br>

1.3.2.2) 10.0.0.1 - Не возможен<br>
Команда: ipcalc 10.0.0.1<br>
![Shluz2](../screensShluz2.png)<br>

1.3.2.3) 10.10.0.2 - Возможен<br>
Команда: ipcalc 10.10.0.2<br>
![Shluz3](../screensShluz3.png)<br>

1.3.2.4) 10.10.10.10 - Возможен<br>
Команда: ipcalc 10.10.10.10<br>
![Shluz4](../screensShluz4.png)<br>

1.3.2.5) 10.10.100.1 - Не возможен<br>
Команда: ipcalc 10.10.100.1<br>
![Shluz5](../screensShluz5.png)<br>

1.3.2.6) 10.10.1.255 - Возможен<br>
Команда: ipcalc 10.10.1.255<br>
![Shluz6](../screensShluz6.png)<br>

# Part 2. Статическая маршрутизация между двумя машинами

Проверка какие сетевые интерфейсы присутствуют на данный момент у машины ws11 и ws 21<br>
Команда: ip a или netstat -rn<br>
WS11:<br>
![WS11Interfeis_1](../screensWS11Interface_1.png)<br>
WS21:<br>
![WS21Interfeis_1](../screensWS21Interface_1.png)<br>

Прописываем в файле /etc/netplan/00-installer-config.yaml у машин ws11 и ws 21 новые порты:<br>
ws11:<br>
    -> Имя порта: enp0s8.<br>
    -> IP-адрес: 192.168.100.10/16.<br>
![WS11Interfeis_2](../screensWS11Interface_2.png)<br>
ws21:<br>
    -> Имя порта: enp0s8.<br>
    -> IP-адрес: 172.24.116.8/12.<br>
![WS21Interfeis_2](../screensWS21Interface_2.png)<br>
Примечание: проверьте через ipcalc IP-адрес, для подтверждения, что его можно использовать.<br>

Перезагружаем сетевые интерфейсы и проверяем появление порта enp0s8 на каждой машине:<br>
Команда: sudo netplan apply для перезагрузки<br>
Команда: ip a для просмотра всех портов<br>
ws11:<br>
![WS11Interfeis_3](../screensWS11Interface_3.png)<br>
ws21:<br>
![WS21Interfeis_3](../screensWS21Interface_3.png)<br>

## 2.1. Добавление статического маршрута вручную

Прописываем статистический маршрут:<br>
Команда: ip r add <ip1> via <ip2>, - где ip1(IP адрес порта назначения), ip2(IP адрес порта машины).<br>
ws11:<br>
![WS11IPRADD](../screensWS11IPRADD.png)<br>
ws21:<br>
![WS21IPRADD](../screensWS11IPRADD.png)<br>

Проверяем:<br>
Команда: ping -c <кол-во запросов> <ip>.<br>
ws11:<br>
![WS11Ping1](../screensWS11Ping1.png)<br>
ws21:<br>
![WS21Ping1](../screensWS21Ping1.png)<br>


## 2.2. Добавление статического маршрута с сохранением

Для добавления маршрута с сохранением нужно исправить /etc/netplan/00-installer-config.yaml у двух машин:<br>
ws11:<br>
![WS11Interface_4](../screensWS11Interface_4.png)<br>
ws21:<br>
![WS21Interface_4](../screensWS21Interface_4.png)<br>

После чего перезагружаем сетевые интерфейсы:<br>
Команда: sudo netplan apply.<br>

Проверяем:<br>
Команда: ping -c <кол-во запросов> <ip>.<br>
ws11:<br>
![WS11Ping2](../screensWS11Ping2.png)<br>
ws21:<br>
![WS21Ping2](../screensWS21Ping2.png)<br>

# Part 3. Утилита iperf3
## 3.1. Скорость соединения
Перевод значений:<br>
8 Mbps в MB/s   | 8 Mbps = 1 MB/s.<br>
100 MB/s в Kbps | 100 MB/s = 800000 Kbps.<br>
1 Gbps в Mbps   | 1 Gbps = 1000 Mbps.<br>

## 3.2. Утилита iperf3
Тест утилиты iperf3<br>
Команда на ws11: iperf3 -s.<br>
Команда на ws21: iperf3 -c 192.168.100.10 -p 5201.<br>
ws11:<br>
![WS11IPERF](../screensWS11IPERF.png)<br>
ws21:<br>
![WS21IPERF](../screensWS21IPERF.png)<br>

# Part 4. Сетевой экран
## 4.1. Утилита iptables
Открытие на машинах портов 22(ssh) и 80(http).<br>
И отображение статуса портов.<br>
ws11:<br>
![WS11OpenPorts](../screensWS11OpenPorts.png)<br>
ws21:<br>
![WS21OpenPorts](../screensWS21OpenPorts.png)<br>

Отображение файла /etc/firewall.sh.<br>
ws11:<br>
![WS11Firewall](../screensWS11Firewall.png)<br>
ws21:<br>
![WS21Firewall](../screensWS21Firewall.png)<br>

Запуск команд `chmod +x /etc/firewall.sh` и `/etc/firewall.sh`.<br>
ws11:<br>
![WS11FilesStarting](../screensWS11FilesStarting.png)<br>
ws21:<br>
![WS21FilesStarting](../screensWS21FilesStarting.png)<br>

Описание разницы стратегий:<br>
Виртуальную машину ws11 мы исподьзуем запрещающее правило (REJECT) и после разрешающее правило (RETURN) не работает. С виртуальной машиной ws21 мы применяем обратную стратегию.<br>

## 4.2. Утилита nmap

Проверка работы.<br>
ws11:<br>
![WS11Try](../screensWS11Try.png)<br>

На скриншоте видно, что хоть пакте не доставлен, однако nmap отобразил, что 1 хост имеется.<br>

# Part 5. Статическая маршрутизация сети
Сеть: \
<img src="../misc/images/part5_network.png" alt="part5_network" width="500"/>

## 5.1. Настройка адресов машин

Изменение файла: etc/netplan/00-installer-config.yaml на всех виртуальных машинах согласно образу:<br>
ws11<br>
![WS11Installer](../screensWS11Installer.png)<br>

ws21<br>
![WS21Installer](../screensWS21Installer.png)<br>

ws22<br>
![WS22Installer](../screensWS22Installer.png)<br>

r1<br>
![R1Installer](../screensR1Installer.png)<br>

r2<br>
![R2Installer](../screensR2Installer.png)<br>

Перезапуск сервиса сети: sudo netplan apply<br>

Проверка успешного изменения файла: etc/netplan/00-installer-config.yaml на всех виртуальных машинах.<br>
Команада: ip -4 a.<br>
ws11<br>
![WS11InstallerCheck](../screensWS11InstallerCheck.png)<br>

ws21<br>
![WS21InstallerCheck](../screensWS21InstallerCheck.png)<br>

ws22<br>
![WS22InstallerCheck](../screensWS22InstallerCheck.png)<br>

r1<br>
![R1InstallerCheck](../screensR1InstallerCheck.png)<br>

r2<br>
![R2InstallerCheck](../screensR2InstallerCheck.png)<br>

Проверка успешности создания сети:<br>
ws11<br>
![WS11PingCheck](../screensWS11PingCheck.png)<br>

ws21<br>
![WS21PingCheck](../screensWS21PingCheck.png)<br>

ws22<br>
![WS22PingCheck](../screensWS22PingCheck.png)<br>

r1<br>
![R1PingCheck](../screensR1PingCheck.png)<br>

r2<br>
![R2PingCheck](../screensR2PingCheck.png)<br>


## 5.2. Включение переадресации IP-адресов

Для включения переадресации IP, выполним команду на роутерах:
`sysctl -w net.ipv4.ip_forward=1`<br>
*При таком подходе переадресация не будет работать после перезагрузки системы.*

r1<br>
![R1Forwarding](../screensR1Forwarding.png)<br>

r2<br>
![R2Forwarding](../screensR2Forwarding.png)<br>

Откройте файл */etc/sysctl.conf* и добавьте в него следующую строку:
`net.ipv4.ip_forward = 1`<br>
*При использовании этого подхода, IP-переадресация включена на постоянной основе.*

r1<br>
![R1SysctlChange](../screensR1SysctlChange.png)<br>

r2<br>
![R2SysctlChange](../screensR2SysctlChange.png)<br>

## 5.3. Установка маршрута по умолчанию
Пример вывода команды `ip r` после добавления шлюза:
```
default via 10.10.0.1 dev eth0
10.10.0.0/18 dev eth0 proto kernel scope link src 10.10.0.2
```
Добавление шлюза по умолчанию, для этого необходимо в 00-installer-config.yaml добавить поле `gateway4 [ip]` на порте<br>

ws11<br>
![WS11GatewayAdding](../screensWS11GatewayAdding.png)<br>

ws21<br>
![WS21GatewayAdding](../screensWS21GatewayAdding.png)<br>

ws22<br>
![WS22GatewayAdding](../screensWS22GatewayAdding.png)<br>

r1<br>
![R1GatewayAdding](../screensR1GatewayAdding.png)<br>

r2<br>
![R2GatewayAdding](../screensR2GatewayAdding.png)<br>

Проверка `ip r`:<br>

ws11<br>
![WS11PingCheck_2](../screensWS11PingCheck_2.png)<br>

ws21<br>
![WS21PingCheck_2](../screensWS21PingCheck_2.png)<br>

ws22<br>
![WS22PingCheck_2](../screensWS22PingCheck_2.png)<br>

r1<br>
![R1PingCheck_2](../screensR1PingCheck_2.png)<br>

r2<br>
![R2PingCheck_2](../screensR2PingCheck_2.png)<br>

Пропинговать с ws11 роутер r2 и показать на r2, что пинг доходит. Для этого использовать команду:
`tcpdump -tn -i enp0s9  `<br>

ws11<br>
![WS11PingCheck_3](../screensWS11PingCheck_3.png)<br>

r2<br>
![R2PingCheck_3](../screensR2PingCheck_3.png)<br>

## 5.4. Добавление статистических маршрутов

Добавление в роутеры r1 и r2 статических маршрутов в файле конфигураций.<br>
r1<br>
![R1StaticAdding](../screensR1StaticAdding.png)<br>

r2<br>
![R2StaticAdding](../screensR2StaticAdding.png)<br>

Проверка `ip r`:<br>

r1<br>
![R1IpRShow](../screensR1IpRShow.png)<br>

r2<br>
![R2IpRShow](../screensR2IpRShow.png)<br>

Запустить команды на ws11:
`ip r list 10.10.0.0/18` и `ip r list 0.0.0.0/0`<br>

ws11<br>
![WS11IpRShow](../screensWS11IpRShow.png)<br>

- В отчёте объяснить, почему для адреса 10.10.0.0/\[маска сети\] был выбран маршрут, отличный от 0.0.0.0/0, хотя он попадает под маршрут по-умолчанию.<br>
Объеснение: по той причине, что он является адресов сети и доступен без шлюза.<br>

## 5.5. Построение списка маршрутизаторов

При помощи утилиты **traceroute** построить список маршрутизаторов на пути от ws11 до ws21.<br>
- `sudo tcpdump -tnv -i enp0s8`<br>
- `traceroute 10.20.0.10`<br>

ws11<br>
![WS11PingWS21](../screensWS11PingWS21.png)<br>

r1<br>
![R1TCPDUMP](../screensR1TCPDUMP.png)<br>

- В отчёте, опираясь на вывод, полученный из дампа на r1, объяснить принцип работы построения пути при помощи **traceroute**<br>
Обяснение: Команда traceroute linux использует UDP пакеты. Она отправляет пакет с TTL=1 и смотрит адрес ответившего узла, дальше TTL=2, TTL=3 и так пока не достигнет цели. Каждый раз отправляется по три пакета и для каждого из них измеряется время прохождения. Пакет отправляется на случайный порт, который, скорее всего, не занят. Когда утилита traceroute получает сообщение от целевого узла о том, что порт недоступен трассировка считается завершенной.

## 5.6. Использование протокола ICMP при маршрутизации

Запустить на r1 перехват сетевого трафика, проходящего через eth0 с помощью команды:
tcpdump -n -i eth0 icmp

r1<br>
![R1TCPDUMP_2](../screensR1TCPDUMP_2.png)<br>

Пропинговать с ws11 несуществующий IP (например, 10.30.0.111) с помощью команды:
ping -c 1 10.30.0.111

ws11<br>
![WS11PingNO](../screensWS11PingNO.png)<br>

# Part 6. Динамическая настройка IP с помощью DHCP
Для r1 и r2 настроить:
- 1) В файле /etc/dhcp/dhcpd.conf конфигурацию службы DHCP прописать для r2 
```shell    
subnet 10.100.0.0 netmask 255.255.0.0 {}

subnet 10.20.0.0 netmask 255.255.255.192
{
    range 10.20.0.2 10.20.0.50;
    option routers 10.20.0.1;
    option domain-name-servers 10.20.0.1;
}
```
- Для r1 настроить аналогично r2, но сделать выдачу адресов с жесткой привязкой к MAC-адресу (ws11).<br>

r1<br>
![R1DHCPD](../screensR1DHCPD.png)<br>
r2<br>
![R2DHCPD](../screensR2DHCPD.png)<br>

- 2) В файле *resolv.conf* прописать `nameserver 8.8.8.8.`:<br>

r1<br>
![R1RESOLV](../screensR1RESOLV.png)<br>
r2<br>
![R2RESOLV](../screensR2RESOLV.png)<br>

Перезагрузить службу DHCP командой `systemctl restart isc-dhcp-server`.<br>
r1<br>
![R1DHCPRE](../screensR1DHCPRE.png)<br>
r2<br>
![R2DHCPRE](../screensR2DHCPRE.png)<br>

Отображение IP-адреса у WS21:<br>

ws21<br>
![WS21PORTSHOW](../screensWS21PORTSHOW.png)<br>

Пропинговка WS21->WS22(скрин WS21) и WS22->WS21(скрин WS22).<br>
ws21<br>
![WS21PINGW22](../screensWS21PINGW22.png)<br>

ws22<br>
![WS22PINGW21](../screensWS22PINGW21.png)<br>

Указать MAC адрес у ws11, для этого в *etc/netplan/00-installer-config.yaml* надо добавить строки: `macaddress: 10:10:10:10:10:BA`, `dhcp4: true`.<br>

r1<br>
![R1DHCPD](../screensR1DHCPD.png)<br>

r1<br>
![R1RESOLV](../screensR1RESOLV.png)<br>

r1<br>
![R1DHCPRE](../screensR1DHCPRE.png)<br>


ws11<br>
![WS11CONFCHANGE](../screensWS11CONFCHANGE.png)<br>

Запросить с ws21 обновление ip адреса:<br>

ws21<br>
![WS21Before](../screensWS21Before.png)<br>

Использованные команды<br>
![UsedCommands](../screensUsedCommands.png)<br>

ws21<br>
![WS21After](../screensWS21After.png)<br>

`dhclient -r [интерфейс]` - удаление ip адреса у порта<br>
`dhclient -v [интерфейс]` - получение ip адречса на порт<br>

# Part 7. NAT
В файле */etc/apache2/ports.conf* на ws22 и r1 изменить строку `Listen 80` на `Listen 0.0.0.0:80`, то есть сделать сервер Apache2 общедоступным<br>
r1<br>
![APACHECHANGER1](../screensR1ApacheChange.png)<br>

ws22<br>
![APACHECHANGEW22](../screensWS22ApacheChange.png)<br>

Запустить веб-сервер Apache командой `service apache2 start` на ws22 и r1<br>
r1<br>
![APACHESTARTR1](../screensR1ApacheStart.png)<br>

ws22<br>
![APACHESTARTW22](../screensWS22ApacheStart.png)<br>

Добавить в фаервол, созданный по аналогии с фаерволом из Части 4, на r2 следующие правила:<br>
1) Удаление правил в таблице filter - `iptables -F`<br>
2) Удаление правил в таблице "NAT" - `iptables -F -t nat`<br>
3) Отбрасывать все маршрутизируемые пакеты - `iptables --policy FORWARD DROP`<br>

r2<br>
![IPTABLESCHANGER2](../screensR2IptablesChange.png)<br>

Запускать файл также, как в Части 4<br>

r2<br>
![IPTABLESSTART2](../screensR2IptablesStart.png)<br>

Проверить соединение между ws22 и r1 командой `ping`
*При запуске файла с этими правилами, ws22 не должна "пинговаться" с r1*
r1<br>
![R1PINGWS22](../screensR1PingWS22.png)<br>

ws22<br>
![WS22PINGR1](../screensWS22PingR1.png)<br>

Он не пингуется.<br>

Добавить в файл ещё одно правило:
4) Разрешить маршрутизацию всех пакетов протокола **ICMP**<br>
r2<br>
![R2FirewallChange](../screensR2FirewallChange.png)<br>

Запускать файл также, как в Части 4<br>
r2<br>
![R2FirewallStart](../screensR2FirewallStart.png)<br>

Проверить соединение между ws22 и r1 командой `ping`<br>
*При запуске файла с этими правилами, ws22 должна "пинговаться" с r1*<br>
r1<br>
![R1PINGWS22_2](../screensR1PingWS22_2.png)<br>

Добавить в файл ещё два правила:
5) Включить **SNAT**, а именно маскирование всех локальных ip из локальной сети, находящейся за r2 (по обозначениям из Части 5 - сеть 10.20.0.0)
*Совет: стоит подумать о маршрутизации внутренних пакетов, а также внешних пакетов с установленным соединением*
6) Включить **DNAT** на 8080 порт машины r2 и добавить к веб-серверу Apache, запущенному на ws22, доступ извне сети
*Совет: стоит учесть, что при попытке подключения возникнет новое tcp-соединение, предназначенное ws22 и 80 порту*

r2<br>
![R2Rule5](../screensR2Rule5.png)<br>
r2<br>
![R2Rule6](../screensR2Rule6.png)<br>

Запускать файл также, как в Части 4<br>
*Перед тестированием рекомендуется отключить сетевой интерфейс **NAT** (его наличие можно проверить командой `ip a`) в VirtualBox, если он включен*<br>
r2<br>
![R2StartAllRules](../screensR2StartAllRules.png)<br>
Проверил соединение **SNAT** для этого с ws22 подключиться к серверу Apache на r1 командой:<br>
`telnet [адрес] [порт]`<br>

ws22<br>
![WS22SnatCheck](../screensWS22SnatCheck.png)<br>


Проверил соединение по TCP для **DNAT**, для этого с r1 подключил к серверу Apache на ws22 командой `telnet` (обращаться по адресу r2 и порту 8080)<br>
r1<br>
![R1DnatCheck](../screensR1DnatCheck.png)<br>

# Part 8. Дополнительно. Знакомство с SSH Tunnels

Запустить на r2 фаервол с правилами из Части 7
Запустить веб-сервер **Apache** на ws22 только на localhost (то есть в файле */etc/apache2/ports.conf* изменить строку `Listen 80` на `Listen localhost:80`)<br>
ws22<br>
![WS22PortsChange_2](../screensWS22PortsChange_2.png)<br>
ws22<br>
![WS22PortsCheck_2](../screensWS22PortsCheck_2.png)<br>

Воспользоваться *Local TCP forwarding* с ws21 до ws22, чтобы получить доступ к веб-серверу на ws22 с ws21<br>
Воспользоваться *Remote TCP forwarding* c ws11 до ws22, чтобы получить доступ к веб-серверу на ws22 с ws11<br>
Для проверки, сработало ли подключение в обоих предыдущих пунктах, перейдите во второй терминал (например, клавишами Alt + F2) и выполните команду:<br>
`telnet 127.0.0.1 [локальный порт]`<br>

ws22<br>
![WS22PortsCheck_3](../screensWS22PortsCheck_3.png)<br>
