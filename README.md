# TrazoStudio

**Editor de imágenes, selección de regiones y vectorización de contornos para dibujos técnicos y planos.**

TrazoStudio es una aplicación web desarrollada en HTML, CSS y JavaScript que permite importar imágenes, seleccionar zonas de interés, procesarlas y convertir sus contornos en archivos vectoriales compatibles con herramientas de diseño y CAD.

La aplicación reúne en una misma interfaz herramientas de recorte, segmentación por color, detección de contornos, edición manual, sombreado y exportación, con el objetivo de facilitar la preparación de imágenes para su posterior procesamiento.

## Funcionalidades principales

### Importación y preparación de imágenes
- Carga imágenes para trabajar directamente en el editor.
- Visualiza la imagen original y el resultado procesado.
- Utiliza zoom, ajuste a pantalla y cuadrícula para facilitar el trabajo.

### Selección y recorte
Permite delimitar la zona que se desea conservar mediante diferentes herramientas:

- **Rectángulo:** selecciona una región rectangular.
- **Círculo:** delimita una zona circular.
- **Selección libre:** dibuja el contorno a mano alzada.
- **Selección por puntos:** marca vértices sucesivos que se unen mediante líneas para definir un polígono cerrado.

Una vez definida la selección, es posible recortarla, eliminar zonas o continuar directamente con el procesamiento de la imagen.

### Segmentación por color
Permite seleccionar un color de la imagen y ajustar la tolerancia RGB para eliminar los píxeles similares o conservar únicamente el color elegido. Esta función ayuda a limpiar fondos y aislar elementos antes de generar los contornos.

### Generación y edición de contornos
La aplicación utiliza técnicas de procesamiento de imágenes, con OpenCV.js cuando está disponible, para generar contornos a partir de la imagen.

Incluye controles para ajustar umbrales, desenfoque, grosor de línea e inversión, además de perfiles de trazado. Después de generar los contornos, es posible dibujar, pintar, borrar y deshacer trazos manualmente.

### Sombreado tonal
Permite generar y ajustar sombreado mediante controles de brillo y contraste. El resultado se puede incorporar a la exportación como isolíneas para determinados flujos de trabajo CAD.

### Exportación
Los resultados se pueden descargar en distintos formatos:

- **PNG:** imagen de mapa de bits.
- **JPG:** imagen comprimida.
- **SVG:** contornos vectoriales.
- **DXF:** geometría para aplicaciones CAD, con opciones para incluir contornos y sombreado.

La exportación DXF permite configurar el ancho del dibujo en milímetros y ajustar el nivel de detalle del sombreado cuando está disponible.

## Gestión de proyectos

TrazoStudio también incluye herramientas para organizar el trabajo:

- Guardar, recuperar y categorizar proyectos.
- Importar y exportar copias de proyectos en formato JSON.
- Compartir proyectos mediante las opciones disponibles en el navegador.
- Consultar un calendario de proyectos y eventos.
- Organizar tareas mediante un tablero Kanban.
- Crear copias de seguridad locales y recuperar copias anteriores.
- Utilizar un tutorial guiado para conocer la interfaz.

Los proyectos se guardan principalmente en el almacenamiento del navegador, con mecanismos alternativos de persistencia cuando están disponibles.

## Cómo funciona

1. **Importar:** carga la imagen o el plano que deseas procesar.
2. **Seleccionar:** delimita el elemento mediante rectángulo, círculo, trazo libre o puntos.
3. **Limpiar:** elimina colores o regiones que no necesitas.
4. **Procesar:** genera los contornos y ajusta los parámetros hasta obtener el resultado deseado.
5. **Editar:** corrige manualmente líneas y trazos, y aplica sombreado si es necesario.
6. **Exportar:** descarga el resultado como imagen, SVG o DXF para continuar trabajando en otras aplicaciones.

## Tecnología

- HTML5
- CSS3
- JavaScript
- Canvas API para la visualización y manipulación de imágenes
- OpenCV.js para funciones de procesamiento de imágenes
- IndexedDB y localStorage para guardar datos en el navegador
- Formatos PNG, JPG, SVG, DXF y JSON

## Ejecución

TrazoStudio está diseñado como una aplicación web de archivo HTML. Para probarlo, descarga el archivo `TrazoStudio V1.28.html` y ábrelo en un navegador moderno.

Algunas funciones utilizan recursos externos que se cargan desde Internet. La disponibilidad de esos recursos puede afectar a determinadas operaciones de procesamiento.

## Estado del proyecto

TrazoStudio continúa evolucionando con mejoras en la selección de regiones, limpieza de imágenes, generación de contornos y organización de proyectos.

La detección automática de objetos se basa en técnicas de procesamiento de imágenes; no debe confundirse con una segmentación avanzada mediante IA externa, que requeriría una integración adicional.

---

**TrazoStudio: de la imagen al contorno, del contorno al vector.**
