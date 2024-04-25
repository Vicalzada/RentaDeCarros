Calzada Torres Victor

Ensayo de modelo-vista-controlador de una aplicación web en PHP.

Instituto Tecnológico Nacional de México Campus Tláhuac I.

Ingeniería en Sistemas Computacionales.

Grupo 8S2.		Programación PHP con MVC.

21 de marzo de 2024.


Índice
Resumen	1
Introducción	2
Desarrollo	2
El Modelo-Vista-Controlador (MVC)	2
Diagrama de clases	4
Catálogo de vehículos	5
Descripción de código php para el archivo cars.php	6
Listados de propiedades	7
Descripción del código php para el archivo propiedades.php.	7
Galería de imágenes e Información detallada:	8
Descripción para el código del archivo publicación.php.	9
Formulario de contacto:	10
Descripción para el código del archivo contacto.php.	10
Gestión de Propiedades.	11
Descripción para el código del archivo index.php del administrador de propiedades.	12
Conclusiones	13
Referencias	13

Resumen
El crea una página web para una inmobiliaria ofrece numerosas ventajas, como mayor accesibilidad para los clientes, publicidad inmobiliaria a menor costo y una mejor imagen de la agencia. Algunas de las ventajas más destacadas incluyen una inversión mínima, una mejor imagen de la agencia, la oportunidad de llegar a un público más amplio, ofrecer un servicio 24 horas y ofrecer un servicio de atención al cliente más eficiente a través de secciones de preguntas frecuentes . 
Además, tener una página web para una inmobiliaria es esencial en el mundo digital actual, ya que la mayoría de los usuarios buscan información online sobre propiedades antes de acercarse a una inmobiliaria. Esto aumenta el éxito inmobiliario al insertar la agencia en el mundo de los negocios digitales. Al crear una página web para una inmobiliaria, es importante tener una plantilla que se adapa a las necesidades del negocio y agregar y editar contenido relevante, como información sobre el negocio, los servicios que se ofrecen, las propiedades disponibles y la información de contacto. 
Introducción
En el mundo actual, la presencia en línea se ha vuelto indispensable para cualquier negocio que busque alcanzar su máximo potencial y llegar a una audiencia más amplia. En este contexto, la creación de una página web para un servicio de renta de autos se presenta como una estrategia fundamental para posicionarse en el mercado y ofrecer una experiencia completa y accesible a los clientes.
El propósito de este documento es introducir el proyecto de desarrollo de una página web para nuestro servicio de renta de autos, utilizando el modelo MVC (Modelo-Vista-Controlador) con PHP. Exploraremos los fundamentos de este modelo arquitectónico y cómo aplicarlo de manera efectiva para crear una plataforma web dinámica, robusta y fácil de mantener.
A lo largo de este documento, examinaremos las razones por las cuales optamos por el modelo MVC para nuestro proyecto, sus ventajas y beneficios en términos de estructura, modularidad y mantenimiento del código. Además, describiremos los componentes clave de nuestro servicio de renta de autos y cómo serán implementados dentro del modelo MVC.
En última instancia, este documento servirá como guía inicial para el desarrollo de nuestra página web, proporcionando una visión general del enfoque metodológico y las herramientas tecnológicas que utilizaremos para llevar a cabo este emocionante proyecto.
Desarrollo

crear una página web sobre renta de carros es una inversión importante que puede ayudar a aumentar la visibilidad en línea, generar clientes potenciales, proporcionar información detallada, facilitar reservas en línea, ofrecer atención al cliente y servir como una poderosa herramienta de marketing para hacer crecer tu negocio de renta de carros.

El Modelo-Vista-Controlador (MVC) 
El modelo, vista y controlador es un patrón de diseño de software que separa la lógica de negocios de su visualización. Se utiliza para implementar interfaces de usuario, datos y lógica de control.
En este proyecto se estructura de la siguiente manera, donde muestra en una estructura MVC y se guardan los archivos correspondientes.
 
Dentro de la carpeta controlador.
Se encuentran las carpetas y archivos que dan la instrucción de manejo de los archivos php.
 
Dentro de la carpeta modelo.
Se encuentran los archivos que dan la instrucción de conexiones entre el controlador y el modelo de los archivos php.

 

Dentro de la vista
Se encuentran los archivos que dan la vista la cual se mostrara dentro del navegador web.
 
Diagrama de clases
 


Las funcionalidades principales para una página web de renta de carros
Al desarrollar un proyecto web para una página de inmobiliaria, es esencial incluir una serie de funcionalidades específicas para brindar una experiencia completa a los usuarios. Aquí se muestran las funcionalidades principales que debería tener este tipo de proyecto.
Para una página web de renta de carros, algunas funcionalidades principales que deberían considerarse son:
Catálogo de vehículos


 

Mostrar una lista completa y detallada de los vehículos disponibles para renta, incluyendo imágenes, especificaciones técnicas, características destacadas y disponibilidad.






Descripción de código php para el archivo cars.php

 
Este código PHP define una clase llamada Cars que actúa como controlador en una aplicación web. Aquí está lo que hace cada parte del código:
La classe Cars extends Controller: Define una clase llamada Cars que hereda de la clase Controller. Esto sugiere que el controlador está utilizando algún tipo de patrón de diseño MVC (Modelo-Vista-Controlador).

public function __construct() {...}: Define el constructor de la clase Cars. Este constructor inicia una sesión PHP con session_start() y luego llama al constructor de la clase padre con parent::__construct(). Esto indica que la clase padre (Controller) realiza algunas tareas de inicialización importantes.

public function index() {...}: Define un método llamado Index(), que es el controlador para la página principal de la sección de vehículos. Dentro de este método, se define un array asociativo llamado $data que contiene algunas variables como active, title, detail y vehiculos. Luego, se llama a un método getVehiculos() del modelo (asumiendo que $this->model es una instancia del modelo asociado) para obtener una lista de vehículos, y finalmente se llama al método getView() para renderizar la vista de la página de vehículos (cars.php) pasando el array $data.

public function single($valor) {...}: Define un método llamado single() que toma un parámetro $valor. Este método es responsable de mostrar los detalles de un vehículo específico. Dentro del método, se obtiene el ID del vehículo del parámetro $valor, luego se llama al método getVehiculo() del modelo para obtener los detalles de ese vehículo en particular. 

Finalmente, se renderiza la vista de la página de detalles del vehículo (car-single.php) pasando los detalles del vehículo como datos.


