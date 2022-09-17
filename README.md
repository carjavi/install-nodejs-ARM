<p align="center"><img src="https://raw.githubusercontent.com/carjavi/install-nodejs-ARM/master/img/nodejs-npm_logos.png" height="250" alt="MarlinFirmware's logo" /></p>

<br>

<h1 align="center">Installation NODEJS & NPM ARM</h1>

<img src="https://img.shields.io/badge/OS%20-Raspbian%20GNU%2FLinux%2011%20(bulleye)-yellowgreen">

<img src="https://img.shields.io/badge/Hardware-Raspberry%20ver%204-red">
<img src="https://img.shields.io/badge/Hardware-Raspberry%20ver%203-red">

<h4 align="right">Aug 22</h4>

<br>

<!--
***Option 0***
excellent for a file.sh node v17.9.0 /npm v8.5.5
```
sudo su
curl -fsSL https://deb.nodesource.com/setup_17.x | bash -
```
```
sudo apt install nodejs
npm install -g npm@8.19.2 // new
```
### Uninstall/ Remove NodeJS and NPM
```
sudo apt remove nodejs
```
-->

  ***Option 1***

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
---
ver v0.34.0
```
$ curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.34.0/install.sh | bash
```
Una vez instalado, cierra la terminal y abre otra.
```
$ nvm install node
```
---

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

---

***Option 2***

```
sudo wget https://nodejs.org/dist/v16.16.0/node-v16.16.0-linux-armv7l.tar.xz
sudo apt install tar
sudo tar -xvf node-v16.16.0-linux-armv7l.tar.xz
sudo chmod -R 755 /usr/local
```
<br>

---
Copyright &copy; 2022 [carjavi](https://github.com/carjavi). <br>
```www.instintodigital.net``` <br>
carjavi@hotmail.com <br>
<p align="center">
    <a href="https://instintodigital.net/" target="_blank"><img src="https://raw.githubusercontent.com/carjavi/install-nodejs-ARM/master/img/developer.png" height="100" alt="www.instintodigital.net"></a>
</p>
