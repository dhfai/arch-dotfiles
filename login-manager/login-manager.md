# Login Manager (SDDM)

SDDM is a modern display manager for X11 aiming to be fast, simple and beautiful. It uses modern technologies like QtQuick, which in turn gives the designer the ability to create smooth, animated user interfaces. SDDM is the successor of the LXDM display manager.

## Installation
```zsh
sudo pacman -S sddm
```

## Configuration
Enable the SDDM service:
```zsh
sudo systemctl enable sddm.service
sudo systemctl start sddm.service
```

Disable the lightDm service:
```zsh
sudo systemctl disable lightdm.service
sudo systemctl stop lightdm.service
```

## Themes
1. Clone the repository:
```zsh
sudo git clone https://github.com/keyitdev/sddm-astronaut-theme.git /usr/share/sddm/themes/sddm-astronaut-theme
sudo cp /usr/share/sddm/themes/sddm-astronaut-theme/Fonts/* /usr/share/fonts/
```

2. Edit the SDDM configuration file:
```zsh
/usr/lib/sddm/sddm.conf.d/default.conf
```
3. Search for the `Current` line and change the value to `sddm-astronaut-theme`.
```zsh
[Theme]
Current=sddm-astronaut-theme
```

4. Restart the SDDM service:
```zsh
sudo systemctl restart sddm.service
```

## And that's it! You have successfully installed and configured SDDM.


