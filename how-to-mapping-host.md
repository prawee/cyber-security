# How to mapping host

## Checking
```bash
ping myapp.local
```
Result
```bash
ping: cannot resolve myapp.local: Unknown host
```

## Update hosts
- /etc/hosts
```bash
sudo nano /etc/hosts
```

```bash
127.0.0.1   myapp.local
```

## Checking again
```bash
ping myapp.local
```

```bash
PING myapp.local (127.0.0.1): 56 data bytes
64 bytes from 127.0.0.1: icmp_seq=0 ttl=64 time=0.047 ms
64 bytes from 127.0.0.1: icmp_seq=1 ttl=64 time=0.135 ms
64 bytes from 127.0.0.1: icmp_seq=2 ttl=64 time=0.071 ms
```

## Web Server
- Apache
- Nginx
- Caddy


## Reference
<https://hub.docker.com/_/caddy>
<https://caddyserver.com/docs/caddyfile/concepts>