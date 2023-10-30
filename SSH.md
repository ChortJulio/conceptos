# SSH keys on Linux
> Con OpenSSH

## Installar OpenSSH en Linux
- Instalo OpenSSH: 
    ```bash 
    sudo apt update && sudo apt install openssh-client
    ```
- Chequeo si se instaló correctamente:
    ```bash 
    ssh -V
    ```

## Empezar el agente SSH
- Empiezo el agente: 
    ```bash 
    eval $(ssh-agent)
    ```
- Podría colocarlo dentro del `~/.bashrc` para que comience cada vez que abro la terminal, para esto puedo hacer lo siguiente:
  - Me fijo si existe `~/.bashrc`, o `~/.profile` en su defecto.
  - Dependiendo cuál exista ejecuto el siguiente comando:
  - ```bash 
    echo 'eval $(ssh-agent)'' >> ~/.bashrc
    ```

## Crear un par de keys SSH
- Ir al directorio raíz:
  ```bash 
  cd ~
  ```
- Me fijo si existe la carpeta `/.ssh` ejecutando el comando
  ```bash 
  explorer.exe .
  ```
  en el directorio raíz.
- Generar un par de claves SSH con el siguiente comando:
  ```bash 
  ssh-keygen -t ed25519 -b 4096 -C "{username@emaildomain.com}" -f {ssh-key-name}
  ```
  En donde `{username@emaildomain.com}` es el mail asociado con Bitbucket Cloud y `{ssh-key-name}` es el nombre que tendrán los archivos de las claves.
- Por último, pide colocar una contraseña. Se puede dejar vacío también. Se pedirá cada vez que se necesite utilizar (git push, git pull, git fetch).
- Se crearon 2 archivitos, la clave privada (nombre que colocamos) y la clave pública (termina en .pub).

## Crear un par de keys SSH
> Para añadir las claves SSH al agente SSH
- Ejecutar el siguiente comando remplazando `{ssh-key-name}` con el nombre que elegimos:
  ```bash 
  ssh-add ~/{ssh-key-name}
  ```
  Si no funciona, asegurarse de que el agente se está ejecutando.
- Para asegurarse de que la clave SSH correcta se utiliza al conectarse a Bitbucket, crear o actualizar la configuración de SSH (`~/.ssh/config`). Fijarse primero si existe el archivo `config` dentro de la carpeta `/.ssh`:
- Si existe, creo el architio `config` dentro de ésta:
  ```bash 
  explorer.exe .
  ```
  Navegar dentro de la carpeta `/.ssh`
- Y le doy los permisos que necesita:
  ```bash 
  chmod 600 ~/.ssh/config
  ```
- Por último, lo abro con vscode:
  ```bash 
  chmod 600 ~/.ssh/config
  ```
- Añadir la siguiente información:
  ``` 
  Host bitbucket.org
  AddKeysToAgent yes
  IdentityFile ~/.ssh/{ssh-key-name}
  ```
  Donde `{ssh-key-name}` es el lugar en donde está almacenada la clave privada una vez que se añadió al `ssh-agent`.


