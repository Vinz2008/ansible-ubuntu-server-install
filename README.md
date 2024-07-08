Run command for homeserver
```
ansible-playbook nas.yml -K --ask-pass --ask-vault-pass
```

Run command  for rapsberry pi
```
ansible-playbook raspberry_pi.yml -K --ask-pass --ask-vault-pass
```

For creating custom iso, run 
```
ansible-playbook iso.yml -i "localhost," -c local --ask-vault-pass
```

To edit secrets, run
```
ansible-vault edit group_vars/all/secret.yml
```

To index nextcloud files, run 
```
docker exec -u www-data nextcloud php occ files:scan --all
```

Services to manually install to secondary server (for example a raspberry pi)

- pihole
- unbound
- uptime kuma
