Run command 
```
ansible-playbook run.yml -K --ask-pass --ask-vault-pass
```

For creating custom iso, run 
```
ansible-playbook iso.yml -i "localhost," -c local --ask-vault-pass
```

To index nextcloud files, run 
```
docker exec -u www-data nextcloud php occ files:scan --all
```