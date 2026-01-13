# VuAdmin Updates

A public GitHub Pages site displaying the latest updates, features, and bug fixes for VuAdmin.

## 🌐 Live Site

The updates page is available at: `https://auditeers.github.io/vuadmin_updates/`

## 📝 How to Update

To add new updates to the page:

1. Edit the `index.html` file
2. Add a new update section following the existing format:

```html
<div class="update">
    <div class="update-header">
        <div>
            <span class="version">Version X.X.X</span>
            <span class="update-type feature">New Features</span>
            <!-- OR use: update-type improvement, update-type bugfix -->
        </div>
        <span class="date">Month Day, Year</span>
    </div>
    <div class="update-content">
        <h3>🎉 New Features</h3>
        <ul>
            <li>Feature description</li>
        </ul>
        <h3>⚡ Improvements</h3>
        <ul>
            <li>Improvement description</li>
        </ul>
        <h3>🐛 Bug Fixes</h3>
        <ul>
            <li>Bug fix description</li>
        </ul>
    </div>
</div>
```

3. Commit and push your changes
4. The GitHub Pages site will automatically update within a few minutes

## 🎨 Update Types

- **feature** (green) - Use for new features
- **improvement** (blue) - Use for enhancements and improvements
- **bugfix** (red) - Use for bug fixes

## 🚀 GitHub Pages Setup

This repository is configured to use GitHub Pages. To enable it:

1. Go to repository Settings
2. Navigate to Pages section
3. Under "Source", select the main/master branch
4. Click Save

The site will be published at `https://auditeers.github.io/vuadmin_updates/`

## 📄 Files

- `index.html` - Main updates page with styling
- `_config.yml` - GitHub Pages configuration
- `README.md` - This file

## 🔧 Local Testing

To test the page locally:

1. Open `index.html` directly in your browser, or
2. Use a local server:
   ```bash
   python -m http.server 8000
   # Then visit http://localhost:8000
   ```

## 💡 Tips

- Keep update descriptions clear and concise
- Include dates for each version release
- Organize updates with newest at the top
- Use consistent formatting for better readability
- Update the "Last updated" date in the footer when making changes
