MODELADO CINÉTICO DE LA UNIÓN DE SONDAS FLUORESCENTES Y ANÁLISIS DE FLUJO EN BIOPELÍCULAS 

![Python](https://img.shields.io/badge/python-3.9+-blue.svg)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange.svg)
![SciPy](https://img.shields.io/badge/SciPy-Data_Analysis-success.svg)

Este repositorio contiene el análisis computacional utilizado para investigar la cinética de unión y los efectos de flujo de sondas fluorescentes en biopelículas de *E. coli* TRMG1655. Proyecto realizado en las Pasantias de Investigacion InspiraSTEM 2026 y presentado en la Sesión de Posteres InspiraSTEM 2026.


📌 Estructura del Proyecto
El análisis está dividido en 6 Jupyter Notebooks modulares para facilitar su validación científica:
*   **`1_tasa_asociacion.ipynb`**: Aísla la inyección de la sonda y ajusta un modelo de pseudo-primer orden.
*   **`2_tasa_disociacion.ipynb`**: Modela el decaimiento exponencial durante la fase de lavado.
*   **`3_calculo_parametros_finales.ipynb`**: Calcula la afinidad aparente y la fuerza de retención molecular.
*   **`4_curvas_finales.ipynb`**: Contiene los datos espectrofluorométricos crudos. Las series de datos han sido segmentadas en sus fases respectivas (asociación tras la inyección y disociación tras el lavado).
*   **`5_figura_final.ipynb`**: Reconstruye los modelos teóricos superpuestos a los datos experimentales para generar una gráfica de calidad de publicación.
*   **`6_practica_datos_numero_damkohler.ipynb`**: Análisis de dinámica de fluidos para descartar artefactos de arrastre (*bulk flow*).


📂 Datos Experimentales (Datasets)
El análisis se fundamenta en un flujo de procesamiento de datos estructurado, desde la captura hasta el modelado:
*   **`DatosEnCrudo.xlsx`**: Datos originales obtenidos directamente del equipo sin procesamiento previo. Contiene la serie de tiempo completa y las lecturas de fluorescencia base.
*   **`DatosLimpiosFasedeAsociacion.xlsx`**: Subconjunto de datos procesados, filtrados y normalizados en tiempo para la fase de inyección de la sonda. Es el *input* directo para calcular la tasa observada ($k_{obs}$).
*   **`DatosLimpiosFasedeDisociacion.xlsx`**: Subconjunto de datos procesados correspondientes exclusivamente a la fase de lavado con buffer. Es el *input* directo para calcular la tasa de disociación ($k_{off}$).
*   **`simulated_damkohler_scenario_data.csv`**: Conjunto de datos con simulaciones a diferentes tasas de flujo volumétrico (0.005, 0.05 y 0.5 mL/min). Se utiliza en el Script 5 para calcular el Número de Damköhler y separar el efecto biológico del arrastre físico.


🚀 Cómo visualizar el proyecto
Al estar estructurado en formato `.ipynb`, puedes hacer clic en cualquiera de los archivos directamente en este repositorio para leer el código, visualizar y analizar las gráficas sin necesidad de ejecutar un entorno local.



👨‍💻 Autor
Eduardo Espino
Estudiante de Ingenieria en Sistemas
Universidad Católica de El Salvador
