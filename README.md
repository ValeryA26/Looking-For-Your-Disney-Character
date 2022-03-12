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
De errar alguna de las preguntas (llegar a un estado que no lleva a ningún estado final) se devolverá al estado incial, de tal manera que no puede haber errores al contestar si se quiere llegar hasta el final. Por este motivo, se propone el siguiente lenguaje formal:

Sea A el automata definido: A = ( Q , ∑ , δ , q0 , F ) 

Su conjunto de estados: Q = {q0, q1, q2, q3, q4, q5, q6, q7, q8, q9, q10, q11, q12, q13, q14, q15, q16, q17, q18, q19, q20, q21, q22, q23, q24, q25, q26, q27, q28, q29, q30, q31, q32, q33, q34, q35, q36, q37, q38, q39, q40, q41, q42, q43, q44, q45, q46, q47, q48, q49, q50, q51, q52, q53, q54, q55, q56, q57, q58, q59, q60, q61, q62, q63, q64, q65, q66, q67, q68, q69, q70, q71, q72, q73, q74, q75, q76, q77, q78, q79, q80, q81, q82, q83, q84, q85, q86, q87, q88, q89, q90, q100, q101, q102, q103, q104, q105, q106, q107, q108, q109, q110, q111, q112, q113, q114, q115, q116, q117, q118, q119, q120, q121, q122, q123, q124, q125, q126, q127, q128, q129, q130, q131, q132, q133, q134, q135, q136, q137, q138, q139, q140, q141, q142, q143, q144, q145, q146, q147, q148, q149, q150, q151, q152, q153, q154, q155, q156, q157, q158, q159, q160, q161, q162, q163, q164, q165, q166}

Su alfabeto: ∑ = {a, b, c, d}

Sus transiciones:

