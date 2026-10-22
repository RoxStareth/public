Subject: [Office style 1/3] Visual language: palette, type, building, mood

Hello. This is the first of three emails (style 1 to 3) that I sent to myself. They describe only the visual styling of an "agent office" page that I built in another project, which I like a great deal. Please do not change the agents, the board content or any of the logic of the office that already exists in this project. Restyle only: colours, type, shapes, the way things are drawn, and the feel of the page. To find them, search my mailbox for subjects that start with "[Office style" and read them in number order (1, 2, 3); if one is missing, tell me which and stop. Read all three before you change anything, then tell me your plan and wait for me to say go.

What the office looks like in one paragraph: a top-down, Game Boy era pixel-art building seen from the front, five floors high, with a grey lift shaft on the right and a front door at the bottom, standing on a bright green lawn. Each floor has rooms side by side along a front corridor. Every room has a back wall band, a patterned floor, and a few simple pieces of furniture drawn as flat blocks with a dark outline. Small pixel people walk the corridors, sit at desks, ride the lift and show a speech bubble. Around the picture sit chunky cards with thick dark borders and a hard offset shadow, in a monospace type. The rest of the site stays calm and neutral, so the pixel office is the only thing with a strong personality.

Principles to keep:
1. Flat colour only. No gradients, no blur, no soft shadows inside the picture. Shadows are hard offsets.
2. One dark outline colour (a blue-grey near black, #3c3a4a) used for everything: outlines of the building, people, furniture, card borders and text on speech bubbles.
3. The picture is drawn at a very small size (320 by 368 pixels) and scaled up with nearest-neighbour scaling so every pixel stays square and crisp.
4. Warm, cheerful, slightly muted colours for the world; a calm neutral page around it.
5. Monospace type for anything inside the world (labels, bubbles, cards, buttons); a normal system sans-serif type for the neutral page.
6. Motion is small: a bouncing alert mark, a blinking menu arrow, and walking. Everything animated must stop when the viewer has reduced motion switched on.
7. Cards read like game dialogue boxes: cream background, thick border, rounded corners of 6 to 8 pixels, a hard shadow offset by 4 pixels.

The palette follows as JSON. "world" colours are used inside the pixel picture. "page" colours are the calm neutral site around it, with a light and a dark version. "card" colours are for the chunky cards.

{
  "outline": "#3c3a4a",
  "world": {
    "grass": "#8fe36b", "grassTuft": "#5cbf4a", "sand": "#f6eaa6",
    "brick": "#c9b8a6", "brickLine": "#b3a290",
    "roof": "#5b6b8a", "roofHighlight": "#7486a6",
    "backWall": "#e9e4d8", "backWallLine": "#cdc5b3",
    "floorWood": ["#e2aa66", "#c98e4d"],
    "floorTile": ["#f3e9bb", "#e6d9a0"],
    "floorPink": ["#f7d3cd", "#ebb8b0"],
    "floorBlue": ["#d6e6f5", "#c2d7ec"],
    "corridor": ["#e8e2cf", "#ddd5bd"],
    "deskTop": "#b97a3c", "deskSide": "#8a5a2b",
    "monitorScreen": "#6ec1f0", "plantLeaf": "#3f9a3f", "plantLeafLight": "#62c25a", "plantPot": "#c0603a",
    "paper": "#ffffff", "skin": "#f6c89f", "shoe": "#3c3a4a",
    "liftShaft": "#4a4a5a", "liftCar": "#b8bec8", "liftSignal": "#e05a4f",
    "floorPlate": "#fff8d8", "doorMat": "#b5554a"
  },
  "page": {
    "light": { "bg": "#f4f4f1", "panel": "#ffffff", "ink": "#1c1f23", "muted": "#5d646d", "line": "#dcdcd6", "lineSoft": "#ebebe6", "accent": "#2f4858", "accentInk": "#ffffff", "focus": "#1d6fdc", "ok": "#047857", "warn": "#b45309", "bad": "#b91c1c" },
    "dark": { "bg": "#14161a", "panel": "#1d2025", "ink": "#e8e9ea", "muted": "#a1a8b1", "line": "#343941", "lineSoft": "#292d33", "accent": "#8fb3c9", "accentInk": "#10161a", "focus": "#6aa8ff", "ok": "#4cc79b", "warn": "#f0b35a", "bad": "#ff8585" }
  },
  "card": {
    "background": "#fffdf3", "ink": "#1c1f23", "border": "3px solid #3c3a4a", "radius": "8px",
    "shadow": "4px 4px 0 rgba(0,0,0,.15)", "labelMuted": "#6a6450",
    "highlight": "#fff3a8", "askBackground": "#fff3dc", "askBorder": "2px dashed #b45309",
    "linkBlue": "#3d7be0", "alertRed": "#d03030", "progressGreen": "#4bb06a", "progressTrack": "#e8e2cf"
  },
  "dialogueBox": {
    "background": "#f8f8e8", "ink": "#202820", "border": "3px solid #202820",
    "extraRing": "0 0 0 3px #f8f8e8, 0 0 0 5px #202820", "radius": "6px"
  },
  "type": {
    "world": "ui-monospace, SFMono-Regular, Menlo, Consolas, monospace",
    "page": "system-ui, -apple-system, 'Segoe UI', Roboto, sans-serif",
    "pageSize": "15px / 1.5", "cardTitle": "800 17px / 1.2 mono", "cardSectionLabel": "800 11px mono, uppercase, letter-spacing .08em, colour labelMuted",
    "bubble": "700 mono, size between 8px and 12px depending on width", "roofSign": "800 mono, letter-spacing .2em, colour #fff8d8"
  }
}

Please confirm you have received style 1 and that you have not changed anything yet.
