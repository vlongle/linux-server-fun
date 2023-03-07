## Install nvidia drivers
When cannot log-in into linux (login loop error), might need to install nvidia-driver.
Ctrl+alt+f3 to get to the terminal screen. Then, find XAuthority. If not available, need to install 
nvidia-driver
```
ubuntu-drivers devices
```
Then select one driver and install. For example,
```
sudo apt install nvidia-driver-515
```

## Setup SSH
Server-side
1. Get your ip address

```
hostname -I
```

2. Install SSH
```
sudo apt install openssh-server
```

Client-side
We can now access our remote machine

```
ssh -Y username@ip_address
```

## Useful things to install

```
sudo apt install htop
sudo apt install gpustat
sudo apt install tmux
```


Install conda following [conda website instruction](https://docs.conda.io/projects/conda/en/latest/user-guide/install/linux.html)

Change default shell to bash
```
chsh -s /bin/bash
```

## Create users

```
sudo useradd -m username
```

```
sudo passwd username
```

Add to sudo (give admin privilege)
```
sudo usermod -a -G sudo USERNAME
```

## Memory management

System memory
```
df -h
```

Memory in a specific folders
```
du -sh folder_name/*
```


## Motherboard
https://download.asrock.com/Manual/TRX40%20Creator.pdf


## Not seeing cool folders

[ask ubuntu](https://askubuntu.com/questions/574609/why-do-i-not-see-my-bin-var-etc-directories-in-my-root-partition)

```
cd /
ls -al
```
Should see stuff like /etc/  and bin folders


