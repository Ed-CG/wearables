---
nav_exclude: true
layout: default
title: Escribir en Markdown
nav_order: 4
---

# Escribir en Markdown

Markdown es el formato principal para escribir contenido en tu sitio (Just the Docs). La idea es que puedas crear pÃ¡ginas claras y consistentes, sin depender de Word ni formatos complicados.

---

## 1) Regla de oro

- En cada pÃ¡gina usa **un solo H1** (el tÃ­tulo de la pÃ¡gina).
- Dentro del contenido usa **H2 para secciones** y **H3 para subsecciones**.
- MantÃ©n frases cortas y listas para pasos o requerimientos.

---

## 2) Encabezados (tÃ­tulos)

CÃ³digo:

```md
# TÃ­tulo de la pÃ¡gina (H1)
## SecciÃ³n (H2)
### SubsecciÃ³n (H3)
```

Ejemplo (cÃ³mo se ve):

**TÃ­tulo de la pÃ¡gina (H1)**  
**SecciÃ³n (H2)**  
**SubsecciÃ³n (H3)**

RecomendaciÃ³n: usa **H2** como secciones principales dentro de pÃ¡ginas; evita mÃºltiples H1.

---

## 3) Negritas, cursivas y texto en lÃ­nea

CÃ³digo:

```md
**negrita**
*cursiva*
`codigo en linea`
```

Ejemplos (cÃ³mo se ve):
- **Entrega final** el viernes.
- *Entrega final* el viernes.
- Usa `git status` para ver cambios.

---

## 4) Listas (viÃ±etas, numeradas y tareas)

### ViÃ±etas

CÃ³digo:

```md
- Punto 1
- Punto 2
  - Subpunto 2.1
```

Ejemplo (cÃ³mo se ve):
- Punto 1
- Punto 2
  - Subpunto 2.1

### Numeradas (pasos)

CÃ³digo:

```md
1. Abre Codespaces
2. Edita el archivo
3. Haz commit
4. Haz push
```

Ejemplo (cÃ³mo se ve):
1. Abre Codespaces
2. Edita el archivo
3. Haz commit
4. Haz push

### Checklists (Ãºtiles para entregas)

CÃ³digo:

```md
- [ ] AgreguÃ© portada (index.md)
- [ ] PubliquÃ© en GitHub Pages
- [ ] VerifiquÃ© Actions en verde
```

Ejemplo (cÃ³mo se ve):
- [ ] AgreguÃ© portada (index.md)
- [ ] PubliquÃ© en GitHub Pages
- [ ] VerifiquÃ© Actions en verde

---

## 5) Enlaces (a pÃ¡ginas, secciones, archivos y web)

### Enlace a otra pÃ¡gina del sitio

CÃ³digo:

```md
[Ir a Estructura del repositorio](02-estructura-del-repo.md)
```

Ejemplo (cÃ³mo se ve):  
[Ir a Estructura del repositorio](02-estructura-del-repo.md)

### Enlace a una secciÃ³n dentro de la misma pÃ¡gina (ancla)

Primero, crea un encabezado:

```md
## Mi Seccion Importante
```

Luego enlaza asÃ­:

```md
[Ir a Mi Seccion Importante](#mi-seccion-importante)
```

