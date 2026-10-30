# 🚀 Postulaciones AI - Asistente de Búsqueda de Empleo

Este es un proyecto web del lado del cliente (Frontend) diseñado para automatizar y acelerar el proceso de postulación a ofertas de empleo. Utiliza la API de **Google Gemini** para analizar ofertas de trabajo (en texto o imagen), redactar correos de presentación personalizados y extraer datos clave para tu registro de postulaciones.

## ✨ Características Principales

- **Análisis Multimodal:** Pega el texto de una oferta de trabajo o sube/pega una captura de pantalla. Gemini extraerá la información clave.
- **Redacción Inteligente:** Genera un correo de presentación profesional y persuasivo adaptado al tono seleccionado (Profesional, Directo o Técnico).
- **Firma Automatizada:** Incluye tus datos de contacto (Nombre, Teléfono, LinkedIn, Portafolio) al final del correo generado.
- **Envío Rápido:** 
  - Abre Gmail Web con el correo pre-redactado en un solo clic.
  - Abre WhatsApp Web/App con un mensaje formateado para el reclutador.
- **Exportación a Excel / Google Sheets:** Extrae los datos de la vacante (Puesto, Empresa, Plataforma, Requisitos, Modalidad, Ubicación, Link) y los copia en formato TSV. Solo necesitas hacer `Ctrl + V` en tu hoja de cálculo para que se distribuyan automáticamente en las columnas.

## 🛠️ Requisitos Previos

1. Un navegador web moderno (Chrome, Edge, Firefox, Safari).
2. Una **API Key de Google Gemini** (Es gratuita para uso básico).
3. No requiere instalación de servidores locales ni bases de datos (es 100% HTML + JS).

## 🚀 Cómo empezar

### 1. Obtener tu API Key de Gemini
1. Ve a [Google AI Studio](https://aistudio.google.com/app/apikey).
2. Inicia sesión con tu cuenta de Google.
3. Haz clic en **"Create API key"** (Crear clave de API).
4. Copia la clave generada (comienza con `AIza...`).

### 2. Configurar el proyecto
1. Descarga o copia el código HTML en un archivo llamado `correosIA.html`.
2. Ábrelo en tu navegador web.
3. En la esquina superior derecha, pega tu API Key en el campo correspondiente y haz clic en **Guardar**. 
   *(Nota: La clave se guarda de forma segura en el almacenamiento local de tu navegador (`localStorage`), por lo que no tendrás que ingresarla de nuevo cada vez que abras el archivo).*

## 💡 Guía de Uso

El flujo de trabajo está dividido en 3 pasos dentro de la interfaz:

1. **Entrada de la Vacante:**
   - Pega el texto de la oferta o arrastra una captura de pantalla.
   - Selecciona el tono de redacción.
   - Verifica que tus datos de contacto para la firma estén correctos.
   - Haz clic en **"Analizar con IA y Redactar"**.

2. **Revisa, Edita y Envía:**
   - La IA rellenará el asunto y el cuerpo del correo. Puedes editarlos libremente.
   - Usa los botones rojos o verdes para abrir Gmail o WhatsApp y enviar tu postulación.

3. **Exportar a Excel / Google Sheets:**
   - Revisa los datos extraídos automáticamente (Empresa, Requisitos, etc.).
   - Haz clic en **"Copiar Fila"**.
   - Abre tu documento de Google Sheets o Excel, selecciona la celda donde quieres empezar la fila y presiona `Ctrl + V` (o `Cmd + V` en Mac).
   - También tienes un botón directo para abrir tu hoja de cálculo configurada.

## ⚠️ Notas Importantes y Seguridad

- **Privacidad de la API Key:** Este proyecto está diseñado para uso personal local. Si decides subir este archivo a un servidor web público (como GitHub Pages), **no incluyas tu API Key en el código directamente**, ya que cualquiera podría verla y consumir tu cuota. El código actual está preparado para que el usuario la ingrese manualmente en la interfaz.
- **Formato de WhatsApp:** En el campo de WhatsApp, el número debe incluir el código de país. Para México, el formato actual es `52` + 10 dígitos (ej. `525512345678`). Si el enlace no abre el chat, prueba agregando un `1` después del `52` (ej. `5215512345678`), ya que algunos dispositivos aún esperan ese formato antiguo.
- **Modelos de IA:** El código incluye un selector de modelos (`gemini-3.8-flash`, `gemini-3.5-flash`, etc.). Google actualiza sus modelos frecuentemente. Si el modelo seleccionado arroja un error de "no disponible", simplemente selecciona otra opción del menú desplegable.

## 🧰 Tecnologías Utilizadas

- **HTML5 / CSS3** (Estilizado con [Tailwind CSS](https://tailwindcss.com/))
- **JavaScript (Vanilla)** (Sin frameworks adicionales)
- **Google Gemini API** (Modelo `generateContent`)
- **FontAwesome** (Iconos)
- **Google Fonts** (Tipografía Inter)

---
*Desarrollado para optimizar y agilizar la búsqueda de empleo.*