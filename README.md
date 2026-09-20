# opsm-pr1-biruk
# Практична робота № 1
Дисципліна: Основи побудови інформаційних систем та мереж

Тема: Спостереження за процесом звернення до вебресурсу. Побудова власної моделі рівнів взаємодії

| Прізвище, ім'я     | Бiрюк Владислав
|
| ------------- | ------------- |
| Група | F5 2.02  |
| Номер варіанта  | 1  |
| Домен варіанта  | icann.com |
| Середовище виконання	  | Windows  |
| Версія curl  | curl 8.21.0  |
| Дата виконання  | 20/09/2026  |
# Частина A. Збір експериментальних даних
# A.1. Запит із діагностичним виводом
Команда:
```text
curl -v icann.com
```
Вивід:
*   Trying 192.0.43.22:80...
* Established connection to icann.com (192.0.43.22 port 80) from 192.168.0.122 port 63556
* using HTTP/1.x
> GET / HTTP/1.1
> Host: icann.com
> User-Agent: curl/8.21.0
> Accept: */*
>
* Request completely sent off
< HTTP/1.1 301 Moved Permanently
< Date: Sun, 20 Sep 2026 17:20:53 GMT
< Server: Apache
< Location: https://icann.com/
< Cache-Control: max-age=345600
< Expires: Thu, 24 Sep 2026 17:20:53 GMT
< Content-Length: 266
< Content-Type: text/html; charset=iso-8859-1
<
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN" "http://www.w3.org/TR/html4/strict.dtd">
<html><head>
<title>301 Moved Permanently</title>
</head><body>
<h1>Moved Permanently</h1>
<p>The document has moved <a href="https://icann.com/">here</a>.</p>
</body></html>
* Connection #0 to host icann.com:80 left intact
запит Resolve-DnsName icann.com
Name                                           Type   TTL   Section    IPAddress
----                                           ----   ---   -------    ---------
icann.com                                      AAAA   85840 Answer     2001:500:88:200::22
icann.com                                      A      85840 Answer     192.0.43.22
