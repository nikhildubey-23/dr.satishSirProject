# Dr. Satish Kaushik's Practice Website

A modern, responsive website for Dr. Satish Kaushik's homeopathy practice. Built with HTML5, CSS3, and vanilla JavaScript with Bootstrap 5.

## Features

- ✨ Fully responsive design (mobile-first)
- 🌙 Dark mode toggle with localStorage persistence
- 📚 Books library with PDF support
- 📰 Articles section with inline viewer
- 📅 Appointment booking form
- 📧 Contact form with validation
- 🎨 Modern UI with smooth animations
- ⚡ No external dependencies (except Bootstrap & Font Awesome CDN)
- 🔒 Clean, maintainable code

## Project Structure

```
dr project/
├── index.html              # Home page
├── about.html              # About Dr. Satish Kaushik
├── books.html              # Books library
├── book-viewer.html        # Book viewer page
├── articles.html           # Articles section
├── appointment.html        # Appointment booking
├── contact.html            # Contact form
├── vercel.json             # Vercel deployment config
├── .vercelignore           # Files to ignore in Vercel
├── assets/
│   ├── css/
│   │   └── style.css       # Main stylesheet
│   ├── images/
│   │   └── dockerimg.jpg   # Doctor image
│   └── pdf/
│       └── chronic diseases.pdf  # Sample PDF book
└── README.md               # This file
```

## Local Development

### Requirements
- Any modern web browser
- Python 3 (for local server)

### Running Locally

1. **Clone the repository:**
```bash
git clone https://github.com/nikhildubey-23/dr.satishSirProject.git
cd dr.satishSirProject
```

2. **Start a local server:**
```bash
python3 -m http.server 8000
```

3. **Open in browser:**
```
http://localhost:8000
```

## Deployment on Vercel

### Option 1: Deploy with Git (Recommended)

1. **Prerequisites:**
   - GitHub account
   - Repository already pushed to GitHub (done ✓)
   - Vercel account (free at vercel.com)

2. **Deploy Steps:**
   - Go to [Vercel Dashboard](https://vercel.com/dashboard)
   - Click "Add New Project"
   - Import your GitHub repository: `dr.satishSirProject`
   - Vercel will auto-detect `vercel.json` config
   - Click "Deploy"

3. **That's it!** Your site will be live at: `https://your-project.vercel.app`

### Option 2: Deploy with Vercel CLI

1. **Install Vercel CLI:**
```bash
npm i -g vercel
```

2. **Deploy:**
```bash
vercel
```

3. **Follow the prompts** (link to GitHub repo when asked)

### Option 3: Manual Folder Upload

1. Go to [Vercel Dashboard](https://vercel.com/dashboard)
2. Click "Add New Project" → "Import Project"
3. Select "Other" → "Continue"
4. Drag and drop the project folder
5. Vercel will auto-detect `vercel.json`
6. Click "Deploy"

## Vercel Configuration (`vercel.json`)

The `vercel.json` file includes:
- **Static site configuration** - No build process needed
- **Caching headers** - Assets cached for performance
- **Security headers** - X-Frame-Options, Content-Type protection
- **Clean URLs** - Access pages without `.html` extension
- **Rewrites** - Handles routing for single-page feel

## Features & Usage

### Dark Mode
- Click the moon icon (🌙) in navbar to toggle dark mode
- Setting persists across sessions using localStorage

### Books Library
- Browse all available books
- Search/filter books by title or description
- Click "Read Book" to open PDF in new tab

### Articles
- Read articles about homeopathy
- Search/filter articles
- View full article content in-page

### Appointment Booking
- Fill appointment form with validation
- Dates and times validation
- Confirmation modal on submission
- Data saved to browser localStorage

### Contact Form
- Contact form with email validation
- Phone number validation
- Toast notifications on success/error

## Browser Support

- ✅ Chrome/Edge (latest)
- ✅ Firefox (latest)
- ✅ Safari (iOS 12+)
- ✅ Mobile browsers (all modern)

## Performance

- **Fully responsive** on all device sizes (320px - 4K)
- **Fast load time** - No build process, static files only
- **CDN delivery** - Vercel serves from edge locations
- **Optimized assets** - Minimal CSS/JS, lazy-loaded content

## Customization

### Update Doctor Information
Edit these files:
- `index.html` - Hero section, about section
- `about.html` - Qualifications, experience, testimonials
- `contact.html` - Address, phone, email, hours

### Add/Edit Books
Edit `books.html` or any HTML file with `bookGrid`:
```html
<div class="col-md-4 mb-4">
  <div class="card h-100">
    <img src="..." class="card-img-top" alt="Book Title">
    <div class="card-body d-flex flex-column">
      <h5 class="card-title">Book Title</h5>
      <p class="card-text">Description here</p>
      <button class="btn btn-primary mt-auto" onclick="viewBookPdf(id)">Read Book</button>
    </div>
  </div>
</div>
```

### Add/Edit Articles
Edit `articles.html` or any HTML file with `articleGrid`:
```html
<div class="col-md-4 mb-4">
  <div class="card h-100 article-card">
    <img src="..." class="card-img-top" alt="Article Title">
    <div class="card-body d-flex flex-column">
      <h5 class="card-title">Article Title</h5>
      <p class="card-text">Short description</p>
      <button class="btn btn-primary mt-auto" onclick="viewArticle(id)">Read More</button>
    </div>
  </div>
</div>
```

## Troubleshooting

### Images not loading
- Ensure images are in `assets/images/` folder
- Check file paths are relative: `./assets/images/filename.jpg`

### PDFs not opening
- Ensure PDFs are in `assets/pdf/` folder
- Verify filename in JavaScript matches actual file

### Dark mode not persisting
- Check browser localStorage is enabled
- Clear cache and reload

### Forms not working
- Check browser console (F12) for errors
- Ensure Bootstrap JS is loaded (CDN link)

## Support

For issues or questions about deployment:
1. Check Vercel documentation: https://vercel.com/docs
2. Review GitHub repo: https://github.com/nikhildubey-23/dr.satishSirProject
3. Contact the developer

## License

© 2025 Dr. Satish Kaushik. All rights reserved.

---

**Happy deploying! 🚀**
