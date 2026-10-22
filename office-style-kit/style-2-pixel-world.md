Subject: [Office style 2/3] Pixel world: building, rooms, furniture, people

This is the second of three style emails. It describes how the pixel picture is built. If your office already has a picture, redraw it to match this. If it has none, build one.

THE CANVAS
- One canvas, 320 wide by 368 high, drawn once as a background and kept. People are separate small canvases drawn on top, moved each frame.
- Scale it up to the width of its column using nearest-neighbour scaling (CSS: image-rendering pixelated, then crisp-edges as a fallback). Keep the aspect ratio 320 to 368. A 3-pixel #3c3a4a border, 6-pixel corner radius and a soft drop shadow of 0 6px 0 rgba(0,0,0,.12) frame it.
- A small helper draws a "box": a filled rectangle with a 1-pixel outline in #3c3a4a. Everything in the building is made from boxes and plain filled rectangles. There are no curves.

THE BUILDING (all coordinates in the 320 by 368 picture)
- Lawn fills the whole canvas in grass green, with about 60 tiny two-pixel tufts of darker green scattered along the bottom strip. Use a fixed random seed so the lawn never changes between loads.
- Outer shell: a brick box from x 4, y 4, width 312, height 346. Add one-pixel brick lines every 4 pixels in the darker brick colour.
- Roof: a 14-pixel band at the top in roof blue-grey, with a 2-pixel lighter highlight line and a dark line under it. Two small grey chimney boxes sit on it at x 30 and x 270.
- Lift shaft: a dark grey vertical band, 26 pixels wide, centred at x 302, running the full height. On each floor a light grey lift door box (22 by 22) with a thin dark centre line and a small red signal light above it.
- Five floors, top to bottom, starting at y 20, 86, 152, 218 and 284. Each floor is 64 pixels high and spans x 22 to x 288. A dark slab is drawn first, then the rooms on top.
- Each floor has a front corridor, 15 pixels high, at the bottom of the floor, filled with a two-tone checker pattern in the corridor colours. A faint dark line (35 per cent opacity) separates rooms from corridor.
- Rooms sit side by side. Each room has: a floor pattern 36 pixels high in one of four themes (wood, tile, pink, blue), a back wall band 11 pixels high in the back wall colour with a thin line under it, and a 2-pixel dark divider on its left edge.
- A small cream floor plate box (15 by 10) with the floor name (4F, 3F, 2F, 1F, GF) sits at the left edge of each floor.
- Front door at the bottom: a dark lintel with a red-brown mat (24 by 4) and a sand coloured doorway (16 by 18), with a short sand path.

FLOOR PATTERNS
Each pattern is a checker or stripe of the two colours given in the palette for that theme, with squares of 4 by 4 pixels.

FURNITURE (all made from boxes, in these colours)
- Desk: wooden top (desk top colour) over a darker front (desk side), 24 wide by about 8 high, outline all round.
- Monitor: a small dark box with a light blue screen rectangle inside.
- Chair: a small dark box below and in front of the desk.
- Plant: a terracotta pot box with two or three leaf-green rectangles on top and a lighter green highlight.
- Shelf: a long thin wood box on the back wall with 4 to 6 tiny coloured book rectangles standing in it.
- Rug: a flat coloured rectangle in front of a desk.
- Whiteboard or poster: a white box on the back wall with a coloured stripe along the top and two or three grey text lines beneath it.
- Filing cabinet: a grey box with three drawers, each a dark line with a small gold handle.
Each room gets a desk, a monitor, a chair and one or two extras that tell you what the room is for. Keep rooms uncluttered: three to five objects.

PEOPLE (sprites)
- Each person is a 10 by 13 pixel canvas, drawn from letter maps with a 1-pixel outline pass first, then the colour pass.
- Letters: H hair, S skin, E eye, C shirt, P trousers, B shoe, a dot means empty.
- The facing-down body rows, in order: "..HHHH..", ".HHHHHH.", ".HSSSSH.", ".SESSES.", "..SSSS..", ".CCCCCC.", "SCCCCCCS", ".CCCCCC.", "..PPPP..".
- The facing-up body rows: "..HHHH..", ".HHHHHH.", ".HHHHHH.", ".HHHHHH.", "..HHHH..", ".CCCCCC.", "SCCCCCCS", ".CCCCCC.", "..PPPP..".
- The facing-left body rows: "..HHHH..", ".HHHHHH.", ".SSSHHH.", ".ESSSHH.", "..SSSS..", "..CCCC..", "..SCCC..", "..CCCC..", "..PPPP..". Facing right is the same rows mirrored.
- Four leg frames appended under the body: ["..P..P..", ".BB..BB."], [".P....P.", "BB....BB"], ["..P..P..", ".BB..BB."], ["...PP...", "..BBBB.."]. Cycle through the frames while walking, and use the first frame when standing still.
- Outline: before colouring, paint the dark outline colour on every filled cell and its four neighbours, then paint the real colours on top. That produces the thick rounded outline.
- Each person has their own hair colour and shirt colour, and a role outfit: a suit has a white collar and a coloured tie (two white pixels, then three tie-coloured pixels down the chest); a hi-vis worker has an orange shirt, a pale yellow stripe on the shirt row and a yellow hard hat; a manager in a signature colour can have a small cream sparkle on the chest.
- Walking speed is about 34 pixels per second. People walk along corridors, enter rooms through the front, sit at the desk seat (18 pixels from the room's left edge, 42 below the floor top) and visit another room's door (16 pixels from its right edge). Use the lift between floors: walk to the lift, ride vertically, then walk out.
- People keep wandering when idle. A person who needs the owner's attention stands still instead and shows a red round alert mark that hops 3 pixels up and down.

SPEECH BUBBLES AND SIGNS
- Bubbles are HTML elements positioned over the canvas, not drawn on it: white background, 2-pixel dark border, 4-pixel radius, bold monospace text, a small rotated square tail under the bubble. A second line in smaller grey text shows the status.
- Room signs: small dark labels with white monospace text on the corridor side of each room, floor signs in cream with dark text, and a spaced-out roof sign across the roof in cream.
- A day and night tint is a full-size transparent overlay above the canvas whose colour fades over two seconds.

An optional "classic" palette switch tints the whole canvas into four shades of green like a monochrome handheld, using a grayscale, sepia and hue-rotate filter on the canvas.

Please confirm you have received style 2 and that you have not changed anything yet.
