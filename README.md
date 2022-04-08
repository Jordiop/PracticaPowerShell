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

```
if (4 -eq 4) {
    Write-Host "4 is equal to 4"
}

if ("hello" -eq "hello") {
    Write-Host "Both strings are equal to each other"
} 

[int]$x = 10
[int]$y = 10

if ($x -eq $y) {
    Write-Host "the x and y variables are equal to each other"
}
else {
    Write-Host "The x and y variables are NOT equal to each other"
}

$yourName = "Ian"

if ($yourName -eq "Ian") {
    Write-Host "Hay my name is Ian too!"
}
else {
    Write-Host "Hi $yourName, nice to meet you!"
}

[string]$playerInput = ""

$playerInput = Read-Host -Prompt "You walk into a room with two doorways. One to the left and one to the right. Type 'left' or 'Right' to walk through one of the doors."

if ($playerInput -eq "left") {
    Write-Host "Player typed left"
}
elseif ($playerInput -eq "right") {
    Write-Host "Player typed right"
}
else {
    Write-Host "Player typed something we didn't understand"
}

if (5 -eq 5) {
    #5 is equal to 5
}
   
if (3 -ne 4) {
    #3 is not equal to 4
}
   
if (4 -gt 2) {
    #4 is greater than 2
}
   
if (2 -ge 1) {
    #2 is greater than or equal to 1
}
   
if (1 -lt 2) {
    #1 is less than 1
}

if (1 -le 2) {
    #1 is less than or equal to 2
} 

if ("hello how are you?" -like "hello*") {
    #use a wildcard character * to match strings
}

if ("HELLO" -notlike "BYE") {
    #HELLO is not like BYE
} 

if ("HELLO" -match "H") {
    #H exists in the 
    string "HELLO"
}
   	
if ("HELLO" -notmatch "A") {
    #A does not match in the 
    string "HELLO"
}

$list = @(1, 2, 3, 4, 5)
if ($list -contains 3) {
    #the list does contain a 3
}

$list = @(1, 2, 3, 4, 5)
if ($list -notcontains 8) {
    #$list does not contain 8
}

$list = @(1, 2, 3, 4, 5)
if (3 -in $list) {
    #the list does contain a 3
} 

$list = @(1, 2, 3, 4, 5)
if (6 -notin $list) {
    #6 is not in the list
}
	
$var = "This is a string"
if ($var -is [string]) {
    #The variable is a string
}

$var = "This is a string"
if ($var -isnot [bool]) {
    #The variable is a string and not a Boolean value so results in true.
} 
   
[int]$number = 2
switch ($number) {
    1 { "The number is one" }
    2 { "The number is two" }
    default { "I dont know what the number is" }
}

[string]$favouriteColour = "Blue"
switch ($favouriteColour) {
    "Red" {
        "Your favourite colour is Red"
        "I like red too."
    }
 
    "Blue" {
        "Your favourite colour is Blue"
        "I like Blue too."
    }
 
    default { "I dont recognise that colour" }
}

```
