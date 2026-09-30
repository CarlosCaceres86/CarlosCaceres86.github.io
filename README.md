# Tokenz — web pública

Presentación informativa de Tokenz, con la estética de la app y un tablero de demostración independiente. HTML/CSS/JavaScript estático, sin dependencias de producción, backend, cuentas, formularios, publicidad ni analítica añadida.

- Web: https://carloscaceres86.github.io/
- Repositorio: https://github.com/CarlosCaceres86/CarlosCaceres86.github.io
- Publicación: GitHub Pages desde `main`, carpeta `/`, HTTPS y `.nojekyll`.

## Desarrollo y comprobaciones

```sh
python3 -m http.server 4173 --bind 127.0.0.1
node --test tests/demo.test.mjs
python3 scripts/check_site.py
```

La demo funciona solo en memoria. Su estado puro vive en `demo-state.mjs`; `app.js` coordina pestañas, accesibilidad, puntos, diálogo de canje y reinicio. Cancelar/Escape no canjea. Después de canjear, las normas quedan bloqueadas hasta reiniciar el ejemplo para evitar saldos negativos. No se escribe en cookies ni local/session storage.

Diseño: Nunito local con licencia OFL, colores y recursos existentes de Tokenz; [procedencia](assets/PROVENANCE.md). El código móvil, las claves, la configuración privada y el backend no pertenecen a este repositorio. No se concede una licencia abierta a la marca o ilustraciones por publicar estos archivos.

## Antes del lanzamiento de la app

La app se presenta como próxima. No añadir enlaces ficticios a tiendas, compras web, formularios de datos familiares o testimonios inventados. La página de privacidad actual describe únicamente este sitio; faltan la política completa de la app y un contacto privado confirmado por el propietario.

La raíz del dominio permite alojar `/.well-known/assetlinks.json` y `/.well-known/apple-app-site-association`. Estos archivos **no están publicados**: deben contener las huellas reales de firma y los identificadores de Apple. No usar valores de ejemplo. Publicarlos no basta: comprobar HTTP, MIME, ausencia de redirects y asociación efectiva desde cada app. El sitio no cambia la configuración de enlaces/auth del cliente ni de Supabase.

GitHub Pages se utiliza exclusivamente para contenido informativo y esta demostración efímera; licencias y compras se gestionarán en la app mediante Google Play, y el backend seguirá en Supabase.

## Entrega

La especificación y tareas se conservan en `SPEC.md` y `tasks/`. Antes de publicar cambios: pruebas, integridad, revisión visual desktop/móvil y navegación con teclado. Evitar custom workflows de pago y no aumentar límites de gasto. Comprobar HTTPS y las respuestas reales después de desplegar.
