# TEAMTAU - Software & DevOps Portfolio

A modern, responsive Jekyll-based portfolio website showcasing software development and DevOps services.

## 🌐 Live Site
https://teamtau.com/

## 📋 Project Overview

This is a static website built with Jekyll and hosted on GitHub Pages. It features:

- **Responsive Design**: Built with Bootstrap framework for mobile-first approach
- **Portfolio Section**: Showcase of completed projects (Dansbutiken, CircleCI)
- **Service Offering**: Software development and DevOps services
- **Parallax Effects**: Engaging visual elements with parallax scrolling
- **Optimized Assets**: Minified CSS and JS, image optimization
- **SEO Ready**: Jekyll SEO tag plugin for search engine optimization

## 🏗️ Project Structure

```
.
├── _config.yml              # Jekyll configuration
├── _layouts/
│   ├── default.html        # Main layout template
│   └── debug.html          # Debug layout
├── _includes/
│   ├── footer.html         # Footer component
│   └── github.html         # GitHub integration
├── _posts/
│   └── portfolio/          # Portfolio project posts
├── assets/
│   ├── css/                # Stylesheets (custom, theme, menu, helper)
│   ├── js/                 # JavaScript files (custom, theme)
│   └── vendor/             # Third-party libraries
│       ├── bootstrap/
│       ├── jquery/
│       ├── font-awesome/
│       ├── owl-carousel/
│       ├── magnific-popup/
│       └── ytplayer/
├── index.html              # Homepage
└── 404.html                # Custom 404 page
```

## 🛠️ Technologies & Dependencies

- **Jekyll**: Static site generator
- **Bootstrap**: Responsive framework
- **jQuery**: JavaScript library
- **Font Awesome**: Icon library
- **Owl Carousel**: Image carousel
- **Magnific Popup**: Lightbox/popup
- **YouTube Player**: Embedded video player
- **Masonry**: Grid layout
- **Waypoints**: Scroll trigger animations
- **CounterUp**: Number animation plugin

## 🚀 Getting Started

### Prerequisites
- Ruby and Jekyll installed

### Local Development

1. Clone the repository:
   ```bash
   git clone https://github.com/teamtau/teamtau.github.io.git
   cd teamtau.github.io
   ```

2. Run your Jekyll site locally:
   ```bash
   jekyll serve
   ```

3. Open your web browser and navigate to:
   ```
   http://localhost:4000
   ```

## 📁 Key Files

- `_config.yml` - Site title, plugins (jekyll-minifier, jekyll-seo-tag, jekyll-feed)
- `index.html` - Homepage with hero section and "What We Do" content
- `assets/css/custom.css` - Custom styling
- `assets/css/theme.css` - Theme styles
- `assets/js/custom.js` - Custom JavaScript
- `CNAME` - Domain configuration (teamtau.com)

## 📞 Contact

If you have questions about this project:

- Email: hello@teamtau.com
- Website: https://teamtau.com/

## 📄 License

See LICENSE file for details.

## 🔧 Maintenance

- Keep Jekyll plugins updated
- Optimize images in `assets/img/`
- Test responsive design across browsers
- Monitor SEO performance
- Regular content updates for portfolio section
