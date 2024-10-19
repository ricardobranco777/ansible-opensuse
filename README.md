Ansible playbook for openSUSE Tumbleweed:

```
sudo zypper install ansible
zypper ansible-galaxy collection install community.general
```

Check:
`ansible-playbook -v -i inventory -C main.yml`

Run with:
`ansible-playbook -v -i inventory main.yml`

Disable GDM suspend when AC is connected:
```
sudo sudo -u gdm dbus-launch gsettings set org.gnome.settings-daemon.plugins.power sleep-inactive-ac-type blank
```

NOTES:
  - This configures a bridge over Ethernet for KVM, so connect to the wireless interface
  - Run `zypper addlock cups cups-client emacs` to avoid unwanted packages
