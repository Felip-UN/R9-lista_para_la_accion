# R9-lista_para_la_accion
## Retos
1. Desarrollar un algoritmo que calcule el promedio de un arreglo de reales
2. Desarrollar un algoritmo que calcule el producto punto de dos arreglos de números enteros (reales) de igual tamaño
3. Hacer un algoritmo que deje al final de un arreglo de números todos los ceros que aparezcan en dicho arreglo
# Desarrollo
## 1.
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
## 2.
