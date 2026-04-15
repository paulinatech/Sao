# Minimum CSS — Homepage
## Tiendanube · Viento · Homepage only

| Element / Section | Change Needed | Why It Matters | Can launch without it? |
|---|---|---|---|
| **Global** | Import Google Fonts: Barlow Condensed, Inter, IBM Plex Mono via `@import` | No custom fonts load without this. Everything else depends on it. | No |
| **Global — buttons** | Override `.btn-primary` to outlined: transparent background, `1.5px solid #0F0F0F`, fill on hover | Viento's outlined toggle may not produce the exact style. Button is present on the hero and product page. | No |
| **Global — border radius** | Set `border-radius: 0` on buttons, cards, inputs, badges, image containers | Viento defaults to rounded corners. Every rounded corner breaks the editorial system. | No |
| **Header** | Transparent initial state → `background: #F0EBE1` + `border-bottom: 1px solid #8A8278` on scroll (via `.scrolled` class or `position: sticky`) | Without this, the header either covers the hero image with a white bar or disappears into it. | No |
| **Hero — eyebrow label** | Style the small label above the headline: IBM Plex Mono, 11px, uppercase, `letter-spacing: 0.2em`, color `#8A8278` | This is the catalog reference (`NUEVA ENTRADA / ARG · 003`). Without styling it renders as unstyled body text and loses its meaning. | No |
| **Featured collections — text over image** | Set collection name and label color to `#F0EBE1` inside `.collection-item` or equivalent tile overlay | Viento may render dark text over dark images. Unreadable without this fix. | No |
| **Brand statement block** | Apply background `#0F0F0F`, headline in Barlow Condensed 900 white, body in Inter grey (`#8A8278`), link in mono | Section 6 is custom HTML. Without CSS it renders as unstyled plain text on a white background. | No |
| **Product cards — hide buy button** | `display: none` on the add-to-cart button inside product cards | If the theme setting doesn't suppress it, every card has a buy button that conflicts with the click-through-only card model. | Yes — degrades UX but doesn't break the page |
| **Badges (Nuevo / Últimas unidades)** | Background `#C41E22`, color `#F0EBE1`, `border-radius: 0`, IBM Plex Mono 10px uppercase | Default Tiendanube badge styling is rounded and uses the primary color generically. Needs to match the Sello system. | Yes — badge still shows, just unstyled |
| **Section title labels** | Style `Lo nuevo` and `Los más pedidos` titles: Barlow Condensed 900, uppercase, `#0F0F0F` | If fonts don't cascade automatically from the `@import`, section titles fall back to the system font. | Yes — if font import works, this is handled |
| **Footer** | Background `#0F0F0F`, text `#F0EBE1`, links `#8A8278`, link hover `#F0EBE1` | Theme settings should handle this, but Viento sometimes overrides footer color with a lighter variant. Verify after applying theme settings — add CSS only if needed. | Yes — only add if theme settings don't apply correctly |
