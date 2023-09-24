# ansible


## GH 
1. clone repo
2. install ansible if not installed
3. run the playbook

```
ansible-playbook --ask-vault-pass rust_libs
```
3. load ssh key

```
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/github
```

