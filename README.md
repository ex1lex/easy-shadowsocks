# Shadowsocks за 10 минут

```Bash
sudo apt update
sudo apt install shadowsocks-libev
```

**Редактировать фаил /etc/shadowsocks-libev/config.json**

```JSON
{
	"server":"SERVER_IP",
	"mode":"tcp_and_udp",
	"server_port":*SERVER_PORT*,
	"local_port":1080,
	"password":"SERVER_PASSWORD",
	"timeout":86400,
	"method":"chacha20-ietf-poly1305"
}
```

**Перезапустить службу:**

```Bash
sudo systemctl restart shadowsocks-libev
```

**Создать строку по шаблону:**

```Plain
method:password@hostname:port
```

**Пример:**

```Plain
chacha20-ietf-poly1305:111111111@90.100.20.300:9999
```

**Создать base64 строку:**

```Plain
ss://Y2hhY2hh0303aWV0Zi1wb2x6565wNTox222xMTExMTFAOTAuMTAwLjIwLj4444443388
```

**Вставить получившуюся строку в VPN клиент, поддерживающий shadowsocks**

## Документация

<https://shadowsocks.org/doc/deploying.html>
