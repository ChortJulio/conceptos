# WSL
Permite ejecutar un entorno de GNU/Linux directamente dentro de Windows.

# Links interesantes
### https://learn.microsoft.com/es-es/windows/wsl/about
### https://learn.microsoft.com/es-es/windows/wsl/setup/environment

# Pasos que debo seguir
## Primer paso
- Buscar "Activar o desactivar las características de Windows".
- Activar (si están desactivadas):
  - Subsitema de Windows para Linux
  - Plataforma de Máquina Virtual
- Reiniciar la computadora después de activar estas dos opciones.

## Segundo paso
- Abrir un cmd como administrador.
- Ejecutar el siguiente comando:
  - wsl --install
- Esperar a que instale.
- Colocar nombre y contraseña (la última es escritura ciega).

## Tercer paso
- Se recomienda actualizar regularmente los paquetes con el comando:
  - sudo apt update && sudo apt upgrade
- Windows no actualiza automáticamente las distribuciones de Linux.

## Cuarto paso: Configuración de la terminal de Windows
- Cada vez que se instala una nueva distribución de Linux de WSL, se creará una nueva instancia para ella dentro de Terminal Windows que se puede personalizar con sus preferencias.
- Paleta de comandos: Ctrl + Shift + P

## File Storage
- Para abrir un proyecto de WSL en el explorador de archivos de Windows:
  - explorer.exe .
- El punto final del comando es importante para abrir el directorio actual.

## Instalar la extensión en VSCode
- Buscar en extensiones, se llama "Remote Explorer".



