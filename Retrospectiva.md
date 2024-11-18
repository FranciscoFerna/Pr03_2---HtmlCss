### Retrospectiva PR03_2-HTML-CSS 

### Metadatos Básicos  
En el `<head>`, incluí aspectos fundamentales:  
- **charset="UTF-8"**: Me aseguré de que la página soportara todos los caracteres necesarios, sin problemas de codificación.  
- **viewport**: Configuré la página para que fuera completamente responsive, ajustándose bien a dispositivos móviles.  

### Título y SEO  
- **title**: Definí un título descriptivo y directo que reflejara el propósito del sitio.  
- **description y keywords**: Añadí metadatos para mejorar la visibilidad en buscadores y optimizar el SEO. Esto ayuda a que el sitio tenga más alcance en búsquedas relacionadas.  

### Redes Sociales  
Implementé etiquetas específicas para mejorar cómo se comparte el contenido:  
- **Open Graph**: Adapté el contenido para que se viera genial al compartirlo en Facebook.  
- **Twitter Card**: Hice lo mismo pero pensando en Twitter, cuidando los detalles para optimizar su apariencia.  

### Enlace Canónico  
Usé una etiqueta canónica para informar a los motores de búsqueda cuál era la versión principal de una página. Esto evita problemas de contenido duplicado.  

### Iconos  
Configuré un favicon y un Apple Touch Icon para reforzar la identidad visual del sitio tanto en navegadores como en dispositivos Apple.

---

## `<header>`  

### Estructura del Header  
Al diseñar el `<header>`, lo dividí en dos secciones principales:  
1. **left-section**: Aquí coloqué el logo para que fuera fácilmente reconocible.  
   ```html
   <img src="ITBFlix-Logo.png" alt="ITBFlix Logo Oficial" />
   ```  
   Este detalle es clave para reforzar la identidad visual de ITBFlix.  
2. **right-section**: Incluí un menú de navegación con listas desordenadas (`<ul>`) y elementos (`<li>`). Esto permite acceder a las diferentes secciones del sitio, como "Inicio", "Series", "Películas", y "Contacto".  

### CSS del Header  
Usé CSS para lograr un diseño atractivo y funcional:  
- **Diseño Flex**: Implementé `display: flex` con `justify-content: space-between` para alinear y distribuir los elementos de manera eficiente.  
- **Estilo del Logo**: Ajusté su tamaño y márgenes para que fuera visualmente atractivo sin ocupar demasiado espacio.  
- **Estilo del Menú**: Modifiqué la lista para eliminar el estilo por defecto, le añadí un gap entre los elementos y estilicé los enlaces para hacerlos más llamativos (color blanco, texto en negrita y efectos al pasar el ratón).  

---

### Hero Section  

#### Estructura del Hero Section  
1. **Video de Fondo**  
   - Un video de fondo reproduce automáticamente un tráiler de Batman, con las propiedades `autoplay`, `muted`, `loop`, y `playsinline`. Esto asegura una experiencia fluida y sin interrupciones.  
   - Utilicé el atributo `poster` para mostrar una imagen mientras el video se carga, mejorando la percepción de carga del contenido.  

2. **Contenedor de Contenido**  
   - El `content-wrapper` incluye el título, descripción y botones de acción, destacando la información esencial sobre el video.  

#### Video  
```html
<video autoplay muted loop playsinline poster="batman-poster.jpg">
    <source src="batman-trailer.mp4" type="video/mp4">
</video>
```  

#### Título y Descripción  
- **Título (.title)**: Posicionado en la parte inferior del video y adaptado con `clamp` para un diseño responsivo.  
- **Descripción (.description)**: Breve y contextual, para informar al usuario sobre el contenido del video.  

#### Botones de Acción  
- **Botón Primario**: Llama al usuario a reproducir el contenido.  
- **Botón Secundario**: Proporciona acceso a más información.  

---

### CSS del Hero Section  
1. **Diseño Responsivo**  
   - Utilicé `clamp` para que los textos y botones se ajusten automáticamente a diferentes tamaños de pantalla.  

2. **Posicionamiento Absoluto**  
   - La clase `content-wrapper` está posicionada sobre el video con `position: absolute` para asegurar visibilidad.  

