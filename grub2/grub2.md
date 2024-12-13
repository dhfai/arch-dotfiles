# Grub Menu Configuration
Grub is a bootloader that allows you to select which operating system to boot when you start your computer. It is the first program that runs when you turn on your computer. The Grub menu is the screen that appears when you boot your computer, showing a list of operating systems you can boot into.

## 1. Install Grub Customizer

```zsh
sudo pacman -S grub-customizer grub efibootmgr
```

## 2. Create `/boot/grub` directory

```zsh
sudo mkdir -p /boot/grub
```

## 3. Install grub-install
```zsh
sudo grub-install --target=x86_64-efi --efi-directory=/boot --bootloader-id=GRUB
```

## 4. Open Grub Customizer

```zsh
git clone https://github.com/vinceliuice/Wuthering-grub2-themes
cd Wuthering-grub2-themes
./install.sh
```

## 5. After installation, open Grub Customizer

```zsh
sudo nano /etc/default/grub
```
and change the `GRUB_THEME` to `"/usr/share/grub/themes/Wuthering-changli/theme.txt"`

## 6. Reboot your system

```zsh
rebooot
```