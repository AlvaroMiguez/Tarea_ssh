# Tarea SSH

### Conectarse al usuario admin de otra máquina por medio de claves publica y privado

1. Primero debemos crear la clave pública de nuestro ssh mediante el comando `ssh-keygen`.
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

2. Para ver la clave ejecutamos `cat ~/.ssh/id_rsa.pub`.
   
3. Para copiar nuestra clave en el equipo del compañero hacemos:(para que la clave se copie en la sesion que va a utilizar y la ip del equipo) `ssh-copy-id nombre_usuario@ip_equipo_dest` en mi caso `ssh admin@10.0.9.12`.

4. Ya nos dejaría entrar y tendríamos por pantalla en el nombre de la terminal el del equipo destino.


### Como configurar el acceso ssh en el GitHub

1. Como ya tenemos la clave creada hacemos un `cat id_rsa.pub`y copiamos la clave y la pegamos en nuestra cuenta de github en opciones ssh keys.

2. Creamos el repositorio en github y copiamos la ruta

3. Hcemos un `git init` para iniciar el servicio, a continuación hacemos el `git clone [url_repositorio]`.

4. Nos metemos dentro del repositorio en local y por ejemplo hacemos un  README.md:
   ```
   cd [carpeta del repositorio]
   touch README.md
   ```
5. Lo añaimos al repositrio y hacemos un commit:
   ```
   git add README.md
   git commit -m "Creación README.md"
   ```
   
6. En el editor de texto que prefiera, abra el archivo en `~/.ssh/config`. Si este archivo no existe, puede crearlo si escribe `touch ~/.ssh/config` en el terminal.
