# [Introducción a Selenium con Python](https://platzi.com/clases/intro-selenium/)

## ¿Qué es Selenium?  
Es una SUIT de herramientas para la automatización de navegadores Web.  
El objetivo de Selenium NO fue para el Testing ni para el Web Scraping (aunque se puede usar para eso), por lo tanto, no es el más optimo para estas actividades.  
Protocolo: WebDriver, herramienta que se conecta a un API.  
Selenium WebDriver es la herramienta que utilizaremos en el curso.  
-Selenium NO es un Software, ES una SUIT de Softwares.  
*DDT: Data Drive Testing: Ingresar datos para que realice varias pruebas (sin intervención humana).  

### Selenium IDE  
- Pros  
Excelente para iniciar  
No requiere saber programar  
Exporta scripts para Selenium RC y Selenium WebDriver  
Genera reportes  
- Contras  
Disponible para Google Chrome y FireFox  
No soporta DDT. No permite colocar datos para múltiples pruebas.  

### Selenium RC  
- Pros  
Soporte para  
Varias plataformas, navegadores y lenguajes.  
Operaciones lógicas y condicionales  
DDT  
Posee una API madura  
- Contras  
Complejo de instalar  
Necesita de un servidor corriendo.  
Comandos redundantes en una API  
Navegación no tan realista  
### Selenium Web Driven  
- Pros  
Soporte para múltiples lenguajes  
Facil de instalar.  
Comunicación directa con el navegador.  
Interacción más realista.  
- Contra  
No soporta nuevos navegadores tan rápido.  
No genera reportes o resultados de pruebas.  
Requiere de saber programar.  

## 4 [Configurar entorno de trabajo](https://platzi.com/clases/1927-intro-selenium/29386-configurar-entorno-de-trabajo/)


- Python versión superior a versión 3.6
- Selenium
- PyUnitReport

si estas en la terminal de ubuntu
1 : sudo apt update
2 : apt install python3-pip
3 : pip3 --version
4 : pip3 install selenium
5 : pip3 install pyunitreport
y listo ya puedes disfrutar del resto del curso.

## 6 [¡Hola, mundo!](https://platzi.com/clases/1927-intro-selenium/29387-hola-mundo/)

https://platzi.com/tutoriales/1751-webscraping/4981-crear-un-entorno-virtual-en-python/




https://chromedriver.chromium.org/downloads