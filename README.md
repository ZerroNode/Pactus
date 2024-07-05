### Download new version

```
ver="1.1.8" && \
filename="pactus-cli_${ver}_linux_amd64.tar.gz" && \
wget https://github.com/pactus-project/pactus/releases/download/v${ver}/$filename && \
tar -xzf $filename && rm -rf $filename && rm -rf node_pactus && mv pactus-cli_${ver} node_pactus && \
./node_pactus/pactus-daemon version
```

### If running in tmux, attach to your session and run this
```
./node_pactus/pactus-daemon start
```

### If running with services
```
systemctl restart pactusd && journalctl -u pactusd -f -o cat
```
