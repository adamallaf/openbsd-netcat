# OpenBSD-Netcat

Added ability to bind to specified network interface with `-B` flag.

Usage:
```bash
./nc -B tun0 x.x.x.x port
```

### examples:

connect using `tun0` interface
```bash
./nc -B tun0 10.4.24.2 1337
```

init connection using address 127.0.0.222, port 8080 and bind to `lo` interface
```bash
./nc -B lo -s 127.0.0.222 -p 8080 127.0.0.1 1337
```

listen on `eth2` interface only
```bash
./nc -B eth2 -lv 80
```
