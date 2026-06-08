 
```python
sudo responder -I eth0 -dw 
```

cuando ejecutamos  este comando basicamente le deciamos a la maquina a  la cual le hicimos peticiones  que somos la maquina que el busca   de igual manera nos proporciona un hash en 
***NTLMv2***   el cual es necesaio crakear  con [[john the ripper]] 

```python
john --wordlist=Descargas/rockyou.txt hash.txt
```

  cuando ejecutamos este comando   es para crackear el hash utilizando un directorio que en este caso se llama rockyou esto nos proporciona una contraseña y un usuario como lo vemos en la imagen