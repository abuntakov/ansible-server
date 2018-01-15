### Installing

```sh
ansible-galaxy install --roles-path ./roles -r requirements.yml
```

### Deployment

Change `hosts`, then...

```sh
ansible-playbook -i hosts site.yml
```
