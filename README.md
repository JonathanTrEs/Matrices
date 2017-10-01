Curso: 3º 
Asignatura: Lenguaje y Paradigmas de programacion 
Grupo: 10 
Practica: 8 
Representantes: 2 
Nombre: Jonathan Trujillo Estevez 
Nombre: Ruben Guanche Flores

Descripcion: En esta practica implmentaremos una clase matriz y sus metodos usando el desarollo dirigido por pruebas (TDD) con la herramienta Rspec. Tambien se ha utilizado la herramienta Travis para seguir la metodologia de integracion continua. Y ademas se ha utilizado la herramienta Guard de comprobacion continua.


|-- Gemfile
|-- Guardfile
|-- lib
|   `-- Matriz.rb
|-- prueba
|-- Rakefile
|-- README.md
`-- spec
    `-- matriz_spec.rb

Dentro del directorio principal tenemos los siguientes ficheros:

    1,mg+lwm

    Fichero README.md: Fichero con la documentacion de la practica
    
    Fichero Gemfile: fichero en el que indicamos las gemas que queremos utilizar.

Dentro del directorio /spec tenemos el fichero:

Fichero racional_spec.rb: Este fichero contiene todas las pruebas TDD que ejecutamos para realizar la practica.


En el directorio /lib tenemos los siguientes ficheros:

    Fichero matriz.rb: En este fichero tenemos implementada la clase Matriz con cada uno de los elementos necesarios y 
 sus metodos.

         Metodo: initialize que es llamado por el metodo .new, en este metodo
         inicializamos la matriz que se ha creado.

         Metodo to_s: este metodo devuelve el objeto Matriz que hallamos creado en forma
         de string.

         Metodo +: este metodo nos permite sumar dos matrices de igual tamano.

         Metodo -: este metodo nos permite restar dos matrices de igual tamano.

         Metodo *: este metodo nos permita multiplicar dos matrices donde el numero de fil de la prim coincide con el numero de col de la seg.

         Metodo X: nos permite multiplicar una matriz cualquiera por un escalar.

         Metodo igual: nos compara dos matrices y nos dice si son o no iguales.

         Metodo deter: nos halla el determinante de la matriz.

         Metodo t: nos calcula la traspuesta de una matriz.

