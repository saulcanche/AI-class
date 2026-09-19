# Reporte Ejercicio 1 - Búsqueda en el Mapa de Rumania

## 1. Ciudades elegidas
Evaluaremos la ruta de Oradea a Bucharest. Los algoritmos muestran comportamientos distintos en el pathfinding al utilizar diferentes criterios para la expansión de estados.

## 2. Resultados por Algoritmo

| Algoritmo | Depth (saltos) | Costo | Nodos Expandidos | Ruta |
| :---: | :---: | :---: | :---: | --- |
| **BFS** | 3 | 461 km | 5 | Oradea, Sibiu, Fagaras, Bucharest |
| **UCS** | 4 | 429 km | 10 | Oradea, Sibiu, Rimnicu Vilcea, Pitesti, Bucharest |
| **DFS** | 9 | 1024 km | 9 | Oradea, Sibiu, Arad, Timisoara, Lugoj, Mehadia, Drobeta, Craiova, Pitesti, Bucharest |
| **DLS (lim=2)** | - | - | 3 | `cutoff` |
| **DLS (lim=3)** | 3 | 461 km | 4 | Oradea, Sibiu, Fagaras, Bucharest |
| **IDS** | 3 | 461 km | 8 | Oradea, Sibiu, Fagaras, Bucharest |

## 3. Análisis de las Búsquedas

BFS encuentra el shortest path asumiendo un grafo no ponderado. Toma la transición por Fagaras para llegar a la meta utilizando el mínimo número de aristas.

UCS es literalmente Dijkstra. El algoritmo expande los nodos basándose en el menor peso acumulado. Durante la relajación de las aristas, evalúa que procesar el subgrafo por Rimnicu Vilcea y Pitesti minimiza el costo global a 429 km, aceptando un salto extra para optimizar la métrica de peso.

DFS ejecuta su traversal de manera greedy sobre el orden lexicográfico de los nodos. Estando en Sibiu, hace la transición hacia Arad y avanza sobre esa rama profundizando en el árbol de recursión hasta tocar Bucharest de pura suerte. Retorna ese path larguísimo ignorando cualquier tipo de optimalidad en peso o profundidad.

DLS restringe la profundidad máxima del traversal. Con un límite de 2 el estado devuelve cutoff al detener la expansión. Con límite 3 alcanza el nodo objetivo. IDS aplica DFS incrementando la profundidad máxima progresivamente. Esto garantiza encontrar el camino con la menor cantidad de aristas como BFS, expandiendo unos cuantos nodos extra al reprocesar los estados superiores de la búsqueda.
