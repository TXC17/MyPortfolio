# Project Structure

```
MyPortfolio/
├── assets/
│   ├── css/
│   │   └── styles.css          # Main stylesheet
│   ├── js/
│   │   └── script.js           # Main JavaScript file
│   └── images/                 # Image assets (currently using external CDN)
├── .github/
│   └── workflows/
│       └── deploy.yml          # GitHub Actions deployment workflow
├── index.html                  # Main HTML file
├── README.md                   # Project documentation
├── DEPLOY.md                   # Deployment instructions
├── .gitignore                  # Git ignore rules
└── PROJECT_STRUCTURE.md        # This file

```

## File Organization

### Root Level
- `index.html` - Main entry point of the portfolio website

### Assets Directory
- `assets/css/` - All stylesheets
- `assets/js/` - All JavaScript files
- `assets/images/` - Image assets (currently using external CDN for profile photo)

### Configuration Files
- `.github/workflows/deploy.yml` - Automated deployment to GitHub Pages
- `.gitignore` - Excludes unnecessary files from version control
- `README.md` - Project overview and setup instructions
- `DEPLOY.md` - Detailed deployment guide

## External Dependencies
- Google Fonts (Inter font family)
- Profile image hosted on postimg.cc

## Notes
- All unnecessary downloaded files have been excluded via .gitignore
- The project uses a clean, organized structure for easy maintenance
- Static assets are properly organized in the assets directory
