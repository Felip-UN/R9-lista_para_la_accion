# R9-lista_para_la_accion
## Retos
1. Desarrollar un algoritmo que calcule el promedio de un arreglo de reales
2. Desarrollar un algoritmo que calcule el producto punto de dos arreglos de números enteros (reales) de igual tamaño
3. Hacer un algoritmo que deje al final de un arreglo de números todos los ceros que aparezcan en dicho arreglo
## Desarrollo
### 1. Promedio
Desarrollar un algoritmo que calcule el promedio de un arreglo de reales

**Programa:**
```python
if __name__=="main"
  numeros_r=input("ingresa una cantidad de numeros reales"\
                 " separados por un espacio: ")
  lista_r = list(map(float, numeros_r.split(" "))) #map para transformar la lista de numeros, tipo cadena, en flotantes
  #nota: no es la primera vez que uso map, pero si la primera donde lo uso de una manera mas comoda despues de la clase de "strings"
  sum=0
  print("Tus numeros son: ",lista_r)
  for n in lista_r:
   sum+=n
  promedio=sum/len(lista_r)
  print("Tu promedio es:",promedio)
```
**Entrada por consola:** 
```python
'3 4 5 6 7' #Se ingresa una cadena
```
**Salida de consola:** 
```python
Tus numeros son:  [3.0, 4.0, 5.0, 6.0, 7.0]
Tu promedio es: 5.0
```
### 2. Producto Punto
Segun lo leido en el enlace proporcionado se multiplicaba el primer valor de un vector con el primer valor de otro vector y este se sumama con el segundo por el segundo asi que cree un programa con una condicion especial, ambos vectores DEBEN tener la misma longitud
```python
print("Producto punto de 2 vectores")
while True:
	vec1=list(map(int, input("Ingresa los valores del vector 1 separados por un espacio: ").split(" ")))
	print("Vector 1 =",vec1)
	vec2=list(map(int, input("Ingresa los valores del vector 2 separados por un espacio: ").split(" ")))
	print("Vector 2 =",vec2)
	if len(vec1) != len(vec2):
		print("los vectores deben tener la misma cantidad de valores"\
		      " vuelve a intentarlo")
	if len(vec1) == len(vec2):
		break
resultado=[]
for i in range(len(vec1)):
	resultado.append(vec1[i] * vec2[i])
p_dot=sum(resultado)
print("Producto punto entre ambos: ",p_dot)
```
**Entradas de consola:** '1 2 3 4 5' , '5 4 3 2 1'

**Salida de consola:** 

Producto punto de 2 vectores

Ingresa los valores del vector 1 separados por un espacio: 1 2 3 4 5

Vector 1 = [1, 2, 3, 4, 5]

Ingresa los valores del vector 2 separados por un espacio: 5 4 3 2 1

Vector 2 = [5, 4, 3, 2, 1]

Producto punto entre ambos:  35

#### Caso de error (la longitud de ambos vectores es distinta)
**Entradas de consola:** '2 3 4' , '2 3'

**Salida de consola:**

Producto punto de 2 vectores

Ingresa los valores del vector 1 separados por un espacio: 2 3 4

Vector 1 = [2, 3, 4]

Ingresa los valores del vector 2 separados por un espacio: 2 3

Vector 2 = [2, 3]

los vectores deben tener la misma cantidad de valores vuelve a intentarlo **<-Mensaje de error**

Ingresa los valores del vector 1 separados por un espacio: 2 3 4

Vector 1 = [2, 3, 4]

Ingresa los valores del vector 2 separados por un espacio: 4 3 2

Vector 2 = [4, 3, 2]

Producto punto entre ambos:  25

### 3. Ceros en un arreglo de numeros
Este reto pudo hacerce de una manera mas simple, pero quice darle una poco de "vida" asi que hice que los valores que tomara el arreglo de numeros sean completamente aleatoreos

```python
import random #Los valores que tomara el arreglo seran completamente aleatoreos :)
arreglo=[]
for i in range(19):
  arreglo.append(random.randint(0,9)) 
print(arreglo)
ceros=arreglo.count(0)
print("Hay un total de %s ceros en la lista" % ceros)
```
**Ejemplos de salidas aleatoreas:**

[6, 1, 4, 8, 3, 4, 8, 8, 5, 6, 6, 2, 7, 4, 7, 4, 0, 0, 4, 8]

Hay un total de 2 ceros en la lista

-------------------------------------------------------------------

[0, 6, 4, 5, 8, 1, 2, 0, 4, 0, 6, 5, 0, 0, 8, 1, 5, 0, 9]

Hay un total de 6 ceros en la lista

-------------------------------------------------------------------

[2, 1, 7, 1, 4, 4, 5, 0, 9, 5, 7, 4, 2, 1, 9, 9, 1, 7, 1]

Hay un total de 1 ceros en la lista
