# nix-secrets
## Commands

1. convert host **public** key to **age** format
``` shell
cat /etc/ssh/ssh_host_ed25519_key.pub | ssh-to-age
```
2. export host **private** key to **age** format
``` shell
mkdir -p ~/.config/sops/age/ && sudo ssh-to-age -private-key -i /etc/ssh/ssh_host_ed25519_key | install -D -m 400 /dev/stdin ~/.config/sops/age/keys.txt
```
3. decrypt secrets file and open in `$EDITOR`
``` shell
sops secrets.yaml
```
4. add new key
    - insert key into `.sops.yaml`
    - run `sops updatekeys secrets.yaml`

## To add
- ssh config
- ssh-keys
- user passwords