3. **Estilo de los Botones**  
   ```css
   .btn {
       padding: 10px 20px;
       border-radius: 5px;
       transition: all 0.3s ease;
   }
   .btn--primary {
       background-color: #ff5733;
       color: #fff;
   }
   .btn--secondary {
       background-color: #fff;
       color: #333;
   }
   .btn:hover {
       transform: scale(1.1);
       box-shadow: 0px 4px 6px rgba(0, 0, 0, 0.1);
   }
   ```  

---

### Sección de Películas  

#### 1. Estructura de la Sección  
- **Contenedor de Películas**: Agrupé todas las películas destacadas dentro de un `movies-wrapper`.  
- **Título de la Sección**: Incluí un encabezado (`h2`) para resaltar las "10 películas más populares hoy".  
- **Tarjetas de Películas**: Cada película está representada por un `article.movie-card` que incluye su póster, título y un badge opcional.  

#### 2. Tarjetas de Películas  
- **Imagen del Póster**: Utilicé un contenedor `.movie-poster-wrapper` para mantener proporciones consistentes y estilizar las imágenes con `object-fit: cover`.  
- **Badges**: Las etiquetas `.movie-badge` destacan las películas nuevas o relevantes.  
- **Nombres de Películas**: Cada tarjeta muestra el nombre de la película (`h3.movie-name`).  

#### 3. CSS de las Tarjetas de Películas  
1. **Estilo de las Tarjetas**  
   ```css
   .movie-card {
       border-radius: 10px;
       overflow: hidden;
       transition: transform 0.3s ease, box-shadow 0.3s ease;
   }
   .movie-card:hover {
       transform: scale(1.05);
       box-shadow: 0px 8px 15px rgba(0, 0, 0, 0.2);
   }
   ```  

2. **Posicionamiento de Badges**  
   ```css
   .movie-badge {
       position: absolute;
       top: 10px;
       left: 10px;
       background-color: #ff5733;
       color: #fff;
       padding: 5px 10px;
       border-radius: 20px;
   }
   ```  

3. **Ajuste de Imagen**  
   ```css
   .movie-poster-wrapper img {
       width: 100%;
       height: 100%;
       object-fit: cover;
   }
   ```  

### **Retrospectiva de la Sección de Actores**

#### **1. Estructura de la Sección:**
- **Contenedor Principal:** La clase `actors-wrapper` organiza y agrupa a los actores destacados.
- **Encabezado:** Destaca el contenido con un título claro: *"Top 10 mejores actores"*, atrayendo la atención del usuario.
- **Tarjetas de Actores:** Cada actor tiene una representación individual que incluye:
  - **Foto:** Imágenes destacadas y personalizadas para cada actor.
  - **Nombre:** Proporciona identidad clara a través de un `h3`.
  - **Calificación:** Representada visualmente con estrellas.

#### **2. Detalles de Diseño de Tarjetas:**
- **Foto del Actor:** Diseñadas para ser atractivas, utilizando un formato circular (con `border-radius: 50%`), asegurando un enfoque elegante y moderno.
- **Nombre:** Centrados y estilizados para visibilidad, complementan las imágenes de los actores.
- **Calificación:** Sistema de estrellas con diseño responsivo que refuerza la evaluación visual del actor.

#### **3. CSS y Usabilidad:**
- **Diseño Responsivo:** Adaptación fluida mediante tamaños dinámicos y márgenes bien definidos.
- **Efectos Visuales:** 
  - Sombra suave alrededor de las tarjetas para dar profundidad.
  - Transiciones suaves para una experiencia interactiva agradable.
- **Estructura Centralizada:** Alineación precisa y balanceada para destacar las tarjetas en cualquier tamaño de pantalla.

---

### **Sección de Festivales y Series**

#### **1. Estructura General:**
- **División en Subsecciones:**
  - **Festivales:** Imágenes grandes y destacadas que captan la atención del usuario.
  - **Series:** Tarjetas organizadas en cuadrícula que permiten explorar múltiples opciones de contenido.

#### **2. Detalles de Contenido:**
- **Festivales:**
  - **Pósters de Alta Calidad:** Se organizan verticalmente, con efectos interactivos (hover).
  - **Interactividad:** Añaden curiosidad al usuario con cursores visuales que indican clics.