- δ( q0 , a) = q3
- δ( q0 , b) = q4
- δ( q0 , c) = q2
- δ( q0 , d) = q1
- δ( q1 , a) = q6
- δ( q1 , b) = q7
- δ( q1 , c) = q5
- δ( q1 , d) = q8
- δ( q2 , a) = q9
- δ( q2 , b) = q10
- δ( q2 , c) = q12
- δ( q2 , d) = q11
- δ( q3 , a) = q2
- δ( q3 , b) = q15
- δ( q3 , c) = q13
- δ( q3 , d) = q14
- δ( q4 , a) = q0
- δ( q4 , b) = q102
- δ( q5 , a) = q1
- δ( q5 , b) = q117
- δ( q6 , a) = q17
- δ( q6 , b) = q16
- δ( q6 , c) = q18
- δ( q7 , a) = q20
- δ( q7 , b) = q19
- δ( q7 , c) = q21
- δ( q8 , a) = q22
- δ( q8 , b) = q23
- δ( q8 , c) = q24
- δ( q8 , d) = q25
- δ( q9 , a) = q26
- δ( q9 , b) = q27
- δ( q9 , c) = q28
- δ( q10 , a) = q2
- δ( q10 , b) = q149
- δ( q11 , a) = q29
- δ( q11 , b) = q30
- δ( q11 , c) = q31
- δ( q12 , a) = q2
- δ( q12 , b) = q154
- δ( q13 , a) = q32
- δ( q13 , b) = q33
- δ( q13 , c) = q34
- δ( q13 , d) = q35
- δ( q14 , a) = q36
- δ( q14 , b) = q37
- δ( q14 , c) = q38
- δ( q14 , d) = q39
- δ( q15 , a) = q3
- δ( q15 , b) = q157
- δ( q16 , a) = q6
- δ( q16 , b) = q103
- δ( q17 , a) = q40
- δ( q17 , b) = q41
- δ( q17 , c) = q42
- δ( q18 , a) = q43
- δ( q18 , b) = q44
- δ( q18 , c) = q45
- δ( q19 , a) = q7
- δ( q19 , b) = q110
- δ( q20 , a) = q46
- δ( q20 , b) = q47
- δ( q20 , c) = q48
- δ( q21 , a) = q7
- δ( q21 , b) = q111
- δ( q22 , a) = q49
- δ( q22 , b) = q50
- δ( q22 , c) = q51
- δ( q22 , d) = q52
- δ( q23 , a) = q8
- δ( q23 , b) = q119
- δ( q24 , a) = q53
- δ( q24 , b) = q54
- δ( q24 , c) = q55
- δ( q24 , d) = q56
- δ( q25 , a) = q8
- δ( q25 , b) = q118
- δ( q26 , a) = q11
- δ( q26 , b) = q150
- δ( q27 , a) = q46
- δ( q27 , b) = q47
- δ( q27 , c) = q48
- δ( q28 , a) = q11
- δ( q28 , b) = q151
- δ( q29 , a) = q11
- δ( q29 , b) = q156
- δ( q31 , a) = q11
- δ( q31 , b) = q155
- δ( q32 , a) = q60
- δ( q32 , b) = q61
- δ( q32 , c) = q62
- δ( q33 , a) = q63
- δ( q33 , b) = q64
- δ( q33 , c) = q32
- δ( q34 , a) = q13
- δ( q34 , b) = q159
- δ( q35 , a) = q13
- δ( q35 , b) = q158
- δ( q36 , a) = q14
- δ( q36 , b) = q166
- δ( q37 , a) = q14
- δ( q37 , b) = q165
- δ( q38 , a) = q14
- δ( q38 , b) = q164
- δ( q40 , a) = q17
- δ( q40 , b) = q104
- δ( q41 , a) = q17
- δ( q41 , b) = q105
- δ( q43 , a) = q18
- δ( q43 , b) = q106
- δ( q44 , a) = q18
- δ( q44 , b) = q107
- δ( q45 , a) = q65
- δ( q45 , b) = q66
- δ( q45 , c) = q67
- δ( q46 , a) = q68
- δ( q46 , b) = q69
- δ( q46 , c) = q70
- δ( q46 , d) = q71
- δ( q47 , a) = q20
- δ( q47 , b) = q117
- δ( q48 , a) = q20
- δ( q48 , b) = q112
- δ( q49 , a) = q22
- δ( q49 , b) = q120
- δ( q50 , a) = q22
- δ( q50 , b) = q121
- δ( q51 , a) = q22
- δ( q51 , b) = q122
- δ( q52 , a) = q72
- δ( q52 , b) = q73
- δ( q52 , c) = q74
- δ( q52 , d) = q75
- δ( q53 , a) = q76
- δ( q53 , b) = q77
- δ( q53 , c) = q78
- δ( q53 , d) = q79
- δ( q54 , a) = q24
- δ( q54 , b) = q135
- δ( q55 , a) = q24
- δ( q55 , b) = q142
- δ( q56 , a) = q80
- δ( q56 , b) = q81
- δ( q56 , c) = q82
- δ( q56 , d) = q83
- δ( q57 , a) = q27
- δ( q57 , b) = q152
- δ( q59 , a) = q27
- δ( q59 , b) = q153
- δ( q61 , a) = q32
- δ( q61 , b) = q163
- δ( q62 , a) = q32
- δ( q62 , b) = q162
- δ( q63 , a) = q33
- δ( q63 , b) = q161
- δ( q64 , a) = q33
- δ( q64 , b) = q160
- δ( q65 , a) = q45
- δ( q65 , b) = q108
- δ( q67 , a) = q45
- δ( q67 , b) = q109
- δ( q68 , a) = q46
- δ( q68 , b) = q114
- δ( q69 , a) = q46
- δ( q69 , b) = q115
- δ( q71 , a) = q46
- δ( q71 , b) = q116
- δ( q72 , a) = q52
- δ( q72 , b) = q123
- δ( q73 , a) = q84
- δ( q73 , b) = q85
- δ( q73 , c) = q86
- δ( q73 , d) = q87
- δ( q74 , a) = q52
- δ( q74 , b) = q124
- δ( q75 , a) = q52
- δ( q75 , b) = q125
- δ( q76 , a) = q53
- δ( q76 , b) = q136
- δ( q77 , a) = q53
- δ( q77 , b) = q137
- δ( q78 , a) = q88
- δ( q78 , b) = q73
- δ( q78 , c) = q89
- δ( q78 , d) = q90
- δ( q79 , a) = q53
- δ( q79 , b) = q138
- δ( q80 , a) = q56
- δ( q80 , b) = q145
- δ( q81 , a) = q91
- δ( q81 , b) = q92
- δ( q81 , c) = q73
- δ( q81 , d) = q93
- δ( q82 , a) = q56
- δ( q82 , b) = q144
- δ( q83 , a) = q56
- δ( q83 , b) = q143
- δ( q84 , a) = q73
- δ( q84 , b) = q126
- δ( q85 , a) = q73
- δ( q85 , b) = q127
- δ( q86 , a) = q73
- δ( q86 , b) = q128
- δ( q87 , a) = q94
- δ( q87 , b) = q95
- δ( q87 , c) = q96
- δ( q87 , d) = q97
- δ( q88 , a) = q78
- δ( q88 , b) = q139
- δ( q89 , a) = q78
- δ( q89 , b) = q140
- δ( q90 , a) = q78
- δ( q90 , b) = q141
- δ( q91 , a) = q81
- δ( q91 , b) = q146
- δ( q92 , a) = q81
- δ( q92 , b) = q147
- δ( q93 , a) = q81
- δ( q93 , b) = q148
- δ( q94 , a) = q87
- δ( q94 , b) = q129
- δ( q95 , a) = q98
- δ( q95 , b) = q99
- δ( q95 , c) = q100
- δ( q95 , d) = q101
- δ( q96 , a) = q87
- δ( q96 , b) = q131
- δ( q97 , a) = q87
- δ( q97 , b) = q130
- δ( q98 , a) = q95
- δ( q98 , b) = q132
- δ( q99 , a) = q95
- δ( q99 , b) = q133
- δ( q101 , a) = q95
- δ( q101 , b) = q134

