# Enosfera · landing

Nueva versión de la landing de prelanzamiento, reescrita a partir de la revisión integral de Lucho. Cambia el enfoque: Enosfera se presenta como un espacio creado por y para quienes hacen, comparten y disfrutan el mundo del vino, no solo como una herramienta de venta para creadores.

- **Sitio publicado:** https://lucasfloreslucero-agil.github.io/enofera/
- **Landing anterior (sin cambios):** https://lucasfloreslucero-agil.github.io/enosfera/
- **Publicación:** GitHub Pages desde la rama `main` (raíz). Cada push a `main` actualiza el sitio.
- **Estado:** en revisión. La página lleva `noindex` para que los buscadores no la listen todavía.

## Qué cambió respecto de la landing anterior

- **Nombre y eslogan:** "Enosfera" en toda la página y "El mundo del vino en tus manos" como eslogan.
- **Tono:** cercano y profesional. Sin expresiones como "tu gente", "la plata", "a mano", "qué descorchar" o "te leen".
- **Arquitectura:** presentación, para quién es, propósito, cómo funciona, herramientas, qué podés hacer, compras anticipadas, ecosistema conectado, miembros, pagos y gestión, cómo participar, preguntas frecuentes y cierre.
- **Miembros:** sección propia y botón "Sumate como miembro" en hero, para quién es, cómo participar y cierre.
- **Preventas:** se presentan como compras anticipadas, con la aclaración explícita de que no son una inversión. Se quitó la frase sobre las plataformas internacionales.
- **Pagos:** se explica qué paga y qué recibe cada parte (precio, cargo por servicio y comisión de Mercado Pago).
- **Ejemplos:** marcados como ilustrativos y ficticios; fechas y cantidades corregidas (la cata pasa al sábado 12 de diciembre; la preventa se mide en cajas).
- **Formulario:** empieza por "Perfil o actividad" (anfitrión/a, bodega, profesional del vino, comunicador/a, comercio o miembro). Si es miembro, pide menos datos y cambia los textos. Campos renombrados según la revisión. El campo antispam ya no muestra ningún texto.
- **Sin datos de ejemplo de contacto:** se quitaron el email `creadores@enosfera.example`, los íconos de redes y "Hecho en Mendoza".

## Estructura

- `index.html` — la landing completa (sitio estático, sin build).
- `assets/css/tokens.css` — tokens y componentes del sistema de diseño (no editar a mano).
- `assets/css/landing.css` — estilos propios de la landing.
- `assets/js/landing.js` — modal, formulario por perfil y gráfico de comunidades.
- `assets/img/` — fotos de las carpetas de Drive del proyecto, sin marcas ni caras visibles.
- `scripts/google-sheets/Code.gs` — script que guarda cada envío como fila en la planilla de postulaciones.
- `scripts/dev-server.js` — servidor local: `node scripts/dev-server.js` → http://localhost:4327

## Formulario

Envía a la misma planilla que la landing anterior ("Enosfera · Postulaciones de creadores"). Los campos nuevos se guardan en las columnas existentes: "Tipo de creador" recibe el perfil, "Seguidores" la comunidad actual, "Preventa" el proyecto en mente y "Cómo vende hoy" la forma de comercializar. El envío incluye `landing: "Enosfera · ecosistema"`, pero el script actual no guarda ese dato: para distinguir el origen hay que sumar una columna en el script. Para revisar los estados sin enviar nada, abrir la página con `?demo=ok` o `?demo=error`.

## Pendientes antes de difundir

- Validar con asesoría legal las afirmaciones sobre preventas, devoluciones, transferencias y cargos.
- Conectar Términos y condiciones, Política de privacidad y Botón de arrepentimiento a documentos reales.
- Definir un email de contacto y las redes oficiales.
- Confirmar con Seba y Lucho el uso de las fotos en una página pública.
- Sacar `noindex` de `index.html`.
