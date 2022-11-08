# Setup openLDAP directory server

These scripts will install and bootstrap openLDAP directory server as well as MIT kerberos backed by this server.

## Sample setup as a proxmox LXC container:

```bash
pct create 110 \
  images:vztmpl/debian-11-standard_11.0-1_amd64.tar.gz \
  --hostname dir-01 \
  --net0 name=eth0,bridge=vmbr1,gw=10.1.1.1,ip=10.1.1.2/24 \
  --password \
  --unprivileged 1 \
  --storage local-btrfs \
  --onboot 1 \
  --start 1
```
