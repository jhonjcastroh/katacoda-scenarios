En el caso de querer administrar nodos con sistema operativo windows debemos establecer la variable `ansible_connection` con el valor `winrm`.

Tenemos que tener en cuenta que **los nodos o servidores Windows deben tener activo la característica de WinRM** ya que sin ella el nodo de control de Ansible no puede establecer conexión hacia el/los nodos administrados.

Tambien para evitar conflictos en la conexión con servidores Windows y la revisión de certificados de cada servidor con su IP se establece la variable `ansible_winrm_server_cert_validation` con el valor `false`.

<pre class="file" data-filename="windows_hosts.cfg" data-target="replace">
[win:vars]
ansible_winrm_server_cert_validation=ignore
ansible_connection=winrm
ansible_user=USER
ansible_password=PASSWOR

[win]
HOST_WINDOWS

</pre>
