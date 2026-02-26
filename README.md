# South Florida Psalter Website

A static website for the South Florida Psalter project, built with pure HTML/CSS/JS for GitHub Pages hosting.

## 📁 Project Structure

```
sfp-website/
├── index.html           # Homepage
├── psalms.html          # Psalm catalog with search/filter
├── chord-charts.html    # Chord charts browser
├── vision.html          # Vision & 95 Theses
├── articles.html        # Articles (existing)
├── for-churches.html    # Church resources (existing)
├── review/
│   └── index.html       # Chord chart review/approval system
├── assets/
│   ├── sfp-logo.png
│   ├── sfp-logo-400.png
│   └── ...
└── README.md
```

## 🚀 Deployment

This website is designed to be hosted on **GitHub Pages**.

### Option 1: GitHub Pages (Recommended)

1. **Create a GitHub repository** (e.g., `south-florida-psalter`)

2. **Upload files:**
   ```bash
   # From the sfp-website directory
   git init
   git add .
   git commit -m "Initial website commit"
   git remote add origin https://github.com/YOUR_USERNAME/south-florida-psalter.git
   git push -u origin main
   ```

3. **Enable GitHub Pages:**
   - Go to repository Settings → Pages
   - Select branch: `main`
   - Select folder: `/ (root)`
   - Click Save

4. **Access your site:**
   - URL: `https://YOUR_USERNAME.github.io/south-florida-psalter/`

### Option 2: Manual Upload

1. Zip all files in `sfp-website/`
2. Upload to your web host via FTP/cPanel
3. Extract to the public_html folder

## 🔄 Updating the Website

### Making Changes

1. Edit the relevant HTML file(s)
2. Test locally by opening files in a browser
3. Commit and push changes:
   ```bash
   git add .
   git commit -m "Description of changes"
   git push
   ```

4. GitHub Pages will automatically update (may take 1-2 minutes)

### Adding New Chord Charts

1. Add the chord chart markdown file to the appropriate location
2. Update `chord-charts.html` to include the new chart in the data array
3. Update `review/index.html` if the chart needs review

### Updating Psalm Data

The psalm data is hardcoded in `psalms.html` for performance. To update:

1. Edit the `psalmsData` array in `psalms.html`
2. Format: `[psalm_number, "title", "duration", "youtube_video_id"]`

## 🎨 Design System

### Colors
- **Navy:** `#1a1a2e` - Primary dark
- **Gold:** `#d4a574` - Accent
- **Cream:** `#f5f0e8` - Background
- **Burgundy:** `#6b2737` - Secondary accent
- **Green:** `#2d4a3e` - Success/tertiary

### Typography
- **Headings:** Playfair Display (serif)
- **Body:** Source Sans Pro (sans-serif)

## 📱 Responsive Breakpoints

- Desktop: > 1024px
- Tablet: 768px - 1024px
- Mobile: < 768px

## 🔧 Review/Approval Workflow

The `/review/` page provides a staging area for chord charts:

1. **Draft** - Initial upload, not ready for review
2. **Under Review** - Being reviewed for accuracy
3. **Approved** - Ready to publish
4. **Published** - Live on the chord charts page

### Status Management

Currently, status is managed via the JavaScript data array in `review/index.html`. In production, this should connect to:
- A JSON file or API endpoint
- GitHub Issues/Projects
- A simple backend database

## 🔗 Integration Points

### YouTube Playlist
- Main playlist: `https://www.youtube.com/playlist?list=PLmCYMN7HLjZ3sptw2DLvvOjXMUJKG_FIv`
- Individual videos linked in psalms.html

### Dashboard
- Clark's Dashboard: `https://clarkaddisonx222.github.io/clark-dashboard/`
- Linked from chord-charts.html

### Pray150
- Website: `https://pray150.com`
- Companion project for daily Psalm reading

## 🛠️ Development Notes

### No Build Step Required
This is a static site with no build process. Simply edit HTML files directly.

### Local Development
1. Open any HTML file directly in a browser
2. Or use a local server:
   ```bash
   python3 -m http.server 8000
   # Then visit http://localhost:8000
   ```

### Adding New Pages
1. Create new `.html` file
2. Copy the navigation and footer from an existing page
3. Add page-specific content
4. Update all navigation menus to include the new page

## 📋 Todo / Future Enhancements

- [ ] Connect review system to GitHub API for real workflow
- [ ] Add user authentication for review page
- [ ] Auto-generate chord chart listings from file system
- [ ] Add PDF download option for chord charts
- [ ] Implement dark mode toggle
- [ ] Add "Play All" playlist functionality

## 👥 Team

- **Project Lead:** Scott Vander Ploeg
- **Web Developer:** Theo Voss
- **Chord Charts:** Selah Voss

---

*Last updated: 2026-02-26*
