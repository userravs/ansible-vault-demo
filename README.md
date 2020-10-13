# ansible-vault-demo
- Managed node username: ansible
- Managed node password: password
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
