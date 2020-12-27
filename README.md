# pi-setup
Instructions for setting up Raspberry Pi 4 for development

---

## Generate Keys


  ```bash
  ssh-keygen -t ed25519 -C "larry@larrytooley.com"
  eval "$(ssh-agent -s)"
  ssh-add ~/.ssh/id_ed25519
  ```

  Instructions can be found [here](https://docs.github.com/en/free-pro-team@latest/github/authenticating-to-github/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent).

---

## Edit Keymap to Swap Escape and Caps Lock 

  * Open keyboard file and add XKBOPTION
  ```bash
  sudo vim /etc/default/keyboard
  ```
  Add the following to XKBOPTIONS: "caps:swapescape"

  More can be found at:
  ```bash
  /usr/share/X11/xkb/rules/xorg.lst
  ```

---

## Download Software

```bash
$ sudo apt update
$ sudo apt install -y vim zsh build-essential vagrant gdb git
```
Install rust from the website.

---

## Check Python 3 Version

Raspberry Pi OS currently ships with 3.7.3

Prefer 3.8 or newer.

---

## Install Pipenv

```bash
pip3 install pipenv
```

---

## Change Shell

zsh should have been installed during download software step.

```bash
$ which zsh
/usr/bin/zsh
$ chsh -s /usr/bin/zsh
```

---

## Install oh-my-zsh

Go to [https://ohmyz.sh/](https://ohmyz.sh/)

---

## Overclock

Add the last two line to the ```/boot/config.txt``` file and reboot.
```bash
#uncomment to overclock the arm. 700 MHz is the default.
#arm_freq=800
over_voltage=2
arm_freq=1750
```

---

## Enable SSH

```bash
$ raspi-config
```

Go to interfaces and enable ssh.

---

#TODO: write script to do all this
