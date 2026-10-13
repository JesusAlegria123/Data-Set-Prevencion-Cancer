# Preprocesamiento de imágenes del dataset HAM10000

**Universidad Nacional de San Antonio Abad del Cusco**
**Curso:** Visión Computacional — **Docente:** Hans Harley C.

Análisis y preprocesamiento de imágenes dermatoscópicas para la clasificación de lesiones cutáneas (HAM10000).

## Integrantes
- Jesus Augusto Alegria Mendoza — 215780
- Brandon Ccoyo Mejia — 210923
- Gustavo Pantoja Olave — 210939

## Dataset y archivos en Drive
📁 **Carpeta de Google Drive (dataset del proyecto):**
https://drive.google.com/drive/folders/1yG3neMo39Ywxi5MZsagBV-f5YMsCuKBs

> Si la carpeta no aparece en *Mi unidad*, ábrela en Drive → *Compartido conmigo* → clic derecho → **Organizar → Agregar acceso directo a Drive**.

## Contenido
| Ruta | Descripción |
|------|-------------|
| `notebooks/HAM10000_Preprocesamiento_Colab.ipynb` | Notebook autosuficiente para Google Colab |

## Qué hace el notebook
1. Entorno y rutas (montaje de Drive y módulos de apoyo `hamvc`)
2. Copia local e inventario de imágenes
3. Exploración de metadatos (clases, edad, sexo, localización)
4. Estructura por lesión y validación de calidad
5. Pipeline: recorte de bordes negros → eliminación de vello → constancia de color (Shades of Gray) → cuadrado + redimensión
6. Ejecución sobre todo el dataset (paralela y reanudable)
7. Detección de casi-duplicados (pHash)
8. Partición train/val/test sin fuga (`StratifiedGroupKFold`)
9. Estadísticas de entrenamiento y manejo del desbalance

## Cómo ejecutarlo
1. Abre el notebook en Colab (Archivo → Abrir cuaderno → GitHub, o súbelo).
2. Asegúrate de tener acceso a la carpeta de Drive indicada arriba.
3. Ejecuta las celdas en orden.

Dependencias: ver `requirements.txt` (Colab las instala en la primera celda).
