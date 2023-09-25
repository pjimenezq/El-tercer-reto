# Reto 3
**Instrucción**
1. Plantear el algoritmo para obtener los números primos hasta n, usando pseudocódigo y diagramas de flujo.

2. Revise el procedimiento matemático para hallar raíces cuadradas (son divisiones y restas), plantee el algoritmo en pseudocódigo y en diagrama de flujo.

3. Cree un repositorio en github en donde muestre el desarrollo de la actividad y comparta el enlace por el canal de slack reto_3

## Algoritmo para obtener los números primos

**Pseudocógigo**

```pseudocode
n : entero
i : entero
x : entero
inicio
  i := 2
  x := 2
  n :>=2
  Mientras i<=n hacer
    Si  (x<=(i**0.5)) entonces
      Si modulo(i,x) == 0 entonces
        escribir("i no es primo")
        i := i + 1
        x := 2
      Sino
        x := x + 1
    Sino entonces
      escribir "i es primo"
      i := i + 1
      x := 2
    Fin Si
  Fin mientras 
fin
```
**Diagrama de flujo**

```mermaid
flowchart TD
A(inicio)-->B[número n mayor o igual a 2]
B-->C[i=2]
C-->D[x=2]
D-->E{residuo de i/x es cero?}
E--no-->P[x=x+1]
P-->F{x es menor o igual a la raiz cuadrada de i?}
E--sí-->G[i no es primo]
F--no-->H[i es primo]
F--sí-->E
H-->I[i=i+1]
G-->I
I-->J{i es menor o igual a n?}
J--sí-->D
J--no-->K(fin)
```
