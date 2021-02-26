Para ejecutar un comando Ansible debemos contar con un nodo de control y otro administrado. Comprobemos en cuál nodo estamos y habilitemos la consola para los nodos necesarios:

`hostname`{{execute}}

`IP host02 [[HOST2_IP]]`

`ping host02`{{execute}}
`^C`{{execute}}
`ping localhost`{{execute}}
`^C`{{execute}}

En Ansible contamos con comandos **ad-hoc** para ejecutar módulos sin necesidad de playbooks. El siguiente comando **ad-hoc** con la bandera `-m` ejecuta el módulo `ping` que no recibe parámetros:
`ansible localhost -m ping`{{execute}}

Ahora te propongo unos RETOS para practicar lo aprendido en este escenario:

**RETO 1:** Encontrar la documentación sobre el módulo ping.

**RETO 2:** Modificar el inventario `multiple_hosts.cfg` para que pueda ejecutar comandos sobre el Host 2.

**RETO 3:** Crear playbook llamado `ping.yml` para ejecutar el módulo ping en el Host 2.

En el siguiente comando para ejecutar el playbook `ping.yml` encontramos la bandera -i para indicar el inventario a utilizar y el nombre del archivo del playbook. Comprobemos si el reto fue superado:
`ansible-playbook -i multiple_hosts.cfg ping.yml`{{execute}}

La salida del comando debe ser algo parecido a lo siguiente:
```

```