- **Series:**
  - **Cuadrícula:** Organización clara y dinámica en tres columnas.
  - **Títulos con Sombreado:** Refuerzan el contraste y mejoran la legibilidad.

#### **3. CSS de la Sección:**
- **Diseño de Cuadrícula:** `display: grid` asegura un diseño limpio y simétrico.
- **Efectos Interactivos:**
  - Escalado y sombras al pasar el cursor, generando una sensación de movimiento.
  - Fondos degradados para realzar la jerarquía visual de los títulos.
- **Adaptabilidad:** Elementos que se ajustan fácilmente a dispositivos pequeños o grandes.

---

### **Sección "Lo más visto"**

#### **1. Estructura Principal:**
- **Contenedor:** Agrupa las tarjetas más relevantes con la clase `mas-visto`, optimizando el espacio disponible.
- **Encabezado:** Destaca con un título claro: *"Lo más visto"*, guiando al usuario hacia contenido destacado.

#### **2. Tarjetas de Contenido:**
- **Clasificación:** 
  - Uso de badges visuales para destacar el rango de popularidad (posición en el ranking).
  - Posición superior derecha que no interfiere con la imagen principal.
- **Estadísticas:** Representan información clave como visualizaciones y calificaciones, resaltadas con fondos degradados.
- **Pósters:** Imágenes de alta calidad con ajustes proporcionales (`object-fit: cover`).

#### **3. CSS y Estilo Visual:**
- **Diseño General:** Uso de cuadrículas ajustables (`auto-fit, minmax`) para adaptar el contenido a cualquier pantalla.
- **Interactividad:** 
  - Sombras y escalado al pasar el cursor.
  - Transiciones suaves para atraer al usuario.
- **Organización Visual:** Uso estratégico de colores y degradados para jerarquizar la información.

### **Footer**

#### **1. Estructura del Footer**
- **Secciones Informativas:** 
  - Organizado en varias áreas funcionales (`footer-section`), cada una con un propósito específico:
    - **Empresa:** Información general y enlaces a redes sociales.
    - **Ayuda y Soporte:** Recursos útiles para usuarios, como preguntas frecuentes y opciones de contacto.
    - **Aspectos Legales:** Documentos y políticas clave como términos de uso y política de privacidad.
    - **Compañía:** Datos corporativos y enlaces relacionados con oportunidades laborales, inversores y más.
- **Redes Sociales:**
  - Iconos interactivos que enlazan a plataformas sociales, integrados dentro de la sección de empresa para facilitar la interacción.

---

#### **2. Contenido de las Secciones**
- **Info de la Compañía:**
  - **Logo:** Refleja la identidad visual de *ITBFlix*, aportando reconocimiento de marca.
  - **Descripción:** Breve texto que comunica la misión o valores principales de la empresa.
  - **Enlaces Sociales:** Iconos de redes sociales como Facebook, Twitter, e Instagram, para fomentar la conexión con los usuarios.
  
- **Ayuda y Soporte:**
  - **Centro de Recursos:** Enlaces a FAQ, contacto, y administración de cuenta para una experiencia centrada en el usuario.
  
- **Legal:**
  - **Políticas y Avisos:** Incluye enlaces a términos de uso, política de privacidad, cookies, aviso legal, y ajustes de preferencias.
  
- **Compañía:**
  - **Información Corporativa:** Sección sobre oportunidades laborales, inversores, sala de prensa y responsabilidad social corporativa.

---

#### **3. CSS del Footer**
- **Diseño de Cuadrícula:**
  - Utiliza `grid-template-columns` para dividir las secciones en cuatro columnas, asegurando un diseño estructurado y fácil de navegar.
  - Espaciado uniforme entre columnas y márgenes bien definidos.

- **Estilización de Enlaces:**
  - Color base que combina con la paleta de la marca, con efecto `hover` que resalta los enlaces al pasar el ratón.
  - Tipografía legible y tamaño ajustable para mejorar la accesibilidad.

- **Estilo de Redes Sociales:**
  - Iconos estilizados con un tamaño uniforme, diseñados para destacar sin ser intrusivos.
  - Efecto de cambio de color en `hover` que invita a la interacción.

- **Sección Inferior del Footer:**
  - Fondo oscuro con texto centrado que incluye derechos de autor y marcas registradas.
  - Contraste adecuado entre el texto y el fondo para garantizar la legibilidad.
