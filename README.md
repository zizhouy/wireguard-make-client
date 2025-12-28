# wireguard-make-client
### Create a wireguard .conf file
wgmakeconf \<client wireguard ip\> \<client name\>

### Looks like
#### {client name}.conf

```
[Interface]
PrivateKey = <client private key>
Address = {client wireguard ip}/32
DNS = <DNS ip>
MTU = <wireguard default 1420, lower if needed>

[Peer]
PublicKey = <server public key\>
AllowedIPs = <wireguard ip range, or whatever range required>
Endpoint = <wireguard public ip>:<wireguard port, probably 51820>
PersistentKeepalive = 25
```

### Note
\<\> should be replaced in the script with static changes desired
