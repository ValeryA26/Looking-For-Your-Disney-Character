# Looking For Your Disney Character
**Asignatura: Autómatas y Lenguajes Formales**

**Profesor: Luis Carlos Guayacán**

**Estudiantes:**
- Rodríguez Romero Julián Andrey - 2191956
- Melchor Suárez Valery Andrea - 2191916
- Adel Mauricio - 2191932

**Escuela de Ingeniería de Sistemas e Informática**

*Marzo de 2022*

## Introducción
Para la realización de este proyecto se hizo uso de los conceptos de: Autómatas finitos deterministas. Se implementó mediante el uso de la librería: [automatalib]() y también mediante la herramienta [JFLAP.](https://softfamous.com/postdownload-file/jflap/8447/3913/) 

El proyecto se inspira en el juego de la búsqueda del tesoro, en el que con acertijos y preguntas el jugador sigue el camino que le lleva hasta un personaje u objetivo, que es el final del juego y el "tesoro".

## Definición formal
Como trabajo previo a la elaboración de este juego, se realizó un autómata finito determinista en JFLAP, el cual comienza desde una primera pregunta y con cada respuesta encuentra un nuevo camino que se abre hasta llegar a un estado final, que sería la meta del juego. 
De errar alguna de las preguntas (llegar a un estado que no lleva a ningún estado final) se devolverá al estado incial, de tal manera que no puede haber errores al contestar si se quiere llegar hasta el final. 

Sea A el automata definido: A = ( Q , ∑ , δ , q0 , F ) 

su conjunto de estados: Q = {q0 , q1 , q2 , q3 , q4 , q5 , q6 , q7 , q8 , q9 , q10 , q11 , q12 , q13 , q14 , q15 , q16 , q17 , q18 , q19 , q20 , q21 , q22 , q23 , q24 , q25 , q26 , q27 , q28 , q29 , q30 , q31 , q32 , q33 , q34 , q35 , q36 , q37 , q38 , q39 , q40 , q41 , q42}

su alfabeto: ∑ = {g , a , l , x , 2 , y , z , h , p , f , t , s , c , 1 , 0 , 3 , 4 , m , b , d , e , v ,  i ,  j ,  k , n , o , q}

sus estados finales: F = {q25 , q26 , q41 , q42}

sus transiciones:

δ( q0 , g ) = q1

δ( q0 , a ) = q2

δ( q1 ,  l ) = q3

δ( q2 , x ) = q4

δ( q3 , 2 ) = q5

δ( q4 , 2 ) = q6

δ( q5 , y ) = q7

δ( q5 , z ) = q8

δ( q6 , z ) = q9

δ( q6 , h ) = q1

δ( q7 , p ) = q27

δ( q8 , p ) = q28

δ( q9 , f ) = q11

δ( q10 , f ) = q12

δ( q11 , s ) = q13

δ( q12 , c ) = q14

δ( q13 , 3 ) = q15

δ( q14 , 4 ) = q16

δ( q15 , b ) = q17

δ( q16 , b ) = q18

δ( q17 , e ) = q19

δ( q18 , e ) = q20

δ( q19 , i ) = q21

δ( q20 , j ) = q22

δ( q21 , k ) = q23

δ( q22 , k ) = q24

δ( q23 , o ) = q25

δ( q24 , q ) = q26

δ( q27 , t ) = q29

δ( q28 , s ) = q30

δ( q29 , 1 ) = q31

δ( q30 , 0 ) = q32

δ( q31 , m ) = q33

δ( q32 , m ) = q34

δ( q33 , d ) = q35

δ( q34 , d ) = q36

δ( q35 , v ) = q37

δ𝛾( q36 , v ) = q38

δ( q37 , j ) = q39

δ( q38 , j ) = q40

δ( q39 , n ) = q41

δ( q40 , n ) = q42



[diagrama](https://drive.google.com/file/d/103hLQLLh4glETt4X3D3nxZ5OaGMw8qKJ/view?usp=sharing)

[listado de preguntas](https://drive.google.com/file/d/1cjxeoveqF0qUlD7x8UZh7IiKzrFdxMNw/view?usp=sharing)

**Código:**
def punto1():
    from automatalib.fa.dfa import DFA
    d = DFA(
        states = {'q0', 'q1', 'q2', 'q3', 'q4', 'q5'},
        input_symbols = {'a', 'b', 'c', 'd' },
        transitions = { 
            'q0': {'c': 'q0', 'd': 'q0', 'a': 'q1'},
            'q1': {'b': 'q2'},
            'q2': {'b': 'q2', 'a': 'q3'},
            'q3': {'d': 'q4'},
            'q4': {'a': 'q5'},
            'q5': {'d': 'q4'}
        },
        initial_state = 'q0',
        final_states = {'q4'}
    )
    return d

import urllib, urllib.parse, inspect 
src1 = urllib.parse.quote_plus(inspect.getsource(punto1))

