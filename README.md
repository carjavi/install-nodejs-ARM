<p align="center"><img src="https://raw.githubusercontent.com/carjavi/install-nodejs-ARM/master/img/nodejs-npm_logos.png" height="250" alt="MarlinFirmware's logo" /></p>

<br>

<h1 align="center">Installation NODEJS & NPM ARM</h1>

<img src="https://img.shields.io/badge/OS-Rasbian%20GNU%20linux ver%2011-green">

<img src="https://img.shields.io/badge/Hardware-raspberry%20ver%204-red">

<h4 align="right">Aug 22</h4>

<br>

  ***Option 1***

```
$ curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.34.0/install.sh | bash
```
Una vez instalado, cierra la terminal y abre otra.
```
$ nvm install node
```
Eso instalará la última versión disponible

### Probar instalación
```
$ node --version
$ npm --version
```

### Desinstalar nodejs si está instalado

```
$ sudo apt remove nodejs
```
### Nota
puede que se necesite instalar NVM
```
$ npm i nvm
```

<br>

***Option 2***

```
sudo wget https://nodejs.org/dist/v16.16.0/node-v16.16.0-linux-armv7l.tar.xz
sudo apt install tar
sudo tar -xvf node-v16.16.0-linux-armv7l.tar.xz
sudo chmod -R 755 /usr/local
```