Ejemplo (cÃ³mo se ve):  
[Ir a Mi Seccion Importante](#mi-seccion-importante)

> Nota: los espacios se convierten en guiones y todo queda en minÃºsculas.

### Enlace a un archivo (PDF, ZIP, etc.)

Guarda el archivo en `assets/files/` y enlaza asÃ­:

```md
[Descargar hoja de datos](assets/files/calendario.pdf)
```

Ejemplo (cÃ³mo se ve):  
[Descargar hoja de datos](assets/files/calendario.pdf)

### Enlace externo

CÃ³digo:

```md
[GitHub](https://github.com)
```

Ejemplo (cÃ³mo se ve):  
[GitHub](https://github.com)

---

## 6) ImÃ¡genes (y buenas prÃ¡cticas de rutas)

Guarda imÃ¡genes en `assets/img/`.

CÃ³digo:

```md
![Diagrama del sistema](assets/img/diagrama-sistema.png)
```

Ejemplo (cÃ³mo se ve):  
(El ejemplo renderiza cuando la imagen existe en esa ruta)

<!-- Ejemplo sugerido usando un archivo que normalmente ya existe en la plantilla -->
![Ejemplo (logo)](assets/img/logotipo.png)

Buenas prÃ¡cticas:
- Usa nombres consistentes: `fig15-...`, `diagrama-...`, `captura-...`
- Evita espacios y acentos en nombres de archivo.
- Respeta mayÃºsculas/minÃºsculas (en web sÃ­ importa).

---

## 7) Video (opciones recomendadas)

### OpciÃ³n A: Enlace

Ideal para no romper el diseÃ±o.

CÃ³digo:

```md
[Ver video de demostraciÃ³n (YouTube)](https://www.youtube.com/watch?v=ID_DEL_VIDEO)
```

Ejemplo (cÃ³mo se ve):  
[Ver video de demostraciÃ³n (YouTube)](https://www.youtube.com/watch?v=6om9bh6pz_s)

### OpciÃ³n B: Embed

Puedes incrustar un video con HTML. Ãšsalo con moderaciÃ³n.

CÃ³digo:

```html
<iframe width="560" height="315" src="https://www.youtube.com/watch?v=ID_DEL_VIDEO" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen>
</iframe>
```

Ejemplo (cÃ³mo se ve):

<iframe width="560" height="315" src="https://www.youtube.com/embed/6om9bh6pz_s?si=vGGN_nxT5MHCHusO" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen>
</iframe>

### OpciÃ³n C: Video MP4 (archivo local en tu repositorio)

1) Guarda tu video en una carpeta del repo, por ejemplo:
- `assets/videos/` (recomendado para mantener orden), o
- `assets/img/` (si ya estÃ¡s usando esa ruta en tu curso)

2) Inserta el video con HTML:

CÃ³digo:

```html
<video controls width="720">
  <source src="{{ '/assets/videos/demo.mp4' | relative_url }}" type="video/mp4">
  Tu navegador no soporta video HTML5.
</video>
```

Ejemplo (cÃ³mo se ve):  
(Solo renderiza cuando exista `assets/videos/demo.mp4` en tu repo)

<video controls width="720">
  <source src="{{ '/assets/videos/demo.mp4' | relative_url }}" type="video/mp4">
  Tu navegador no soporta video HTML5.
</video>

Recomendaciones:
- MantÃ©n los MP4 **ligeros** (clips cortos). Archivos muy grandes hacen el repo pesado y lento de descargar.
- Usa nombres simples: `demo-robot.mp4`, `calibracion-01.mp4`.

---

## 8) CÃ³digo (bloques con resaltado y fragmentos)

### Bloque con resaltado

CÃ³digo:

````md
```python
print("hola")
```
````

Ejemplo (cÃ³mo se ve):

```python
print("hola")
```

### Bloque sin lenguaje (texto plano)

CÃ³digo:

````md
```text
git status
git add .
git commit -m "mensaje"
git push
```
````

Ejemplo (cÃ³mo se ve):

```text
git status
git add .
git commit -m "mensaje"
git push
```

### CÃ³digo en lÃ­nea

CÃ³digo:

```md
Usa `git status` para ver cambios.
```

Ejemplo (cÃ³mo se ve):  
Usa `git status` para ver cambios.

---

## 9) Tablas

CÃ³digo:

```md
| Campo | Tipo | Ejemplo |
|------:|:----:|:--------|
| RAM   | GB   | 8       |
| CPU   | x86  | i5      |
```

Ejemplo (cÃ³mo se ve):

| Campo | Tipo | Ejemplo |
|------:|:----:|:--------|
| RAM   | GB   | 8       |
| CPU   | x86  | i5      |

Buenas prÃ¡cticas:
- No abuses de tablas anchas (en mÃ³vil se vuelven incÃ³modas).
- Si la tabla se vuelve enorme, considera dividir en 2 o pasar a lista.

---

## 10) Citas y separadores

### Cita (blockquote)

CÃ³digo:

```md
> Esto es una cita o nota rÃ¡pida.
```

Ejemplo (cÃ³mo se ve):

> Esto es una cita o nota rÃ¡pida.

### Separador

CÃ³digo:

```md
---
```

Ejemplo (cÃ³mo se ve):

---


---

## 11) Bloques colapsables 

Puedes usar HTML nativo.

CÃ³digo:

```html
<details>
  <summary>Ver soluciÃ³n</summary>

  AquÃ­ va la explicaciÃ³n o soluciÃ³n paso a paso.
</details>
```

Ejemplo (cÃ³mo se ve):

<details>
  <summary>Ver soluciÃ³n</summary>

  AquÃ­ va la explicaciÃ³n o soluciÃ³n paso a paso.
</details>

---

## 12) Plantilla rÃ¡pida para una pÃ¡gina del curso

Copia y adapta.

CÃ³digo (front matter):

```yml
---
layout: default
title: Titulo de mi pagina
nav_order: 50
---
```

Ejemplo (cÃ³mo se verÃ­a al inicio de un archivo `mi-pagina.md`):

```yml
---
layout: default
title: Mi pagina de ejemplo
nav_order: 50
---
```

Y debajo, tu contenido:

```md
## Objetivo
- Explicar un concepto de forma clara.

## Materiales
- 1 imagen
- 1 enlace
- 1 PDF

## Pasos
1. Paso 1
2. Paso 2

## Evidencia
- Foto / captura / enlace
```

---

## Siguiente secciÃ³n

[Estilos y personalizaciÃ³n visual](04-estilos.md)
