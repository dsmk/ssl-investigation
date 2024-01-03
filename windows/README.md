# Windows SSL test

This directory contains Ansible to create and configure various Windows Server SSL test systems.  Right now it has only been tested in the AWS app-nonprod 
account but should theoretically work with other AWS accounts.  


## Posh-ACME (`setup-posh-acme.yaml``)

This sets up IIS with Posh-ACME.  Right now it activates IIS, installs/configures Posh-ACME, and then does a hard-coded hostname certificate.

```bash
(aws) $ ansible-playbook -i hosts-1.yaml setup-posh-acme.yaml -vv 
```

## Setting up Ansible and Python for RHEL 9 systems

```bash
$ python3.11 -m venv ~/aws
$ . ~/aws/bin/activate
(aws) $ pip install -r ./python-requirements.txt
(aws) $ ansible-galaxy collection install -r ./requirements.yml
```