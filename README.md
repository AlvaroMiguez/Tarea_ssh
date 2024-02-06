# Tarea SSH

### Conectarse al usuario admin de otra máquina por medio de claves publica y privado

1. Primero debemos crear la clave pública de nuestro ssh mediante el comando `ssh-keygen`
   Si generó previamente un par de claves SSH, es posible que vea un mensaje como el siguiente:
   ```
   /home/username/.ssh/id_rsa already exists.Overwrite (y/n)?
   ```
   Una vez terminado aparecerá un mensaje como este:
```
   Your identification has been saved in /home/username/.ssh/id_rsa.
Your public key has been saved in /home/username/.ssh/id_rsa.pub.
The key fingerprint is:
a9:49:2e:2a:5e:33:3e:a9:de:4e:77:11:58:b6:90:26 username@remote_host
The key's randomart image is:
+--[ RSA 2048]----+
|     ..o         |
|   E o= .        |
|    o. o         |
|        ..       |
|      ..S        |
|     o o.        |
|   =o.+.         |
|. =++..          |
|o=++.            |
+-----------------+
```

3. 
