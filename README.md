# Pizza Taktook site (demo v1)

Open `index.html` in a browser. Single file, no build step.

- Menu, prices, hours, delivery fee and WhatsApp number live in the `CONFIG` / `MENU` block at the top of the script.
- Photos: drop PNGs into `images/` named by item id (hero-pizza, margherita, hot-esh, pineapple-chili, spanish, feta-tomato, greek, country, bianca-mushroom, ziva, sambusak, malawach, garlic-sticks, greek-salad, tuna-salad, can, water, soda, small, big). Missing photos fall back to the built-in illustrations.
- Orders: demo ends with a formatted WhatsApp message to the pizzeria. Live version would add real payment (Grow/Cardcom) and automatic order delivery.
- Special pizzas are family size only (73/75 ₪) because no personal-size price was published.

## Privacy (Amendment 13) and accessibility
- Checkout step 2 has a required, unchecked-by-default consent box linking to the privacy policy, plus a separate optional marketing opt-in (recorded in the WhatsApp order).
- Footer links open draft privacy policy and accessibility statement (in `LEGAL` in the script). Both are drafts: a lawyer must review before launch; fill business name, privacy email and accessibility coordinator in `CONFIG`/`LEGAL`.

## Motion
- Vendored locally in `vendor/`: GSAP 3.12.5 + ScrollTrigger (GSAP standard license), Lenis 1.1.13 (MIT) for smooth scroll.
- Design guidance followed: Anthropic's open-source `frontend-design` skill (github.com/anthropics/skills). Per its advice, motion is concentrated in one orchestrated hero intro plus motion that answers actions (toppings dropping on the pizza, dish flying into the cart), with a pizza that turns as you scroll past the builder. No generic fade-up on every section.
- Respects `prefers-reduced-motion` (all motion off).
