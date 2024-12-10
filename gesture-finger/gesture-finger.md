# Gesture Finger - Touchpad Gestures


## 1. Dependency Installation

 Make sure libinputInstalled:

```zsh
sudo pacman -S libinput
```

Install libinput-gestures detect touchpad gestures:

```zsh
yay -S libinput-gestures
```

Add your users to the group inputto have access to the touchpad:

```zsh
sudo gpasswd -a $USER input
```
<b>After that, log out and log back in to implement group changes.</b>

To check if the user is in the input group, run the following command:

```zsh
groups
```
The output should contain the input group.

```zsh
# Example
input wheel $USER
```

## 2. Configuration libinput-gestures

Copy the default configuration file to the user directory:

```zsh
cp /etc/libinput-gestures.conf ~/.config/libinput-gestures.conf
```

Edit configuration file:

```zsh
nano ~/.config/libinput-gestures.conf
```
Add or change the following line to define the three-finger gesture to the left and right:

```zsh
gesture swipe left  3 bspc desktop -f next
gesture swipe right 3 bspc desktop -f prev
```
swipe left: Three fingers slide to the left to move to the next workspace. swipe right: Three fingers slide to the right to move to the previous workspace.


## 3. Enable libinput-gestures
 Run the following command to activate and test the gesture:

```zsh

libinput-gestures-setup autostart
libinput-gestures-setup start
```
To ensure it runs automatically at startup, add to the user service system:

```zsh
libinput-gestures-setup autostart
```