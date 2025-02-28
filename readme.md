# Odoo instance

## Instalación

### Requerimientos

Instalar dotenv

```bash
sudo apt-get install python3-dotenv 
```

### Configurar el archivo .env

En este archivo se encuentra lo necesario para configurar Odoo. 

### Buildear el Dockerfile

Inicialmente no existe el Dockerflie, ya que se require que se llene Informacion dentro del .env asi como la version, este comando nos generara el Dockerfile ideal.

 ```bash
./odoo build
```
### Estructura de la carpeta a utilizar

```bash
- src /
    custom/
        /repository-1
        /repository-2
        /repository-n
    enterprise/
```

### Instalar el CLI

```bash
sudo ./setup
```

### Inicio, Reinicio y Stop del Ambiente

Estos comandos son acortadores a los comandos naturales de docker compose. como up y down.
(Este detectara automaticamente el proyecto si estas en su carpeta)

#### Iniciar Odoo
```bash
odoo run
```
#### Reiniciar Odoo
```bash
odoo restart  
```
#### Detener Odoo
```bash
odoo stop
```
#### Visualizar Logs
```bash
odoo logs
```
#### Abrir bash del contenedor 
```bash
odoo bash
```
#### Acceder a la base de datos
```bash
odoo psql db_name
```
#### Resetear la contraseña de un usuario de la base de datos
```bash
odoo reset db_name 
odoo reset db_name -l login
```
#### Actualizar los modulos de la base de datos
```bash
odoo u db_name module1,module2
```
#### Acceder a la shell de odoo
```bash
odoo shell db_name
```

### FAQ

#### Donde configuro el addons_path?

Al incluir un repositorio nuevo a la carpeta custom, este lo detectara automaticamente.

