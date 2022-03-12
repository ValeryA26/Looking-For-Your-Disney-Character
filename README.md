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

- δ( q0 , g ) = q1
- δ( q0 , a ) = q2
- δ( q1 ,  l ) = q3
- δ( q2 , x ) = q4
- δ( q3 , 2 ) = q5
- δ( q4 , 2 ) = q6
- δ( q5 , y ) = q7
- δ( q5 , z ) = q8
- δ( q6 , z ) = q9
- δ( q6 , h ) = q1
- δ( q7 , p ) = q27
- δ( q8 , p ) = q28
- δ( q9 , f ) = q11
- δ( q10 , f ) = q12
- δ( q11 , s ) = q13
- δ( q12 , c ) = q14
- δ( q13 , 3 ) = q15
- δ( q14 , 4 ) = q16
- δ( q15 , b ) = q17
- δ( q16 , b ) = q18
- δ( q17 , e ) = q19
- δ( q18 , e ) = q20
- δ( q19 , i ) = q21 
- δ( q20 , j ) = q22
- δ( q21 , k ) = q23
- δ( q22 , k ) = q24
- δ( q23 , o ) = q25
- δ( q24 , q ) = q26
- δ( q27 , t ) = q29
- δ( q28 , s ) = q30
- δ( q29 , 1 ) = q31
- δ( q30 , 0 ) = q32
- δ( q31 , m ) = q33
- δ( q32 , m ) = q34
- δ( q33 , d ) = q35
- δ( q34 , d ) = q36
- δ( q35 , v ) = q37
- δ𝛾( q36 , v ) = q38
- δ( q37 , j ) = q39
- δ( q38 , j ) = q40
- δ( q39 , n ) = q41
- δ( q40 , n ) = q42


