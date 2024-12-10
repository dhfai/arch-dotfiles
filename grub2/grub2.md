# Grub Menu Configuration
Grub is a bootloader that allows you to select which operating system to boot when you start your computer. It is the first program that runs when you turn on your computer. The Grub menu is the screen that appears when you boot your computer, showing a list of operating systems you can boot into.

## 1. Install Grub Customizer

```zsh
sudo pacman -S grub-customizer grub efibootmgr
```

## 2. Open Grub Customizer

```zsh
git clone https://github.com/vinceliuice/Wuthering-grub2-themes
cd Wuthering-grub2-themes
./install.sh
```