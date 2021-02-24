Para ejecutar acciones en multiples nodos debemos tener en cuenta el metodo de autenticación para cada nodo. El metodo se establece con la variable `ansible_connection` y su valor puede ser `smart`, `ssh`, `paramiko` o  `local`. Por defecto esta variable tiene como valor `ssh`.

Para evitar conflictos en la conexión a los nodos por HostKey repetidas debemos agregar la variable y el valor `ansible_ssh_common_args='-o StrictHostKeyChecking=no'`

El siguiente es un ejemplo de inventario con los diferentes tipos de opciones para agregar un host y su metodo de conexioón:

<pre class="file" data-filename="multiple_hosts.cfg" data-target="replace">
localhost ansible_connection=local

[servers]
host_ip ansible_ssh_pass=HARDPASS ansible_connection=ssh

[servers:children]
manager
workers

[manager]
MANAGER_NAME ansible_host=MANAGER_IP

[workers]
WORKER01_NAME ansible_host=WORKER01_IP
WORKER02_NAME ansible_host=WORKER02_IP

[servers:vars]
ansible_python_interpreter=/usr/bin/python3
ansible_ssh_common_args='-o StrictHostKeyChecking=no'
ansible_ssh_user=root
ansible_ssh_private_key_file=.ssh/key.pem
VARIABLE_NAME=VALOR
</pre>