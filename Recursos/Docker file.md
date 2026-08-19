```python
FROM python:2.7

RUN pip install --no-cache-dir "setuptools<45" && pip install --no-cache-dir "cryptography==3.3.2" && pip install --no-cache-dir "impacket==0.9.22"

WORKDIR /word
CMD ["/bin/bash"]

```
  este archivo de configuración de Docker que nos sirve para que Docker instale lo que necesite  y se configure básicamente que se creé un contenedor con lo que yo necesito 

los comandos para ejecutar el Docker son :
```python
sudo docker build -t python2 .
```
esto de inicio no omitamos el punto al final  
esto es para  construir el Docker lo de l parte superior es solo un archivo este es el comando que lo construye 

```python
udo docker run --rm -it --net=host -v /home/kali/Documentos:/work python2
```
y este comando ya es para ejecutarlo  teniendo en cuenta que ya tenemos otra terminal a la escucha como se había determinado