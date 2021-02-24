La configuración de Ansible se establece en un archivo llamado `ansible.cfg`. 

Por defecto ese archivo se encuentra ubicado en `/etc/ansible/ansible.cfg` pero tenemos varias formas de establecer un nuevo archivo de configuración tomando en cuenta las siguientes prioridades:

* Estableciendo la variable de entorno `ANSIBLE_CONFIG`.
* Con un archivo `ansible.cfg` en el directorio actual.
* Con un archivo `~/.ansible.cfg` en el directorio home.
* Con el archivo ubicado en `/etc/ansible/ansible.cfg` (por defecto).

`vim /etc/ansible/ansible.cfg`{{execute}}

Para salir, escriba `:q!`{{execute}}
