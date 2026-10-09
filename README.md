# DISPONIBLE — frontend

Paquete para desplegar el frontend estático de DISPONIBLE en Vercel.

## Archivos
- `index.html` y `app.js`: bienvenida, autenticación Google, elección de rol y experiencia de trabajador/negocio.
- `admin.html` y `admin.js`: acceso y panel de administración.
- `config.js`: URL y publishable key del proyecto Supabase DISPONIBLE.
- `styles.css`: estilos.
- `vercel.json`: configuración de URLs limpias y slash final.

## Recorrido de ingreso
1. Persona sin sesión: bienvenida y botón para continuar con Google.
2. Después de autenticar: si la cuenta no tiene rol, elige trabajador o negocio.
3. Si ya tiene rol, entra directamente a su espacio.
4. La cuenta con rol `admin` se redirige a `/admin.html`.

## Despliegue
Subí el contenido de esta carpeta al proyecto Vercel existente `admin` como una nueva versión. No crees otro proyecto si querés conservar el dominio actual.

No agregues nunca una Supabase service-role key al frontend. La `sb_publishable_...` incluida en `config.js` es la clave pública de cliente.
