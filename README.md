<h1 align="center"> Renta de Carros</h1>


Calzada Torres Victor

Ensayo de modelo-vista-controlador de una aplicación web en PHP.

Instituto Tecnológico Nacional de México Campus Tláhuac I.

Ingeniería en Sistemas Computacionales.

Grupo 8S2.		Programación PHP con MVC.

21 de marzo de 2024.
_____________________________________________________________________________________

<h1 align="center"> Indice</h1>

Resumen                                                        	

Introducción	                                                   

Desarrollo	                                                     

El Modelo-Vista-Controlador (MVC)                              

Diagrama de clases                                             

Catálogo de vehículos                                        

Descripción de código php para el archivo cars.php             

Listados de propiedades	                                        

Descripción del código php para el archivo propiedades.php.	    

Galería de imágenes e Información detallada:                   	

Descripción para el código del archivo publicación.php.        	

Formulario de contacto:	                                        

Descripción para el código del archivo contacto.php.	           

Gestión de Propiedades.                                        	

Descripción para el código del archivo index.php del administrador de propiedades.	

Conclusiones	                                                   

Referencias                                                     
___________________________________________________________________
<h1 align="center"> Resumen</h1>

Este ensayo analiza el diseño de una página web dedicada a la renta de automóviles, destacando su importancia en la experiencia del usuario y su impacto en el exito del negocio. En este ensayo se explorara cómo elementos de la navegacion intuitiva, con un diseño responsivo y la presentacion clara de la informacion que haga que influya en la eficiencia del proyecto, asi se podra atraer y retener clientes. Además, se examina la integracion de caracteristicas especiales que generan confianza, opciones de personalizacion y herramientas de soporte para un buen manejo de usabilidad y satisfaccion hacia el usuario.

se integra una estrategia de diseño en cuanto la accesibilidad, seguridad y confianza para garantizar una experiencia positiva hacia el usuario y el cliente comprometiendolo al mercado de renta de vehiculos.
-_____________________________________________________________________
<h1 align="center"> Introducción</h1>

En el mundo actual, la presencia en línea se ha vuelto indispensable para cualquier negocio que busque alcanzar su máximo potencial y llegar a una audiencia más amplia. En este contexto, la creación de una página web para un servicio de renta de autos se presenta como una estrategia fundamental para posicionarse en el mercado y ofrecer una experiencia completa y accesible a los clientes.
El propósito de este documento es introducir el proyecto de desarrollo de una página web para nuestro servicio de renta de autos, utilizando el modelo MVC (Modelo-Vista-Controlador) con PHP. Exploraremos los fundamentos de este modelo arquitectónico y cómo aplicarlo de manera efectiva para crear una plataforma web dinámica, robusta y fácil de mantener.
A lo largo de este documento, examinaremos las razones por las cuales optamos por el modelo MVC para nuestro proyecto, sus ventajas y beneficios en términos de estructura, modularidad y mantenimiento del código. Además, describiremos los componentes clave de nuestro servicio de renta de autos y cómo serán implementados dentro del modelo MVC.
En última instancia, este documento servirá como guía inicial para el desarrollo de nuestra página web, proporcionando una visión general del enfoque metodológico y las herramientas tecnológicas que utilizaremos para llevar a cabo este emocionante proyecto.

------------------------------------------------------------------------
<h1 align="center"> Instalacion</h1>

Este trabajo se ejecuta bajo el servidor local XAMMP, este servidor maneja un servidor local con la utilizacion del puertos del mismo sistema esto para la ejecucion de archivos php, integra MySql para la gestion de Base de datos.

