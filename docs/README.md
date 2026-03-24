# Website Documentation

This directory contains the companion learning website for **Build A Reasoning Model (From Scratch)**.

## Overview

The website provides an interactive, user-friendly interface for learning how to build reasoning models with:

- Progressive chapter navigation
- Interactive code examples
- Exercise tracking
- Bonus materials
- Resource library
- Setup guides

## Structure

```
docs/
├── index.html              # Homepage
├── css/
│   ├── style.css          # Main stylesheet
│   └── chapter.css        # Chapter-specific styles
├── js/
│   └── script.js          # Interactive functionality
├── chapters/
│   ├── chapter02.html     # Individual chapter pages
│   ├── chapter03.html
│   └── ...
├── resources/
│   ├── troubleshooting.html
│   ├── setup.html
│   ├── bonus.html
│   └── checkpoints.html
└── _config.yml            # GitHub Pages configuration
```

## Features

### Homepage
- Hero section with book cover and description
- Mental model visualization
- Feature highlights
- Complete chapter listing
- Setup instructions
- Resource links

### Chapter Pages
- Chapter overview and learning objectives
- Links to Jupyter notebooks on GitHub
- Code examples with syntax highlighting
- Exercise lists with difficulty indicators
- Solutions access
- Bonus materials
- Navigation between chapters

### Resources
- Troubleshooting guide
- Setup instructions
- Model checkpoints download
- Discussion forum links
- Bonus content index

## Technology Stack

- **HTML5**: Semantic markup
- **CSS3**: Modern styling with CSS Grid and Flexbox
- **JavaScript**: Interactive features and smooth scrolling
- **Prism.js**: Syntax highlighting for code blocks
- **Font Awesome**: Icons
- **GitHub Pages**: Hosting

## Development

### Local Testing

To test the website locally:

1. Use a simple HTTP server:
   ```bash
   cd docs
   python -m http.server 8000
   ```

2. Open `http://localhost:8000` in your browser

### GitHub Pages Deployment

The website is automatically deployed to GitHub Pages from the `docs/` directory.

To enable:

1. Go to repository Settings > Pages
2. Set Source to "Deploy from a branch"
3. Select branch: `main` or your current branch
4. Set folder to `/docs`
5. Save

The site will be available at: `https://kodecraze.github.io/reasoning-from-scratch/`

## Customization

### Colors
Edit CSS variables in `css/style.css`:
```css
:root {
    --primary-color: #2563eb;
    --secondary-color: #7c3aed;
    --accent-color: #f59e0b;
    /* ... */
}
```

### Content
- Update chapter descriptions in `index.html`
- Add new chapter pages in `chapters/`
- Modify resource pages in `resources/`

## Browser Support

- Chrome/Edge (latest)
- Firefox (latest)
- Safari (latest)
- Mobile browsers

## Contributing

This website mirrors the book content. For content suggestions or bug reports, please use the main repository's issue tracker.

## License

Licensed under Apache License 2.0, matching the main repository.
