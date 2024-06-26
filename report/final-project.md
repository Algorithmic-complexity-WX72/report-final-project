<hr>

# <center>COURSE PROJECT</center>

<p align="center">
	<strong>Universidad Peruana de Ciencias Aplicadas</strong><br>
<br>
	<img src="/assets/logo-upc.png"></img><br>
<br>
	<strong>Ingeniería de Software </strong><br>
<br>
	<strong>Complejidad Algorítmica - WX72 </strong><br> 
<br>
	<strong>Profesor: Luis M. Canaval S.</strong><br>
	<br> <strong>INFORME DE TRABAJO FINAL - TP </strong>
</p>

<p align="center">
	<strong>Tema:  Risk </strong>
</p>

<h3 align="center" >Team Members:</h3>
<div>
	<table align="center">
    	<tr>
        	<th style="text-align:center;">Member</th>
        	<th style="text-align:center;">Code</th>
    	</tr>
    	<tr>
        	<td>Maita Falckenheiner, Romina Guadalupe </td>
            <td>U202213765</td>
    	</tr>
    	<tr>
        	<td>Escalante Baygorrea, Janiel Franz</td>
            <td>U201912668</td>
    	</tr>
    	<tr>
        	<td>Adriana Maria Diestra Zambrano</td>
            <td>U202218110</td>
    	</tr>
	</table>
</div>
<br>

# Descripción del problema

## Contexto:
El juego Risk es un clásico juego de mesa de estrategia que ha cautivado a jugadores de todo el mundo desde su lanzamiento en la década de 1950. Su atractivo radica en su combinación de estrategia militar, diplomacia y toma de decisiones tácticas, lo que lo convierte en un desafío emocionante y dinámico para los jugadores.


El juego consiste en un tablero que tiene 42 territorios, agrupados en 6 continentes. Cada continente es de un color distinto y contiene de 4 a 12 territorios.
El jugador tiene cierta cantidad de soldados al inicio y de acuerdo a la cantidad de países que ataca su ejército crece.
El objetivo es conquistar todos los territorios. Sin embargo, el jugador no puede saltar de un país a otro sino que debe pasar por ciertos países para llegar el destino.

De acuerdo con Du Satoy, Risk es un problema clásico de combinatoria y probabilidad, que convierte el juego en una preciosidad matemática de topología, con cadenas de Markov y probabilidad básica.

## Problema
En la dinámica competitiva del juego Risk, los jugadores se enfrentan a una serie de decisiones estratégicas complejas y desafíos tácticos mientras intentan conquistar territorios y dominar el mapa mundial. Sin embargo, la naturaleza del juego puede plantear diversos problemas y dilemas para los jugadores, desde la toma de decisiones sobre qué territorios atacar o fortificar, hasta la gestión de alianzas y recursos limitados.
Sin embargo, hemos adaptado la dinámica del juego para que sean planetas invadidos en vez de países.
Es por ello que el algoritmo que desarrollaremos competirá con el jugador tomando una decisión acertada respecto a qué planetas puede invadir de acuerdo a la cantidad de soldados que tenga el planeta invadido.

## Descripción y visualización del conjunto de datos (dataset)

El dataset ha sido generado por nosotros mismos usando un algoritmo de generación de datos sintéticos en el lenguaje Python y las librerias csv y random.
El dataset contiene 1500 registros y 2 columnas. Las columnas son las siguientes:
- La primera columna tiene el nombre del planeta
- La segunda columna tiene la cantidad de tropas que posee el planeta

### Codigo del Algoritmo
A continuación se muestra el código del algoritmo que hemos usado para generar el dataset:

```
import csv
import random

vowels = ["A", "E","I","O","U"]
cons = ["B", "C", "D", "F", "G","H", "I", "J", "K", "L", "M", "N", "Ñ", "O", "P", "Q", "R", "S", "T", "U", "V", "Z"]
def buildWord():
    randomNumberForName = random.randint(00,99)
    randomNumber = random.randint(2,4)
    name = ""
    for x in range(randomNumber):
        randomVowel = random.choice(vowels)
        randomCons = random.choice(cons)
        name = name + randomVowel + randomCons 
    name = name + "-" + str(randomNumberForName)
    return name
    
def buildNumber():
    randomNumber = random.randint(10,99)
    return randomNumber


def writeToCsv():
    with open ('names.csv', 'a') as file:
        writer = csv.writer(file)
        name = buildWord()
        number = buildNumber()
        writer.writerow([name] + [number])


for i in range(1500):
    writeToCsv()
```
### Subgrafos de los datos recolectados

<img src="/assets/nodos.JPG" alt="subgrafo"/></img>

## Propuesta
#  Implementación del juego Risk en Python
El objetivo de este proyecto es crear una versión del juego de mesa Risk en Python. Risk es un juego de estrategia en el que los jugadores compiten por el control territorial de un mapa mundial dividido en regiones.
## Características:
* Tablero de juego: Crearemos un tablero de juego que represente el espacio. Cada planeta tendrá un nombre y estará conectada a otros planetas.
* Fichas de jugador: Implementaremos fichas para representar las tropas de cada jugador en el tablero.
* Fase de colocación: Permite a los jugadores colocar sus tropas en las regiones que controlan al comienzo de cada turno.
* Fase de ataque: Permite a los jugadores atacar las regiones vecinas y conquistarlas.
* Fase de movimiento: Permite a los jugadores mover tropas entre regiones que controlan.
* Combate: Implementaremos un sistema de combate para resolver los enfrentamientos entre tropas.
* Gestión de Jugadores: Mantener un seguimiento de los jugadores activos y sus territorios.
* Gestión de Turnos: Alternar entre los turnos de los jugadores y permitirles realizar acciones durante su turno.
## Lenguaje de programación:
Python es el lenguaje principal de programación que usaremos para este proyecto.
Estructuras de datos para el manejo eficiente del tablero de juego, las fichas de jugador y la gestión de turnos.
## Objetivos:
* Crear una versión funcional del juego Risk que permita a los jugadores jugar contra la computadora.
* Implementar una interfaz de usuario intuitiva que muestre el tablero de juego y las opciones disponibles para cada jugador en su turno.
