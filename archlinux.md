

```
# ls /sys/firmware/efi/efivars
# dhcpcd/wifi-menu
# ping -c 4 www.baidu.com
```

```
# timedatectl set-ntp true
```

```
# fdisk -l
```

```
# mkfs.fat -F32 /dev/sdx1
# mkfs.ext4 /dev/sdx3
# mkswap /dev/sdx2
# swapon /dev/sdx2
```

```
# mount /dev/sdx3 /mnt
# mkdir /mnt/boot
# mount /dev/sdx1 /mnt/boot
```

```
# vim /etc/pacman.d/mirrorlist
	修改server
	Server = https://mirrors.tuna.tsinghua.edu.cn/archlinux/$repo/os/$arch
	Server = https://mirrors.aliyun.com/archlinux/$repo/os/$arch
```

```
# pacstrap /mnt base base-devel linux linux-firmware vim nano dhcpcd wpa_supplicant
```

```
# genfstab -U /mnt >> /mnt/etc/fstab
```

```
# arch-chroot /mnt
	进入新安装的系统
```

```
# ln -sf /usr/share/zoneinfo/Asia/Shanghai /etc/localtime
```

```
# hwclock --systohc
```

```
# vim /etc/locale.gen
	en_US.UTF-8 UTF-8
# locale-gen
```

```
# vim /etc/locale.conf
	LANG=en_US.UTF-8
```

```
# vim /etc/hostname
	myhostname
```

```
# vim /etc/hosts
	127.0.0.1	localhost
	::1		localhost
	127.0.1.1	myhostname.localdomain	myhostname
```

```
# useradd -m -g users -s /bin/bash 用户名 
# nano /etc/sudoers
	root ALL=(ALL)ALL
	用户名 ALL=(ALL)ALL
```

```
# passwd
	设置root密码
```

```
# pacman -S intl-ucode
	intel处理器用户安装
# pacman -S os-prober
	硬盘存在其他操作系统需安装
# pacman -S grub efibootmgr
	安装grub efi启动管理工具
# grub-install --target=x86_64-efi --efi-directory=/boot --bootloader-id=Archlinux
# grub-mkconfig -o /boot/grub/grub.cfg
# pacman -S iw wpa_supplicant dialog netctl
	笔记本安装上网工具
# systemctl enable dhcpcd
# systemctl start dhcpcd
# exit
	退出chroot环境
# umount -R /mnt
	卸载被挂载的分区
# reboot
```

```
# lspci | grep VGA
# pacman -S 驱动包
	显卡			驱动包
	通用			xf86-video-vesa
	intel-		 xf86-video-intel
	amdgpu		 xf86-video-amdgpu
	Geforce7±	 xf86-video-nouveau
	Geforce6/7	 xf86-video-304xx
	ati			 xf86-video-ati
```

```
# pacman -S xorg
# pacman -S xf86-input-synaptics
# pacman -S pacman -S ttf-dejavu wqy-microhei wqy-zenhei

```

```
# loadkeys de-latin1
```

```
# loadkeys de-latin1
```

```
# loadkeys de-latin1
```

```
# loadkeys de-latin1
```

```
# loadkeys de-latin1
```

```
# loadkeys de-latin1
```

```
# loadkeys de-latin1
```

```
# loadkeys de-latin1
```

```
# loadkeys de-latin1
```

```
# loadkeys de-latin1
```

```
# loadkeys de-latin1
```

```
# loadkeys de-latin1
```

```
# loadkeys de-latin1
```

```
# loadkeys de-latin1
```

