# Portfolio — Catalina Guzmán

Landing page one-page para **Catalina Guzmán · AI Systems Engineer**.
Stack: HTML + Tailwind CDN + JS vanilla. Sin build. Listo para GitHub Pages.

## Archivos

- `index.html` — la landing completa (todo el HTML, Tailwind via CDN, JS inline).
- `yo_github.png` — avatar usado en el Hero.

## Probar en local

Doble click en `index.html` o, mejor, levanta un servidor estático rápido:

```powershell
# desde la carpeta portafolio/
python -m http.server 8080
# abre http://localhost:8080
```

## Deploy a GitHub Pages

```powershell
cd C:\Users\CatalinaGuzmán\Proyectos\Claude-code\portafolio
git init
git add .
git commit -m "Portfolio landing — initial"
git branch -M main
git remote add origin https://github.com/cataguzmang/<nombre-del-repo>.git
git push -u origin main
```

Luego en GitHub:

1. **Settings → Pages**
2. Source: **Deploy from a branch**
3. Branch: `main` · Folder: `/ (root)` → **Save**
4. En 1–2 minutos estará en `https://cataguzmang.github.io/<nombre-del-repo>/`.

> Si quieres usarlo como sitio personal (sin sufijo), nombra el repo exactamente `cataguzmang.github.io`.

## Personalización rápida

- **Textos:** edita el objeto `i18n` al final de `index.html` (claves `en` y `es`).
- **Colores:** sección `tailwind.config` en `<head>` (`brand.blue`, `brand.beige`, etc.).
- **Avatar:** reemplaza `yo_github.png` manteniendo el nombre.
- **Email / GitHub / LinkedIn:** sección `#contact` en `index.html`.

## Features

- Bilingüe ES/EN con toggle en navbar (persistente en `localStorage`).
- Dark mode automático (`prefers-color-scheme`) + toggle manual.
- Fade-in on scroll con `IntersectionObserver`.
- Smooth scroll, navbar sticky con backdrop blur, hover effects sutiles.
- 100% responsivo, mobile-first.
