# Tu Hogar - Portal del Sol

Sitio web para la inmobiliaria Portal del Sol, diseñado para mostrar modelos de casas disponibles y facilitar el contacto con clientes interesados.

## 📋 Descripción

Sitio web institucional desarrollado para presentar cuatro modelos de viviendas disponibles. Incluye información detallada de cada modelo, tours virtuales, formulario de contacto integrado con EmailJS y botones de contacto directo vía WhatsApp.

## ✨ Características

- **Catálogo de modelos**: Presentación de 4 modelos de casas diferentes
- **Tours virtuales**: Enlaces a recorridos 360° de los modelos disponibles
- **Formulario de contacto**: Sistema de contacto integrado con EmailJS
- **Integración WhatsApp**: Botones flotantes y CTAs para contacto directo
- **Diseño responsive**: Optimizado para dispositivos móviles, tablets y desktop
- **Información descargable**: PDFs informativos disponibles para cada modelo

## 🛠️ Tecnologías Utilizadas

- **Pug**: Motor de plantillas para HTML
- **Sass/SCSS**: Preprocesador CSS con Bootstrap 5
- **Bootstrap 5.2.1**: Framework CSS responsivo
- **EmailJS**: Servicio para envío de formularios por email
- **Font Awesome & Bootstrap Icons**: Iconografía

## 📦 Instalación

1. Clonar el repositorio:
```bash
git clone [url-del-repositorio]
cd tu-hogar
```

2. Instalar dependencias:
```bash
npm install
```

## 🚀 Desarrollo

Para iniciar el servidor de desarrollo con recarga automática (Browsersync):
```bash
npm run watch
```

Esto iniciará un servidor local y abrirá el navegador automáticamente. Los cambios en los archivos se reflejarán en tiempo real.

## 🏗️ Build de Producción

Para generar los archivos optimizados para producción:
```bash
npm run build
```

Los archivos compilados se generarán en la carpeta `./public/`.

## 📁 Estructura del Proyecto

```
tu-hogar/
├── public/                 # Archivos compilados (generados)
│   ├── css/               # CSS compilado
│   ├── js/                # JavaScript
│   ├── images/            # Imágenes públicas
│   └── index.html         # HTML compilado
├── src/                   # Archivos fuente
│   ├── pug/               # Plantillas Pug
│   │   └── index.pug      # Página principal
│   ├── scss/              # Estilos SCSS
│   └── assets/            # Assets estáticos
│       ├── images/        # Imágenes fuente
│       └── tu-hogar/      # Recursos del proyecto
│           ├── images/    # Imágenes de modelos y detalles
│           └── pdf-info-casas/  # PDFs informativos
└── package.json           # Dependencias y scripts
```

## ⚙️ Scripts Disponibles

- `npm run build`: Genera los archivos de producción
- `npm run watch`: Servidor de desarrollo con recarga automática
- `npm run clean`: Limpia la carpeta public/
- `npm run templates`: Compila las plantillas Pug
- `npm run css`: Compila y minifica los estilos CSS


## 🎨 Personalización

### Colores principales
El sitio utiliza una paleta de colores personalizada basada en tonos marrones/beige (#ba9d79, #916e49).

### Modificar modelos
Los modelos se encuentran en la sección `#modelos` del archivo `src/pug/index.pug`. Cada modelo incluye:
- Imágenes (normal y hover)
- Nombre del modelo
- Enlaces a tours virtuales (opcional)
- Enlaces a PDFs informativos

## 📄 Licencia

Este proyecto es privado y pertenece a Inmobiliaria Portal del Sol.

---

Desarrollado para **Portal del Sol** - Encontrá tu hogar ideal.
