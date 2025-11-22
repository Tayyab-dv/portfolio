# Portfolio - AI Tools & Applications

A collection of AI-powered tools and applications built with modern web technologies.

## 🚀 Live Site

Deploy this portfolio to any static hosting platform:

- **GitHub Pages**: Enable in repository settings
- **Netlify**: Connect repository and deploy
- **Vercel**: Import repository and deploy
- **Cloudflare Pages**: Connect and deploy

## 📦 Projects

### Resume Analysis System
AI-powered resume analyzer that compares resumes against job descriptions using Claude AI.

**Features:**
- PDF/DOCX/TXT file upload support
- Automatic text extraction
- Match analysis with requirement tracking
- Numerical ratings (0-100 scale)
- Critical feedback with actionable insights
- Minimalist monochrome UI
- Privacy-first (no data storage)

**Tech Stack:**
- React 18
- Tailwind CSS
- PDF.js & Mammoth.js
- Anthropic Claude API

**Live Demo:** `resume-analyzer.html`

## 🛠️ Local Development

No build process required! Simply:

1. Clone the repository
   ```bash
   git clone <repository-url>
   cd portfolio
   ```

2. Open `index.html` in your browser
   ```bash
   # macOS
   open index.html

   # Linux
   xdg-open index.html

   # Windows
   start index.html
   ```

3. Or use a local server:
   ```bash
   # Python 3
   python -m http.server 8000

   # Node.js
   npx serve

   # PHP
   php -S localhost:8000
   ```

4. Visit `http://localhost:8000`

## 📁 File Structure

```
portfolio/
├── index.html                      # Portfolio homepage
├── resume-analyzer.html            # Resume analysis tool
├── README.md                       # This file
├── RESUME_ANALYZER_README.md       # Resume analyzer documentation
├── sample-resume.txt               # Test resume file
├── sample-job-description.txt      # Test job description
└── .gitignore                      # Git ignore rules
```

## 🌐 Deployment

### GitHub Pages

1. Go to repository Settings → Pages
2. Source: Deploy from a branch
3. Branch: Select your branch → `/root` folder
4. Save
5. Site will be live at: `https://<username>.github.io/<repo-name>/`

### Netlify

1. Login to [Netlify](https://netlify.com)
2. Click "Add new site" → "Import an existing project"
3. Connect to your Git repository
4. Build settings:
   - Build command: (leave empty)
   - Publish directory: `/`
5. Deploy site

### Vercel

1. Login to [Vercel](https://vercel.com)
2. Click "New Project"
3. Import your Git repository
4. Framework Preset: Other
5. Build settings:
   - Build command: (leave empty)
   - Output directory: (leave empty)
6. Deploy

### Cloudflare Pages

1. Login to [Cloudflare](https://pages.cloudflare.com)
2. Create a project
3. Connect to Git repository
4. Build settings:
   - Build command: (leave empty)
   - Build output directory: `/`
5. Save and deploy

## 🔑 API Keys

The Resume Analyzer requires an Anthropic API key:

1. Visit [Anthropic Console](https://console.anthropic.com/)
2. Create account or sign in
3. Navigate to API Keys
4. Generate new key
5. Copy key (starts with `sk-ant-`)
6. Paste into the tool's API key field

**Note:** API keys are stored only in browser memory and never persisted.

## 🎨 Design Philosophy

- **Minimalist**: Clean interfaces with monochrome aesthetics
- **Functional**: Focus on utility over decoration
- **Fast**: No build process, instant loading
- **Privacy**: No tracking, analytics, or data storage
- **Accessible**: Works on all modern browsers

## 🔒 Privacy & Security

- No cookies or localStorage
- No analytics or tracking scripts
- No data sent to third parties (except API calls)
- API keys stored only in memory
- Files processed client-side
- Open source and auditable

## 🧪 Testing

To test the Resume Analyzer:

1. Open `resume-analyzer.html`
2. Use provided sample files:
   - `sample-resume.txt`
   - `sample-job-description.txt`
3. Add your Anthropic API key
4. Click "Analyze"
5. Review results

## 📝 License

MIT License - feel free to use for personal or commercial projects.

## 🤝 Contributing

Contributions welcome! To add new tools:

1. Create new HTML file for your tool
2. Follow minimalist design principles
3. Add tool card to `index.html`
4. Update this README
5. Submit pull request

## 📧 Support

For issues or questions:
- Check tool-specific README files
- Review browser console for errors
- Verify API keys and file formats
- Ensure modern browser with JavaScript enabled

## 🚧 Roadmap

- [ ] Additional AI-powered tools
- [ ] Dark mode support
- [ ] Offline functionality
- [ ] PWA capabilities
- [ ] More file format support
- [ ] Batch processing features

---

Built with ❤️ using React, Tailwind CSS, and Claude AI
