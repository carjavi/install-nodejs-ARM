<p align="center"><img src="https://raw.githubusercontent.com/carjavi/install-nodejs-ARM/master/img/node_raspberry.png" height="250" alt="MarlinFirmware's logo" /></p>

<br>

<h1 align="center">Installation NODEJS & NPM for ARM</h1>

<img src="https://img.shields.io/badge/OS%20-Raspbian%20GNU%2FLinux%2011%20(bulleye)-yellowgreen">
<img src="https://img.shields.io/badge/OS%20-Raspbian%20GNU%2FLinux%2010%20(buster)-yellowgreen">

<img src="https://img.shields.io/badge/Hardware-Raspberry%20ver%204-red">
<img src="https://img.shields.io/badge/Hardware-Raspberry%203B%2B-red">
<img src="https://img.shields.io/badge/Hardware-Raspberry%20Zero-red">

<h4 align="right">Aug 22</h4>


# Installing Node.js with Apt from the Default Repositories
### nodejs 21.6.1 Ubuntu 20.04
```
sudo apt update
sudo apt install nodejs -y && sudo apt install npm -y
node -v && npm -v
```

info: https://www.digitalocean.com/community/tutorials/how-to-install-node-js-on-ubuntu-20-04

<br>

***Option 1***

# nvm (node version manager)

```
curl -sL https://raw.githubusercontent.com/nvm-sh/nvm/v0.35.0/install.sh -o install_nvm.sh
```
```
bash install_nvm.sh
```

> :warning: Una vez instalado, cierra la terminal y abre otra.
```
source .bashrc
nvm install node
npm install -g npm@8.19.2 
```
Eso instalará la última versión disponible

### Probar instalación
```
$ node --version
$ npm --version
```
<br>

> :bulb:  para verificar la versión de nvm instalada. 
```
nvm --version
```

> :bulb: Para verificar que version de node que esta actualmente
```
nvm current
```

> :bulb:  instala la ultima version mas estable 
```
nvm install --lts
```

> :bulb: instalar una aversion especifica
```
nvm install <version>
```

> :bulb: Si alguna vez necesitas cambiar de la versión de node, puedes simplemente ejecutar 
```
nvm use <número de versión>
ej: nvm use v12.18.1
```

> :bulb: Poner una version predeterminada
```
nvm alias default <version>
ej: nvm alias default 8.9.4
```


> :bulb: Para listar las diferentes versiones de node que tiene instaladas con nvm
```
nvm ls
nvm ls-remote
```
> :bulb: Para desintalar una version especifica de node
```
nvm uninstall <version>
```


> :bulb: nvm me permite usar diferentes versiones de node para diferentes proyectos. A veces, puedes estar colaborando en un proyecto con alguien que usa una versión diferente de node y necesitas cambiar las versiones de node a lo que el proyecto requiere. Para esto, nvm es la mejor herramienta.

<br><br>



***Option 2***

# Repositorio NodeSource

```
curl -sL https://deb.nodesource.com/setup_lts.x | sudo -E bash -
sudo apt-get install -y nodejs
sudo apt-get install -y npm
```
> :memo: instalar otras versiones cambiar setup_xx.x
```
setup_current.x
setup_18.x
setup_16.x
setup_14.x
setup_lts.x // versión con soporte a largo plazo
```

<br><br>

***Option 3***

# Decargando el paguete de Nodejs de su sitio web 

```
sudo wget https://nodejs.org/dist/v16.17.0/node-v16.17.0-linux-armv7l.tar.xz
sudo apt install tar
sudo tar -xvf node-v16.17.0-linux-armv7l.tar.xz
sudo cp -R node-v16.17.0-linux-armv7l/* /usr/local
rm -rf node-*
sudo chmod -R 755 /usr/local
node -v && npm -v

```
<br><br>

# NodeJS Install Steps for Pi Zero
Descargar
```
//wget <link to NodeJS ARMv61 from nodejs.org>
wget https://unofficial-builds.nodejs.org/download/release/v14.13.0/node-v14.13.0-linux-armv6l.tar.xz
```

Descomprimir
```
//tar xvfJ <file.tar.xz>
tar xvfJ node-v14.13.0-linux-armv6l.tar.xz
```

Copie el contenido del archivo extraído en el directorio usr/local de su Pi Zero.
```
//sudo cp -R <extracted tar folder>/* /usr/local
sudo cp -R node-v14.13.0-linux-armv6l/* /usr/local
```

Ahora puede limpiar eliminar el archivo que descargó y la carpeta extraída. Este comando eliminará cualquier archivo o carpeta que comience con ```nodo-``` en su directorio actual. Asegúrese de no tener ninguna carpeta importante que use este prefijo, ya que también se eliminarán.
```
rm -rf node-*
```

Ahora puede ejecutar el siguiente comando que verificará qué versión de NPM y NodeJS están instaladas actualmente en su Pi Zero.
```
node -v && npm -v
```

## Extra steps

Es posible que deba hacer lo siguiente si recibe un ```error de comando no encontrado```. Primero, abra el archivo .profile usando nano
```
sudo nano ~/.profile
```

Agregue la siguiente línea al final del archivo y presione Ctrl + X para guardar, y luego presione 'y' e ingrese para confirmar los cambios.
```
PATH=$PATH:/usr/local/bin
```

<br><br>

# Actualizar nodejs & npm

nodejs
```
sudo npm install -g n
sudo n stable
```

npm
```
sudo npm install -g npm@latest
```

## install build tools (instalar herramientas de desarrollo)
```
sudo apt install build-essential
```
<br><br>

# Uninstall nodejs Ubuntu & Debian packages
To completely remove Node.js installed from the deb.nodesource.com package methods above:

use `sudo` on Ubuntu or run this as root on debian
```
apt-get purge nodejs
rm -r /etc/apt/sources.list.d/nodesource.list
```
o

```
sudo apt remove nodejs
```


<br>

---
Copyright &copy; 2022 [carjavi](https://github.com/carjavi). <br>
```www.instintodigital.net``` <br>
carjavi@hotmail.com <br>
<p align="center">
    <a href="https://instintodigital.net/" target="_blank"><img src="https://raw.githubusercontent.com/carjavi/install-nodejs-ARM/master/img/developer.png" height="100" alt="www.instintodigital.net"></a>
</p>
