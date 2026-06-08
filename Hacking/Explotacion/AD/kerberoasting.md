
- Dominio: camilo.corp  
- DC: 192.168.159.136  
- Atacante: Kali Linux  
- Usuario inicial: juan  
- Contraseña inicial: Password2  
- Cuenta de servicio: svc_http

Obtener un ticket Kerberos TGS de una cuenta de servicio y crackearlo offline para recuperar la contraseña. 

# Enumeración de SPNs

```python
impacket-GetUserSPNs 'camilo.corp/juan:Password2' -request
```
![[Pasted image 20260607230551.png]]
vemos que ejecutando este comando obtenemos un hash el cual debemos crakear con la ayuda de [[john the ripper]]
![[Pasted image 20260607230707.png]]
 recordemos que este ataque es para robar la contraseña del ***spn***  