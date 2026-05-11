---
nav_exclude: true
layout: default
title: Publicar en GitHub Pages
nav_order: 2
---

# Publicar sitio en GitHub Pages

En este curso vamos a publicar tu documentaciÃ³n como un **sitio web** usando:

- **GitHub** (para guardar el repositorio y el historial)
- **GitHub Pages** (para convertir el repositorio en una URL pÃºblica)
- **Codespaces** (para editar desde el navegador, sin instalar nada)

---

## 1) Conceptos

- **GitHub**: plataforma para alojar proyectos (repositorios) y colaborar.
- **Repositorio (repo)**: carpeta de proyecto con archivos + historial.
- **Commit**: â€œguardar un cambioâ€ en el historial con un mensaje.
- **Push**: enviar tus commits a GitHub (a la nube).
- **GitHub Pages**: servicio que publica tu repo como sitio web.
- **Pipeline (Actions)**: proceso automÃ¡tico que construye y publica el sitio cuando haces *push*.

![Figura 1 â€” GitHub](assets/img/01-publicar/github.png)
**Figura 1:** PÃ¡gina principal de GitHub.

---

## 2) Crear tu proyecto en GitHub

Vas a partir del repo plantilla (este repositorio).

### Ruta A (recomendada): Fork del repositorio

1. Abre el repositorio a copiar en GitHub.
2. Clic en **Fork**.
3. Configura:
   - **Owner**: tu usuario (o la organizaciÃ³n de tu equipo)
   - **Repository name**: por ejemplo `documentacion-equipo-3`
4. Clic en **Create fork**.

![Figura 2 â€” Fork](assets/img/01-publicar/fork.png)
**Figura 2:** BotÃ³n *Fork* y pantalla de creaciÃ³n.

> Ventaja: no necesitas â€œsubir archivosâ€ manualmente; ya tienes el proyecto completo en tu cuenta.

### Ruta B (alternativa): Crear un repo nuevo y subir los archivos

Ãšsala solo si se necesita â€œcrear repo desde ceroâ€.

1. Abre GitHub â†’ **New repository**.
2. Nombre: `documentacion-equipo-3`.
3. Crea el repo.
4. Descarga el repo en tu computadora:
   - **Code â†’ Download ZIP** (o descarga el `.zip` que te entregÃ³ el profesor).
5. Sube el contenido a tu repo:
   - **Add file â†’ Upload files**
   - Arrastra los archivos (descomprimidos) a la ventana
   - Clic en **Commit changes**
![Figura 3 â€” Download ZIP + Upload files](assets/img/01-publicar/download.png)
**Figura 3:** Descargar ZIP.

![Figura 4 â€” New repo](assets/img/01-publicar/nuevo.png)
![Figura â€” New ](assets/img/01-publicar/new.png)
![Figura  â€” exixting](assets/img/01-publicar/upload.png)
![Figura  â€” upload](assets/img/01-publicar/files.png)
**Figura 4:** Crear repositorio nuevo.

---

## 3) Abrir el proyecto con Codespaces (sin instalar nada)

1. En tu repo (tu fork o tu repo nuevo):
   - Clic en **Code â†’ Codespaces â†’ Create codespace on main**
2. Se abre un VS Code en el navegador.

![Figura 5 â€” Codespaces](assets/img/01-publicar/codespace.png)
**Figura 5:** Crear Codespace.

> Nota: Codespaces puede tardar 1â€“3 minutos en iniciar la primera vez.

---

## 4) Configurar `_config.yml` para que funcione tu URL

En el explorador de archivos abre `_config.yml` y ajusta **solo**:

```yml
url: "https://TU_USUARIO.github.io"
baseurl: "/TU_REPO"
```

Ejemplo tÃ­pico:
- Usuario: `ana-ibero`
- Repo: `documentacion-equipo-3`

Entonces:

```yml
url: "https://ana-ibero.github.io"
baseurl: "/documentacion-equipo-3"
```

![Figura 6 â€” Edit config](assets/img/01-publicar/config.png)
**Figura 6:** Editando `_config.yml` en Codespaces.

> Si `baseurl` no coincide con el nombre del repo, los links y estilos suelen â€œromperseâ€.

---

## 5) Hacer tu primer cambio (commit) y subirlo (push)

En Codespaces:

1. Modifica un archivo sencillo, por ejemplo `index.md`.
2. Ve a la pestaÃ±a **Source Control** (Ã­cono de rama).
3. En **Message**, escribe un mensaje de commit, por ejemplo:
   - `Actualiza portada`
4. Clic en **Commit**.
5. Clic en **Sync Changes** (o **Push**).

![Figura 7 â€” Commit y Push](assets/img/01-publicar/codespace.png))
**Figura 7:** Source Control â†’ Commit â†’ Sync Changes.

### Â¿QuÃ© pasÃ³ en realidad?

Cuando haces **push**:
1. Tus archivos se guardan en GitHub.
2. Se dispara un **pipeline (GitHub Actions)**.
3. GitHub construye el sitio (Jekyll + Just the Docs).
4. GitHub publica la versiÃ³n nueva en **GitHub Pages**.

---

## 6) Activar GitHub Pages y obtener tu URL

En tu repositorio (en GitHub, no en Codespaces):

1. **Settings â†’ Pages**
2. En **Build and deployment**:
   - Source: **Deploy from a branch**
   - Branch: `main`
   - Folder: `/ (root)`
3. Guarda.

GitHub te mostrarÃ¡ tu URL con este formato:

- `https://TU_USUARIO.github.io/TU_REPO/`

![Figura  â€” Pages ](assets/img/01-publicar/pages.png)
![Figura 8 â€” Pages settings](assets/img/01-publicar/website.png)
**Figura 8:** Settings â†’ Pages (branch y folder).

---

## 7) Verificar que el sitio ya estÃ¡ publicado

### VerificaciÃ³n rÃ¡pida (lo mÃ­nimo)

1. En el repo, abre la pestaÃ±a **Actions**.
2. Busca el workflow que dice algo como **pages build and deployment**.
3. Espera a que salga en **verde (success)**.
4. Regresa a **Settings â†’ Pages** y abre la URL.

![Figura 9 â€” Actions success](assets/img/01-publicar/actions.png)
**Figura 9:** Actions con ejecuciÃ³n exitosa.


### SeÃ±ales tÃ­picas

- Si **Actions** sigue corriendo: espera (es normal).
- Si falla (rojo): abre el job y lee el error (a veces es un YAML mal indentado o un archivo faltante).

---

## Checklist 

- [ ] Hacer **commit** y **push** (desde Codespaces).
- [ ] Ajustaste `url` y `baseurl` en `_config.yml`.
- [ ] Activaste **Settings â†’ Pages** con `main` y `/ (root)`.
- [ ] En **Actions** la ejecuciÃ³n estÃ¡ en verde.
- [ ] Tu URL abre y el menÃº lateral aparece.

---

## Siguiente secciÃ³n
[Estructura del repositorio ](02-estructura-del-repo.md)
