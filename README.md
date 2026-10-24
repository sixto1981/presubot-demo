# PresuBot — Demostración

Prototipo visual para profesionales de reformas, pintura, fontanería, electricidad e instalaciones. No es un SaaS operativo ni debe utilizarse para gestionar datos reales de clientes.

## Probar localmente

1. Descarga el repositorio o abre `index.html` en un navegador moderno.
2. Introduce únicamente datos ficticios.
3. Genera una solicitud y guárdala en el panel local para probar los estados.

## Privacidad y límites

- Las solicitudes de esta demo se procesan en el navegador y el panel usa `localStorage` del navegador.
- No hay backend, base de datos, cuentas, autenticación, pagos, WhatsApp real ni llamadas a modelos de IA.
- El navegador carga Tailwind CSS y la fuente Inter desde servicios externos (CDN/Google Fonts); por tanto, al abrir la demo se realizan solicitudes de recursos a esos proveedores.
- No introduzcas datos personales o de clientes reales. `localStorage` no es un almacenamiento seguro ni compartido entre dispositivos.
- Los precios son hipótesis de validación, no una oferta de contratación. Los textos legales de `legal.html` son borradores incompletos con marcadores y no sustituyen asesoramiento jurídico.

## Publicación con GitHub Pages

Esta demo todavía no debe considerarse lista para publicar. Primero revisa y prueba la rama `fix/presubot-demo-xss`. La rama `main` se conserva sin cambios.

Cuando la versión corregida se haya probado y decidas publicarla, abre Settings → Pages en el repositorio y configura la publicación desde la rama y carpeta correctas. La URL habitual para este repositorio sería `https://sixto1981.github.io/presubot-demo/`, pero solo funcionará si GitHub Pages queda habilitado correctamente.

## Seguridad de la demo

La rama de corrección evita insertar texto aportado por el usuario mediante `innerHTML` en el resumen y el panel; el panel construye los elementos con `createElement` y `textContent`. Esta corrección reduce el riesgo de XSS en esas vistas, pero no convierte la demo en una aplicación segura para producción. Debe probarse antes de publicarla.

## Precios mostrados

Los planes de 29 €, 49 € y 79 €/mes son hipótesis visuales. No hay cobros ni servicios contratables activos.
