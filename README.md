# Linux Kernal Modules

>[!warning]
>Used Kernal : Linux 5.15.0-1079-azure

## Kernal Modules

>[!info]
> 1. simple.c
>     - when loaded, print kernal logs. (HZ, jiffies information)
>     - `sudo dmesg`
>     - when unloaded, print simple logs.
> 2. createProc
>     - when loaded, creates a process called /proc/hello which prints Hello World every time the process is read.
>     - `cat /proc/hello` -> "Hello World!"
>     - when unloaded , Removes process /proc/hello
>   


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
> Build Kernal Modules

```bash
sudo insmod simple.ko
```
> load


```bash
sudo rmmod simple.ko
```
> unload
