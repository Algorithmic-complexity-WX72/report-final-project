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

