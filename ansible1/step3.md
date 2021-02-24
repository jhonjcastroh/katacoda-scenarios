### ¿Qué son los Inventarios de Ansible?
Los inventarios son ficheros donde encontramos los nodos administrados por Ansible, incluyendo al localhost.

En concreto, en un inventario podemos encontrar:
* Host
* Grupos de Host
* Variables globales, de grupo y/o de host

Ansible nos provee de un archivo de ejemplo de inventarios con algunas opciones que podemos usar:
`cat /etc/ansible/hosts`{{execute}}

### Inventarios para servidor local

Para ejecutar acciones únicamente en el nodo manager (servidor local) debemos tener un inventario que indique el localhost como único host localhost y la variable `ansible_connection`. 

<pre class="file" data-filename="localhost.cfg" data-target="replace">
[servers:vars]
ansible_python_interpreter=/usr/bin/python3
ansible_connection=local

[servers]
localhost ansible_connection=local
</pre>

