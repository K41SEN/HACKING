
los primero que se hace es  ejecutar el comando 

```python
netexec smb 192.168.159.0/24 
```

este comando frente al objetivo se ejecuta con el fin de listar las direcciones IP que están  dentro del objetivo.
![[Pasted image 20260607153100.png]]

seguidamente lo que hacemos es que nos ponemos a la escucha de la red con la herramienta [[Responder]]  antes de ejecutar el responder debemos desactivar mediante
**sudo nano /etc./responder/Responder.conf  dentro de nano lo que hacemos es que editamos y desactivamos las opciones de HTTP y SMB con el fin de no capturar  los hashes de estos protocolos
![[Pasted image 20260607153307.png]]
 cuándo ya tenemos todo configurado y las herramientas a la escucha es donde se lanza el ataque mediante 
 
```python
sudo impacket-ntlmrelayx -tf targets.txt -smb2support -c 'shutdown /s /t 0 ' 
```
la herramienta de ataque en este caso es [[ntlmrelayx]]  donde este ataque consiste en que con el responder,  trata de autenticarse contra una maquina  o objetivos con el fin de ejecutar comandos de manera remota

![[Pasted image 20260607154402.png]]
en esta imagen vemos como con peticiones falsas  recibimos señales en nuestra maquina atacante la cual esta a la escucha 
![[Pasted image 20260607154457.png]]
  esta es nuestra maquina en la escucha que esta recibiendo las señales del objetivo  que por medio del comando del ataque logramos apagar la maquina y además ver la información que se ejecuto en el administrador de archivos 
  
![[Pasted image 20260607154821.png]]
