### Deployment

Change `hosts`, then...

```sh
ansible-playbook -i hosts site.yml
```

``` bash
openssl req -x509 -nodes -newkey rsa:2048 -days 365 -keyout logstash-forwarder.key -out logstash-forwarder.crt -subj /CN=vm.local
openssl pkcs8 -in logstash-forwarder.key  -topk8 -nocrypt -out logstash-forwarder.key.pem
chmod 644 logstash-forwarder.key.pem
```