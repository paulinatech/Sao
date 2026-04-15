# Part 1 — Homepage Build Plan
## Tiendanube · Viento Theme · Section by Section

---

### Before You Start

In Tiendanube admin go to:
**Diseño → Personalizar diseño → Secciones (homepage)**

Sections are drag-and-drop. Build them in the order below.
Each section maps to a native Viento widget unless marked **[HTML]**.

---

## Section Order

```
1. Barra de notificaciones
2. Header (global — configured separately)
3. Banner principal
4. Colecciones destacadas
5. Productos destacados — Lo nuevo
6. Bloque de texto / HTML — Brand statement
7. Productos destacados — Los más pedidos
8. Instagram
9. Footer (global — configured separately)
```

---

## Section 1 — Announcement Bar
**Widget:** `Barra de notificaciones`

| Setting | Value |
|---|---|
| Text | `Envíos a todo el país · Producción limitada` |
| Background color | `#0F0F0F` |
| Text color | `#F0EBE1` |
| Link | Leave empty |
| Dismissible | No |

**Notes:**
- One line only. No punctuation other than the middle dot `·`.
- Swap text seasonally for drop announcements: e.g. `Cayó algo nuevo — ARG / 003`

---

## Section 2 — Header
**Widget:** Global header (Diseño → Header)

| Setting | Value |
|---|---|
| Logo | Upload SVG or PNG, max height 32px, dark version on light bg |
| Layout | Logo left · Nav center · Icons right |
| Sticky header | On |
| Nav links | `Colecciones` (dropdown) · `Tienda` · `Nosotros` |
| Dropdown under Colecciones | Conciertos · Rock · Argentina · Mundial · Países |
| Show search icon | Yes |
| Show cart icon | Yes, with item count |
| Background on scroll | `#F0EBE1` |

**Notes:**
- Header starts transparent over the hero, turns `#F0EBE1` on scroll.
- This transition requires a CSS line — covered in Part 3.

---

## Section 3 — Hero Banner
**Widget:** `Banner principal`

| Setting | Value |
|---|---|
| Layout | Imagen derecha · Texto izquierda (50/50 split) |
| Image | Type C campaign photo — 1440 × 900px, JPG, dark/high contrast |
| Image position | Center |
| Background color (text side) | `#0F0F0F` |
| Eyebrow / label text | `NUEVA ENTRADA / ARG · 003` |
| Headline | `El año que no termina.` |
| Subline | `Remera · Argentina 2022` |
| Button text | `VER PRODUCTO` |
| Button link | Direct URL of the featured product |
| Button style | Outlined (configured in Part 3 CSS) |
| Overlay | None — image should be dark enough on its own |
| Minimum height | 90vh |

**Notes:**
- Change this section every time a new drop launches.
- The eyebrow label (`NUEVA ENTRADA / ARG · 003`) requires CSS styling — covered in Part 3.
- On mobile: image stacks above text block. Verify this in the Viento mobile preview.

---

## Section 4 — Featured Collections
**Widget:** `Colecciones destacadas`

| Setting | Value |
|---|---|
| Number of collections | 3 |
| Collections shown | Conciertos · Argentina · Rock |
| Layout | 3 columnas iguales |
| Image style | Imagen de fondo con texto encima |
| Text position | Bottom left |
| Section title | `Colecciones` |
| Title style | Small, `IBM Plex Mono`, uppercase (CSS) |
| Image per collection | 800 × 1000px portrait, dark campaign photo |
| Overlay | Dark gradient at bottom — 30% opacity, bottom only |
| Show collection name | Yes |
| Show product count | No |

**Notes:**
- Each collection needs its own cover image set in: **Categorías → [collection] → Imagen**.
- The text over images should be `#F0EBE1` — set in CSS.

---

## Section 5 — New Arrivals
**Widget:** `Productos destacados`

| Setting | Value |
|---|---|
| Section title | `Lo nuevo` |
| Products shown | 4 |
| Sort by | Más recientes |
| Layout | Grilla — 4 columnas desktop · 2 columnas mobile |
| Show product name | Yes |
| Show price | Yes |
| Show "Add to cart" button on card | No (hidden via CSS) |
| Show stock badge | Yes — displays when stock ≤ 3 |
| Badge text for low stock | `Últimas unidades` |

