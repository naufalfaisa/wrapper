# Wrapper

Wrapper to decrypt ALAC files from Apple Music

## Compatibility

- Windows: Can be run via Docker Desktop.
- Linux: Supports x86_64 & ARM64.

### Usage (Docker)

Build image: 
```bash
docker build --tag wrapper .
```

Run: 
```bash
docker run -v ./rootfs/data:/app/rootfs/data -p 10020:10020 -p 20020:20020 -e args="-L username:password -F -H 0.0.0.0" wrapper
```

### Usage (Linux x86_64 & ARM64)

```bash
sudo -i
chmod +x wrapper
./wrapper -L username:password -F -H 0.0.0.0
```

### Options:
```
./wrapper [OPTION]...
  -h, --help               Print help and exit
  -V, --version            Print version and exit
  -H, --host=STRING        (default: `127.0.0.1`)
  -D, --decrypt-port=INT   (default: `10020`)
  -M, --m3u8-port=INT      (default: `20020`)
  -P, --proxy=STRING       (default: `''`)
  -L, --login=STRING       ([username]:[password])
```
