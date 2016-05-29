# OpenShift Enterprise mit Ansible

## Azure

```shell
git clone https://github.com/tagliateller/openshift-ansible.git

cd openshift-ansible

export ANSIBLE_HOST_KEY_CHECKING=False

azure login
```

Browser öffnen, aka.ms/devicelogin ansteuern, Code lt. Kommandozeilenausgabe einfügen, Login in Azure eingeben

```shell
ansible-playbook -i azure-create.inventory playbooks/azure/openshift-enterprise-cluster-create.yml
```

Damit ist zunächst die VM angelegt. Es folgt die Installation von OpenShift mit der Quick-Installation-Methode:
Vault ist für Subskriptionsname und die anzulegenden User

```shell
$ ansible-playbook -i azure.inventory --private-key ~/id_azure_vm playbooks/azure/openshift-enterprise-cluster-after-create.yml --ask
-vault
``` 
