# Linked-Lists
Different types of implementation of the Linked Lists in python

# Listas doblemente enlazadas
¿Qué son las listas soblemente enlazadas?
- Es una estructura de datos dinámica que se compone de un conjunto de nodos en secuencia enlazados mediante dos apuntadores (uno hacia adelante y otro hacia atrás).
- Una lista doblemente enlazada puede estar vacía o consistir de una secuencia de nodos, donde cada nodo contiene un dato y sabe dónde están tanto el siguiente como el anterior nodo.

![image](https://user-images.githubusercontent.com/129640150/236700135-214f6e8b-85a2-49ea-8291-2ff4a6e87869.png)

### Ventajas
- Se puede navegar y ser analizada en ambas direcciones. La referencia al siguiente nodo ayuda a mover hacia adelante y la referencia al nodo anterior ayuda a movernos en dirección contraria.
- Las operaciones básicas como agregar elemento y eliminar son fáciles de implementar.

### Desventajas
- Utilizan mas memoria que los arreglos debido al almacenamiento utilizado por sus apuntadores.
- Es necesario realizar algunos pasos adicionales para realizar operaciones de inserción y eliminación.

## Inserción de nodos
#### Ejemplo de inserción después de un nodo

![image](https://user-images.githubusercontent.com/129640150/236700288-e2106897-db87-4f8c-b3c2-d3b961fb64fa.png)

#### Ejemplo de inserción antes de un nodo

![image](https://user-images.githubusercontent.com/129640150/236700300-db43d864-e1a9-44e6-83e0-5ac7942b47e8.png)

## Invertir una lista doblemnte enlazada
1. Utilizaremos dos apuntadores de apoyo para movernos a través de la lista y lo que vamos a invertir no es el orden, si no las referencias de los nodos. Un apuntador p apuntara al primer nodo y un apuntador q apuntara al segundo nodo.
2. El primer paso es referenciar el apuntador siguiente del primer nodo a None ya que este se convertirá en el último nodo y el apuntador anterior hacia el segundo nodo ya que este se convertirá en el penúltimo nodo.
3. Una vez estableciendo estas bases utilizaremos un ciclo while para invertir las referencias de q y para movernos un lugar a la derecha de la lista.
4. En este punto comenzamos a invertir las referencias del nodo q, el anterior de q ahora será el siguiente de q y el siguiente ahora será p el cual es el anterior.
5. Después de esto nos movemos a la derecha de la lista y repetimos el proceso.
6. Al terminar todas las referencias ahora referenciamos a root al ultimo nodo de la lista el cual será ahora el primer nodo.
