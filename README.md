# nix-secrets
## Commands
`nix-shell -p sops --run "sops secrets.yaml"` - decrypt secrets file and open in `$EDITOR`  
`nix-shell -p ssh-to-age --run 'cat /etc/ssh/ssh_host_ed25519_key.pub | ssh-to-age'` - convert host public key to **age** format  

## To add
- ssh config
- user passwords
