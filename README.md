El siguiente documento es el proyecto realizado para la Semana i por parte del equipo de Spacium. Es un sistema de vision por coputador que detecta la cantidad de espacios disponibles en una oficina o salón.

Setup:
Descargar anaconda para python 3.6 y las siguientes dependecias.

Dependencias:
TensorFlow
pillow
lxml
jupyter
matplotlib

En windows: 
Descargar protoc-3.4.0-win32.zip de https://github.com/protocolbuffers/protobuf/releases y extraerlo en la carpeta donde se encuentra nuestra carpeta "object_detection". De los archivos extraidos debemos asegurarnos que en la carpeta bin se encuentra el archivo "protoc.exe".
Abrir la terminal en la carpeta local donde guardo nuestra carpeta object_detection, en mi caso "C:\Users\PROPIETARIO\Documents\10_Semestre\Semanai\proyecto" y desde aquí ejecutaremos el archivo protoc.exe, por lo que deberemos referenciar a su ubicacion y ejecutar el siguiente comando "protoc object_detection/protos/*.proto --python_out=." en mi caso debe verse asi el terminal (solo es necesario hacer este paso la primera vez):

C:\Users\PROPIETARIO\Documents\10_Semestre\Semanai\proyecto> C:\Users\PROPIETARIO\Documents\10_Semestre\Semanai\proyecto\bin\protoc object_detection/protos/*.proto --python_out=.

Una vez realizado este paso, podemos ejecutar directamente nuestro archivo. Inicie el prompt de anaconda desde adentro de la carpeta "object_detection" y ejecuta el siguiente comando "python object_detection_tutorial_CONVERTED.py" y en seguida la aplicacion empieza a ejecutarse y despues de unos minutos estara en acción.
Mi caso:
C:\Users\PROPIETARIO\Documents\10_Semestre\Semanai\proyecto\object_detection> python object_detection_tutorial_CONVERTED.py

Nota: Si desea cambiar de la camara incorporada en su laptop a una externa, antes de correr el archivo "object_detection_tutorial_CONVERTED.py" debera abrirlo en cualquier editor de texto y cambiar la linea de codigo "cap = cv2.VideoCapture(0)" por "cap = cv2.VideoCapture(1)", guardarlo y ejecutarlo como se mencionó anteriormente.