Jesus Julian Abreu 2021-0047

---

# Documentación del Programa de Búsqueda Semántica

## Importante:
El projecto se debe de correr en Google Colab, posteriormente cambiar a uso de la GPU:

Pasos para cambiar a la GPU en colab:
1. Click en entorno de ejecución
2. Cambiar tipo de entorna de ejecución
3. Elegir T4 GPU

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


---
Busqueda semantica
[https://colab.research.google.com/drive/1APwtTfHf5X-6ya2jOWSwI5fY5NbZOE8_#scrollTo=rfej_Fl64K00](https://colab.research.google.com/drive/1APwtTfHf5X-6ya2jOWSwI5fY5NbZOE8_#scrollTo=cA2XwPGt3B1g)
---
https://colab.research.google.com/drive/1GgOBCk1fqNqzeCHBlox4AII1Mu8hTq5J?usp=sharing 
https://colab.research.google.com/drive/1hsGUqNYwhlZgoabIktShvz_M5Bt6K4YV#scrollTo=vc1QFsjwn5e1 

