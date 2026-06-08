# Buscar puertos de un host

```python
sudo nmap -p- {IP} --min-rate 5000 -Pn -vvv -sS
```

- ****-p-*** : esta opción es para que nuestro escaneo revise todos los 65535 puertos 
- ***--min-rate 5000*** : esta opción sirve  para enviar  5000 paquetes  por minuto
-  ***-Pn*** : esta opción es para  que no haga pruebas ping no esperar la respuesta de cada puerto porque seria demasiado lento  
- ***-vvv*** : esta opción se llama verbose y se usa para ver información 
- ***sS*** : esta opción es para hacer un  syn port scan lo que significa   que le preguntamos a la maquina si esta escuchando y si nos autoriza pero  corta la comunicación a mitad de camino porque solo queríamos sabes si estaba viva  


# Escaneo de versiones y servicios

```python
sudo nmap -p22,80,445 -sVC {IP} -T5 -v
```

-  ***-p*** : esta opción es para escanear  los puertos que se encontraron en el escaneo anterior (22,80,445)
- ***sVC*** : esta opcion es la mezcla de dos scripts de nmap son ***sV***   Y   ***sC***  donde una nos dice los servicios, enumera información relevante de cada uno   y la otra nos dice las versiones 
- ***-T5*** : esta opción es para la velocidad y agresividad que queremos en el escaneo también tenemos  T4 - T3 -T2 
- ***v*** :  es verbose  para ver información  


