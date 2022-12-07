# Moodle

Primer que tot el que necessites és una màquina virtual amb Ubuntu server 22.04.1 LTS, amb un adaptador pont a la interfície de xarxa.

![Moodle ](https://user-images.githubusercontent.com/114162326/206173667-4177f795-a197-43b5-bc8b-8b7a2e05b02e.png)
![Moodle AP](https://user-images.githubusercontent.com/114162326/206173683-1abf05ea-677e-4696-8b0e-ad067003cb16.png)

### SSH

Per a poder posar les comandes d'una manera més còmoda, el que he fet ha sigut connectar-me per SSH a la màquina virtual amb l'Ubuntu server.

```
ssh (nom_de_usuari)@(Ip_de_la_maquina)
```
![ssh 1](https://user-images.githubusercontent.com/114162326/206188967-fe294b30-9aaa-48d5-817b-ca216dcab6ec.png)

Tot seguit em demanara la contraseña.
![ssh 2](https://user-images.githubusercontent.com/114162326/206189565-8a8a1ba9-233b-4751-ac94-adee0f833205.png)

### Actualització dels paquets d'Ubuntu.

Primer que tot el que he fet a sigut actualitzar el paquets d'Ubuntu, per a no tenir cap problema a l'hora de instal·lar tot el que necessitem per al Moodle.

```
sudo apt-get update
```
![Install Apache 1](https://user-images.githubusercontent.com/114162326/206176671-352e0ae1-800c-4780-9942-cbac741730f9.png)

### Instal·lació Apache 2

Després d'actualitzar els paquets he instal·lat el servidor Apache 2 amb la següent comanda.

```
sudo apt-get install apache2
```
![Install apache 2](https://user-images.githubusercontent.com/114162326/206177895-39b2bdea-d2ca-41ff-a02b-0800cbc51b9d.png)

### Instal·lació de MariaDB

Una vegada instal·lat el servidor Apache 2, el que he fet ha sigut instal·lar la base de dades MariaDB, amb la següent comanda.

```
sudo apt-get install mariadb-server
```
![Instal Mariadb 1](https://user-images.githubusercontent.com/114162326/206178703-6ff0ffcb-bd39-4ec1-afbf-3fc72ff0a888.png)

Una vegada instal·lada la base de dades he executat la configuració de seguretat amb la següent comanda.

```
sudo mysql_secure_installation
```
![Install Mariadb 2](https://user-images.githubusercontent.com/114162326/206179117-80b01099-4cdc-4edb-9772-26ef55f71706.png)

### Instal·lació PHP7.3

Per a instal·lar PHP7.3 he utilitzat les següents comandes.

```
sudo apt-get install software-properties-common
```
![Install PHP 1](https://user-images.githubusercontent.com/114162326/206179818-155a796a-af83-400b-9e9a-4f353f36e2af.png)

```
sudo add-apt-repository ppa:ondrej/php
```
![Install PHP 2](https://user-images.githubusercontent.com/114162326/206180643-55258b40-4a46-4139-8f9f-86c25b7dc58a.png)

```
sudo apt-get update
```
![Install PHP 3](https://user-images.githubusercontent.com/114162326/206181151-8bdeeb80-84ba-40b1-bc67-9ff2475cf6a6.png)

```
sudo aptr-get install -y php7.3
```
![Install PHP4](https://user-images.githubusercontent.com/114162326/206181273-ac60b748-8dd9-48f1-8c57-ab83d4037e9d.png)

### Instal·lació Moodle


