# Instrucciones para instalar las cosas

## Instalación de Anaconda
Para este curso es necesario utilizar Anaconda para trabajar con ambientes de python. Descargalo de la página oficial de [Anaconda](https://www.anaconda.com/). Sigue las instrucciones correspondientes para instalarlo en el SO con que trabajarás..

## Instalación de TensorFlow
TensorFlow es muy sencillo de instalar usando Anaconda. Es soportado en la versión de 64-bits de Windows 7 o superior, en la versión de 64-bits Ubuntu Linux 14.04 o superior y en la versión de macOS 10.10 o superior.

1. En Windows debes abrir la aplicación Anaconda Command Prompt, instalada junto a Anaconda. En macOS o Linux es suficiente con abrir una terminal de bash.

2. Elija el nombre de su entorno de TensorFlow. Se recomienda un nombre sencillo y fácil de recordar para facilitar el acceso constante que se tendra al entorno/ambiente.

3. Para instalar la versión actual de TensorFlow solo para:

### a.- GPU

```bash
conda create -n nombre_del_ambiente python=3.9.12 ipython
conda activate nombre_del_ambiente
conda install -c conda-forge cudatoolkit=11.2 cudnn=8.1.0
pip install --upgrade pip
pip install tensorflow
```

Y prueba la instalación ejecutando

```bash
ipython -c "import tensorflow as tf; print(tf.config.list_physical_devices('GPU'))"
```
Si regresa una lista de dispositivos GPU, la instalación a sido exitosa. 

### b.- CPU
```bash
conda create -n nombre_del_ambiente python=3.9.12 ipython
conda activate nombre_del_ambiente
pip install --upgrade pip
pip install tensorflow-cpu
```

Y prueba la instalación ejecutando

```bash
ipython -c "import tensorflow as tf; print(tf.reduce_sum(tf.random.normal([1000, 1000])))"
```
Si regresa un tensor, la instalación a sido exitosa. 

4. Una vez dentro del ambiente, es necesario instalar las siguientes librerías
```bash
pip install -U scikit-learn		#Librería para el análisis de datos predictivo
pip install -U matplotlib		#Librería para trabajar con datos y estadísticas
pip install split-folders		#Librería para separar folders con archivos en train, test y validation
pip install opencv-python		#Librería de visión artificial
pip install jupyterlab			#Es el enviroment para notebooks para poder trabajar 
pip install seaborn			#Librería para el manejo de gráficas y análisis de datos
pip install pandas			#Librería para el manejo y análisis de estructuras de datos
pip install scipy			#Librería para el análisis de lenguaje
python -m spacy download en --user	#Complemento de Spacy para el análisis del idioma Inglés
pip install tqdm			#Barra de progreso para visualizar el entrenamiento de las redes
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

Debería imprimir `2.9.2` o una versión superior.
