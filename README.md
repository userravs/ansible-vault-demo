# ansible-vault-demo
- Information about "sensitive_content.yml":

Variable name | value
--- | --- 
`managed_node_ip` | 192.168.10.131
`managed_node_user` | ansible
`managed_node_pass` | password

- **Vault password**: password

---

## Runbook
1. Edit file *sensitive_content.yml*: `vi sensitive_content.yml`, with following lines:
```yaml
---
managed_node_ip:	192.168.10.131
managed_node_user:	ansible
managed_node_pass:	password
```
2. Encrypt file: `ansible-vault encrypt sensitive_content.yml --ask-vault-pass`
3. Run playbook: `ansible-playbook -i inventory.yml playbook.yml --ask-vault-pass`
4. Decrypt content if required: `ansible-vault decrypt sensitive_content.yml --ask-vault-pass`
