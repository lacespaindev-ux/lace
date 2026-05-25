# Registro de cambios — Lace

## 2026-04-24

### Notificación email en formulario
- Configurado hook en Netlify (via API) para reenviar cada envío del formulario a lacespaindev@gmail.com con todos los campos

### Formulario de contacto
- Nueva sección "Contacto" con formulario Netlify Forms (sin backend)
- Campos: nombre, email, descripción del proceso, tiempo actual, herramientas
- Los envíos llegan al dashboard de Netlify en Forms

### Botón flotante WhatsApp
- Botón fijo esquina inferior derecha que abre chat directo con +34 722 197 596
- Mensaje pre-rellenado: "Hola, me gustaría saber más sobre tus automatizaciones"
- También enlace de texto alternativo bajo el formulario

### Logo en cabecera
- Diseñado logo SVG: dos hilos entrelazados sobre cuadrado verde redondeado (motivo encaje + flujo de automatización)
- Añadido inline en el nav junto al wordmark "Lace"
- Guardado también como `logo.svg` para uso independiente

## 2026-04-22

### Despliegue inicial
- Primera publicación de la landing en Netlify (lace-dev.netlify.app)

### Automatización de despliegue
- Configurado hook en `.claude/settings.json` para desplegar automáticamente cada vez que Claude edita un archivo
- Actualizado `deploy.sh` para excluir la carpeta `.claude/` del zip

### Fix: HTML servido como texto plano
- Netlify estaba sirviendo `text/html` como `text/plain`
- Creado archivo `_headers` para forzar `Content-Type: text/html; charset=UTF-8`
