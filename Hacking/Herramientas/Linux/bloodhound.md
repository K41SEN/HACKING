
```python
bloodhound-python -u 'juan@camilo.corp' -p 'Password2' -ns 192.168.159.136 -d camilo.corp -c all

```
  antes  de usar esta herramientas necesito crear una carpeta  usando {***mkdir-nombre***  }  porque cuando usamos esta herramienta con este código lo que hace es que nos descarga una serie de archivos (.json) 
  ![[Pasted image 20260620170203.png]]
  ```python
  sudo bloodhound-start
  ```
   después de que ya hemos descargado todo lo ejecutamos el siguiente comando lo que hacemos con este comando es iniciar el ***bloodhound***  en el navegador porque nos va desplegar y mostrar toda la estructura del AD gráficamente   cuando lo iniciamos se nos abrirá una ventana en el navegadora la cual pide que la configuremos lo único que debemos hacer es loguearnos con credenciales por defecto (neo4j)  es la misma  luego de esto se nos abrirá una ventana donde dice que debemos cambiar la contraseña  podemos lo que queramos y luego nos vamos  de regreso a la terminal y usando el comando 
   ```python
    sudo nano /etc/bhapi/bhapi.json
   ```
para que usamos  esto para ingresar la contraseña que anteriormente configuramos  esto debemos modificar únicamente la parte que dice ***secret***  a continuación mostreare de donde se obtuvo esta ruta 
![[Pasted image 20260620171920.png]]
  