## Ejecución de playbook de Ansible

Para ejecutar un comando Ansible debemos contar con un nodo de control y otro administrado. Comprobemos en cuál nodo estamos y habilitemos la consola para los nodos necesarios:
<pre>
`hostname`{{execute}}

`echo "Ejecutar en Terminal del Host 1 (nodo de control)"`{{execute HOST1}}

`echo "Ejecutar en Terminal del Host 2 (nodo administrado)"`{{execute HOST2}}
</pre>

En Ansible contamos con comandos **ad-hoc** para ejecutar módulos sin necesidad de playbooks. El siguiente comando **ad-hoc** com la bandera `-m` ejecuta el módulo `ping` que no recibe parámetros:
`ansible host2 -m ping`{{execute}}

RETO 1: modificar el inventario `multiple_hosts.cfg` para que pueda ejecutar comandos sobre el Host 2.
RETO 2: Crear playbook llamado `ping.yml` para ejecutar el módulo ping en el Host 2.

En el siguiente comando para ejecutar el playbook `ping.yml` encontramos la bandera -i para indicar el inventario a utilizar el nombre del archivo del playbook.Comprobemos si el reto fue superado:
`ansible-playbook -i multiple_hosts.cfg ping.yml`{{execute}}
La salida del comando debe ser algo parecido a lo siguiente:
```

```
