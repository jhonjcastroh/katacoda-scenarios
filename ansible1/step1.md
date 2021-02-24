Para instalar Ansible debemos tener instalado Python 2 (versión 2.7) o Python 3 (versiones 3.5 o superior) y debes ejecutar los siguientes comandos:
```
sudo apt update -y
sudo apt install -y software-properties-common
sudo apt-add-repository --yes --update ppa:ansible/ansible
sudo apt install -y ansible
```

Como Ansible ya está instalado en este ambiente puedes confirmar y verifcar la versión de Ansible instalada al ejecutar: `ansible --version`{{execute}}

Para mayor información sobre la instalación de Ansible puedes consultar la guía de instalación https://docs.ansible.com/ansible/latest/installation_guide/index.html

**Nota:** Recuerda que no se requiere tener Ansible instalado en los nodos que van a ser administrados ya que es una herramienta agentless.