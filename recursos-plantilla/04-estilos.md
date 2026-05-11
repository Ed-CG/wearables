---
nav_exclude: true
layout: default
title: Estilos y personalizaciÃ³n visual
nav_order: 5
---

# Estilos y personalizaciÃ³n visual

Esta secciÃ³n explica **cÃ³mo funciona la personalizaciÃ³n visual** en este repositorio y quÃ© debes modificar para poner el sitio con tu identidad (logo, colores, footer, etc.) **sin romper la estructura**.

---

## 1) Â¿QuÃ© archivos controlan el estilo?

En este repositorio, el estilo y algunos elementos visuales se controlan con **tres piezas**:

1) **CSS** con los colores y ajustes visuales:  
   - `assets/css/custom.css`

2) **Head** (carga el CSS, favicon y agrega el logo en el tÃ­tulo):  
   - `_includes/head_custom.html`

3) **Footer** (tu footer â€œpropioâ€, con licencia y â€œLast modifiedâ€):  
   - `_includes/footer_custom.html`

Estructura:

```text
.
â”œâ”€ _includes/
â”‚  â”œâ”€ head_custom.html
â”‚  â””â”€ footer_custom.html
â”œâ”€ assets/
â”‚  â”œâ”€ css/
â”‚  â”‚  â””â”€ custom.css
â”‚  â””â”€ img/
â”‚     â”œâ”€ logotipo.png
â”‚     â””â”€ favicon.ico
â””â”€ ...
```

---

## 2) â€œLo mÃ­nimoâ€ para poner tu identidad

Si solo quieres â€œponer tu marcaâ€ y seguir avanzando con el curso, haz esto:

### Paso A â€” Cambia el logo
Reemplaza el archivo:

- `assets/img/logotipo.png`

**Regla importante:** conserva **exactamente** el nombre `logotipo.png` para no tener que cambiar rutas.

### Paso B â€” Cambia el favicon
Reemplaza el archivo:

- `assets/img/favicon.ico`

### Paso C â€” Ajusta colores (si lo necesitas)
Edita:

- `assets/css/custom.css`

MÃ¡s abajo tienes una guÃ­a de â€œquÃ© cambiarâ€ sin perderte.

---

## 3) CÃ³mo funciona `head_custom.html` (logo + favicon + CSS)

Este archivo se inserta en el `<head>` del sitio y hace 3 cosas:

- Carga `custom.css`.
- Define el favicon.
- Inserta el logo **antes del texto** del tÃ­tulo del sitio (en la barra lateral / encabezado, segÃºn el tema).

CÃ³digo relevante:

```html
<link rel="stylesheet" href="{{ '/assets/css/custom.css' | relative_url }}">
<link rel="icon" href="{{ '/assets/img/favicon.ico' | relative_url }}" sizes="any">

<script>
  document.addEventListener('DOMContentLoaded', () => {
    const titleLink = document.querySelector('.site-title');
    if (!titleLink || titleLink.querySelector('img')) return;

    const img = document.createElement('img');
    img.src = "{{ '/assets/img/logotipo.png' | relative_url }}";
    img.alt = "Logo";
    img.className = "site-logo";
    titleLink.prepend(img);
  });
</script>
```

**QuÃ© modificar aquÃ­:**
- Normalmente **no necesitas cambiar nada** si mantienes:
  - `assets/css/custom.css`
  - `assets/img/logotipo.png`
  - `assets/img/favicon.ico`

**CuÃ¡ndo sÃ­ lo cambiarÃ­as:**
- Si decides renombrar archivos (no recomendado).
- Si quieres insertar otro elemento adicional en el `<head>` (por ejemplo: analytics, meta tags especiales, etc.).

---

## 4) CÃ³mo funciona `custom.css` (quÃ© tocar y quÃ© NO tocar)

`assets/css/custom.css` contiene reglas para:

- Colores del header y sidebar.
- Colores de enlaces (y quitar el morado/azul por defecto).
- Estados hover/active del menÃº.
- JerarquÃ­a visual del menÃº (nivel 1, 2, 3).
- Ajustes del botÃ³n hamburguesa en mÃ³vil.
- Ocultar el footer original del tema y mostrar tu footer personalizado.
- TamaÃ±o del logo en el tÃ­tulo.

### 4.1 Paleta rÃ¡pida (quÃ© buscar)

En este CSS verÃ¡s repetidos estos colores:

- **Rojo principal:** `#E00034`
- **Rosa claro/acento:** `#FFD5DE`
- **Rojo oscuro hover:** `#b00028`

RecomendaciÃ³n prÃ¡ctica:
- Para cambiar la â€œmarcaâ€, normalmente te basta con cambiar:
  - `#E00034` (color principal)
  - `#FFD5DE` (acento)
  - y la variable `--link-color`.

Ejemplo de variable de enlaces:

```css
:root { --link-color: #E00034; }
a, a:visited { color: var(--link-color); }
```

### 4.2 Sidebar y navegaciÃ³n (menÃº lateral)

El CSS fuerza el sidebar en rojo y los links en blanco:

```css
.side-bar,
.side-bar .site-nav,
.side-bar .nav-list { background-color: #E00034 !important; }

.nav-list .nav-list-link,
.nav-list .nav-list-link:visited { color: #ffffff !important; }
```

Y define estados activos/hover mÃ¡s visibles.

### 4.3 Footer: ocultar el del tema y usar el tuyo

El CSS oculta el footer del tema:

```css
footer.site-footer { display: none !important; }
```

Y define estilos para tu footer:

```css
.custom-footer { ... }
.custom-footer a { ... }
```

Esto funciona en conjunto con `_includes/footer_custom.html`.

---

## 5) Footer personalizado (`footer_custom.html`)

Tu footer actual:

- Muestra copyright.
- Enlaza a tu perfil.
- Enlaza a la licencia CC BY 4.0.
- Enlaza a la pÃ¡gina â€œUso de IAâ€.
- Muestra â€œLast modifiedâ€ con fecha/hora.

Ejemplo:

```html
<footer class="custom-footer">
  <p class="custom-footer__copy">
    Copyright Â© 2026 IBERO.
    <a href="...">Huber Giron</a>.
    <a href="...">CC BY 4.0</a>.
    <a href="{{ '/uso-ia/' | relative_url }}">Uso de IA</a>
  </p>

  <p class="custom-footer__modified">
    <strong>Last modified:</strong>
    {{ modified | date: "%A, %B %-d, %Y at %H:%M" }}
  </p>
</footer>
```

### QuÃ© cambiar aquÃ­
- El texto â€œCopyright Â© 2026 â€¦â€.
- Tu nombre y enlace.
- La licencia (si aplica).
- El enlace â€œUso de IAâ€ (si quieres ocultarlo o moverlo).

---

## 6) Checklist rÃ¡pido cuando â€œno se veâ€ el cambio

- **Guardaste el archivo** (en Codespaces o en tu editor).
- Hiciste **commit** y **push** al repositorio.
- Esperaste a que **GitHub Actions** termine (verde).
- Abriste tu sitio y forzaste recarga:
   - Windows: `Ctrl + F5` o `Ctrl + Shift + R`
   - macOS: `Cmd + Shift + R`

Tip de diagnÃ³stico:
- Abre directamente el CSS en el navegador:  
  `TU_URL/assets/css/custom.css`  
  Si no carga, el problema es de ruta o de build.


---

## Siguiente secciÃ³n

Este es el Ãºltimo tema de personalizaciÃ³n. Puedes volver a:

- [Inicio](index.md)
- [Publicar en GitHub Pages](01-publicar-en-github-pages.md)
