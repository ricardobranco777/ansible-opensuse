Ansible playbook for openSUSE Tumbleweed:

```
sudo zypper install ansible
zypper ansible-galaxy collection install community.general
```

Check:
`ansible-playbook -v -i inventory -C main.yml`

Run with:
`ansible-playbook -v -i inventory main.yml`
