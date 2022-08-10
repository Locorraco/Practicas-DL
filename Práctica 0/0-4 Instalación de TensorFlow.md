# Instrucciones para instalar las cosas

## Instalación de Anaconda
Para este curso es necesario utilizar Anaconda para trabajar con ambientes de python. Descargalo de la página oficial de [Anaconda](https://www.anaconda.com/). Sigue las instrucciones correspondientes para instalarlo en el SO con que trabajarás..

## Instalación de TensorFlow
TensorFlow es muy sencillo de instalar usando Anaconda. Es soportado en la versión de 64-bits de Windows 7 o superior, en la versión de 64-bits Ubuntu Linux 14.04 o superior y en la versión de macOS 10.10 o superior.

1. En Windows debes abrir la aplicación Anaconda Command Prompt, instalada junto a Anaconda. En macOS o Linux es suficiente con abrir una terminal de bash.

2. Elija el nombre de su entorno de TensorFlow. Se recomienda un nombre sencillo y fácil de recordar para facilitar el acceso constante que se tendra al entorno/ambiente.

3. Para instalar la versión actual de TensorFlow solo para CPU usa el siguiente comando
```bash
conda create -n nombre_del_ambiente tensorflow python=3.9.12 ipython
conda activate nombre_del_ambiente
```

O bien, si cuentas con una tarjeta de video dedicada o GPU, instala la versión actual de TensorFlow GPU para Windows o Linux
```bash
conda create -n nombre_del_ambiente tensorflow-gpu python=3.9.12 ipython
conda activate nombre_del_ambiente
```

Una vez dentro del ambiente, es necesario instalar las siguientes librerías
```bash
conda install -c conda-forge jupyterlab --yes 	#Es el enviroment para notebooks para poder trabajar
conda install -c conda-forge matplotlib --yes 	#Librería para trabajar con datos y estadísticas
conda install -c conda-forge opencv --yes	#Librería de visión artificial 
conda install -c conda-forge keras --yes	#Librería de Redes Neuronales que se ejecuta sobre TensorFlow
conda install -c conda-forge spacy --yes	#Librería para el análisis de lenguaje
conda install -c conda-forge tqdm --yes		#Barra de progreso para visualizar el entrenamiento de las redes
conda install -c anaconda scikit-learn --yes	#Librería para el análisis de datos predictivo
conda install -c anaconda seaborn --yes		#Librería para el manejo de gráficas y análisis de datos
conda install -c anaconda pandas --yes		#Librería para el manejo y análisis de estructuras de datos
conda install -c anaconda numpy	--yes		#Librería para crear vectores y matrices multidimencionaes
python -m spacy download en --user		#Complemento de Spacy para el análisis del idioma Inglés
```

Para corroborar las versiones y mantener todos los paquetes al día se debe de ejecutar el siguiente comando:

```bash
conda update --all
```

Para abrir Jupyter es necesario ejecutar el comando:

```bash
jupyter-lab
```

Abrirá el manejador de libretas (o notebooks). Para probar que todo funcione, crea un nuevo notebook y escribe:

```bash
import tensorflow as tf 
print(tf.__version__)
```

Debería imprimir `2.6.0`.