[diagrama](https://drive.google.com/file/d/103hLQLLh4glETt4X3D3nxZ5OaGMw8qKJ/view?usp=sharing)

[listado de preguntas](https://drive.google.com/file/d/1cjxeoveqF0qUlD7x8UZh7IiKzrFdxMNw/view?usp=sharing)

**Código:**

```
def projecto:
    from automatalib.fa.dfa import DFA
    d = DFA(
        states = {'q0', 'q1', 'q2', 'q3', 'q4', 'q5', 'q6', 'q7', 'q8', 'q9', 'q10', 'q11', 'q12', 
        'q13', 'q14', 'q15', 'q16', 'q17', 'q18', 'q19', 'q20', 'q21', 'q22', 'q23', 'q24', 'q25', 
        'q26', 'q27', 'q28', 'q29', 'q30', 'q31', 'q32', 'q33', 'q34', 'q35', 'q36', 'q37', 'q38', 
        'q39', 'q40', 'q41', 'q42', 'q43', 'q44', 'q45', 'q46', 'q47', 'q48', 'q49', 'q50', 'q51', 
        'q52', 'q53', 'q54', 'q55', 'q56', 'q57', 'q58', 'q59', 'q60', 'q61', 'q62', 'q63', 'q64', 
        'q65', 'q66', 'q67', 'q68', 'q69', 'q70', 'q71', 'q72', 'q73', 'q74', 'q75', 'q76', 'q77', 
        'q78', 'q79', 'q80', 'q81', 'q82', 'q83', 'q84', 'q85', 'q86', 'q87', 'q88', 'q89', 'q90', 
        'q100', 'q101', 'q102', 'q103', 'q104'},
        input_symbols = {'a', 'b', 'c', 'd' },
        transitions = { 
            'q0': {'a': 'q3', 'b': 'q4', 'c': 'q2', 'd': 'q1'},
            'q1': {'a': 'q6', 'b': 'q7', 'c': 'q5', 'd': 'q8'},
            'q2': {'a': 'q9', 'b': 'q10', 'c': 'q12', 'd': 'q11'},
            'q3': {'a': 'q2', 'b': 'q15', 'c': 'q13', 'd': 'q14'},
            'q4': {'a': 'q0', 'b': 'q102'},
            'q5': {'a': 'q1', 'b': 'q117'},
            'q6': {'a': 'q17', 'b': 'q16', 'c': 'q18'},
            'q7': {'a': 'q20', 'b': 'q19', 'c': 'q21'},
            'q8': {'a': 'q22', 'b': 'q23', 'c': 'q24', 'd': 'q25'},
            'q9': {'a': 'q26', 'b': 'q27', 'c': 'q28'},
            'q10': {'a': 'q2', 'b': 'q149'},
            'q11': {'a': 'q29', 'b': 'q30', 'c': 'q31'},
            'q12': {'a': 'q2', 'b': 'q154'},
            'q13': {'a': 'q32', 'b': 'q33', 'c': 'q34', 'd': 'q35'},
            'q14': {'a': 'q36', 'b': 'q37', 'c': 'q38', 'd': 'q39'},
            'q15': {'a': 'q3', 'b': 'q157'},
            'q16': {'a': 'q6', 'b': 'q103'},
            'q17': {'a': 'q40', 'b': 'q41', 'c': 'q42'},
            'q18': {'a': 'q43', 'b': 'q44', 'c': 'q45'},
            'q19': {'a': 'q7', 'b': 'q110'},
            'q20': {'a': 'q46', 'b': 'q47', 'c': 'q48'},
            'q21': {'a': 'q7', 'b': 'q111'},
            'q22': {'a': 'q49', 'b': 'q50', 'c': 'q51', 'd': 'q52'},
            'q23': {'a': 'q8', 'b': 'q119'},
            'q24': {'a': 'q53', 'b': 'q54', 'c': 'q55', 'd': 'q56'},
            'q25': {'a': 'q8', 'b': 'q118'},
            'q26': {'a': 'q11', 'b': 'q150'},
            'q27': {'a': 'q46', 'b': 'q47', 'c': 'q48'},
            'q28': {'a': 'q11', 'b': 'q151'},
            'q29': {'a': 'q11', 'b': 'q156'},
            'q31': {'a': 'q11', 'b': 'q155'},
            'q32': {'a': 'q60', 'b': 'q61', 'c': 'q62'},
            'q33': {'a': 'q63', 'b': 'q64', 'c': 'q32'},
            'q34': {'a': 'q13', 'b': 'q159'},
            'q35': {'a': 'q13', 'b': 'q158'},
            'q36': {'a': 'q14', 'b': 'q166'},
            'q37': {'a': 'q14', 'b': 'q165'},
            'q38': {'a': 'q14', 'b': 'q164'},
            'q40': {'a': 'q17', 'b': 'q104'},
            'q41': {'a': 'q17', 'b': 'q105'},
            'q43': {'a': 'q18', 'b': 'q106'},
            'q44': {'a': 'q18', 'b': 'q107'},
            'q45': {'a': 'q65', 'b': 'q66', 'c': 'q67'},
            'q46': {'a': 'q68', 'b': 'q69', 'c': 'q70', 'd': 'q71'},
            'q47': {'a': 'q20', 'b': 'q117'},
            'q48': {'a': 'q20', 'b': 'q112'},
            'q49': {'a': 'q22', 'b': 'q120'},
            'q50': {'a': 'q22', 'b': 'q121'},
            'q51': {'a': 'q22', 'b': 'q122'},
            'q52': {'a': 'q72', 'b': 'q73', 'c': 'q74', 'd': 'q75'},
            'q53': {'a': 'q76', 'b': 'q77', 'c': 'q78', 'd': 'q79'},
            'q54': {'a': 'q24', 'b': 'q135'},
            'q55': {'a': 'q24', 'b': 'q142'},
            'q56': {'a': 'q80', 'b': 'q81', 'c': 'q82', 'd': 'q83'},
            'q57': {'a': 'q27', 'b': 'q152'},
            'q59': {'a': 'q27', 'b': 'q153'},
            'q61': {'a': 'q32', 'b': 'q163'},
            'q62': {'a': 'q32', 'b': 'q162'},
            'q63': {'a': 'q33', 'b': 'q161'},
            'q64': {'a': 'q33', 'b': 'q160'},
            'q65': {'a': 'q45', 'b': 'q108'},
            'q67': {'a': 'q45', 'b': 'q109'},
            'q68': {'a': 'q46', 'b': 'q114'},
            'q69': {'a': 'q46', 'b': 'q115'},
            'q71': {'a': 'q46', 'b': 'q116'},
            'q72': {'a': 'q52', 'b': 'q123'},
            'q73': {'a': 'q84', 'b': 'q85', 'c': 'q86', 'd': 'q87'},
            'q74': {},
            'q75': {},
            'q76': {},
            'q77': {},
            'q78': {},
            'q79': {},
            'q80': {},
            'q81': {},
            'q82': {},
            'q83': {},
            'q84': {},
            'q85': {},
            'q86': {},
            'q87': {},
            'q88': {},
            'q89': {},
            'q90': {},
            'q91': {},
            'q92': {},
            'q93': {},
            'q94': {},
            'q95': {},
            'q96': {},
            'q97': {},
            'q98': {},
            'q99': {},
            'q100': {},
            'q101': {},
            'q102': {},
            'q103': {},
            'q104': {},
            'q105': {},
            'q106': {},
            'q107': {},
            'q108': {},
            'q109': {},
            'q110': {},
            'q111': {},
            'q112': {},
            'q113': {},
            'q114': {},
            'q115': {},
            'q116': {},
            'q117': {},
            'q118': {},
            'q119': {},
            'q120': {},
            'q121': {},
            'q122': {},
            'q123': {},
            'q124': {},
            'q125': {},
            'q126': {},
            'q127': {},
            'q128': {},
            'q129': {},
            'q130': {},
            'q131': {},
            'q132': {},
            'q133': {},
            'q134': {},
            'q135': {},
            'q136': {},
            'q137': {},
            'q138': {},
            'q139': {},
            'q140': {},
            'q141': {},
            'q142': {},
        },
        initial_state = 'q0',
        final_states = {'q30', 'q39', 'q42', 'q58', 'q60', 'q66', 'q70', '}
    )
    return d

import urllib, urllib.parse, inspect 
src1 = urllib.parse.quote_plus(inspect.getsource(proyecto))
```

