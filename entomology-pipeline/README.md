# EntomoDB - Specimen Digitization Pipeline Landing Page

An immersive, scroll-driven landing page demonstrating an AI-powered entomological specimen digitization pipeline.

## 🖼️ Image Setup

Place your images in the `images/` folder with these exact filenames:

```
images/
├── base.jpg           # Full specimen box photograph
├── butterfly.png      # Isolated Morpho butterfly (transparent bg)
├── beetle.png         # Isolated Megasoma beetle (transparent bg)
├── mantid.png         # Isolated praying mantis (transparent bg)
├── wasp.png           # Isolated Polistes wasp (transparent bg)
├── color.png          # Color checker chart (transparent bg)
├── labels.png         # Specimen labels (optional)
├── morpho_label.png   # Butterfly label (optional)
├── megasoma_label.png # Beetle label (optional)
├── mantis_label.png   # Mantis label (optional)
└── polistes_label.png # Wasp label (optional)
```

### Image Requirements:
- **base.jpg**: The complete photograph of the entomological display box
- **Isolated specimens**: Same dimensions as base, with transparent backgrounds
- All images should be the same dimensions for proper overlay alignment

## 🚀 Usage

Simply open `index.html` in a modern browser. No build step required.

For development with live reload:
```bash
# Using Python
python -m http.server 8000

# Using Node.js
npx serve .
```

## ✨ Features

### Scroll-Driven Animations
1. **Step 1 - Capture**: Base image fades in showing the full specimen box
2. **Step 2 - Detection**: Scanline effect with glowing bounding boxes highlighting each specimen
3. **Step 3 - Extraction**: Data cards animate in showing extracted information
4. **Step 4 - Database**: Table rows populate with synced status indicators

### Visual Effects
- Specimen glow effects (cyan, amber, violet, rose for each insect type)
- Animated scanline during detection phase
- Progress indicator sidebar
- Parallax hero section
- Smooth scroll transitions

### Responsive Design
- Desktop: Full two-column layouts with progress sidebar
- Tablet: Single column with reordered content
- Mobile: Condensed tables and stacked cards

## 🎨 Customization

### Colors
Edit CSS variables in `:root`:
```css
--accent-cyan: #00e5b8;    /* Butterfly / primary */
--accent-amber: #ffb020;   /* Beetle */
--accent-violet: #a78bfa;  /* Mantis */
--accent-rose: #fb7185;    /* Wasp */
--accent-blue: #60a5fa;    /* Color checker */
```

### Specimen Data
Update the extraction cards and database rows with your actual specimen data by editing the HTML content.

### Detection Box Positions
Adjust positions in CSS to match your specimen layout:
```css
.detection-box.butterfly {
    top: 5%; left: 3%; width: 28%; height: 44%;
}
```

## 📁 File Structure

```
entomology-pipeline/
├── index.html          # Main landing page
├── README.md           # This file
└── images/             # Your specimen images
```

## 🔧 Technical Notes

- Pure HTML/CSS/JS - no dependencies
- Uses Google Fonts: Cormorant Garamond, JetBrains Mono, Instrument Sans
- Intersection Observer API for scroll animations
- CSS custom properties for theming
- Responsive grid layouts

## License

MIT License - Feel free to use and modify for your projects.
