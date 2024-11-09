# Propuesta de examen
**Objetivo:**
* Crear archivos y aplicar formatos necesarios con aplicaciones google.
* Generar nuevos datos con analisis estadístico en colab
* Guardar en Github
* Publicar en netlify

---
  
# Análisis de Ventas Tecnológicas

Este proyecto analiza las ventas de productos tecnológicos durante el año 2023.

# Estructura del Proyecto

- `index.html`: Página principal del proyecto
- `styles.css`: Estilos de la página
- `netlify.toml`: Configuración para publicación en netlify
- `informe_ventas.doc`: Documento con el informe detallado
- `ventas_tecnologia.csv`: Datos de ventas en formato CSV
- `ventas_analisis.ipynb`: Notebook de Jupyter con el análisis

## Visualización

Puedes ver el proyecto desplegado en: [(https://proyectointeg1.netlify.app/)]

## 1. Archivo ventas_tecnologia.csv
```csv
Mes,Laptops,Smartphones,Tablets,Auriculares,SmartTV
Enero 2023,45,120,35,89,12
Febrero 2023,38,145,42,95,15
Marzo 2023,52,135,38,102,18
Abril 2023,49,155,45,115,20
Mayo 2023,55,160,48,125,22
Junio 2023,60,175,52,135,25
Julio 2023,65,185,55,142,28
Agosto 2023,58,195,58,148,24
Septiembre 2023,62,180,54,138,26
Octubre 2023,70,190,60,155,30
Noviembre 2023,85,210,65,175,35
Diciembre 2023,95,230,70,190,40
```

## 2. Archivo informe_ventas.doc
_Redacta lo siguiente para este archivo_
 
> # Informe de Ventas de Productos Tecnológicos 2023
>
> ## Objetivo
> Este informe presenta un análisis detallado de las ventas de productos tecnológicos durante el año 2023, incluyendo laptops, smartphones, tablets, auriculares y Smart TVs.
> 
> ## Metodología
> Los datos fueron recopilados mensualmente y almacenados en formato CSV para su posterior análisis utilizando Google Colab. Se realizaron análisis de tendencias y patrones de ventas para cada categoría de producto.
> 
> ## Datos
> Los datos incluyen las siguientes categorías:
> - Laptops
> - Smartphones
> - Tablets
> - Auriculares
> - Smart TVs
> 
> ## Análisis
> El análisis se realizará utilizando Python en Google Colab, donde se generarán visualizaciones y estadísticas descriptivas de los datos.
> 
> ## Conclusiones
> [Este espacio será completado después del análisis en Colab]
>
---

## 3. Código para Google Colab (ventas_analisis.ipynb)
```python
# Importar librerías necesarias
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns

# Cargar datos desde GitHub
# Reemplazar con tu URL de GitHub raw
url = 'URL_DE_TU_ARCHIVO_CSV_EN_GITHUB'
df = pd.read_csv(url)

# Crear gráfico de líneas para todas las categorías
plt.figure(figsize=(15, 8))
for columna in df.columns[1:]:  # Excluimos la columna 'Mes'
    plt.plot(df['Mes'], df[columna], marker='o', label=columna)

plt.title('Ventas de Productos Tecnológicos 2023')
plt.xlabel('Mes')
plt.ylabel('Unidades Vendidas')
plt.xticks(rotation=45)
plt.legend()
plt.grid(True)
plt.tight_layout()
plt.show()

# Espacio para análisis adicional del alumno
# [AQUÍ EL ALUMNO PUEDE AGREGAR MÁS CÓDIGO]
"""
Ideas para análisis adicional:
1. Calcular estadísticas descriptivas
2. Crear gráficos de barras para comparar categorías
3. Analizar tendencias estacionales
4. Calcular correlaciones entre productos
5. Crear visualizaciones personalizadas
"""

```

## 4. Instrucciones para implementación
### Pasos iniciales con Google:
1. Tener abierto su usuario de google
2. Utiliza aplicaciones de google para abrir documentos, Hoja de Cálculos
3. Genera/crea los archivos *informe_ventas.doc* y *ventas_tecnologia.csv*

### Pasos para descargar desde Google Drive a tu computadora local:
Abre Google Drive en tu navegador
Selecciona los archivos que quieres subir a GitHub
Haz clic derecho y selecciona "Descargar"
Los archivos se guardarán en tu carpeta de descargas local

### Pasos para GitHub:
1. Abrir con tu usuario Github
2. Crear un nuevo repositorio en GitHub llamado **proyecto_integrado_1**
3. Subir los archivos:
   - ventas_tecnologia.csv
   - informe_ventas.doc
4. Crea los siguientes archivos: *ventas_analisis.ipynb*, *index.html*, *style.css*, *netlify.toml*  
   - Utiliza los archivos disponibles en este repositorio y copia el código en tus archivos.

### Pasos para Google Colab:
1. Abrir Google Colab
2. Crear un nuevo notebook
3. Importar el código proporcionado
4. Reemplazar 'URL_DE_TU_ARCHIVO_CSV_EN_GITHUB' con la URL raw del archivo CSV en GitHub
5. Ejecutar el análisis
6. Guardar el notebook en GitHub

### Pasos para Netlify:
1. Abrir tu cuenta en Netlify
2. Conectar con el repositorio de GitHub
3. Configurar la implementación:
   - Directorio base: /
   - Comando de construcción: (dejar en blanco)
   - Directorio de publicación: /

### Notas importantes:
- Para que el CSV sea accesible desde Colab, asegúrate de usar la URL "raw" de GitHub
- El notebook de Colab debe estar configurado para ser público
- Recuerda guardar frecuentemente los cambios en GitHub

## Pasos para ENVIAR SU PROYECTO
Pulsar en el vinculo para enviar su proyecto

[(https://forms.gle/dJJeVwetDWroajTcA))]
