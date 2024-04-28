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
