## instalacion de Ansible

###Prerequisitos
* Python 2 (versión 2.7) or Python 3 (versiones 3.5 o superior) instalado.

Para instalar Ansible debes ejecutar los siguientes comandos:
```
sudo apt update -y
sudo apt install -y software-properties-common
sudo apt-add-repository --yes --update ppa:ansible/ansible
sudo apt install -y ansible
```{{execute}}

Puedes confirmar y verifcar la versión de Ansible instalada ejecutar:
`ansible --version`{{execute}}

Para mayor información consultar la guía de instalación https://docs.ansible.com/ansible/latest/installation_guide/index.html