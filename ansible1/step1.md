## Conociendo el archivo de configuración de Ansible

La configuración de Ansible se establece en un archivo llamado ansible.cfg. Por defecto ese archivo se encuentra ubicado en `/etc/ansible/ansible.cfg`, pero tenemos varias formas de establecer un nuevo archivo de configuración tomando en cuanta las siguientes prioridades:

* ANSIBLE_CONFIG (estableciendo la variable de entorno)
* ansible.cfg (en el directorio actual)
* ~/.ansible.cfg (en el directorio home)
* /etc/ansible/ansible.cfg

`vim /etc/ansible/ansible.cfg`{{execute}}

