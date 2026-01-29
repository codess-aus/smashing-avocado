# Smashing Avocado Blog 🥑

A modern, responsive blog built with MkDocs and Material theme. Features gradient colors, modern fonts, hero images, and full accessibility support.

## 🌟 Features

- **Modern Design**: Gradient color scheme with deep purple and pink accents
- **Responsive**: Mobile-first design that works on all devices
- **Accessible**: WCAG compliant with proper semantic HTML and keyboard navigation
- **Hero Images**: Beautiful gradient hero images on every page
- **Dark Mode**: Automatic theme switching between light and dark modes
- **Fast Search**: Instant search functionality across all content
- **Modern Fonts**: Inter for text and JetBrains Mono for code

## 🚀 Quick Start

### Prerequisites

- Python 3.x
- pip

### Installation

1. Install dependencies:
```bash
pip install -r requirements.txt
```

### Local Development

1. Start the development server:
```bash
mkdocs serve
```

2. Open your browser to `http://127.0.0.1:8000`

3. Make changes to files in the `docs/` directory and see them live!

### Building the Site

Build the static site:
```bash
mkdocs build
```

The built site will be in the `site/` directory.

## 📁 Project Structure

```
smashing-avocado/
├── docs/                      # Content files
│   ├── index.md              # Home page (Welcome to my blog)
│   ├── first-post.md         # First blog post
│   ├── second-post.md        # Second blog post
│   ├── contact.md            # Contact page
│   ├── images/               # Hero images
│   │   ├── welcome-hero.svg
│   │   ├── first-post-hero.svg
│   │   ├── second-post-hero.svg
│   │   └── contact-hero.svg
│   └── stylesheets/          # Custom CSS
│       └── extra.css
├── mkdocs.yml                # MkDocs configuration
├── requirements.txt          # Python dependencies
└── .github/workflows/        # GitHub Actions
    └── deploy.yml            # Auto-deploy to GitHub Pages
```

## 🎨 Customization

### Colors

Edit the gradient colors in `docs/stylesheets/extra.css`:
```css
:root {
  --gradient-primary: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  --gradient-secondary: linear-gradient(135deg, #f093fb 0%, #f5576c 100%);
  --gradient-accent: linear-gradient(135deg, #4facfe 0%, #00f2fe 100%);
}
```

### Theme

Modify theme settings in `mkdocs.yml`:
```yaml
theme:
  palette:
    - scheme: default
      primary: deep purple
      accent: pink
```

### Fonts

Change fonts in `mkdocs.yml`:
```yaml
theme:
  font:
    text: Inter
    code: JetBrains Mono
```

## 🚀 Deployment

### GitHub Pages

The site automatically deploys to GitHub Pages when you push to the `main` branch. Make sure GitHub Pages is enabled in your repository settings.

### Azure Static Web Apps

To deploy to Azure Static Web Apps (planned):

1. Create an Azure Static Web App resource
2. Configure the build settings:
   - Build command: `pip install -r requirements.txt && mkdocs build`
   - Output directory: `site`
3. Connect your GitHub repository

## 📝 Adding New Content

1. Create a new markdown file in the `docs/` directory
2. Add a hero image (optional) in `docs/images/`
3. Update `mkdocs.yml` navigation:
```yaml
nav:
  - Home: index.md
  - Blog:
      - First Post: first-post.md
      - Second Post: second-post.md
      - Your New Post: new-post.md
  - Contact: contact.md
```

### Hero Image Template

Use this markdown at the top of your content:
```markdown
<div class="hero-section" markdown="1">
![Hero Image](images/your-hero.svg){ .hero-image }
</div>

# Your Page Title
```

## 🛠 Technologies

- [MkDocs](https://www.mkdocs.org/) - Static site generator
- [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/) - Modern theme
- [PyMdown Extensions](https://facelessuser.github.io/pymdown-extensions/) - Markdown extensions
- [GitHub Actions](https://github.com/features/actions) - CI/CD
- [GitHub Pages](https://pages.github.com/) - Hosting

## 📄 License

See [LICENSE](LICENSE) file for details.

## 🤝 Contributing

Contributions are welcome! Feel free to open issues or submit pull requests.

---

Built with ❤️ using MkDocs