![Captura de pantalla 2024-04-25 184236](https://github.com/Vicalzada/RentaDeCarros/assets/167146583/d08f53d8-75f8-4795-bc90-8c5db87d2a7a)
Figura 1. Xammp en ejecucuion


La pagina web trabaja en conjunto a composer, que es una dependencia que se encarga de realizar las tareas de instalacion de las carpetas, el repositorio ya tiene los archivos requeridos para que trabaje completamente.

en caso de que no se ejecute hay que instalar composer
comparto la pagina de descarga 
https://getcomposer.org/download/

![Captura de pantalla 2024-05-02 152330](https://github.com/Vicalzada/RentaDeCarros/assets/167146583/5e694bed-2908-4223-bd12-7ef9a0999b6a)

Ya una vez descargado el paquete de instalacion se da doble clic sobre el instalador y se ejecutara:

![Captura de pantalla 2024-05-02 152423](https://github.com/Vicalzada/RentaDeCarros/assets/167146583/936d580a-f473-4ea9-9a27-d75e90ffa477)

se instala por defecto en nuestro PHP:
![Captura de pantalla 2024-05-02 152605](https://github.com/Vicalzada/RentaDeCarros/assets/167146583/5079473b-a168-4b78-bada-f7660ec88587)


Presionamos siguente y continua con la instalacion:
![Captura de pantalla 2024-05-02 152555](https://github.com/Vicalzada/RentaDeCarros/assets/167146583/157bd8c7-df53-404b-b4f2-e75822f42754)

Ahora descargamos nuestro proyecto, descomprimimos en la carpeta de xampp>htdocs>rentacar

![Captura de pantalla 2024-05-02 152906](https://github.com/Vicalzada/RentaDeCarros/assets/167146583/d51af779-f6b2-4ba4-b78d-3b3765679e7f)

ahora en la url tecleamos CMD:

![Captura de pantalla 2024-05-02 152959](https://github.com/Vicalzada/RentaDeCarros/assets/167146583/789b3d71-1a3c-4e32-a31a-7dc642ead321)


Esto se instala dentro de la ubicacion del proyecto: con el comando: composer install
![Captura de pantalla 2024-04-25 173115](https://github.com/Vicalzada/RentaDeCarros/assets/167146583/e0571adb-3022-4d35-95f1-2452fced7f40)

esto inicializara la descarga dentro la carpeta del proyecto y creara la carpeta ventor.

En esta parte esta arroja una advertencia que seria por una extencion de php, para esto nos dirijimos a xampp y presionamos el boton de config y luego al PHP(php.ini)

![Captura de pantalla 2024-05-02 153335](https://github.com/Vicalzada/RentaDeCarros/assets/167146583/e8474123-693e-44b0-96b3-8d50de681ab3)

nos abrira un bloc de notas y aqui debemos buscar esta extencion gd
![Captura de pantalla 2024-05-02 153412](https://github.com/Vicalzada/RentaDeCarros/assets/167146583/2fb58294-fe4b-42d0-a194-4093ce6a86e3)

una vez ubicada la etencion = gd le quitamos los ; del principio
![Captura de pantalla 2024-05-02 153524](https://github.com/Vicalzada/RentaDeCarros/assets/167146583/bd474182-73d7-4ba4-b406-3142a56af30f)

de la misma manera buscamos la extencion zip y procedemos a quitar el ; de la extencion y listo procedemos a cerrar el archivo no sin antes guardar los cambios.

![Captura de pantalla 2024-05-02 153625](https://github.com/Vicalzada/RentaDeCarros/assets/167146583/247d5eec-9854-49b2-abe6-4ca182fc3ad9)

procedemos nuevamente a instalar el composer pero esta vez con el comando comando:composer update
y quedaria de esta manera.

![Captura de pantalla 2024-04-25 173100](https://github.com/Vicalzada/RentaDeCarros/assets/167146583/db4bde73-4a5d-4370-812e-f03e9c8a95f3)

Quizas aparesca del siguiente modo, sin estilos:

![Captura de pantalla 2024-05-02 154233](https://github.com/Vicalzada/RentaDeCarros/assets/167146583/f96dd2ed-87e3-4b19-9cdb-ca1c471d79a2)

ahora lo que se debe realizar es tomar el url del proyecto 
![Captura de pantalla 2024-05-02 154325](https://github.com/Vicalzada/RentaDeCarros/assets/167146583/06a082b6-56e0-41ee-bc32-47b210f62123)


ahora nos dirijimos al directorio config y abrimos el archivo config en un bloc de notas: 

![Captura de pantalla 2024-05-02 154450](https://github.com/Vicalzada/RentaDeCarros/assets/167146583/c0597bc4-949c-4332-8cdd-cccbccad3ba0)

y en el url colocamos la direccion copiada, es preciso mensionar que debe terminar con una diagonal:

![Captura de pantalla 2024-05-02 154609](https://github.com/Vicalzada/RentaDeCarros/assets/167146583/2e06a1b9-eaed-44a7-aa12-2d0b5c0e875e)


guardamos y actualizamos el archivo, y ya se podra ejecutar correctamente con los estilos:

![Captura de pantalla 2024-05-02 154738](https://github.com/Vicalzada/RentaDeCarros/assets/167146583/787ac109-286a-4fee-9283-387d9ec1f873)



<h1 align="center"> Desarrollo </h1>

Se crear una página web sobre renta de carros es una inversión importante que puede ayudar a aumentar la visibilidad en línea, generar clientes potenciales, proporcionar información detallada, facilitar reservas en línea, ofrecer atención al cliente y servir como una poderosa herramienta de marketing para hacer crecer tu negocio de renta de carros.

El Modelo-Vista-Controlador (MVC) 
El modelo, vista y controlador es un patrón de diseño de software que separa la lógica de negocios de su visualización. Se utiliza para implementar interfaces de usuario, datos y lógica de control.
En este proyecto se estructura de la siguiente manera, donde muestra en una estructura MVC y se guardan los archivos correspondientes.

![Captura de pantalla 2024-04-24 220913](https://github.com/Vicalzada/RentaDeCarros/assets/167146583/45397b45-e3d5-49e2-8270-a3709dbbe978)

 
Dentro de la carpeta controlador.
Se encuentran las carpetas y archivos que dan la instrucción de manejo de los archivos php.

 ![Captura de pantalla 2024-04-24 210259](https://github.com/Vicalzada/RentaDeCarros/assets/167146583/11615348-705e-4da6-9983-97f34d3158c4)

Dentro de la carpeta modelo.
Se encuentran los archivos que dan la instrucción de conexiones entre el controlador y el modelo de los archivos php.

 
![Captura de pantalla 2024-04-24 210324](https://github.com/Vicalzada/RentaDeCarros/assets/167146583/e89b7c17-cbce-4e1d-a2ce-dc002d1eec25)

Dentro de la vista
Se encuentran los archivos que dan la vista la cual se mostrara dentro del navegador web.
 ![Captura de pantalla 2024-04-24 210353](https://github.com/Vicalzada/RentaDeCarros/assets/167146583/be5b241a-a115-422f-8bf7-681cd974379c)

Diagrama de clases
 
![Captura de pantalla 2024-04-24 210510](https://github.com/Vicalzada/RentaDeCarros/assets/167146583/c2b70797-dc04-46b2-99d9-2bf69eedb5c5)


Las funcionalidades principales para una página web de renta de carros
Al desarrollar un proyecto web para una página de inmobiliaria, es esencial incluir una serie de funcionalidades específicas para brindar una experiencia completa a los usuarios. Aquí se muestran las funcionalidades principales que debería tener este tipo de proyecto.
Para una página web de renta de carros, algunas funcionalidades principales que deberían considerarse son:
Catálogo de vehículos


 ![Captura de pantalla 2024-04-24 210826](https://github.com/Vicalzada/RentaDeCarros/assets/167146583/d825b865-04f8-4cd4-802e-54de6caec339)


Mostrar una lista completa y detallada de los vehículos disponibles para renta, incluyendo imágenes, especificaciones técnicas, características destacadas y disponibilidad.


Descripción de código php para el archivo cars.php

 ![Captura de pantalla 2024-04-24 210940](https://github.com/Vicalzada/RentaDeCarros/assets/167146583/f2ba7781-85e2-4f32-b269-97d1c43f53ca)

Este código PHP define una clase llamada Cars que actúa como controlador en una aplicación web. Aquí está lo que hace cada parte del código:
La classe Cars extends Controller: Define una clase llamada Cars que hereda de la clase Controller. Esto sugiere que el controlador está utilizando algún tipo de patrón de diseño MVC (Modelo-Vista-Controlador).

public function __construct() {...}: Define el constructor de la clase Cars. Este constructor inicia una sesión PHP con session_start() y luego llama al constructor de la clase padre con parent::__construct(). Esto indica que la clase padre (Controller) realiza algunas tareas de inicialización importantes.

public function index() {...}: Define un método llamado Index(), que es el controlador para la página principal de la sección de vehículos. Dentro de este método, se define un array asociativo llamado $data que contiene algunas variables como active, title, detail y vehiculos. Luego, se llama a un método getVehiculos() del modelo (asumiendo que $this->model es una instancia del modelo asociado) para obtener una lista de vehículos, y finalmente se llama al método getView() para renderizar la vista de la página de vehículos (cars.php) pasando el array $data.

public function single($valor) {...}: Define un método llamado single() que toma un parámetro $valor. Este método es responsable de mostrar los detalles de un vehículo específico. Dentro del método, se obtiene el ID del vehículo del parámetro $valor, luego se llama al método getVehiculo() del modelo para obtener los detalles de ese vehículo en particular. 

Finalmente, se renderiza la vista de la página de detalles del vehículo (car-single.php) pasando los detalles del vehículo como datos.


Tarifas

 

Proporcionar herramientas para que los clientes puedan calcular las tarifas de alquiler de forma transparente, incluyendo costos adicionales como seguros, impuestos y cargos por servicios extras. 

 ![Captura de pantalla 2024-04-24 213725](https://github.com/Vicalzada/RentaDeCarros/assets/167146583/224038f5-acdc-42e7-a43d-111c99ef0146)


Descripción del código php para el archivo pricing.php.

![Captura de pantalla 2024-04-24 213951](https://github.com/Vicalzada/RentaDeCarros/assets/167146583/a3584647-c7b4-4f3e-a7bd-b12d22f60faa)

Este código PHP define una clase llamada Pricing que actúa como controlador en una aplicación web. Aquí está lo que hace cada parte del código:
class Pricing extends Controller: Define una clase llamada Pricing que hereda de la clase Controller. Esto sugiere que el controlador está utilizando algún tipo de patrón de diseño MVC (Modelo-Vista-Controlador).
public function __construct() {...}: Define el constructor de la clase Pricing. Este constructor inicia una sesión PHP con session_start() y luego llama al constructor de la clase padre con parent::__construct(). Esto indica que la clase padre (Controller) realiza algunas tareas de inicialización importantes.
public function index() {...}: Define un método llamado index(), que es el controlador para la página principal de la sección de precios. Dentro de este método, se define un array asociativo llamado $data que contiene algunas variables como active, title, detail y vehiculos. Luego, se llama a un método getVehiculos() del modelo (asumiendo que $this->model es una instancia del modelo asociado) para obtener una lista de vehículos con precios específicos. Finalmente, se llama al método getView() para renderizar la vista de la página de precios (pricing.php) pasando el array $data.
En resumen, este código PHP define un controlador para la sección de precios de la aplicación web. El controlador se encarga de cargar los datos necesarios desde el modelo y renderizar la vista correspondiente para mostrar los precios de los vehículos disponibles.

Gestión de cuentas de usuario:
![Captura de pantalla 2024-04-24 214444](https://github.com/Vicalzada/RentaDeCarros/assets/167146583/0e0904d2-b087-411d-894c-e2ea31b76a2a)

 Permitir a los clientes registrarse, iniciar sesión y administrar sus cuentas de usuario, incluyendo el historial de reservas, preferencias de contacto y datos de facturación.

 
Descripción para el código del archivo login.php.

 ![Captura de pantalla 2024-04-24 214603](https://github.com/Vicalzada/RentaDeCarros/assets/167146583/f2ff879c-44da-4176-a9c3-4885b86dc4c0)


Este código PHP define una clase llamada Login que actúa como controlador en una aplicación web. Aquí está lo que hace cada parte del código:
class Login extends Controller: Define una clase llamada Login que hereda de la clase Controller. Esto sugiere que el controlador está utilizando algún tipo de patrón de diseño MVC (Modelo-Vista-Controlador).
public function __construct() {...}: Define el constructor de la clase Login. Este constructor inicia una sesión PHP con session_start() y luego llama al constructor de la clase padre con parent::__construct(). Esto indica que la clase padre (Controller) realiza algunas tareas de inicialización importantes.
public function index() {...}: Define un método llamado index(), que es el controlador para la página principal de inicio de sesión. Dentro de este método, se define un array asociativo llamado $data que contiene una variable title con el valor "Login". Luego, se llama al método getView() para renderizar la vista de la página de inicio de sesión (login.php) pasando el array $data.
public function validar() {...}: Define un método llamado validar() que se encarga de validar las credenciales de inicio de sesión enviadas a través del formulario de inicio de sesión. Dentro de este método, se obtienen los datos enviados por POST (usuario, clave y rol) y se limpian con la función strClean(). Luego, se verifica si los campos están vacíos. Si no lo están, se realiza una consulta al modelo para verificar las credenciales en la tabla correspondiente (usuarios o clientes). Si las credenciales son válidas, se inicia sesión estableciendo las variables de sesión apropiadas y se devuelve un mensaje de éxito en formato JSON. Si las credenciales son incorrectas, se devuelve un mensaje de error.
En resumen, este código PHP define un controlador para la página de inicio de sesión de una aplicación web. El controlador se encarga de renderizar la vista de inicio de sesión y de validar las credenciales de inicio de sesión proporcionadas por el usuario.
Formulario de contacto: 
Muestra un formulario de contacto para que los usuarios interesados puedan comunicarse con la empresa.

 
Un formulario de contacto en una página web sirve para proporcionar a los visitantes un medio fácil y conveniente para comunicarse con el propietario del sitio web, el equipo de soporte o cualquier otro contacto relevante.


![Captura de pantalla 2024-04-24 214853](https://github.com/Vicalzada/RentaDeCarros/assets/167146583/0bd6e39e-6587-4a19-b252-fdc40346a6c8)






Descripción para el código del archivo contact.php.

 ![Captura de pantalla 2024-04-24 215006](https://github.com/Vicalzada/RentaDeCarros/assets/167146583/18b46205-edc6-4324-97b7-ee931781218b)

Este código PHP representa una página web que incluye un formulario de contacto y algunos detalles de contacto, además de archivos de encabezado (portada.php) y pie de página (footer1.php). Aquí está lo que hace cada parte del código:
<?php include "Views/Templates/portada.php"; ?>: Incluye el archivo portada.php, que probablemente contenga el encabezado de la página, como la barra de navegación y el logotipo.
<section class="ftco-section contact-section">...</section>: Contiene el contenido principal de la página, que incluye detalles de contacto y un formulario de contacto.
<?php include "Views/Templates/footer1.php"; ?>: Incluye el archivo footer1.php, que probablemente contenga el pie de página de la página web, como información de copyright y enlaces adicionales.
<script src="<?php echo base_url; ?>Assets/major/js/pages/contact.js"></script>: Carga un archivo JavaScript (contact.js) que probablemente contiene código para validar y enviar el formulario de contacto.
En resumen, este código PHP crea una página web con un formulario de contacto y detalles de contacto, y utiliza archivos de encabezado y pie de página para mantener la consistencia en el diseño y la funcionalidad de la página.

Gestión de automóviles.
 Explora cómo se maneja la información de los automoviles. Permite a los agentes gestionar listados, fotos, precios y detalles de manera eficiente.
 ![Captura de pantalla 2024-04-24 215721](https://github.com/Vicalzada/RentaDeCarros/assets/167146583/f51cd2dd-4824-4099-a406-19e481066dff)

Descripción para el código del archivo vehiculos.php del administrador de carros.

 ![Captura de pantalla 2024-04-24 220103](https://github.com/Vicalzada/RentaDeCarros/assets/167146583/b1e3e3b0-a8af-42cf-973b-4ba606c3bca8)

Este código PHP define una clase llamada Vehiculos que actúa como controlador en una aplicación web. Aquí está lo que hace cada parte del código:
class Vehiculos extends Controller: Define una clase llamada Vehiculos que hereda de la clase Controller. Esto sugiere que el controlador está utilizando algún tipo de patrón de diseño MVC (Modelo-Vista-Controlador).
public function __construct() {...}: Define el constructor de la clase Vehiculos. Este constructor inicia una sesión PHP con session_start(). Luego, comprueba si el usuario ha iniciado sesión y si tiene el tipo de usuario correcto (administrador). Si no cumple con estos requisitos, redirige al usuario a la página de inicio de sesión. Finalmente, llama al constructor de la clase padre con parent::__construct().
public function index() {...}: Define un método llamado index(), que es el controlador para la página principal de la sección de vehículos. Dentro de este método, se obtienen datos de las marcas y tipos de vehículos desde el modelo utilizando el método getDatos(). Luego, se renderiza la vista de la página principal de vehículos (vehiculos/index) pasando los datos obtenidos.
public function listar() {...}: Define un método llamado listar() que se encarga de obtener y formatear los datos de los vehículos desde el modelo para su visualización en formato JSON. Esto puede ser utilizado en una llamada AJAX para cargar y mostrar los vehículos en una tabla o lista.
public function registrar() {...}: Define un método llamado registrar() que se encarga de registrar un nuevo vehículo en la base de datos. Este método valida los datos recibidos del formulario de registro, maneja la carga de la imagen del vehículo y llama a los métodos correspondientes del modelo para realizar la inserción o modificación de los datos en la base de datos.
public function editar(int $id) {...}: Define un método llamado editar() que se encarga de obtener los datos de un vehículo específico para su edición. Este método recibe el ID del vehículo como parámetro y llama al método correspondiente del modelo para obtener los datos del vehículo en formato JSON.
public function eliminar(int $id) {...}: Define un método llamado eliminar() que se encarga de eliminar un vehículo de la base de datos. Este método recibe el ID del vehículo como parámetro y llama al método correspondiente del modelo para realizar la eliminación de los datos en la base de datos.
public function buscarVehiculo() {...}: Define un método llamado buscarVehiculo() que se encarga de buscar vehículos en la base de datos según un término de búsqueda proporcionado. Este método se utiliza para la funcionalidad de búsqueda en tiempo real y devuelve los resultados en formato JSON.


_________________________________________

<h1 align="center"> Conclusiones</h1>

En resumen, crear una página web sobre renta de carros es una inversión importante que puede ayudar a aumentar la visibilidad en línea, generar clientes potenciales, proporcionar información detallada, facilitar reservas en línea, ofrecer atención al cliente y servir como una poderosa herramienta de marketing para hacer crecer tu negocio de renta de carros.

-_______________________________________________________________

<h1 align="center"> Referencias</h1>

Redacción, A. (2023, June 5). ¿Cómo funciona la renta de autos? Nos Mueves Tú. https://blog.veico.com/como-funciona-la-renta-de-autos/

La nueva forma de rentar un auto - Mex Rent a Car. (n.d.). https://mexrentacar.com/es/descubre/1-renta-autos-la-nueva-forma-de-rentar-un-auto


México, E. R. (n.d.). ¿Cómo rentar un auto en México? | Enterprise México. Enterprise Rent-A-Car. https://enterprise.mx/renta-de-auto-en-mexico

Políticas de renta de autos. (n.d.). Políticas de renta de autos. Políticas De Renta De Autos. https://nationalcar.com.mx/politicas-de-renta

Redacción. (2024, January 18). ¿Cómo funciona el depósito de renta de autos? Nos Mueves Tú. https://blog.veico.com/como-funciona-el-deposito-de-renta-de-autos/

PHP: ¿Qué es PHP? - Manual. (n.d.). https://www.php.net/manual/es/intro-whatis.php

PHP: Iteración de objetos - Manual. (n.d.). https://www.php.net/manual/es/language.oop5.iterations.php

PHP: Constantes de clases - Manual. (n.d.). https://www.php.net/manual/es/language.oop5.constants.php

XAMPP installers and downloads for Apache Friends. (n.d.). https://www.apachefriends.org/es/index.html




