# Practica PowerShell

## Script 1

```
$number = 1

Write-Host "The number is: " $number

$number = 2

Write-Host "The number is: " $number

$number = 3

Write-Host "The number is: " $number

$number = 4

Write-Host "The number is: " $number

```

Este script establece 4 variables, con `$nombrevariable` e imprime por pantalla con `write-host` concatenando una String con la variable correspondiente

## Script 2

```
[int]$repeat = 5

for ($counter = 0; $counter -lt $repeat; $counter++) {
    Write-Host "hello"
} 

[int]$repeat = 5
[int]$counter = 0

while ($counter -lt $repeat) {
    Write-Host "hello"
    $counter++
}

[int]$repeat = 5
[int]$counter = 0
do {
    Write-Host "hello"
    $counter++
}
while ($counter -lt $repeat) 

[string]$stringOfCharacters = "PowerShell for Beginners"

foreach ($character in $stringOfCharacters.ToCharArray()) {
    Write-Host $character
} 

[string]$stringOfCharacters = "PowerShell for Beginners"
$stringOfCharacters.ToCharArray() | ForEach-Object { Write-Host "$_" }

```

![image](https://user-images.githubusercontent.com/95173613/162489932-05dabed6-d2a2-4e4a-85d6-a534295d2339.png)

### For
Lo que hace es reproducir un bucle en el que repite el string 'Hello' hasta que la variable counter sea 1 menos que la variable repeat. 

### While
El siguiente bucle lo que hace es que repite otra vez "Hello" hasta que se cumpla lo mismo que el de arriba solo que en este, el contador está ncluido dentro del bucle en lugar de en la declaración del bucle. Eso es debido a que usa un while para hacer el bucle en lugar de un for.

### Do While
La tercera declaración hace lo mismo pero usando do-while en lugar de un for o un while. Usa el mismo método que el anterior para declarar variables pero la declaración es separada. En el `do` está la acción y en el `while` está el condicional para el bucle.

### ForEach
Se establece una variable de tipo string. Posteriormente, se usa un foreach, que básicamente lo que hace es imprimir cada letra de un string dado.

### ForEach-Object 
Se establece como anteriormente una variable de tipo string. Reproduce el mismo comportamiento que el anterior.


Lo primero que hace es definir una variable. 
