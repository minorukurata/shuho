# 週報 Shuho — Iglesia Adventista Japonesa Paraguay

Boletín semanal interactivo bilingüe 🇯🇵🇵🇾  
**URL:** `minorukurata.github.io/shuho/shuho.html`

---

## ¿Qué es?

Página web para crear y compartir el programa del sábado de la Iglesia Adventista Japonesa de Paraguay. Un solo archivo HTML, sin instalación, funciona desde cualquier celular.

---

## Funciones

### 📖 Vista del boletín
- Diseño estilo papel japonés (washi) con colores dorado, rojo y tinta
- **Parallax** en las imágenes de sección al hacer scroll
- **Zoom tipográfico** — cada línea crece al pasar por el centro de la pantalla
- Orden: Escuela Sabática → Culto → Oración diaria → Pedidos de oración → Anuncios
- **Popup** al abrir con anuncios importantes y pedidos de oración

### 🌐 Selector de idioma
- **🇯🇵 日本語** — vista solo en japonés
- **🌐 両方** — vista en ambos idiomas
- **🇵🇾 Español** — vista solo en español
- La preferencia se guarda automáticamente
- Arquitectura preparada para agregar más idiomas (🇰🇷 coreano, etc.)

### ✏️ Editor
- Todos los campos editables en japonés 🇯🇵 y español 🇵🇾
- **Autocompletado de nombres** — 30+ miembros precargados
- **Sincronización bilingüe** — al seleccionar un nombre en un idioma se completa el otro automáticamente
- **Lista de himnos** — 78 himnos ESP ↔ JPN consultables con buscador
- **ⓘ Tooltips** de ayuda en cada campo
- Fecha occidental y **令和 Reiwa** generadas automáticamente
- Botón **↺ 次の安息日へ / Nueva semana** — calcula el próximo sábado y actualiza todas las fechas

### ☁️ Sincronización en la nube
- Datos guardados en **GitHub Gist** — sin servidores externos
- Token de GitHub ingresado una sola vez desde el editor, guardado en el navegador
- El token **nunca aparece en el código público**
- Todos los miembros ven el boletín actualizado al abrir la página
- Respaldo automático en `localStorage` si no hay conexión

### 🔗 Compartir
- Genera un **link con los datos codificados** en la URL
- Cualquiera que abra el link ve el boletín completo con animaciones

---

## Miembros precargados

| Familia | Miembros |
|---|---|
| 倉田 Kurata | 稔・薫・マルタ・美幸・鳴海・伸寿・ケリー |
| 岸田 Kishida | 省一・毅・雅仁・ルツ・デリア・アラン・シオン |
| 干場 Hoshiba | 康秀・リリアナ |
| 細田 Hosoda | 茂・ローラ・サンドラ |
| 栄田 Eida | 寛三・ベンジ・きざし・ちえみ |
| 大石 Oishi | 美智子・千明・ナンシー・ミリアン・玲子 |
| 合田 Goda | マリア |
| 佃 Tsukuda | よこ |
| 奈良 Nara | ルイサ |
| 国広 Kunihiro | アントニオ |
| 林 Hayashi | 思奴布 |
| Otros | マルセロ・コレア・マリア・テレサ |

---

## Himnario cargado

Fuente: [adventist.jp](https://adventist.jp/international-ministries/hymnal-espanhol-japanese/)  
**78 himnos** con correspondencia ESP (Himnario Adventista) ↔ JPN (希望の讃美歌)

---

## Tecnologías

| Librería | Uso |
|---|---|
| React 18 (pre-compilado) | Interfaz y estado |
| GSAP 3 + ScrollTrigger | Parallax y zoom tipográfico |
| GitHub Gist API | Sincronización en la nube |
| Google Fonts | Noto Serif JP, Noto Sans JP, Cinzel |
| localStorage | Respaldo local, token y preferencias |

> El JSX está pre-compilado — no usa Babel en el navegador, carga rápido en móvil.

---

## Uso semanal

1. Abrir la URL
2. Tocar **✏️ Editor**
3. Tocar **↺ 次の安息日へ** — se calcula el próximo sábado
4. Completar los campos que cambian
5. Tocar **✓ Guardar** — se sube a la nube automáticamente
6. Todos ven los cambios al abrir el link

---

## Changelog

### v1.5 — 2026-07-01
- ✨ Selector de idioma: 🇯🇵 日本語 / 🌐 両方 / 🇵🇾 Español
- ✨ Arquitectura multilenguaje con React Context (preparado para coreano y otros)
- 🔒 Token de GitHub Gist movido a localStorage — ya no se expone en el código
- 🐛 Fix: autocompletado de nombres no sobreescribía con texto parcial al seleccionar
- 🐛 Fix: campos de himno ya no modifican el otro idioma si el número no existe

### v1.4 — 2026-06-25
- ✨ Sincronización en la nube con GitHub Gist
- ✨ Lista de himnos consultable con buscador integrado
- ✨ Campos de himno como texto libre (sin autocompletado forzado)
- 🐛 Fix: pantalla en blanco por Babel Standalone — JSX pre-compilado
- 🐛 Fix: `catch {}` sin parámetro no compatible con Babel
- 🐛 Fix: `??` nullish coalescing no compatible con Babel

### v1.3 — 2026-06-20
- ✨ Autocompletado bilingüe — seleccionar nombre JP completa ES y viceversa
- ✨ 30+ miembros precargados con pares JP/ES
- ✨ Tooltips ⓘ de ayuda en cada campo del editor
- ✨ Botón ↺ Nueva semana calcula próximo sábado automáticamente
- ✨ Fecha en 令和 Reiwa generada automáticamente
- ✨ Popup de anuncios importantes al abrir con temporizador
- ✨ Pedidos de oración editables

### v1.2 — 2026-06-15
- ✨ Autocompletado de nombres con lista de miembros
- ✨ Himnario 78 himnos ESP ↔ JPN
- ✨ Sincronización en la nube con JSONBin (reemplazado en v1.4)
- ✨ localStorage — datos persisten entre sesiones
- 🐛 Fix: nombres mostraban solo texto parcial al seleccionar sugerencia

### v1.1 — 2026-06-10
- ✨ Zoom tipográfico por scroll con GSAP ScrollTrigger
- ✨ Efecto parallax en imágenes hero con apertura de cortina
- ✨ Orden: Escuela Sabática primero, luego Culto
- ✨ Botón compartir por WhatsApp con link codificado en URL
- ✨ Editor bilingüe completo

### v1.0 — 2026-06-06
- 🎉 Lanzamiento inicial
- ✨ Vista del boletín estilo washi
- ✨ Editor básico con campos JP/ES
- ✨ GitHub Pages hosting

---

## Estructura

```
shuho.html    ← todo en un solo archivo (HTML + CSS + JS pre-compilado)
README.md     ← este archivo
.nojekyll     ← desactiva Jekyll en GitHub Pages
```

---

## Autor

倉田稔 Minoru Kurata — Iglesia Adventista Japonesa, Paraguay  
`minorukurata.github.io`
