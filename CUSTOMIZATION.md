# 🚀 Portfolio Website - Complete Setup & Customization Guide

## Project Overview

You now have a **production-ready portfolio website** built with:
- ⚡ **Astro** - Fast static site generation
- 🎨 **Tailwind CSS** - Utility-first styling
- 📊 **Graph-themed animations** - Modern visual design
- ♿ **Full accessibility** - WCAG AA compliant
- 📱 **Responsive design** - Works on all devices

---

## 🎯 Next Steps

### 1. Start the Development Server

```bash
cd /Users/wirahutomo/Projects/web_portfolio
npm run dev
```

Visit **http://localhost:3000** to see your site live with hot-reload enabled.

### 2. Customize Your Information

Update these files with your actual information:

#### A. LinkedIn URL (Hero Section)
**File**: `src/components/Hero.astro`
```astro
<a 
  href="https://linkedin.com/in/YOUR_LINKEDIN_PROFILE"  <!-- Change this -->
  target="_blank" 
  rel="noopener noreferrer"
  class="px-8 py-3 bg-emerald-500 ..."
>
  Contact!
</a>
```

#### B. Email (Contact Section)
**File**: `src/components/Contact.astro`
```astro
<a href="mailto:YOUR_EMAIL@example.com" class="...">
  Send Email
</a>
```

#### C. Social Media Links
**File**: `src/components/Contact.astro` & `src/components/Footer.astro`
```astro
<a href="https://linkedin.com/in/YOUR_PROFILE" target="_blank" ...>
<a href="https://github.com/YOUR_USERNAME" target="_blank" ...>
<a href="https://twitter.com/YOUR_HANDLE" target="_blank" ...>
```

### 3. Add Your Projects

**File**: `src/components/Projects.astro`

Replace each project card:

```astro
<!-- OLD: Placeholder -->
<h3 class="text-xl font-bold">Project Title</h3>

<!-- NEW: Your project -->
<h3 class="text-xl font-bold">Indonesian Lip Reading System</h3>
<p class="text-slate-400 text-sm">
  Deep learning-based computer vision system for lip reading using PyTorch and TensorFlow.
</p>
<span class="inline-block px-2 py-1 bg-emerald-500/20 text-emerald-300 rounded text-xs font-mono">
  PyTorch
</span>
<span class="inline-block px-2 py-1 bg-emerald-500/20 text-emerald-300 rounded text-xs font-mono">
  Computer Vision
</span>
```

#### Adding Project Images

1. **Prepare your image**: Save a screenshot/image of your project as:
   - `/public/assets/project-1.jpg` (or .png)
   - Keep dimensions: ~1200x700px for best quality

2. **Update the HTML** in `Projects.astro`:
   ```astro
   <!-- Replace this placeholder div -->
   <div class="h-48 bg-gradient-to-br from-emerald-900/20 to-slate-900/50 flex items-center justify-center">
     <p class="text-emerald-400">Project Image</p>
   </div>

   <!-- With this image -->
   <img 
     src="/assets/project-1.jpg" 
     alt="Indonesian Lip Reading System"
     class="w-full h-48 object-cover"
   />
   ```

### 4. Fill in Your Experience & Education

**File**: `src/components/Experience.astro`

Update the timeline items:

```astro
<!-- Replace placeholder experience -->
<h3 class="text-xl font-bold text-slate-100 mb-2">Your Job Title</h3>
<p class="text-slate-400 text-sm mb-3">Company Name</p>
<p class="text-slate-500 text-sm">Jan 2023 - Dec 2024 • Jakarta, Indonesia</p>
<p class="text-slate-400 text-sm mt-3">
  Describe your role, key projects, and achievements. Highlight technologies used and impact made.
</p>
```

Example timeline structure (there are 3 slots):
1. **Most Recent**: Job/Internship
2. **Previous**: Education or older position
3. **Earlier**: Education or first job

---

## 🎨 Customizing the Design

### Change the Primary Color

If you want to change from Emerald Green to another color:

**File**: `tailwind.config.mjs`

```javascript
colors: {
  'emerald': {
    400: '#3B82F6',  // Change to blue
    500: '#2563EB',
    600: '#1D4ED8',
    700: '#1E40AF',
  },
}
```

Common colors:
- **Blue**: `#3B82F6`, `#2563EB`, `#1D4ED8`
- **Purple**: `#A855F7`, `#9333EA`, `#7E22CE`
- **Rose**: `#F43F5E`, `#E11D48`, `#BE185D`
- **Cyan**: `#06B6D4`, `#0891B2`, `#0E7490`

### Change the Site Title & Metadata

**File**: `src/layouts/Layout.astro`

```astro
<title>Your Name - Data Scientist & ML Engineer</title>
<meta name="description" content="Your professional description here" />
<meta name="og:title" content="Your Name - Portfolio" />
<meta name="og:description" content="Your description here" />
```

### Customize the Hero Section

**File**: `src/components/Hero.astro`

```astro
<h1 class="text-5xl sm:text-6xl lg:text-7xl font-bold mb-4 text-slate-100">
  Your Name <br />
  <span class="text-emerald-400 animate-glow">Your Last Name</span>
</h1>
<p class="text-xl sm:text-2xl text-slate-400 mb-8">
  Your Professional Title / Role
</p>
```

---

## 📸 Working with Images

### Directory Structure
```
public/
├── assets/
│   ├── project-1.jpg
│   ├── project-2.jpg
│   ├── project-3.jpg
│   ├── profile.jpg          (optional - for about section)
│   └── other-assets.jpg
```

