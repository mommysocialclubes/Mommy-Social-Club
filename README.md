# Mommy Social Club — web

Web estática de una sola página (HTML + CSS + un poco de JS). No necesita build.

```
index.html      la página
img/            logo, fotos, favicon y og-image
vercel.json     cabeceras de caché para las imágenes
```

## Publicar con GitHub + Vercel

```bash
cd mommy-social-club
git init
git add .
git commit -m "Web Mommy Social Club"
git branch -M main
git remote add origin https://github.com/TU-USUARIO/mommy-social-club.git
git push -u origin main
```

En Vercel: **Add New → Project →** importa el repo. Framework preset: **Other**, sin build command ni output directory. Cada `git push` a `main` vuelve a publicar.

Dominio propio: Vercel → Project → **Settings → Domains**.

## Formulario de reservas

Vercel no recoge formularios estáticos. Con Formspree (gratis):

1. Crea un formulario en https://formspree.io y copia su URL (`https://formspree.io/f/xxxxxxx`).
2. En `index.html`, pon esa URL en `action=""` del `<form id="form">`.
3. Haz commit y push. Las reservas llegan por email.

Si el `action` está vacío, el formulario muestra el mensaje de gracias pero **no envía nada**.

## Pendiente en el contenido

- Precio de la entrada premium (ahora "Consúltanos")
- Bios de Astrid y Paola (busca "Breve bio")
- Edades de los niños (FAQ) y hora exacta de inicio ("por la mañana")
- Enlaces a Instagram en el pie
- `og:image` usa ruta relativa; cuando tengáis dominio, cámbiala a la URL completa (`https://tudominio.com/img/og-image.jpg`) para que la vista previa salga bien en WhatsApp e Instagram
