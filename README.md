# Home Lab

## Vangrant
### Powershell

```Powershell
cd "X:\VMs\Controller\production\"

vagrant up

vagrant reload

vagrant halt

vagrant destroy -f

vagrant provision

vagrant ssh

```

## Ansible
### WSL
```bash
cd /mnt/x/VMs/Controller/ansible/

sudo apt update
sudo apt upgrade -y 
sudo apt install software-properties-common -y 
sudo add-apt-repository --yes --update ppa:ansible/ansible 
sudo apt install ansible -y

ansible --version


cd /mnt/x/VMs/Controller/production

cp /mnt/x/VMs/Controller/production/.vagrant/machines/default/virtualbox/private_key ~/.ssh/vagrant_private_key

chmod 600 ~/.ssh/vagrant_private_key

ssh -i ~/.ssh/vagrant_private_key vagrant@192.168.0.2

ssh -i .vagrant/machines/default/virtualbox/private_key vagrant@192.168.0.2


ansible-playbook setup-VM.yml -i inventory.ini


```