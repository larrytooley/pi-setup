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

vim zsh build-essential vagrant gdb git

rust from the website

---

## Check Python Version

---

## Install Pipenv

---

## Change Shell

---

## Install oh-my-zsh

---

## Overclock

---

## Enable SSH
