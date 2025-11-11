# 🍽️ Unimeal Student App - Landing Page

A beautiful, modern, and responsive landing page for the Unimeal Student App.

![Version](https://img.shields.io/badge/version-1.0.0-orange)
![License](https://img.shields.io/badge/license-MIT-blue)

## 🌟 Features

- **Modern Design** - Clean, professional UI with gradient backgrounds
- **Fully Responsive** - Optimized for mobile, tablet, and desktop
- **Smooth Animations** - Engaging scroll animations and transitions
- **SEO Optimized** - Meta tags for social sharing and search engines
- **Fast Loading** - Optimized performance with minimal dependencies
- **QR Code Integration** - Easy mobile download via QR code
- **Call-to-Action** - Multiple download buttons strategically placed

## 🛠️ Tech Stack

- **HTML5** - Semantic markup
- **CSS3** - Modern styling with CSS Grid, Flexbox, and custom properties
- **Vanilla JavaScript** - Smooth scrolling and animations
- **Font Awesome** - Beautiful icons
- **Google Fonts** - Inter font family

## 📁 Project Structure

```
unimeal-student-landing/
├── index.html          # Main HTML file
├── style.css           # Stylesheet
├── script.js           # JavaScript functionality
├── README.md           # Documentation
├── package.json        # Project configuration
├── .gitignore          # Git ignore rules
└── .github/
    └── workflows/
        └── deploy.yml  # GitHub Actions deployment
```

## 🚀 Quick Start

### Local Development

1. Clone the repository:
```bash
git clone https://github.com/asm2212/unimeal-student-landing.git
cd unimeal-student-landing
```

2. Open in browser:
```bash
# Using Python
python3 -m http.server 8000

# Using Node.js
npx serve

# Or simply open index.html in your browser
```

3. Visit `http://localhost:8000`

## 📦 Deployment

### GitHub Pages (Recommended)

1. Push your code to GitHub:
```bash
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/asm2212/unimeal-student-landing.git
git push -u origin main
```

2. Enable GitHub Pages:
   - Go to repository **Settings** → **Pages**
   - Select **GitHub Actions** as source
   - The workflow will automatically deploy your site

3. Your site will be live at:
   `https://asm2212.github.io/unimeal-student-landing/`

### Vercel (Alternative)

```bash
npm install -g vercel
vercel
```

### Netlify (Alternative)

Drag and drop the folder to [Netlify Drop](https://app.netlify.com/drop)

## 🎨 Customization

### Colors

Edit CSS variables in `style.css`:

```css
:root {
    --primary: #f97316;        /* Orange */
    --primary-dark: #ea580c;   /* Dark Orange */
    --secondary: #0ea5e9;      /* Blue */
    --dark: #1f2937;           /* Dark Gray */
    --gray: #6b7280;           /* Gray */
    --light: #f8fafc;          /* Light Gray */
}
```

### Content

Edit text content in `index.html`:
- Hero section title and description
- Feature cards
- Download section
- Footer information

### Download Link

Update the APK download link in `index.html`:
```html
<a href="YOUR_NEW_DOWNLOAD_LINK" class="btn-primary">
```

## 📱 Sections

1. **Header** - Fixed navigation with logo and download button
2. **Hero** - Eye-catching gradient background with CTA buttons
3. **Features** - 6 feature cards highlighting app capabilities
4. **Download** - Prominent download section with QR code
5. **Footer** - Contact information and quick links

## 🌐 Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Mobile browsers

## 📄 License

This project is licensed under the MIT License.

## 👥 Contact

- **Email**: asmareadmasu0@gmail.com
- **Phone**: +251 945 906 550
- **GitHub**: [@asm2212](https://github.com/asm2212)

## 🙏 Acknowledgments

- Font Awesome for icons
- Google Fonts for Inter font
- QR Server API for QR code generation

---

**Made with ❤️ for Students - Unimeal v1.4.0**
