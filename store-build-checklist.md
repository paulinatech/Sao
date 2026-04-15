# Store Build Checklist
## Tiendanube · Viento · Phase 1 Launch

---

### 1. Brand Decisions
*Confirm these before touching Tiendanube.*

- [ ] Brand name confirmed
- [ ] Tagline selected: **`Archivo de lo que importa.`**
- [ ] Positioning line selected: **`Ropa para los que estuvieron.`**
- [ ] Hero headline selected: **`El año que no termina.`**
- [ ] 5 collections confirmed: Conciertos · Rock · Argentina · Mundial · Países
- [ ] First 8 products defined (4 for New Arrivals, 4 for Bestsellers)
- [ ] Catalog code format confirmed: `ARG / 001 / 2024`
- [ ] Instagram handle confirmed for footer and strip
- [ ] Logo files created: dark version + light version (SVG or PNG)

---

### 2. Tiendanube Setup
*Admin → Diseño → Personalizar diseño. Apply in this order.*

**Colors**
- [ ] Color principal → `#C41E22`
- [ ] Color de fondo → `#F0EBE1`
- [ ] Color de texto → `#0F0F0F`
- [ ] Color de botones → `#0F0F0F`
- [ ] Color de texto en botones → `#F0EBE1`
- [ ] Color de links → `#0F0F0F`

**Typography**
- [ ] Fuente para títulos → `Barlow Condensed`, weight `900`
- [ ] Fuente para textos → `Inter`, weight `400`

**Buttons**
- [ ] Estilo de botón → Outlined / Borde
- [ ] Bordes redondeados → `0px`

**Header**
- [ ] Posición del logo → Izquierda
- [ ] Posición del menú → Centro
- [ ] Header fijo (sticky) → Activado
- [ ] Mostrar ícono de búsqueda → Sí
- [ ] Mostrar ícono de carrito → Sí, con contador

**Product cards**
- [ ] Proporción de imágenes → Cuadrada (1:1)
- [ ] Zoom al pasar el cursor → No
- [ ] Segunda imagen en hover → Sí
- [ ] Mostrar botón "Agregar al carrito" → No
- [ ] Mostrar etiquetas / badges → Sí

**Stock**
- [ ] Mostrar nivel de stock → Sí

**Layout**
- [ ] Ancho del contenido → Ancho completo
- [ ] Espaciado entre secciones → Normal

**Announcement bar**
- [ ] Texto → `Envíos a todo el país · Producción limitada`
- [ ] Color de fondo → `#0F0F0F`
- [ ] Color de texto → `#F0EBE1`
- [ ] Visible → Sí

**Footer**
- [ ] Color de fondo → `#0F0F0F`
- [ ] Color de texto → `#F0EBE1`
- [ ] Texto bajo el logo → `Archivo de lo que importa.`
- [ ] Mostrar íconos de redes sociales → Sí (Instagram only)
- [ ] Mostrar métodos de pago → Sí (Mercado Pago, Visa, Mastercard)

**Collections (Categorías)**
- [ ] Create: Conciertos · Rock · Argentina · Mundial · Países
- [ ] Add cover image to each collection (800 × 1000px)
- [ ] Set collection slugs: `/conciertos` · `/rock` · `/argentina` · `/mundial` · `/paises`

**Navigation**
- [ ] Primary nav: `Colecciones` (dropdown) · `Tienda` · `Nosotros`
- [ ] Dropdown: Conciertos · Rock · Argentina · Mundial · Países
- [ ] Connect Instagram in Marketing → Instagram

---

### 3. Homepage Build
*Admin → Diseño → Secciones. Add in this order.*

- [ ] **S1 — Announcement bar** — native `Barra de notificaciones`
- [ ] **S2 — Header** — configure globally (done in step 2)
- [ ] **S3 — Hero banner** — `Banner principal`, image right / text left, 90vh, outlined CTA → `VER PRODUCTO`
- [ ] **S4 — Featured collections** — `Colecciones destacadas`, 3 tiles: Conciertos · Argentina · Rock
- [ ] **S5 — New Arrivals** — `Productos destacados`, sorted by newest, 4 products, title: `Lo nuevo`
- [ ] **S6 — Brand statement** — `HTML personalizado`, paste block from `homepage-build-plan-part-2.md`
- [ ] **S7 — Bestsellers** — second `Productos destacados`, sorted by most sold, 4 products, title: `Los más pedidos`
- [ ] **S8 — Instagram strip** — `Instagram` widget, 6 posts, label: `@[handle]`
- [ ] **S9 — Footer** — configure globally (done in step 2)

---

### 4. Content and Assets to Produce
*23 total assets. All essential unless marked optional.*

**Logo (2 files)**
- [ ] Logo — dark `#0F0F0F` on transparent bg
- [ ] Logo — light `#F0EBE1` on transparent bg

**Hero (2 files)**
- [ ] Hero — desktop 1440 × 900px, campaign photo
- [ ] Hero — mobile crop 750 × 1000px, same image

**Collection covers (3 files, 800 × 1000px each)**
- [ ] Conciertos — concert crowd or venue exterior, dark, high contrast
- [ ] Argentina — stadium or street, late afternoon light
- [ ] Rock — band or crowd detail, dark bg

**Product shots (16 files, 1000 × 1000px each)**
- [ ] 4 × New Arrivals — primary artifact shot
- [ ] 4 × New Arrivals — on-body shot (hover)
- [ ] 4 × Bestsellers — primary artifact shot
- [ ] 4 × Bestsellers — on-body shot (hover)

**Optional**
- [ ] Instagram placeholder (6 × 600px square) — only if account not yet connected

---

### 5. Minimum CSS Customizations
*In Viento: Diseño → Personalizar diseño → CSS personalizado. Apply in this order.*

**Launch-blocking — do these first:**
- [ ] `@import` Google Fonts: Barlow Condensed · Inter · IBM Plex Mono
- [ ] Button outlined style: transparent bg, `1.5px solid #0F0F0F`, fill on hover
- [ ] Global `border-radius: 0` on buttons, cards, inputs, badges
- [ ] Header scroll: transparent → `#F0EBE1` + `1px solid #8A8278` border on scroll
- [ ] Hero eyebrow label: IBM Plex Mono, 11px, uppercase, `letter-spacing: 0.2em`, `#8A8278`
- [ ] Collection tile text: `#F0EBE1` over dark images
- [ ] Brand statement block: full CSS for the custom HTML section

**Apply after launch if needed:**
- [ ] Hide buy button on product cards (`display: none`)
- [ ] Badge color: `#C41E22` bg, `#F0EBE1` text, `border-radius: 0`, Plex Mono 10px
- [ ] Section title font enforcement (if `@import` doesn't cascade automatically)
- [ ] Footer override (only if theme settings don't apply `#0F0F0F` correctly)

---

### 6. What Can Wait — Phase 2

| Item | Why it can wait |
|---|---|
| Horizontal scroll strip on mobile (New Arrivals) | Default grid works at launch |
| Catalog code auto-generation from collection + SKU | Manual codes in product titles work for now |
| Grain texture hover effect on Instagram strip | Visual detail, no impact on conversion |
| About page full editorial design | Homepage launches without it |
| FAQ / Guía de talles page design | Can be a plain Tiendanube page at launch |
| Mundial and Países collections | Launch with 3 collections, expand after |
| Product page accordion for shipping/returns | Tiendanube's default description handles it |
| Mobile-specific hero layout adjustments | Verify on device, fix post-launch if needed |
