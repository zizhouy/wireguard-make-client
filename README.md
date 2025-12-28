# wireguard-make-client
### Create a wireguard .conf file
wgmakeconf \<client name\> \<client wireguard ip\>

### Looks like
#### {client name}.conf

```
[Interface]
PrivateKey = <client private key>
Address = {client wireguard ip}/32
DNS = <DNS ip>
MTU = <wireguard default 1420, lower if needed>

[Peer]
PublicKey = <server public key>
AllowedIPs = <wireguard ip range, or whatever range required>
Endpoint = <wireguard public ip>:<wireguard port, probably 51820>
PersistentKeepalive = 25
```

### Note
Script needs to be modified. See script itself
