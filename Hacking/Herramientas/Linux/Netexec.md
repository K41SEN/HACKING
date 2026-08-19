- [x] smbv
# enumerar computadores del dominio:



```python
 netexec smb 192.168.159.0/24
```
NetExec es una herramienta utilizada para enumerar sistemas Windows, Active Directory y servicios de red.  
  
Su objetivo es recopilar información de hosts, usuarios, servicios y credenciales.
***netexec smb***:  esta herramienta nos permite  ver todos los computadores del AD y ***smb*** es el protocolo por el cual queremos revisar  a tener en cuenta en este comando  se agregan únicamente los tres primeros bloques de la ip se completa con 0/24 

# sintaxis basica 

```python
nxc <protocolo> <objetivo>
```

# protocolos admitidos 

* smb
* ldap
* winrm
* mssql
* rdp
* ssh
* ftp

# funcion

- Descubre hosts Windows.
- Detecta sistema operativo.
- Detecta nombre del equipo.
- Detecta dominio.
- Detecta SMB Signing.

# Enumerar con credenciales

```python
 netexec smb 192.168.159.0/24 -u 'deportado' -p 'Password1' 
```
![[Pasted image 20260607164744.png]]
podemos evidenciar que a la herramienta le proporcionamos las credenciales y nos autentica frente a la victima 