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


Added "disable_mlock" to vault.json dues to - 
Error initializing core: Failed to lock memory: cannot allocate memory

This usually means that the mlock syscall is not available.
Vault uses mlock to prevent memory from being swapped to
disk. This requires root privileges as well as a machine
that supports mlock. Please enable mlock on your system or
disable Vault from using it. To disable Vault from using it,
set the `disable_mlock` configuration option in your configuration
file.

```
