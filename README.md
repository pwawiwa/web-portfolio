# Muhammad Ihsan Prawira Hutomo - Portfolio Website

A modern, responsive portfolio website built with **Astro** and **Tailwind CSS**. Showcasing work in Data Science, ML/AI Engineering, Computer Vision, and Data Engineering.

##  Features

- **Dark Theme with Emerald Accents**: Modern, eye-catching design with graph-themed animations
- **Graph Background & Animations**: Animated grid background with floating nodes and connecting lines
- **Fully Responsive**: Optimized for mobile (iPhone SE), tablet, and desktop
- **Semantic HTML**: Accessible and SEO-friendly markup
- **Smooth Scrolling**: Enhanced user experience with smooth page navigation
- **Section Highlights**:
  - Hero Section with CTA to LinkedIn
  - Comprehensive About Me section
  - Featured Projects Grid
  - Timeline for Experience & Education
  - Contact Section with Social Links
  - Footer with Quick Navigation

##  Tech Stack

- **Framework**: [Astro](https://astro.build)
- **Styling**: [Tailwind CSS](https://tailwindcss.com)
- **Hosting**: [Vercel](https://vercel.com)
- **Fonts**: Inter (headers), Fira Code (code)
- **Animations**: CSS keyframes and transitions

## 🛠️ Installation & Setup

### Prerequisites
- Node.js 18+ and npm/yarn/pnpm installed

### Steps

1. **Install dependencies**:
   ```bash
   npm install
   ```

2. **Start development server**:
   ```bash
   npm run dev
   ```
   The site will be available at `http://localhost:3000`

3. **Build for production**:
   ```bash
   npm run build
   ```

4. **Preview production build**:
   ```bash
   npm run preview
   ```

## 📝 Customization Guide

### 1. Update Personal Information
- **Navigation Logo**: Edit `MIP` text in [src/components/Navigation.astro](src/components/Navigation.astro)
- **Hero Section**: Update name and title in [src/components/Hero.astro](src/components/Hero.astro)
- **LinkedIn URL**: Replace `https://linkedin.com/in/muhammadihsanprawira` with your LinkedIn profile

### 2. Add/Update Project Images
In [src/components/Projects.astro](src/components/Projects.astro), replace the placeholder image divs:

```html
<!-- Original placeholder -->
<div class="h-48 bg-gradient-to-br from-emerald-900/20 to-slate-900/50 flex items-center justify-center">
  <p class="text-emerald-400 font-mono text-sm">Project Image</p>
</div>

<!-- Replace with your image -->
<img 
  src="/path/to/your/image.jpg" 
  alt="Project name" 
  class="w-full h-48 object-cover"
/>
```

> **Image Placement**: Store images in `/public/assets/` directory and reference them as `/assets/image-name.jpg`

### 3. Fill in Project Details
Update the projects section with actual project information:

```astro
<!-- In Projects.astro -->
<h3 class="text-xl font-bold">Your Project Title</h3>
<p>Your project description and the technologies used</p>
<span class="inline-block px-2 py-1 bg-emerald-500/20 text-emerald-300 rounded text-xs font-mono">
  Python
</span>
```

### 4. Update Experience/Timeline
Edit [src/components/Experience.astro](src/components/Experience.astro) to add your education and work experience:

```astro
<h3 class="text-xl font-bold text-slate-100 mb-2">Your Job Title</h3>
<p class="text-slate-400 text-sm mb-3">Company Name</p>
<p class="text-slate-500 text-sm">Jan 2023 - Dec 2024 • Location</p>
<p class="text-slate-400 text-sm mt-3">Description of your role and achievements.</p>
```

### 5. Update Contact Information
In [src/components/Contact.astro](src/components/Contact.astro):
- Change email link: `mailto:your.email@example.com`
- Add calendar scheduling link (e.g., Calendly, Cal.com)
- Update social media links (LinkedIn, GitHub, Twitter/X)

### 6. Customize Colors
Edit [tailwind.config.mjs](tailwind.config.mjs) to change the color scheme:

```javascript
colors: {
  'emerald': {
    400: '#34d399', // Change primary accent color here
    500: '#10b981',
  },
}
```

### 7. Update Site Metadata
In [astro.config.mjs](astro.config.mjs):
- Set your domain: `site: 'https://yourdomain.com'`

In [src/layouts/Layout.astro](src/layouts/Layout.astro):
- Update meta descriptions and OG tags

## 🚀 Deployment to Vercel

1. **Push to GitHub**:
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git push origin main
   ```

2. **Connect to Vercel**:
   - Visit [vercel.com](https://vercel.com)
   - Click "New Project"
   - Import your GitHub repository
   - Vercel auto-detects Astro and applies correct settings
   - Click "Deploy"

3. **Custom Domain** (optional):
   - Add your domain in Vercel project settings
   - Update nameservers at your domain registrar

## 📱 Responsive Design

The website is optimized for:
- **Mobile**: iPhone SE (375px) and up
- **Tablet**: iPad and larger tablets
- **Desktop**: Standard desktop and ultra-wide monitors

All sections use responsive grid layouts that adapt seamlessly.

## ♿ Accessibility

- Semantic HTML5 elements
- Proper heading hierarchy (h1, h2, h3)
- ARIA labels for icon buttons
- Keyboard navigation support
- Focus visible states
- Color contrast meets WCAG AA standards

## 🎨 Design Features

### Animations
- **Graph Background**: Animated grid pattern with opacity changes
- **Floating Nodes**: CSS-animated circular elements
- **Glow Effect**: Text glow animation on hero name
- **Parallax**: Subtle parallax scrolling effects
- **Hover States**: Button and card hover animations

### Theme
- **Dark Mode**: Full dark theme (#0f172a)
- **Emerald Accents**: Royal green (#10b981)
- **Typography**: 
  - Headers: Inter (clean, modern)
  - Code: Fira Code (monospace)

## 📞 Support

For questions or issues:
1. Check the [Astro Documentation](https://docs.astro.build)
2. Review [Tailwind CSS Docs](https://tailwindcss.com/docs)
3. Update components as needed for your content

## 📄 License

This portfolio template is free to use and modify for personal use.

---

**Built with ❤️ for Data Scientists and ML Engineers**
