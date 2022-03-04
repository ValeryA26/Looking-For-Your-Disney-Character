# Looking For Your Disney Character
**Asignatura: Autómatas y Lenguajes Formales**

**Profesor: Luis Carlos Guayacán**

**Estudiantes:**
- Rodriguez Romero Julián Andrey - 2191956
- Melchor Suárez Valery Andrea - 2191916
- Adel Mauricio - 2191932

**Escuela de Ingeniería de Sistemas e Informática**

*Marzo de 2022*

## Introducción
Para la realización de este proyecto se hizo uso de los conceptos de: Autómatas finitos deterministas. Se implementó mediante el uso de la librería: [automatalib]() y también mediante la herramienta [JFLAP.]() 

El proyecto se inspira en el juego de la búsqueda del tesoro, en el que con acertijos y preguntas el jugador sigue el camino que le lleva hasta un personaje u objetivo, que es el final del juego y el "tesoro".

## Definición formal
Como trabajo previo a la elaboración de este juego, se realizó un autómata finito determinista en JFLAP, el cual comienza desde una primera pregunta y con cada respuesta encuentra un nuevo camino que se abre hasta llegar a un estado final, que sería la meta del juego. 
De errar alguna de las preguntas (llegar a un estado que no lleva a ningún estado final) se devolverá al estado incial, de tal manera que no puede haber errores al contestar si se quiere llegar hasta el final. 

https://docs.google.com/document/d/1iCE0JXHYIw46bhOt_snN9yngB7dI5vOm/edit?usp=sharing&ouid=115592118122648990501&rtpof=true&sd=true
https://drive.google.com/file/d/1-P1pGyGXE8lz2KlGURBCBJT3Nf5l8T5F/view?usp=sharing

