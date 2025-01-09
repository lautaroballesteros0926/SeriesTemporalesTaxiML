# **Predicción de Demanda de Taxis con Series Temporales - Sweet Lift Taxi**  

## **Descripción del Proyecto**  

La compañía **Sweet Lift Taxi** se enfrenta al desafío de predecir la cantidad de pedidos de taxis para la próxima hora, especialmente durante las horas pico en los aeropuertos. Este proyecto se centra en el análisis de **series temporales** y la creación de un modelo predictivo para anticipar la demanda de taxis, optimizando así los recursos y mejorando el servicio.  

### **Objetivos Principales**  
- **Predecir la demanda de taxis** en función de datos históricos de pedidos.  
- **Optimizar la asignación de conductores** durante las horas de mayor demanda.  
- Minimizar el **error de predicción** usando la métrica RECM, con un valor objetivo de **48** en el conjunto de prueba.  

## **Enfoque del Proyecto**  

1. **Preprocesamiento de Datos**:  
   - Remuestreo de los datos para asegurar que cada punto de datos se alinee dentro de intervalos de una hora.  
   - Análisis de las características de los datos, incluyendo variables temporales clave, como la hora y la cantidad de pedidos.  

2. **Modelos Utilizados**:  
   - Se entrenaron diversos modelos de **series temporales**, adaptando los hiperparámetros para encontrar la mejor combinación.  
   - Evaluación del rendimiento utilizando un **10% de los datos** para la muestra de prueba.  
   - Se utilizaron modelos como **Bosque de regresion aleatorio** y **LIghtBoost** para la predicción, con ajustes finos para mejorar la precisión.  

3. **Evaluación y Resultados**:  
   - El modelo final fue evaluado utilizando la métrica **RECM**, con un rendimiento superior al objetivo de **48** (es decir menor a este valor)en el conjunto de prueba.  
   - Análisis de los resultados para identificar patrones y mejorar las estrategias de asignación de recursos.  

## **Tecnologías Utilizadas**  

- **Lenguaje**: Python  
- **Bibliotecas**:  
  - `pandas` y `numpy` para manipulación de datos.  
  - `matplotlib` y `seaborn` para visualización de datos.  
  - **Modelos de series temporales**:  `XGBoost`.  
  - **Evaluación de modelos**: `scikit-learn`.  

## **Estructura del Proyecto**  

- **`taxi.csv`**: Conjunto de datos con la información histórica de los pedidos de taxis.  
- **`preprocesamiento.py`**: Script que realiza la limpieza y el remuestreo de los datos.  
- **`model_training.py`**: Entrenamiento y ajuste de los modelos predictivos.  
- **`evaluation.py`**: Evaluación de la precisión del modelo con la métrica RECM.  
- **`README.md`**: Documentación y explicación detallada del proyecto.  

## **Cómo Ejecutar el Proyecto**  

1. **Clona el repositorio**:  
   ```bash
   git clone https://github.com/lautaroballesteros0926/SeriesTemporalesTaxiML.git

   ```  

2. **Instala las dependencias**:  
   ```bash
   pip install -r requirements.txt
   ```  

3. **Ejecuta el script de preprocesamiento**:  
   ```bash
   python preprocesamiento.py
   ```  

4. **Entrena los modelos**:  
   ```bash
   python model_training.py
   ```  

5. **Evalúa el rendimiento**:  
   ```bash
   python evaluation.py
   ```  

## **Impacto del Proyecto**  

Este modelo tiene el potencial de optimizar significativamente la asignación de conductores, reduciendo los tiempos de espera y mejorando la experiencia del cliente. Al predecir con mayor precisión la demanda de taxis, **Sweet Lift Taxi** puede ofrecer un servicio más eficiente y atractivo para los pasajeros, especialmente durante las horas pico.

## **Próximos Pasos**  

- Implementar modelos en tiempo real para ofrecer predicciones instantáneas.  
- Integrar el modelo en la infraestructura de la empresa para una gestión dinámica de los recursos.  
- Experimentar con otras técnicas avanzadas de series temporales y aprendizaje profundo para mejorar la precisión.
