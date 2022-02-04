# vault-autounseal
How to start and autounseal Vault Hashicorp
```
First, lets create volumes

mkdir -p ./volumes/config
mkdir -p ./volumes/logs
mkdir -p ./volumes/file

And create vault configuration and other files - 

nano volumes/config/vault.json  (Included)

nano docker-compose.yml (Included)

nano unseal.sh (Included)

Value in unseal.sh KEY=  will be received from GUI (first start)
"keys_base64": ["0ADA..................................="

Finally start - docker-compose up
```
