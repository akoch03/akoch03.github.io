# Andrew Koch — Portfolio Site

A single-page portfolio with three interactive Draco-compressed 3D models (Three.js)
styled as CAE viewports.

## Folder layout
```
site/
├── index.html                  # everything: markup, styles, JS
├── models/
│   ├── capstone-suspension.glb # front suspension assembly (0.9 MB)
│   ├── capstone-axle.glb       # rear axle assembly (1.0 MB)
│   └── conveyor.glb            # packaging line replica (12.7 MB)
├── assets/
│   ├── capstone-reel.mp4       # Design Day video, web-compressed (10.4 MB)
│   ├── reel-poster.jpg         # video poster frame
│   └── Andrew_Koch_Resume.pdf  # <-- ADD YOUR RESUME PDF HERE (this name)
└── README.md
```

## Run it locally
The 3D models load via fetch, so the site must be served over HTTP
(opening index.html directly from the file system will not load models).

```bash
cd site
python3 -m http.server 8000
# open http://localhost:8000
```

## Already filled in
- Resume PDF is at `assets/Andrew_Koch_Resume.pdf`
- Contact email, phone, and LinkedIn are live in the contact section

## Deploy (free options)
- **GitHub Pages**: push this folder to a repo → Settings → Pages → deploy from branch.
- **Netlify / Vercel**: drag-and-drop the `site` folder onto their dashboard.

The 3D viewers use Three.js r160 from jsDelivr and Google's hosted Draco decoder —
no build step, no dependencies to install.
