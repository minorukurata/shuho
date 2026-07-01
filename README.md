# 週報 Shuho — Iglesia Adventista Japonesa Paraguay

Boletín semanal interactivo bilingüe 🇯🇵🇵🇾  
**URL:** `minorukurata.github.io/shuho`

---

## ¿Qué es?

Página web para crear y compartir el programa del sábado de la Iglesia Adventista Japonesa de Paraguay. Un solo archivo HTML, sin instalación, funciona desde cualquier celular.

---

## Funciones

### 📖 Vista del boletín
- Diseño estilo papel japonés (washi) con colores dorado, rojo y tinta
- **Parallax** en las imágenes de sección al hacer scroll
- **Zoom tipográfico** — cada línea crece al pasar por el centro de la pantalla, facilitando encontrar el propio nombre
- Orden: Escuela Sabática → Culto → Oración diaria → Pedidos de oración → Anuncios
- **Popup** al abrir con anuncios importantes y pedidos de oración, con barra de tiempo y cierre automático

### ✏️ Editor
- Todos los campos editables en japonés 🇯🇵 y español 🇵🇾
- **Autocompletado de nombres** — 28 miembros precargados, aprende nombres nuevos automáticamente
- **Sincronización bilingüe** — al seleccionar un nombre en japonés se completa automáticamente en español y viceversa
- **Campos de himno inteligentes** — escribís el número y se completa el nombre en ambos idiomas (78 himnos ESP ↔ JPN)
- **ⓘ Tooltips** de ayuda en cada campo
- Fecha occidental y **令和 Reiwa** generadas automáticamente
- Botón **↺ 次の安息日へ / Nueva semana** — calcula el próximo sábado y actualiza todas las fechas

### ☁️ Sincronización en la nube
- Los datos se guardan en **JSONBin.io** al tocar Guardar
- Todos los miembros ven el boletín actualizado al abrir la página
- Sin necesidad de subir archivos ni actualizar GitHub cada semana
- Si no hay conexión guarda localmente como respaldo

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
| Otros | マルセロ・コレア・マリア・テレサ・Marisa・Paula Alarcón |

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
| JSONBin.io | Sincronización en la nube |
| Google Fonts | Noto Serif JP, Noto Sans JP, Cinzel |
| localStorage | Respaldo local y nombres |

> El JSX está pre-compilado — no usa Babel en el navegador, carga rápido en móvil.

---

## Uso semanal

1. Abrir `minorukurata.github.io/shuho`
2. Tocar **✏️ Editor**
3. Tocar **↺ 次の安息日へ** — se calcula el próximo sábado
4. Completar los campos que cambian
5. Tocar **✓ Guardar** — se sube a la nube automáticamente
6. Todos ven los cambios al abrir el link

---

## Estructura

```
index.html    ← todo en un solo archivo (HTML + CSS + JS pre-compilado)
README.md     ← este archivo
```

---

## Autor

倉田稔 Minoru Kurata — Iglesia Adventista Japonesa, Paraguay  
`minorukurata.github.io`
