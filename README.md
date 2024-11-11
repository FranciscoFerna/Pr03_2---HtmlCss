
# Proyecto ITBFlix

## Descripción del Proyecto
Este proyecto consiste en crear una página web de películas y series utilizando HTML5 y CSS, sin el uso de frameworks. El diseño incluye una **página principal** con enlaces hacia **páginas de detalles**, un **listado de películas o series**, y una **página de contacto o encuesta**. La página principal incluye un menú con enlaces que cambian de aspecto al pasar el cursor y permanece fijo al hacer scroll.

## Paleta de Colores
Para el diseño visual de la página, he usado la siguiente paleta de colores:
- **Rojo Principal**: `#E03C31`
- **Rojo Oscuro**: `#85112F`
- **Rosa Claro**: `#ec867ff5`
- **Negro** y **Blanco** para texto y fondos

## Estructura del Proyecto
El proyecto se organiza en una carpeta con el nombre `[FernandezFrancisco]`, que contiene todo el código fuente y los recursos del proyecto. A continuación, se detalla la estructura de carpetas y archivos.

```
FernandezFrancisco/
├── index.html                # Página principal de la web
├── peliculas.html            # Listado de películas y series
├── contacto.html             # Página de contacto y encuesta
├── detalle-pelicula.html     # Página de detalle de una película o serie específica
├── css/
│   └── styles.css            # Archivo principal de estilos CSS
├── src/
│   ├── images/               # Carpeta con todas las imágenes usadas en la página
│   │   └── (imágenes del proyecto)
│   └── (otros recursos)
├── README.md                 # Instrucciones detalladas del proyecto
└── FernandezFrancisco_Retro.pdf  # Documento PDF con retrospectiva del proyecto
```

## Instrucciones de Instalación
Para ver el proyecto en funcionamiento:
1. Descarga el archivo `FernandezFrancisco.zip` y descomprímelo.
2. Abre el archivo `index.html` en tu navegador para acceder a la página principal.
3. Usa el menú de navegación para visitar las diferentes secciones del sitio: página de detalles, listado de películas o series, y página de contacto.

## Detalles de Cada Página
### 1. Página Principal (`index.html`)
- **Funcionalidad**: Presenta una vista general de la web, con una introducción y enlaces a los detalles de las películas y series.
- **Menú Fijo**: El menú de navegación permanece fijo en la parte superior cuando se hace scroll.
- **Estilos Interactivos**: Los enlaces y botones cambian de estilo al pasar el cursor sobre ellos.

### 2. Página de Detalle de Película/Serie (`detalle-pelicula.html`)
- **Descripción**: Página específica para mostrar información detallada de una película o serie seleccionada. Se incluye imagen, sinopsis, calificación y otros datos importantes.
- **Enlace de Navegación**: Accesible desde la página principal mediante el enlace “Ver la película” o “Ver la serie”.

### 3. Listado de Películas y Series (`peliculas.html`)
- **Descripción**: Página que muestra un listado de películas y series, organizado en cuadrículas usando Flexbox.
- **Datos por Elemento**: Cada película o serie incluye una imagen, título, edad recomendada, puntuación y un enlace al detalle.
- **Estilo Distinto**: Aunque sigue el estilo general, esta página presenta un diseño ligeramente diferente al de la página principal.

### 4. Página de Contacto/Encuesta (`contacto.html`)
- **Formulario**: Contiene un formulario con distintos tipos de campos (mínimo 6) para permitir comentarios, darse de alta, o responder una encuesta.
- **Método GET**: El formulario usa el método GET para enviar datos.

## Diseño y Estilo
- **HTML Semántico**: La estructura HTML sigue una jerarquía y valor semántico adecuado con etiquetas como `header`, `footer`, `section`, `article`, etc.
- **CSS Modular**: Todos los estilos están definidos en un solo archivo CSS (`styles.css`) de manera clara y organizada, usando solo clases.
- **Flexbox**: Uso de Flexbox para organizar el contenido en la mayoría de las secciones y asegurar la adaptabilidad del diseño.
- **Interactividad**: Se aplican cambios de estilo en botones y enlaces al pasar el cursor, dando un aspecto interactivo a la página.

## Retrospectiva (Archivo PDF)
He incluido un archivo llamado `FernandezFrancisco_Retro.pdf` en el que reflejo:
- Mis decisiones de diseño.
- Los desafíos que enfrenté.
- Lo que he aprendido con esta práctica y aspectos que considero interesantes o útiles.
- Las dificultades que encontré y cómo las superé.

## Capturas de Pantalla
En el archivo `FernandezFrancisco_Retro.pdf`, también he añadido capturas de pantalla de cada una de las páginas para ilustrar el diseño final.

## Contacto
Para cualquier pregunta o comentario sobre el proyecto, puedes contactarme en [fraanfeernaandeez@gmail.com].

---

Este proyecto fue desarrollado como parte de una práctica para aprender y aplicar HTML5 y CSS. La claridad en la organización del código y la escalabilidad del diseño fueron fundamentales en este desarrollo. ¡Gracias por revisar mi trabajo!
```