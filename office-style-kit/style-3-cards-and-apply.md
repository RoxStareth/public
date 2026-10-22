Subject: [Office style 3/3] Cards, controls and how to apply the style

This is the last style email. It gives the style rules for the chunky cards and controls around the pixel picture, as JSON (property names in plain CSS words), and then the steps for applying everything.

{
  "page": { "box-sizing": "border-box", "font": "15px/1.5 system sans-serif", "background": "page.bg", "color": "page.ink" },
  "stageFrame": { "border": "3px solid #3c3a4a", "border-radius": "6px", "overflow": "hidden", "background": "grass", "box-shadow": "0 6px 0 rgba(0,0,0,.12)", "aspect-ratio": "320 / 368" },
  "layout": { "wide-screens-over-1100px": "picture on the left, one 320px card column on the right", "narrow": "stack, picture first" },
  "bubble": { "background": "#fff", "color": "#1c1f23", "border": "2px solid #3c3a4a", "border-radius": "4px", "padding": "1px 6px", "font": "700 8-12px monospace", "tail": "8px square rotated 45deg with dark right and bottom border", "subline": "600, #5d646d", "selected-border": "#1d6fdc", "level-up-background": "#fff4b0" },
  "alertMark": { "background": "#d03030", "color": "#fff", "shape": "circle 1.3em", "animation": "hop 3px up and down, .7s" },
  "sign": { "background": "#3c3a4a", "color": "#fff", "padding": "0 4px", "border-radius": "3px", "font": "700 7-10px monospace" },
  "card": { "background": "#fffdf3", "color": "#1c1f23", "border": "3px solid #3c3a4a", "border-radius": "8px", "padding": "12px 14px", "box-shadow": "4px 4px 0 rgba(0,0,0,.15)", "gap": "10px" },
  "cardTitle": { "font": "800 17px/1.2 monospace" },
  "cardSectionLabel": { "font": "800 11px/1.3 monospace", "text-transform": "uppercase", "letter-spacing": ".08em", "color": "#6a6450" },
  "cardText": { "font-size": "13.5px", "line-height": "1.45" },
  "levelTag": { "font": "800 12px monospace", "background": "#3c3a4a", "color": "#fff8d8", "border-radius": "4px", "padding": "1px 6px" },
  "progressBar": { "height": "8px", "border": "2px solid #3c3a4a", "border-radius": "4px", "track": "#e8e2cf", "fill": "#4bb06a" },
  "askBox": { "border": "2px dashed #b45309", "border-radius": "6px", "padding": "8px 10px", "background": "#fff3dc" },
  "linkButton": { "font": "700 12.5px monospace", "color": "#fff", "background": "#3d7be0", "border": "2px solid #3c3a4a", "border-radius": "6px", "padding": "3px 9px", "secondary": { "background": "#fff", "color": "#1c1f23" } },
  "smallButton": { "font": "700 12px monospace", "border": "2px solid #3c3a4a", "border-radius": "6px", "background": "#fff", "padding": "2px 8px", "selected": { "background": "#3d7be0", "color": "#fff" } },
  "toolbarButton": { "padding": "4px 12px", "border-radius": "8px", "border": "1px solid page.line", "background": "page.panel" },
  "badge": { "font": "700 11px monospace", "border": "2px solid #3c3a4a", "border-radius": "99px", "padding": "1px 8px 1px 5px", "background": "#fff3a8" },
  "rosterTile": { "border": "1px solid page.line", "border-radius": "10px", "background": "page.panel", "padding": "8px 10px", "selected": "2px solid page.focus outline", "layout": "colour badge square 30px on the left, name and two-line description on the right" },
  "statusPill": { "font": "650 11px", "border-radius": "99px", "border": "1px solid page.line", "background": "page.bg", "colours": { "working": "page.ok", "waiting on you": "page.warn", "proposing ideas": "#7c3aed" } },
  "dialogueBox": { "background": "#f8f8e8", "color": "#202820", "border": "3px solid #202820", "box-shadow": "0 0 0 3px #f8f8e8, 0 0 0 5px #202820", "border-radius": "6px", "padding": "8px 12px", "font": "700 10-15px monospace", "position": "over the bottom of the picture, 3% in from both sides", "more-arrow": "small bouncing arrow bottom right" },
  "menuBox": { "same style as dialogueBox": true, "list": "no bullets; the hovered or focused item gets a bouncing triangle on the left; a tick in green #2a7a3a marks done items", "position": "over the top of the picture, max-width 460px, centred" },
  "portrait": { "size": "40 by 52px", "image-rendering": "pixelated", "background": "#e8e2cf", "border": "2px solid #3c3a4a", "border-radius": "6px" },
  "gauge": { "layout": "label 3.5em, bar, value 3em", "bar": "10px high, 2px dark border, 5px radius, track #e8e2cf" },
  "focusRing": "2px solid page.focus, offset 2px, on every control",
  "motion": "hop keyframes translateY(-3px) at 50%; switch every animation off under prefers-reduced-motion"
}

HOW TO APPLY THIS TO MY EXISTING OFFICE
1. Look at the office page that already exists in this project and list what it contains: the agents, their rooms or tiles, the board, any cards or menus. Do not remove or rename any of it.
2. Tell me which of these you will restyle and which parts of the picture you will redraw. Wait for my go.
3. After my go, do the work in this order: (a) the neutral page colours and fonts, light and dark; (b) the card, button and pill rules above; (c) the pixel building, rooms and furniture from style 2; (d) the people sprites and their outfits, using the roles that exist in this project instead of the ones in my examples; (e) bubbles, signs and the dialogue and menu boxes; (f) the day and night tint and the optional classic palette switch.
4. Keep every existing behaviour working. If something in my style conflicts with an accessibility need (contrast of 4.5 to 1 for text, visible keyboard focus, reduced motion), keep accessibility and tell me.
5. Use only these colours and shapes. Do not add new ones without asking. All of this is original artwork. Do not use any real company logos, trade marks or copyrighted game characters or sprites.
6. When you have finished, show me the result, list what you changed, and list anything you could not match.

Please confirm you have received all three style emails, say how many you found, and describe your plan in a few lines before changing anything.
