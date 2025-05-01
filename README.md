Run command for homeserver
```
ansible-playbook nas.yml -K --ask-pass --ask-vault-pass
```

Run command  for raspberry pi
```
ansible-playbook raspberry_pi.yml -K --ask-pass --ask-vault-pass
```

For creating custom iso, run 
```
ansible-playbook iso.yml -i "localhost," -c local --ask-vault-pass
```

To edit secrets, run
```
EDITOR=nano ansible-vault edit group_vars/all/secret.yml
```

To index nextcloud files, run 
```
docker exec -u www-data nextcloud php occ files:scan --all
```

To backup bitwarden manually, run
```
docker exec bitwarden-backup /usr/local/bin/python /app/main.py
```

