Ansible playbook for openSUSE Tumbleweed:

```
sudo zypper install ansible
zypper ansible-galaxy collection install community.general
```

Check:
`ansible-playbook -v -i inventory -C main.yml`

Run with:
`ansible-playbook -v -i inventory main.yml`

TODO:
  - Disable GDM suspend when AC is connected:
```
sudo -u gdm dbus-launch gsettings set org.gnome.desktop.session idle-delay 0
sudo -u gdm dbus-launch gsettings set org.gnome.settings-daemon.plugins.power sleep-inactive-ac-type nothing
```

NOTES:
  - This configures a bridge over Ethernet for KVM, so connect to the wireless interface
