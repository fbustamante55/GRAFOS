# Proyecto GRAFOS - Estructuras de Datos

Este proyecto implementa dos estructuras de datos fundamentales en Java: **Árbol Binario de Búsqueda** y **Grafo Dirigido**, con aplicaciones prácticas en gestión de procesos de negocio (BPM).

## 📋 Descripción

El proyecto está dividido en dos partes principales:

### Parte 1: Árbol Binario de Búsqueda (BST)
Implementación de un árbol binario de búsqueda que permite:
- Insertar valores manteniendo el orden
- Recorrer el árbol en orden (inorden)
- Buscar si un valor existe en el árbol
- Obtener todos los nodos con valores impares

### Parte 2: Grafo Dirigido - MVP BPM
Implementación de un grafo dirigido que modela un proceso de negocio (BPM) con:
- Nodos que representan etapas del proceso con roles asociados
- Matriz de adyacencia para representar las relaciones entre etapas
- Aristas etiquetadas con acciones que conectan las etapas

## 🏗️ Estructura del Proyecto

```
119580779_CE3/
├── src/
│   └── main/
│       └── java/
│           └── CE3/
│               ├── App.java              # Clase principal con ejemplos de uso
│               ├── ArbolBinario.java     # Implementación del árbol binario
│               ├── Grafo.java            # Implementación del grafo dirigido
│               ├── Nodo.java            # Nodo para el árbol binario
│               └── NodoGrafo.java       # Nodo para el grafo (etapa + rol)
└── pom.xml                              # Configuración Maven
```

## 🔧 Requisitos

- **Java**: Versión 23 o superior
- **Maven**: Para compilar y ejecutar el proyecto

## 🚀 Compilación y Ejecución

### Compilar el proyecto

```bash
cd 119580779_CE3
mvn clean compile
```

### Ejecutar el programa

```bash
mvn exec:java
```

O directamente con Java:

```bash
java -cp target/classes CE3.App
```

## 📖 Uso

### Árbol Binario

El programa crea un árbol binario e inserta los siguientes valores: `50, 30, 80, 25, 17, 38, 65, 90, 78`

**Operaciones disponibles:**

- `insertar(int valor)`: Inserta un nuevo valor en el árbol
- `imprimir()`: Muestra el árbol en recorrido inorden
- `contiene(int valor)`: Verifica si un valor existe en el árbol
- `obtenerImpares()`: Retorna un arreglo con todos los valores impares del árbol

**Ejemplo de salida:**
```
Árbol (inorden): 17 25 30 38 50 65 78 80 90
El 17 sí se encuentra en el árbol.
El 63 no se encuentra en el árbol.
Los nodos impares del árbol son: 17, 25, 65
```

### Grafo BPM

El programa modela un proceso de negocio con las siguientes etapas:

1. **Inicio** (Rol: NA)
2. **Recibir Documentos** (Rol: Técnico)
3. **Analizar Solicitud** (Rol: Analista)
4. **Avanzar Continuar** (Rol: Aprobar)
5. **Solicitud** (Rol: Jefe)

**Operaciones disponibles:**

- `insertarNodo(String etapa, String rol)`: Agrega un nuevo nodo al grafo
- `establecerArista(int origen, int destino, String accion)`: Crea una relación entre nodos con una acción
- `imprimirMatriz()`: Muestra la matriz de adyacencia del grafo
- `imprimirNodos()`: Muestra la información de todos los nodos

**Ejemplo de salida:**
```
Matriz de Adyacencia:
-	Recibir	-	-	-	
-	-	Analizar	-	-	
-	-	-	Avanzar	-	
-	-	-	-	Continuar	
-	-	-	-	-	

Información de los nodos:
Nodo 0: Inicio (NA)
Nodo 1: Recibir Documentos (Técnico)
Nodo 2: Analizar Solicitud (Analista)
Nodo 3: Avanzar Continuar (Aprobar)
Nodo 4: Solicitud (Jefe)
```

## 📝 Clases Principales

### `ArbolBinario`
Clase que implementa un árbol binario de búsqueda con métodos recursivos para inserción, búsqueda y recorrido.

### `Grafo`
Clase que implementa un grafo dirigido usando una matriz de adyacencia. Cada arista puede tener una etiqueta (acción).

### `Nodo`
Representa un nodo del árbol binario con un valor entero y referencias a sus hijos izquierdo y derecho.

### `NodoGrafo`
Representa un nodo del grafo con una etapa (String) y un rol (String).

## 👤 Autor

**Fabia**

## 📄 Licencia

Este proyecto está bajo la licencia por defecto de NetBeans.

