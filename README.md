Run command 
```
ansible-playbook run.yml -K --ask-pass --ask-vault-pass
```

For creating custom iso, run 
```
ansible-playbook run.yml -i "localhost," -c local --ask-vault-pass
```