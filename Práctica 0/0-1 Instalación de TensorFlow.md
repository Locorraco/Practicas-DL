# Instrucciones para instalar las cosas

## Instalación de Anaconda
Para este curso es necesario utilizar Anaconda para trabajar con ambientes de python. Descargalo de la página oficial de [Anaconda](https://www.anaconda.com/). Sigue las instrucciones correspondientes para instalarlo en el SO con que trabajarás..

## Instalación de TensorFlow
TensorFlow es muy sencillo de instalar usando Anaconda. Es soportado en la versión de 64-bits de Windows 7 o superior, en la versión de 64-bits Ubuntu Linux 14.04 o superior y en la versión de macOS 10.10 o superior.

1.En Windows debes abrir la aplicación Anaconda Command Prompt, instalada junto a Anaconda. En macOS o Linux es suficiente con abrir una terminal de bash.

2.Elija el nombre de su entorno de TensorFlow. Se recomienda un nombre sencillo y fácil de recordar para facilitar el acceso constante que se tendra al entorno/ambiente.

3. Para instalar la versión actual de TensorFlow solo para CPU usa el siguiente comando
```bash
conda create -n nombre_del_ambiente tensorflow
conda activate nombre_del_ambiente
```

O bien, si cuentas con una tarjeta de video dedicada o GPU, instala la versión actual de TensorFlow GPU para Windows o Linux
```bash
conda create -n nombre_del_ambiente tensorflow-gpu
conda activate nombre_del_ambiente
```
