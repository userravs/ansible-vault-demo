# ansible-vault-demo
- Information about "sensitive_content.yml":

Variable name | value
--- | --- 
`managed_node_ip` | 192.168.10.131
`managed_node_user` | ansible
`managed_node_pass` | password


- Vault password: password

## Runbook
```bash
# Edit file sensitive_content.yml
vi sensitive_content.yml

# Encrypt file
ansible-vault encrypt sensitive_content.yml --ask-vault-pass

# Run playbook
ansible-playbook -i inventory.yml playbook.yml --ask-vault-pass

# Decrypt content if required!
ansible-vault decrypt sensitive_content.yml --ask-vault-pass
```
