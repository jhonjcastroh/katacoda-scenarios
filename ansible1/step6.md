## Playbook de Ansible

Los playbooks de Ansible deben ser escritos en formato Yamel (. yaml ó .yml). En los playbooks Ansible podemos encontrar los siguientes elementos:

* play
* hosts
* vars
* task
    * module

<pre class="file" data-filename="playbook.yml" data-target="replace">
- name: NAME_PLAY
  hosts: HOST
  vars:
    VAR: VALOR
  roles:
    - NAME_ROL_01
    - NAME_ROL_02
    - NAME_ROL_N
  tasks:
    - name: NAME_TASK
      MODULE:
        ARG_MODULE: VALOR
      ARG_TASK: VALOR

</pre>