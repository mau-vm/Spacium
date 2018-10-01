El siguiente documento es el proyecto realizado para la Semana i por parte del equipo de Spacium basado en el trabajo realizado por: 
Jonathan Huang, github: jch1
Vivek Rathod, github: tombstone
Ronny Votel, github: ronnyvotel
Derek Chow, github: derekjchow
Chen Sun, github: jesu9
Menglong Zhu, github: dreamdragon
Alireza Fathi, github: afathi3
Zhichao Lu, github: pkulzc. 
Descarga: https://github.com/tensorflow/models

y seguimos la guía de los tutoriales impartidos por el usuario de youtube sentdex. 
Pagina:https://pythonprogramming.net/introduction-use-tensorflow-object-detection-api-tutorial/

Descripcion: Es un sistema de visión por computador que detecta la cantidad de espacios disponibles en una oficina o salón. Si desea conocer mas puede leer nuestro archivo de PowerPoint "SPACIUM.pptx" o "Spacium.pdf".

Setup:
Descargar anaconda para python 3.6 y las siguientes dependecias.

Dependencias:
TensorFlow
pillow
lxml
jupyter
matplotlib

En windows: 

Paso 1
De los archivos descargados de github debemos asegurarnos que en la carpeta bin se encuentra el archivo "protoc.exe". Si no se encuentra entonces descargar protoc-3.4.0-win32.zip de https://github.com/protocolbuffers/protobuf/releases y extraerlo en la carpeta donde se encuentra nuestra carpeta "object_detection". 
Abrir la terminal en la carpeta local donde guardo nuestra carpeta "object_detection", en mi caso "C:\Users\PROPIETARIO\Documents\10_Semestre\Semanai\proyecto" y desde aquí ejecutaremos el archivo protoc.exe, por lo que deberemos referenciar a su ubicacion y ejecutar el siguiente comando "protoc object_detection/protos/*.proto --python_out=." en mi caso el terminal debe verse asi (solo es necesario hacer este paso la primera vez):

C:\Users\PROPIETARIO\Documents\10_Semestre\Semanai\proyecto> C:\Users\PROPIETARIO\Documents\10_Semestre\Semanai\proyecto\bin\protoc object_detection/protos/*.proto --python_out=.

Paso 2
Una vez realizado lo anterior, podemos ejecutar directamente nuestro archivo. Inicie el prompt de anaconda desde adentro de la carpeta "object_detection" y ejecuta el siguiente comando "python object_detection_tutorial_CONVERTED.py" y en seguida la aplicacion empieza a cargarse y despues de unos minutos estara en acción.
Mi caso:
C:\Users\PROPIETARIO\Documents\10_Semestre\Semanai\proyecto\object_detection> python object_detection_tutorial_CONVERTED.py

Nota: Si desea cambiar de la camara incorporada en su laptop a una externa, antes de realizar el paso 2. Deberá abrir el archivo "object_detection_tutorial_CONVERTED.py" en cualquier editor de texto y cambiar la linea de codigo "cap = cv2.VideoCapture(0)" por "cap = cv2.VideoCapture(1)", guardarlo y ejecutarlo como se menciona en el paso 2. La cantidad de sillas es un valor fijo (en ese caso es 2), por lo que siguiendo el mismo lineamiento marcado al inicio de esta nota, cambiaremos el valor de la variable "numSillas" en el archivo "object_detection_tutorial_CONVERTED.py", guardamos el cambio y podemos ejecutar el paso 2.
