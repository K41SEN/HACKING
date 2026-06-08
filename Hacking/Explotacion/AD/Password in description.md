

# Buscar descripciones con RPC  


```python
rpcclient $>
```
cuando logramos  conectarnos por medio de ***rcp*** utilizamos el comando ***rpcclient $> enumdomusers***
```python
rpcclient $> enumdomusers
```
cuando ejecutamos este comando obtenemos la lista de usuarios con sus respectivas RID
![[Pasted image 20260603223614.png]]

cuando optenemos los usuarios con su respectivos RID ocupamos el comando 
***queryuser 0x454***

```python
queryuser 0x454
```

aquí 0x454 es el RID de un usuario entonces al usar el comando se le agrega ese RDI para ver la información que ese usuario pudiera darnos
   
![[Pasted image 20260603224059.png]]

# Buscar descripciones con netexec

esta manera de buscar descripcciones es mas rapida y practica  con el comando 

```python
netexec smb 192.168.159.0/24 --users  -u 'deportado' -p 'Password1' 
```
 se usa la herramienta netexec contra el objetivo en este comando vemos que solicitamos usuarios para verificar si hay alguna forma de conectarnos esto que vemos ***user*** y ***password***  es informacion recopilada anterior mente con el [[Responder]] y después de haber crakeado un hash con [[john the ripper]]  ya con esta información se la proporcionamos en este comando y se ve asi 
 ![[Pasted image 20260607164337.png]]
 esto también nos arroja información de los usuarios dentro de este objetivo 