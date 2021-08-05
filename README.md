# wrk

Requires the `wrk.lua` source script to be mounted
```bash
sudo ./qemu-guest \
    -m 372 \
    -k build/wrk_kvm-x86_64 \
    -b kraft0 \
    -e ./fs0 \
    -a "netdev.ipv4_addr=172.88.0.5 netdev.ipv4_gw_addr=172.88.0.1 netdev.ipv4_subnet_mask=255.255.0.0 vfs.rootdev=fs0 -- http://172.88.0.1:80"
```
