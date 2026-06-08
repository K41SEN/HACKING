
en el inicio del prceso tuvimos un problema que fue el siguiente 
```python
timedatectl set-ntp off ;rdate -n 192.168.159.136
```
el resultado fue Error ***Operation not permitted***  

El comando falló porque no se ejecutó con privilegios de administrador.
 por lo que necesitamos sincronizar mi maquina atacante con el dc para que kerberos no pueda fallar 
 ```python
 sudo timedatectl set-ntp off
sudo rdate -n 192.168.159.136