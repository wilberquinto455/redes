# Mi Sitio Jekyll

Este es un proyecto simple de sitio Jekyll que sirve como plantilla para crear tu propio blog o sitio web usando Jekyll.

## Estructura del Proyecto

- `_config.yml`: Configuración del sitio Jekyll.
- `_posts/`: Contiene todas las entradas del blog en formato markdown.
  - `2023-01-01-welcome-to-jekyll.md`: Una entrada introductoria sobre el sitio.
- `_layouts/`: Contiene plantillas de diseño para el sitio.
  - `default.html`: El diseño predeterminado para todas las páginas.
- `_includes/`: Contiene fragmentos HTML reutilizables.
  - `header.html`: La sección de encabezado del sitio.
- `_sass/`: Contiene hojas de estilo Sass.
  - `main.scss`: Hoja de estilo principal del sitio.
- `assets/`: Contiene activos estáticos como archivos CSS.
  - `style.css`: Estilos adicionales para el sitio.
- `index.html`: La página principal del sitio.
- `README.md`: Documentación del proyecto.

## Instrucciones de Configuración

1. **Instalar Jekyll**: Asegúrate de tener Ruby y Bundler instalados. Luego, instala Jekyll ejecutando:
   ```
   gem install jekyll bundler
   ```

2. **Clonar el Repositorio**: Clona este repositorio en tu máquina local:
   ```
   git clone https://github.com/yourusername/my-jekyll-site.git
   ```

3. **Navegar al Directorio del Proyecto**:
   ```
   cd my-jekyll-site
   ```

4. **Instalar Dependencias**: Ejecuta el siguiente comando para instalar las gemas necesarias:
   ```
   bundle install
   ```

5. **Ejecutar el Servidor Jekyll**: Inicia el servidor Jekyll para previsualizar tu sitio:
   ```
   bundle exec jekyll serve
   ```


6. **Abrir tu Navegador**: Visita `http://localhost:4000` para ver tu sitio en acción.

## Uso

Puedes agregar nuevas entradas creando archivos markdown en el directorio `_posts`. Asegúrate de seguir la convención de nombres `YYYY-MM-DD-titulo.md` e incluir el front matter necesario en la parte superior del archivo.

Siéntete libre de personalizar los estilos en los archivos `_sass/main.scss` y `assets/style.css` para que coincidan con el aspecto y la sensación deseados.

## Licencia

Este proyecto está licenciado bajo la Licencia MIT.