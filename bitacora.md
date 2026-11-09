# Bitácora de desarrollo - Rueda Libre

**Autor / desarrollador:** José Ulises Valencia Martínez (`Jvalencia023`)  
**Repositorio:** [Rueda Libre](https://github.com/Jvalencia023/rueda-libre/tree/master)  
**Fecha de actualización:** Noviembre de 2026

## Resumen del proyecto

En este proyecto desarrollé el sitio web de **Rueda Libre**, una propuesta de alquiler de bicicletas y recorridos urbanos. Organicé el contenido en una página principal, páginas de tarifas y reservas, una sección para las rutas nocturnas y un espacio separado para probar diseños.

Para construir la interfaz utilicé HTML semántico y clases utilitarias de Tailwind CSS. También preparé un proceso de compilación con Tailwind CLI para la sección nocturna. Trabajé la navegación entre páginas, la presentación adaptable a distintos tamaños de pantalla y la consistencia visual de los componentes.

## Organización y trabajo por carpetas

### Carpeta raíz

- **`index.html`**: desarrollé la página de inicio con la presentación de Rueda Libre, un acceso directo a las reservas y una cuadrícula con seis modelos de bicicletas: urbana clásica, urbana plegable, montaña trail, gravel, eléctrica e infantil. Cada tarjeta presenta una descripción, una tarifa por hora y un enlace para reservar.
- **`bit_cora_de_desarrollo.md`**: documento de seguimiento del proyecto y de las decisiones de organización e implementación.
- **`bitacora.txt`**: registro complementario de actividades y características trabajadas.

### Carpeta `css/`

- **`styles.css`**: dejé el archivo previsto para los estilos compartidos de las páginas principales. En la versión actual, la mayor parte de la presentación visual se construye directamente con clases de Tailwind en el HTML.

### Carpeta `img/`

- **`logo.jpg`**: incorporé la imagen de marca en la navegación de las páginas.
- **`portada.jpg`**: utilicé la imagen en la portada del inicio y como recurso visual en las páginas de rutas nocturnas y componentes.

### Carpeta `paginas/`

- **`tarifas.html`**: organicé dos tablas para que el visitante consulte los precios de alquiler por tipo de bicicleta y duración, además de la información de los recorridos guiados de fin de semana. Añadí notas sobre los elementos incluidos y las recomendaciones para las salidas.
- **`reservas.html`**: preparé el formulario de solicitud de alquiler. Incluí campos para los datos de contacto, fecha, bicicleta, plan, cantidad y comentarios, junto con la aceptación obligatoria de las políticas. Añadí restricciones HTML para validar datos como el formato del correo, el documento, el celular, el rango de fechas, la cantidad de bicicletas y la longitud de los comentarios.

### Carpeta `nocturna/`

Separé aquí la experiencia de las rodadas nocturnas y los archivos necesarios para compilar sus estilos.

- **`index.html`**: presenté tres rutas nocturnas con su nivel, distancia, duración, punto de encuentro y precio. Desde cada opción se puede ir a la página de reservas. La página también describe el horario y los elementos incluidos en la actividad.
- **`componentes.html`**: armé una página de referencia para mantener consistencia en la interfaz. Incluí variantes de botones, una tarjeta de rodada, alertas informativas, de confirmación y advertencia, y campos de correo y celular. En el aviso de confirmación usé atributos para que los lectores de pantalla puedan anunciar el mensaje.
- **`prototipo.html`**: conservé una página sencilla de prototipo para explorar la presentación de la sección nocturna.
- **`package.json`**: configuré los comandos `build:css` y `watch:css`, además de las dependencias de desarrollo de Tailwind CSS y su CLI.
- **`src/input.css`**: establecí el punto de entrada de Tailwind CSS.
- **`src/output.css`**: guardé la hoja generada por el proceso de compilación y enlazada desde las páginas de esta sección.

### Carpeta `pruebas/`

- **`catalogo-bootstrap.html`**: dejé una página aislada para explorar el aspecto de componentes antes de incorporarlos al sitio. Aunque el archivo conserva “bootstrap” en el nombre, su versión actual carga Tailwind CSS y reutiliza los estilos del proyecto.

## Diseño y navegación

Definí una línea visual basada principalmente en tonos slate para fondos y texto, y verde esmeralda para destacar la marca y las acciones. Apliqué tarjetas con bordes redondeados, sombras, estados al pasar el cursor y espaciado uniforme. Usé cuadrículas y diseños flexibles para adaptar el contenido a pantallas pequeñas y grandes.

Mantuve enlaces entre el inicio, las tarifas, las reservas y las rutas nocturnas. También agregué etiquetas y atributos accesibles en elementos como imágenes, navegación, campos de formulario y alertas.

## Tailwind CSS y compilación

En las páginas principales y en el catálogo de pruebas utilicé Tailwind CSS mediante CDN. Para la sección `nocturna/` configuré una compilación local con Tailwind CLI: el archivo de entrada se encuentra en `src/input.css` y el resultado se genera en `src/output.css`. Los comandos definidos en `package.json` permiten generar los estilos o mantener el compilador observando los cambios.

## Cierre

Al organizar el proyecto por carpetas pude separar el contenido institucional, las páginas de servicio, los recursos visuales, la experiencia de rutas nocturnas y las pruebas de diseño. El resultado reúne la información necesaria para conocer la flota, revisar precios y solicitar una reserva desde una interfaz coherente.
