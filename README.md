Aquí tienes la documentación sin el código:

---

# Documentación del Programa de Búsqueda Semántica

## 1. Introducción al Proyecto

Este proyecto desarrolla un sistema de búsqueda semántica para encontrar documentos relevantes en un archivo JSON que contiene información académica, incluyendo autores, títulos, categorías y resúmenes de artículos científicos. Utiliza embeddings generados por modelos de lenguaje preentrenados para convertir textos en vectores. Luego, emplea estos vectores para realizar búsquedas semánticas precisas, permitiendo que las consultas se comparen con los documentos en el dataset.

## 2. Instrucciones de Instalación

Para configurar el entorno y ejecutar el programa, sigue estos pasos:

1. **Instalar las Bibliotecas Necesarias:**

   Debes instalar las bibliotecas `transformers` y `sentence-transformers` utilizando el gestor de paquetes de Python. Estas bibliotecas son esenciales para trabajar con modelos preentrenados y generar embeddings de texto.

2. **Preparar el Entorno:**

   Asegúrate de utilizar un entorno compatible con Google Colab o un entorno local donde tengas acceso a las bibliotecas necesarias. Si estás trabajando en Google Colab, puedes instalar las bibliotecas directamente en una celda del notebook.

## 3. Guía de Uso

### 3.1. Subir y Cargar Datos

Sube el archivo JSON que contiene los datos de los artículos científicos. El archivo debe tener las columnas `authors`, `title`, `categories` y `abstract`. Una vez subido, se creará un DataFrame para almacenar y procesar los datos.

### 3.2. Preprocesar y Generar Embeddings

Se carga un modelo preentrenado de BERT, y se preprocesa el texto de las columnas del DataFrame para convertirlo a minúsculas y eliminar espacios innecesarios. A continuación, se generan embeddings para cada entrada en el DataFrame utilizando el modelo preentrenado. Estos embeddings representan el contenido textual en forma de vectores.

### 3.3. Realizar Búsquedas Semánticas

Se define una función para realizar búsquedas semánticas. La consulta se combina en una sola cadena y se convierte en un embedding utilizando el mismo modelo que se utilizó para los documentos. La similitud entre el embedding de la consulta y los embeddings de los documentos se calcula utilizando similitud coseno. Los documentos más similares a la consulta se seleccionan y se presentan como resultados.

### 3.4. Visualizar Embeddings

Se reduce la dimensionalidad de los embeddings a dos dimensiones utilizando PCA (Análisis de Componentes Principales) para facilitar la visualización. Los embeddings se grafican en un diagrama de dispersión donde cada punto representa un documento. La coloración indica la similitud con la consulta.

### 3.5. Evaluar la Búsqueda

Se define una función para evaluar la efectividad del sistema de búsqueda. La evaluación se basa en la precisión y el recall de los documentos recuperados en comparación con los documentos relevantes esperados. Se calculan estos valores para evaluar el rendimiento del sistema y su capacidad para recuperar documentos relevantes.

---

Esta documentación proporciona una visión general del funcionamiento del sistema de búsqueda semántica, así como instrucciones para su instalación, uso y evaluación.
