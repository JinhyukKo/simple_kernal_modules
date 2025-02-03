# Linux Kennal Modules

## How to start 

if you use Azure CLI
```bash
ssh -i  ${YOUR_PRIVATE_KEY_LOCATION} ${AZURE_USERNAME}@${IP}
```

```bash
lsmod
```
> List all kernal Modules are loaded


```bash
make -C /lib/modules/$(uname -r)/build M=$PWD
```
> Build Kenal Modules

```bash
sudo insmod simple.ko
sudo dmesg
```
> load and check the logs


```bash
sudo rmmod simple.ko
```
> unload
