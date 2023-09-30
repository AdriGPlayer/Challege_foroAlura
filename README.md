# Challege_foroAlura
Este repositorio contiene el código fuente de un proyecto de backend que replica el funcionamiento del Foro Alura. El proyecto se enfoca en la creación de una API REST utilizando el framework Spring. A través de esta API, los usuarios pueden realizar operaciones de creación, lectura, actualización y eliminación de tópicos. Este conjunto de operaciones es comúnmente conocido como CRUD (Create, Read, Update, Delete).

Descripción del Proyecto
El Foro Alura es un lugar donde los alumnos de la plataforma Alura pueden plantear preguntas y discutir temas relacionados con los cursos ofrecidos. El foro fomenta la colaboración entre alumnos, profesores y moderadores y se utiliza para intercambiar conocimientos y resolver dudas.

El objetivo de este proyecto es replicar el funcionamiento del foro a nivel de backend. Esto implica la creación de una API REST que gestionará la creación, recuperación, actualización y eliminación de tópicos. Además, se aplicarán validaciones de acuerdo con las reglas de negocio y se utilizará una base de datos para la persistencia de la información.

Tecnologías Utilizadas
•	Spring Framework: Este proyecto utiliza el framework Spring para desarrollar la API REST. Spring proporciona una amplia gama de herramientas y bibliotecas que facilitan el desarrollo de aplicaciones Java.
•	Base de Datos: Se utiliza una base de datos para almacenar y gestionar la información relacionada con los tópicos y los usuarios en mysql.
•	Insomniac: Para realizar consultas HTTP a través de la API, se ha utilizado la biblioteca Insomniac, que facilita la comunicación con el backend.


Funcionalidades
La API REST desarrollada en este proyecto proporciona las siguientes funcionalidades:
1.	Crear un nuevo tópico: Los usuarios pueden crear nuevos tópicos, especificando detalles como el título, el contenido y el autor.
2.	Mostrar todos los tópicos creados: Se puede acceder a una lista de todos los tópicos existentes en el sistema.
3.	Mostrar un tópico específico: Los usuarios pueden recuperar información detallada sobre un tópico específico proporcionando su identificador único.
4.	Actualizar un tópico: Se permite la actualización de un tópico existente, lo que incluye la modificación del título y el contenido.
5.	Eliminar un tópico: Los usuarios pueden eliminar un tópico existente del sistema.

Configuración y Uso
A continuación, se describen los pasos básicos para configurar y utilizar este proyecto:
1.	Clonar el Repositorio: Clone este repositorio en su máquina local utilizando el comando:
bashCopy code.
git clone https://github.com/tu-usuario/Challege_foroAlura.git 
2.	Configurar la Base de Datos: Primero que nada hay que ejecutar el programa para que cree la base de datos y las tablas, una vez creada la las base de datos se deberá acceder a ella desde su administrador de bases de datos favoritos, acceder a la tabla de usuarios y debes crear un usuario desde insertar:


![image](https://github.com/AdriGPlayer/Challege_foroAlura/assets/130609122/52c1de51-275f-4156-ac3b-95ff6a552253)

Crea un nombre de usuario de tu preferencia, en mi caso use “Adrian”
Para la contraseña deberás usar la pagina https://www.browserling.com/tools/bcrypt
Para encriptar la contraseña, escribe tu contraseña en el cuadro “Password” y dar click en Bcrypt y copiar el resultado y pegarlo la contraseña de la tabla del usuario que estas creando.

![image](https://github.com/AdriGPlayer/Challege_foroAlura/assets/130609122/c1e2de71-548d-4b74-8ff9-6af480213c33)
.
![image](https://github.com/AdriGPlayer/Challege_foroAlura/assets/130609122/593e2fc1-909a-41d2-b65e-53b14bce6b21)
En email puedes poner el de tu preferencia, y en activo deberás ingresar el número 1, asi indicaremos que el usuario esta activo.

3.	Ejecutar la Aplicación: Ejecute la aplicación Spring para iniciar la API REST. Asegúrese de que la configuración de la base de datos sea correcta.
4.	Realizar Consultas HTTP: Utilice Insomniac u otra herramienta similar para realizar consultas HTTP a las rutas implementadas por la API.

Hagamos un ejemplo creando un curso y tópico 
Primero deberás descargar el archivo de insomiac que contendrá las consultas http
Importarlo en Insomiac y listo.
Ahora vamos a la consulta Login usuario y en el JSON deberás ingresar tu nombre de usuario y la contraseña sin encriptar.
Y dar clic en Send, lo que te dara como resultado un token que deberas copiar.

![image](https://github.com/AdriGPlayer/Challege_foroAlura/assets/130609122/3cdf4985-da41-4147-aee7-2f2830ba950f)
Ese token lo deberas pegar en cada petición que se quiera hacer, en la parte de Auth, Bearer Token y pegar el token en “Token”.
![image](https://github.com/AdriGPlayer/Challege_foroAlura/assets/130609122/b1a0a1d1-2a19-49e3-9a00-92eca4d1a043)
Ahora en JSON podemos crear un curso con el nombre y la categoría.
![image](https://github.com/AdriGPlayer/Challege_foroAlura/assets/130609122/b6eda06c-bb58-4c80-a4b8-ef5e72d2ad47)

Dar click en botón send y debería aparecer algo asi con el código 201.
![image](https://github.com/AdriGPlayer/Challege_foroAlura/assets/130609122/85afd0b9-4d50-4110-a960-da97c35d304b)

Si revisamos la base de datos:
![image](https://github.com/AdriGPlayer/Challege_foroAlura/assets/130609122/792b8e0f-6daa-4eb8-a740-485f045fdad0)
Vamos a listar los cursos en el servidor, si es de tu preferencia puedes crear más cursos.
![image](https://github.com/AdriGPlayer/Challege_foroAlura/assets/130609122/37a6b867-096b-48a4-b506-0e279f16d093)
Ahora vamos a crear un tópico en el curso de java.
![image](https://github.com/AdriGPlayer/Challege_foroAlura/assets/130609122/9a58ed76-c490-4edf-9bc3-1510c184faca)

Listo si deseas explorar todas las peticiones puedes hacerlo con el mismo prodecimiento, te invitamos a crear una respuesta para un tópico y visualizar los datos con los métodos GET

Contribución
Si desea contribuir al desarrollo de este proyecto, le invitamos a enviar pull requests y a participar en el proceso de desarrollo.