Su estado inicial: q0 = {q0}

Sus estados finales: F = {q30, q39, q42, q58, q60, q66, q70, q100, q101, q102, q103, q104, q105, q106, q107, q108, q109, q110, q111, q112, q113, q114, q115, q116, q117, q118, q119, q120, q121, q122, q123, q124, q125, q126, q127, q128, q129, q130, q131, q132, q133, q134, q135, q136, q137, q138, q139, q140, q141, q142, q143, q144, q145, q146, q147, q148, q149, q150, q151, q152, q153, q154, q155, q156, q157, q158, q159, q160, q161, q162, q163, q164, q165, q166}

## diagrama
![PROYECTO AUTOMATAS](https://user-images.githubusercontent.com/73613484/158001518-ab38f589-a3b3-484d-8432-129ba3916043.png)


[listado de preguntas](https://drive.google.com/file/d/1cjxeoveqF0qUlD7x8UZh7IiKzrFdxMNw/view?usp=sharing)

### Código:

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
        'q100', 'q101', 'q102', 'q103', 'q104', 'q105', 'q106', 'q107', 'q108', 'q109', 'q110', 'q111', 
        'q112', 'q113', 'q114', 'q115', 'q116', 'q117', 'q118', 'q119', 'q120', 'q121', 'q122', 'q123',
        'q124', 'q125', 'q126', 'q127', 'q128', 'q129', 'q130', 'q131', 'q132', 'q133', 'q134', 'q135',
        'q136', 'q137', 'q138', 'q139', 'q140', 'q141', 'q142', 'q143', 'q144', 'q145', 'q146', 'q147',
        'q148', 'q149', 'q150', 'q151', 'q152', 'q153', 'q154', 'q155', 'q156', 'q157', 'q158', 'q159',
        'q160', 'q161', 'q162', 'q163', 'q164', 'q165', 'q166'},
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
            'q74': {'a': 'q52', 'b': 'q124'},
            'q75': {'a': 'q52', 'b': 'q125'},
            'q76': {'a': 'q53', 'b': 'q136'},
            'q77': {'a': 'q53', 'b': 'q137'},
            'q78': {'a': 'q88', 'b': 'q73', 'c': 'q89', 'd': 'q90'}},
            'q79': {'a': 'q53', 'b': 'q138'},
            'q80': {'a': 'q56', 'b': 'q145'},
            'q81': {'a': 'q91', 'b': 'q92', 'c': 'q73', 'd': 'q93'},
            'q82': {'a': 'q56', 'b': 'q144'},
            'q83': {'a': 'q56', 'b': 'q143'},
            'q84': {'a': 'q73', 'b': 'q126'},
            'q85': {'a': 'q73', 'b': 'q127'},
            'q86': {'a': 'q73', 'b': 'q128'},
            'q87': {'a': 'q94', 'b': 'q95', 'c': 'q96', 'd': 'q97'},
            'q88': {'a': 'q78', 'b': 'q139'},
            'q89': {'a': 'q78', 'b': 'q140'},
            'q90': {'a': 'q78', 'b': 'q141'},
            'q91': {'a': 'q81', 'b': 'q146'},
            'q92': {'a': 'q81', 'b': 'q147'},
            'q93': {'a': 'q81', 'b': 'q148'},
            'q94': {'a': 'q87', 'b': 'q129'},
            'q95': {'a': 'q98', 'b': 'q99', 'c': 'q100', 'd': 'q101'},
            'q96': {'a': 'q87', 'b': 'q131'},
            'q97': {'a': 'q87', 'b': 'q130'},
            'q98': {'a': 'q95', 'b': 'q132'},
            'q99': {'a': 'q95', 'b': 'q133'},
            'q101': {'a': 'q95', 'b': 'q134'}
        },
        initial_state = 'q0',
        final_states = {'q30', 'q39', 'q42', 'q58', 'q60', 'q66', 'q70', 'q100', 'q101', 'q102', 'q103',
        'q104', 'q105', 'q106', 'q107', 'q108', 'q109', 'q110', 'q111', 'q112', 'q113', 'q114', 'q115', 
        'q116', 'q117', 'q118', 'q119', 'q120', 'q121', 'q122', 'q123', 'q124', 'q125', 'q126', 'q127', 
        'q128', 'q129', 'q130', 'q131', 'q132', 'q133', 'q134', 'q135', 'q136', 'q137', 'q138', 'q139', 
        'q140', 'q141', 'q142', 'q143', 'q144', 'q145', 'q146', 'q147', 'q148', 'q149', 'q150', 'q151', 
        'q152', 'q153', 'q154', 'q155', 'q156', 'q157', 'q158', 'q159', 'q160', 'q161', 'q162', 'q163', 
        'q164', 'q165', 'q166'}
    )
    return d

import urllib, urllib.parse, inspect 
src1 = urllib.parse.quote_plus(inspect.getsource(proyecto))
```