**Notes:**
- Cards are click-through only. No buy button on the card.
- New products get the `nuevo` tag in Tiendanube — configure a badge for it in Part 3.

---

## Section 6 — Brand Statement Block
**Widget:** `HTML personalizado` (or `Bloque de texto` if HTML not available)

**Full HTML to paste:**

```html
<section class="brand-statement">
  <p class="brand-statement__headline">No es una tienda de remeras.<br>Es un archivo.</p>
  <p class="brand-statement__body">
    Conciertos, países, años, noches.<br>
    Diseños para los que saben exactamente por qué los quieren.
  </p>
  <a class="brand-statement__link" href="/nosotros">Sobre nosotros →</a>
</section>
```

**CSS for this block — add to custom CSS:**

```css
.brand-statement {
  background-color: #0F0F0F;
  padding: 100px 40px;
  text-align: center;
}

.brand-statement__headline {
  font-family: 'Barlow Condensed', sans-serif;
  font-weight: 900;
  font-size: clamp(36px, 5vw, 72px);
  text-transform: uppercase;
  color: #F0EBE1;
  line-height: 1;
  margin: 0 0 24px;
}

.brand-statement__body {
  font-family: 'Inter', sans-serif;
  font-size: 16px;
  color: #8A8278;
  line-height: 1.7;
  margin: 0 0 32px;
}

.brand-statement__link {
  font-family: 'IBM Plex Mono', monospace;
  font-size: 12px;
  letter-spacing: 0.1em;
  color: #8A8278;
  text-decoration: none;
  text-transform: uppercase;
}

.brand-statement__link:hover {
  color: #F0EBE1;
}
```

---

## Section 7 — Bestsellers
**Widget:** `Productos destacados` (second instance)

| Setting | Value |
|---|---|
| Section title | `Los más pedidos` |
| Products shown | 4 |
| Sort by | Más vendidos |
| Layout | Grilla — 4 columnas desktop · 2 columnas mobile |
| Show product name | Yes |
| Show price | Yes |
| Show "Add to cart" button on card | No (hidden via CSS) |

**Notes:**
- This is a second instance of the same widget as Section 5.
- Viento allows multiple `Productos destacados` sections on the same page.

---

## Section 8 — Instagram Strip
**Widget:** `Instagram`

| Setting | Value |
|---|---|
| Instagram handle | Your handle |
| Number of posts shown | 6 |
| Layout | Fila horizontal (single row) |
| Show handle above | Yes — styled as `@handle` in IBM Plex Mono (CSS) |
| Link | Each image links to Instagram post |
| Image size | Square crop, pulled automatically |

**Notes:**
- Requires connecting your Instagram account in **Marketing → Instagram** first.
- If Instagram feed is unavailable, replace this section with a static image grid using `HTML personalizado` until connected.

---

## Section 9 — Footer
**Widget:** Global footer (Diseño → Footer)

| Setting | Value |
|---|---|
| Background color | `#0F0F0F` |
| Text color | `#F0EBE1` |
| Logo | Light version (white or `#F0EBE1`) |
| Tagline below logo | `Archivo de lo que importa.` |
| Column 1 — Links | Colecciones · Tienda · Nosotros |
| Column 2 — Links | FAQ · Guía de talles · Contacto |
| Column 3 — Links | Política de privacidad · Cambios y devoluciones |
| Social icons | Instagram only (for now) |
| Payment icons | Show — Mercado Pago, Visa, Mastercard |
| Copyright line | `© 2024 — Todos los derechos reservados` |

---

## Final Section Order Checklist

Before publishing, confirm this exact order in the Viento section editor:

- [ ] Barra de notificaciones
- [ ] Banner principal
- [ ] Colecciones destacadas
- [ ] Productos destacados — Lo nuevo
- [ ] HTML — Brand statement
- [ ] Productos destacados — Los más pedidos
- [ ] Instagram

Header and Footer are global and sit outside this list.

---

*Next: Part 2 — Theme settings, typography, and color implementation.*