### Image Best Practices
- **Format**: JPG for photos, PNG for graphics, WebP for modern browsers
- **Size**: 
  - Project images: ~1200x700px
  - Profile pic: ~200x200px
  - Keep under 500KB for web
- **Optimization**: Use [TinyPNG](https://tinypng.com) or [Squoosh](https://squoosh.app)

### Adding a Profile Photo

1. Save your photo to `/public/assets/profile.jpg`
2. Add to About section in `src/components/About.astro`:
   ```astro
   <div>
     <img 
       src="/assets/profile.jpg" 
       alt="Muhammad Ihsan Prawira Hutomo"
       class="w-48 h-48 rounded-lg object-cover"
     />
   </div>
   ```

---

## 🔗 Section Navigation Reference

All sections have anchor links:

```
#first       → Hero Section
#about       → About Me
#projects    → Featured Projects
#experience  → Experience & Education
#contact     → Contact
```

You can link to these from anywhere:
```html
<a href="#projects">View Projects</a>
```

---

## 🚀 Deployment to Vercel

### Step 1: Push to GitHub

```bash
cd /Users/wirahutomo/Projects/web_portfolio
git init
git add .
git commit -m "Initial portfolio website"
git remote add origin https://github.com/YOUR_USERNAME/web_portfolio.git
git push -u origin main
```

### Step 2: Deploy to Vercel

1. Go to **[vercel.com](https://vercel.com)**
2. Sign in with GitHub
3. Click **"New Project"**
4. Select your `web_portfolio` repository
5. Settings should be auto-detected (Astro, npm)
6. Click **"Deploy"**

Done! Your site is live. 🎉

### Step 3: Custom Domain (Optional)

1. In Vercel dashboard, go to your project settings
2. Click **"Domains"**
3. Add your domain (e.g., `muhammadihsanprawira.dev`)
4. Update DNS records at your domain registrar

---

## 🎬 Animation & Effects

The site includes these animations (all CSS-based, no JavaScript overhead):

1. **Grid Background**: Subtle pulsing graph pattern
2. **Floating Nodes**: Animated circles in hero section
3. **Glow Effect**: Name glows with emerald light
4. **Hover Effects**: Cards scale and glow on hover
5. **Scroll Animations**: Elements fade in as you scroll
6. **Parallax**: Subtle depth effects

To modify animations, edit keyframes in component `<style>` blocks.

---

## 📝 Content Template Examples

### Project Card Template
```astro
<h3 class="text-xl font-bold">Project Name</h3>
<p class="text-slate-400 text-sm">
  Problem: What problem did you solve?
  Solution: How did you solve it?
  Tech: What technologies did you use?
</p>
<span class="px-2 py-1 bg-emerald-500/20 text-emerald-300 text-xs font-mono">Python</span>
<span class="px-2 py-1 bg-emerald-500/20 text-emerald-300 text-xs font-mono">PyTorch</span>
```

### Experience Entry Template
```astro
<h3 class="text-xl font-bold">Job Title</h3>
<p class="text-slate-400 text-sm">Company Name</p>
<p class="text-slate-500 text-sm">Jan 2023 - Dec 2024 • Location</p>
<p class="text-slate-400 text-sm">
  • Key responsibility or achievement
  • Another key result
  • Impact or metric you improved
</p>
```

---

## 🔧 Troubleshooting

### Build Fails
```bash
# Clear cache and rebuild
rm -rf node_modules dist
npm install
npm run build
```

### Hot reload not working
- Restart dev server: `Ctrl+C` then `npm run dev`
- Check if port 3000 is available

### Images not showing
- Verify image path: `/assets/filename.ext`
- Check image exists in `/public/assets/`
- File names are case-sensitive

### Styling issues
- Clear browser cache: `Ctrl+Shift+R` (Windows/Linux) or `Cmd+Shift+R` (Mac)
- Rebuild Tailwind: `npm run build`

---

## 📚 Documentation Links

- **Astro**: https://docs.astro.build
- **Tailwind CSS**: https://tailwindcss.com/docs
- **Vercel**: https://vercel.com/docs
- **Google Fonts**: https://fonts.google.com

---

## 🎓 File Guide

| File | Purpose |
|------|---------|
| `src/pages/index.astro` | Main page combining all sections |
| `src/components/*.astro` | Individual section components |
| `src/layouts/Layout.astro` | Base layout wrapper |
| `tailwind.config.mjs` | Tailwind CSS customization |
| `astro.config.mjs` | Astro framework settings |
| `public/assets/` | Your images and media |
| `package.json` | Dependencies and scripts |

---

## ✨ Pro Tips

1. **Use Lighthouse**: Test performance at https://pagespeed.web.dev/
2. **Test Responsiveness**: Use Chrome DevTools device emulation
3. **SEO Check**: Use https://www.seobility.net/ for analysis
4. **Color Accessibility**: Check contrast at https://webaim.org/resources/contrastchecker/
5. **Image Compression**: Reduce file size at https://squoosh.app/

---

## 📞 Need Help?

- Check the main `README.md` for detailed guide
- Review component files - they're well-commented
- Astro documentation: https://docs.astro.build/en/getting-started/

---

**Your portfolio website is ready! 🎉**

Start customizing, deploy to Vercel, and showcase your amazing work!

---

*Built with Astro ⚡ & Tailwind CSS 🎨*  
*Optimized for Data Scientists & ML Engineers*
