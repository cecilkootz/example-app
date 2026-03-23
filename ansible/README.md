# Ansible deployment

This deploys a static "Hello World" site to an Ubuntu VM running NGINX.

## Prereqs
- Control machine has Ansible installed
- Target VM is reachable at `webserver1.codomain.com`
- SSH user: `deploy`
- `deploy` can use `sudo` (you will be prompted for passwords)

## Deploy
From the `ansible/` directory:

```bash
ansible-playbook -i inventory.ini site.yml --ask-pass --ask-become-pass
```

## Validate
- Site: http://www.codomain.com/
- Health: http://www.codomain.com/healthz
