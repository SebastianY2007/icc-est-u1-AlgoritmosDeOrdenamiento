# Comparación de Algoritmos de Ordenamiento

## Enlace al Repositorio
[GitHub - Práctica Algoritmos de Ordenamiento] (https://github.com/SebastianY2007/icc-est-u1-AlgoritmosDeOrdenamiento))  

---

## Descripción

Este proyecto compara el desempeño de cinco algoritmos de ordenamiento:

- Bubble Sort  
- Bubble Sort con ajuste  
- Selection Sort  
- Insertion Sort  
- Shell Sort

El objetivo es medir el tiempo de ejecución de cada algoritmo con distintos tamaños de arreglos y mostrar los resultados mediante gráficas.

---

## Dependencias
- Python 3.13.0
- matplotlib

---

## Generación de Datos

Los arreglos aleatorios fueron generados de forma acumulativa, cumpliendo con el criterio de que los datos de un arreglo más pequeño estén contenidos al inicio de los arreglos mayores.

Ejemplo:

- Arreglo de 5000 elementos:  
  `[23, 405, 12, 28001, 34, 5006, 78, 90, 11, 4443]`

- Arreglo de 10000 elementos:  
  `[23, 405, 12, 28001, 34, 5006, 78, 90, 11, 4443, 67, 89, 24, ...]`

---

## Resultados Obtenidos

### Tabla de Resultados (en segundos)

| Tamaño del Arreglo |  Bubble  | Bubble Mejorado  | Selección | Inserción |  Shell |
|--------------------|----------|------------------|-----------|-----------|--------|
| 5000               | 0.7053   | 0.9242           | 0.0005    | 0.4158    | 0.0097 |
| 10000              | 2.4300   | 3.5123           | 0.0010    | 1.5831    | 0.0204 |
| 30000              | 21.1928  |  32.3002         |0.0030     | 14.2165   | 0.0746 |
| 50000              | 60.2148  | 89.0398          | 0.0048    | 39.9810   | 0.1397 |
| 100000             | 247.5716 | 578.8791         | 0.0218    | 403.3959  | 0.8842 |

---

## Gráfica Comparativa

Se generó una gráfica donde se visualiza el comportamiento de cada algoritmo en función del tamaño del arreglo:

- Eje X: Cantidad de elementos
- Eje Y: Tiempo en segundos

![Grafica de Tiempos](https://github.com/user-attachments/assets/8478f76f-0122-4393-99db-55b1e3cbb72f) 

---

### Análisis de Resultados

- **Bubble Sort**: De complejidad **O(n²)**. Su tiempo crece exponencialmente y es poco eficiente con grandes volúmenes de datos.
- **Bubble Sort con ajuste**: También **O(n²)**, aunque presenta una leve mejora si detecta ordenación parcial.
- **Selection Sort**: Con complejidad **O(n²)**, es más estable que Bubble y ligeramente más eficiente.
- **Insertion Sort**: Muy efectivo con arreglos parcialmente ordenados. Su rendimiento es **O(n²)** en el peor caso y **O(n)** en el mejor.
- **Shell Sort**: El más eficiente entre los implementados. Su rendimiento es cercano a **O(n log n)**, mostrando tiempos muy bajos incluso con grandes volúmenes.

### Conclusiones

- **Shell Sort** es claramente superior en eficiencia para cualquier tamaño de datos.
- Algoritmos con complejidad cuadrática como Bubble, Selection e Insertion deben evitarse para arreglos grandes.
- La complejidad teórica se refleja fielmente en los resultados empíricos.
- Es importante elegir el algoritmo adecuado según la situación del arreglo (ordenado, aleatorio, etc.).

---

## Recomendaciones

- No utilizar Bubble Sort en producción.
- Insertion puede ser útil en arreglos pequeños o parcialmente ordenados.
- Shell Sort es una excelente alternativa para problemas reales donde no se implementan algoritmos como Merge o Quick Sort.
- Revisar teoría de algoritmos y practicar análisis de complejidad.

---

## Cómo Ejecutar

1. Clonar el repositorio:
```bash
git clone https://github.com/SebastianY2007/icc-est-u1-AlgoritmosDeOrdenamiento
cd proyecto-ordenamiento
```

2. Instalar dependencias:
```bash
pip install matplotlib
```

3. Ejecutar el programa:
```bash
python app.py
```

4. Salida esperada (Aproximadamente)
```bash
Medir tiempo de arreglo 1 (5000)
Tiempo con Bubble Sort: 0.7053s
Tiempo con Bubble Sort (ajustado): 0.9242s
Tiempo con Selection Sort: 0.0005s
Tiempo con Insertion Sort: 0.4158s
Tiempo con Shell Sort: 0.0097s

Medir tiempo de arreglo 2 (10000)
Tiempo con Bubble Sort: 2.4300s
Tiempo con Bubble Sort (ajustado): 3.5123s
Tiempo con Selection Sort: 0.0010s
Tiempo con Insertion Sort: 1.5831s
Tiempo con Shell Sort: 0.0204s

Medir tiempo de arreglo 3 (30000)
Tiempo con Bubble Sort: 21.1928s
Tiempo con Bubble Sort (ajustado): 32.3002s
Tiempo con Selection Sort: 0.0030s
Tiempo con Insertion Sort: 14.2165s
Tiempo con Shell Sort: 0.0746s

Medir tiempo de arreglo 4 (50000)
Tiempo con Bubble Sort: 60.2148s
Tiempo con Bubble Sort (ajustado): 89.0398s
Tiempo con Selection Sort: 0.0048s
Tiempo con Insertion Sort: 39.9810s
Tiempo con Shell Sort: 0.1397s

Medir tiempo de arreglo 5 (100000)
Tiempo con Bubble Sort: 247.5716s
Tiempo con Bubble Sort (ajustado): 578.8791s
Tiempo con Selection Sort: 0.0218s
Tiempo con Insertion Sort: 403.3959s
Tiempo con Shell Sort: 0.8842s
```

## Autores
- Sebastian Yupangui
- Javier Barrezueta

## Resultado(s) Obtenido(s)
- Aprendizaje del comportamiento real de algoritmos de ordenamiento.
- Capacidad de medición empírica del rendimiento de algoritmos.
- Identificación del algoritmo más eficiente según el tamaño y orden del arreglo.

## Conclusiones Finales
- Se confirmó que algoritmos de ordenamiento tienen rendimientos distintos según su complejidad.
- Shell Sort mostró ser el algoritmo más eficiente para todos los tamaños de prueba.
- Algoritmos O(n²) son ineficaces para tamaños grandes.
- Este tipo de análisis permite tomar decisiones informadas al elegir estructuras y algoritmos.
