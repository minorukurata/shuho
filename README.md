# 週報 Shuho — Iglesia Adventista Japonesa Paraguay

Boletín semanal interactivo bilingüe 🇯🇵🇵🇾  
**URL:** `minorukurata.github.io/shuho`

---

## ¿Qué es?

Página web para crear y compartir el programa del sábado de la Iglesia Adventista Japonesa de Paraguay. Un solo archivo HTML, sin servidor, sin instalación.

---

## Funciones

### 📖 Vista del boletín
- Diseño estilo papel japonés (washi) con colores dorado, rojo y tinta
- **Parallax** en las imágenes de sección al hacer scroll
- **Zoom tipográfico** — cada línea crece al pasar por el centro de la pantalla, facilitando encontrar el propio nombre
- Secciones: Escuela Sabática → Culto → Oración diaria → Pedidos de oración → Anuncios
- Popup al abrir con anuncios importantes y pedidos de oración, con barra de tiempo y cierre automático

### ✏️ Editor
- Todos los campos editables en japonés 🇯🇵 y español 🇵🇾
- **Campos de himno inteligentes** — escribís el número y se completa automáticamente el nombre en ambos idiomas (base de datos del Himnario Adventista ESP ↔ 希望の讃美歌 JPN)
- **Autocompletado de nombres** — aprende los nombres usados cada semana y los sugiere
- **ⓘ Tooltips** de ayuda en cada campo explicando qué escribir
- Fecha occidental y **令和 (Reiwa)** generadas automáticamente
- Secciones: Escuela Sabática, Culto, Anuncios, Popup, Pedidos de oración, Oración diaria

### 🔄 Nueva semana
- Calcula el **próximo sábado** automáticamente
- Actualiza fecha occidental, fecha Reiwa y las 7 fechas de oración diaria

### 🔗 Compartir
- Genera un **link con todos los datos codificados** en la URL
- Cualquiera que abra el link ve el boletín completo con animaciones y datos actualizados
- Sin servidor, sin base de datos

### 💾 Persistencia
- Los datos se guardan en `localStorage` del navegador
- Los nombres usados se acumulan para el autocompletado (hasta 200)

---

## Tecnologías

| Librería | Uso |
|---|---|
| React 18 (CDN) | Interfaz y estado |
| Babel Standalone | JSX en el navegador |
| GSAP 3 + ScrollTrigger | Parallax y zoom tipográfico |
| Google Fonts | Noto Serif JP, Noto Sans JP, Cinzel |
| localStorage | Persistencia de datos y nombres |

---

## Estructura del archivo

```
index.html          ← todo en un solo archivo
```

No hay dependencias npm, no hay build, no hay servidor.

---

## Uso semanal

1. Abrir `minorukurata.github.io/shuho`
2. Tocar **✏️ Editor**
3. Tocar **↺ Nueva semana** — se calcula el próximo sábado
4. Completar los campos (himno: escribir número; nombres: autocompletado)
5. Tocar **✓ Guardar y ver**
6. Tocar **🔗 Generar link y compartir** → WhatsApp

---

## Himnario cargado

Fuente: [adventist.jp](https://adventist.jp/international-ministries/hymnal-espanhol-japanese/)  
80 himnos con correspondencia ESP (Himnario Adventista) ↔ JPN (希望の讃美歌)

---

## Autor

倉田稔 Minoru Kurata — Iglesia Adventista Japonesa, Paraguay  
`minorukurata.github.io`
