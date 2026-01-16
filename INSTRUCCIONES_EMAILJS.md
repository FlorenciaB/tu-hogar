# Instrucciones para configurar el envío de correos con EmailJS

El formulario de contacto está configurado para usar EmailJS. Para que funcione, necesitas seguir estos pasos:

## Paso 1: Crear cuenta en EmailJS

1. Ve a [https://www.emailjs.com/](https://www.emailjs.com/)
2. Crea una cuenta gratuita (permite hasta 200 correos por mes)

## Paso 2: Configurar un servicio de correo

1. En el dashboard de EmailJS, ve a **Email Services**
2. Haz clic en **Add New Service**
3. Selecciona tu proveedor de correo (Gmail, Outlook, etc.)
4. Sigue las instrucciones para conectar tu cuenta de correo
5. **Copia el Service ID** que se genera

## Paso 3: Crear una plantilla de correo

1. Ve a **Email Templates**
2. Haz clic en **Create New Template**
3. Configura la plantilla con estos campos:
   - **To Email**: `gcomercial@inmobiliariaportaldelsol.com`
   - **From Name**: `{{nombre}} {{apellido}}`
   - **Reply To**: `{{email}}`
   - **Subject**: `Nuevo mensaje de contacto - Portal del Sol`
   - **Content** (HTML o texto):
     ```
     Nombre: {{nombre}} {{apellido}}
     Email: {{email}}
     Teléfono: {{telefono}}
     
     Mensaje:
     {{mensaje}}
     ```
4. **Copia el Template ID** que se genera

## Paso 4: Obtener tu Public Key

1. Ve a **Account** > **General**
2. **Copia tu Public Key**

## Paso 5: Actualizar el código

Abre el archivo `src/pug/index.pug` y busca estas líneas (alrededor de la línea 325):

```javascript
emailjs.init('YOUR_PUBLIC_KEY'); // Reemplazar con tu Public Key de EmailJS
```

Y esta línea (alrededor de la línea 345):

```javascript
emailjs.send('YOUR_SERVICE_ID', 'YOUR_TEMPLATE_ID', formData)
```

Reemplaza:
- `YOUR_PUBLIC_KEY` con tu Public Key
- `YOUR_SERVICE_ID` con tu Service ID
- `YOUR_TEMPLATE_ID` con tu Template ID

## Paso 6: Recompilar el proyecto

Ejecuta el comando de build para generar los archivos HTML actualizados:

```bash
npm run build
```

## Nota importante

El correo se enviará a: **gcomercial@inmobiliariaportaldelsol.com**

## Alternativa: Backend propio

Si prefieres no usar EmailJS, puedo crear un backend con Node.js y Express que envíe correos directamente usando nodemailer. Esto requiere un servidor Node.js pero no depende de servicios externos.



