# Oil Painting Aesthetic Academic Website

A professional, elegant Jekyll-based personal academic website with a rich "oil painting" aesthetic inspired by 16-18th century European art.

## Features

- **Oil Painting Visual Style**: Warm, textured design with classical color palette
- **Serif Typography**: Playfair Display for headings, Merriweather for body text
- **Canvas Texture**: Layered background for authentic painted feel
- **"Picture Frame" Layout**: Content displayed as artwork in an ornate frame
- **Fully Responsive**: Mobile-friendly design that maintains elegance
- **Academic Sections**: Name, Bio, Education, Research, Publications, Contact
- **Easy Content Management**: All data in YAML files for simple updates

## Quick Start

### Prerequisites

- Ruby (version 2.7 or higher)
- RubyGems
- Bundler

### Installation

1. **Open Terminal/Command Prompt** and navigate to the project directory:
   ```bash
   cd C:\Users\sophi\Desktop\Personal_website
   ```

2. **Install dependencies**:
   ```bash
   gem install bundler
   bundle install
   ```

3. **Build and serve the website locally**:
   ```bash
   bundle exec jekyll serve
   ```

4. **View your website**:
   Open your browser and go to: `http://localhost:4000`

   The site will automatically rebuild when you make changes to files.

## Customization Guide

### 1. Personal Information (`_config.yml`)

Edit the main configuration file to add your details:

```yaml
title: "Your Name | Personal Academic Portfolio"
author: "Dr. Your Name"
description: "Your one-sentence bio"
email: "your.email@university.edu"
google_scholar: "your-scholar-id"
# ... etc.
```

### 2. Education (`_data/education.yml`)

Add your degrees in reverse chronological order:

```yaml
- degree: "Ph.D. in Computer Science"
  institution: "Stanford University"
  location: "Stanford, CA"
  start_year: 2020
  end_year: "Present"
  notes: "Dissertation: Machine Learning for X"
  gpa: "4.0/4.0"  # Optional
```

### 3. Research Experience (`_data/research.yml`)

List your research positions:

```yaml
- position: "Graduate Research Assistant"
  institution: "Stanford University"
  group: "AI Lab"
  location: "Stanford, CA"
  start_year: 2020
  end_year: "Present"
  description: |
    Research on deep learning...
    - Achievement 1
    - Achievement 2
```

### 4. Publications (`_data/publications.yml`)

Add your publications (automatically grouped by year):

```yaml
- title: "Your Paper Title"
  authors:
    - "Lastname, F."
    - "Coauthor, S."
  journal: "Conference/Journal Name"
  volume: "12"
  issue: "3"
  pages: "123-145"
  year: 2024
  url: "https://doi.org/..."
  pdf: "/assets/pdfs/paper.pdf"  # Optional
  type: "journal"  # journal, conference, workshop, or preprint
```

### 5. Canvas Texture (Important!)

The placeholder texture file needs to be replaced with a real image:

1. Download a seamless canvas/linen texture from:
   - [Subtle Patterns](https://www.toptal.com/designers/subtlepatterns/)
   - [Transparent Textures](https://www.transparenttextures.com/)
   - Search for "canvas texture seamless"

2. Requirements:
   - Format: PNG
   - Size: 256x256px or 512x512px (tileable)
   - Opacity: Low (~5-15% transparency)
   - File size: < 100KB

3. Replace the file at:
   ```
   assets/images/canvas-texture.png
   ```

**Temporary solution**: Comment out line 43-45 in `assets/css/style.css` if you don't have a texture yet:

```css
/* background-image: url('/assets/images/canvas-texture.png');
background-repeat: repeat;
background-attachment: fixed; */
```

## Color Customization

All colors are defined as CSS variables in `assets/css/style.css` (lines 6-25).

To change the accent color, modify:

```css
:root {
  --accent-venetian-red: #8A3324;  /* Change this hex code */
  /* Or use alternative colors provided: */
  /* --accent-viridian: #004953; */
  /* --accent-old-gold: #CFB53B; */
}
```

## Project Structure

```
Personal_website/
├── _config.yml              # Main configuration
├── _data/                   # Content data files
│   ├── education.yml
│   ├── research.yml
│   └── publications.yml
├── _includes/               # Reusable components
│   ├── header.html
│   └── footer.html
├── _layouts/                # Page templates
│   ├── default.html
│   └── page.html
├── assets/
│   ├── css/
│   │   └── style.css        # All styling (Oil Painting theme)
│   └── images/
│       └── canvas-texture.png
├── index.md                 # Home page
├── education.md             # Education page
├── research.md              # Research page
├── publications.md          # Publications page
├── contact.md               # Contact page
├── Gemfile                  # Ruby dependencies
└── README.md                # This file
```

## Deployment Options

### GitHub Pages

1. Create a GitHub repository
2. Push your website files
3. Go to Settings → Pages
4. Select branch: `main`, folder: `/ (root)`
5. Your site will be at: `https://username.github.io/repository-name/`

**Important**: Update `_config.yml`:
```yaml
url: "https://username.github.io"
baseurl: "/repository-name"
```

### Netlify

1. Sign up at [Netlify](https://www.netlify.com/)
2. Connect your Git repository (or drag & drop the `_site` folder)
3. Build command: `jekyll build`
4. Publish directory: `_site`

### Other Hosting

Build static files and upload to any web host:

```bash
bundle exec jekyll build
```

Upload contents of the `_site/` folder to your web server.

## Troubleshooting

### Jekyll won't start

- Ensure Ruby and Bundler are installed: `ruby -v` and `bundle -v`
- Try: `bundle update` then `bundle exec jekyll serve`

### Styles not loading

- Check that `style.css` path is correct in `_layouts/default.html`
- Clear browser cache (Ctrl+Shift+R / Cmd+Shift+R)

### Fonts not displaying

- Ensure you have internet connection (fonts loaded from Google Fonts)
- Check browser console for errors

### Images not showing

- Verify image paths use forward slashes: `/assets/images/...`
- For GitHub Pages, check `baseurl` in `_config.yml`

## Adding New Sections

To add a new page (e.g., "Teaching"):

1. Create `teaching.md` in root directory:
   ```markdown
   ---
   layout: page
   title: Teaching
   ---

   Your content here...
   ```

2. Add link to navigation in `_includes/header.html`:
   ```html
   <a href="{{ '/teaching/' | relative_url }}">Teaching</a>
   ```

3. (Optional) Create `_data/teaching.yml` for structured data

## Typography Notes

The site uses **oldstyle-nums** for dates, giving them a classical appearance. This feature may not work in all browsers but will gracefully degrade.

## Browser Support

- Chrome/Edge: Full support
- Firefox: Full support
- Safari: Full support
- Internet Explorer: Not supported (use modern browsers)

## Credits

- **Fonts**: [Google Fonts](https://fonts.google.com/) (Playfair Display, Merriweather)
- **Icons**: Feather Icons (SVG in footer)
- **Design Philosophy**: Inspired by classical European oil paintings (16-18th century)

## License

This template is free to use for personal and academic purposes. Attribution appreciated but not required.

## Support

For Jekyll documentation: https://jekyllrb.com/docs/

For issues specific to this template, check:
1. This README
2. CSS comments in `assets/css/style.css`
3. YAML file comments in `_data/` directory

---

**Last Updated**: December 2024

Built with love, Jekyll, and a deep appreciation for classical art. 🎨
