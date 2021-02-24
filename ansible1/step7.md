## Uso de documentación para búsqueda de Módulos de Ansible

La Guía del Usuario de Ansible la podemos encontrar en https://docs.ansible.com/ansible/latest/user_guide/index.html

La documentación de Ansible se usa principalmente para encontrar los módulos de las tareas que deseamos automatizar.

Los módulos son "las unidades de código que Ansible ejecuta. Cada módulo tiene un uso particular, desde la administración de usuarios en un tipo específico de base de datos hasta la gestión de interfaces VLAN en un tipo específico de dispositivo de red. Puedes invocar un solo módulo con una tarea, o invocar varios módulos diferentes en un libro de jugadas".

En el siguiente link encontramos el manual para los módulos https://docs.ansible.com/ansible/latest/user_guide/modules_intro.html

Con el siguiente comando (ad-hoc) pordemos ejecutar el modulo `ping`:
`ansible host2 -m ping`{{execute}}

Para facilitar la búsqueda de módulo contamos con un índice en el siguiente link: https://docs.ansible.com/ansible/latest/collections/index_module.html

Es importante al encontrar el módulo deseado que tengamos en cuenta lo siguiente:
1. Los pre-requisitos para que el módulo funcione. Por lo general se trata de instalación de librerías y/o paquetes.
2. Los argumentos obligatorios o requeridos, ya que sin estos el módulo no funciona.
3. Los valores por defecto de algunos de los argumentos.
4. Lo argunemtos cuyo valor puede ser manejado por una variable