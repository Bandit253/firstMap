# 🛠️ Setup Instructions for second

## 📁 Required Files

Your deployment includes a standalone HTML file that works immediately, but for the best experience, you should also copy the CSS files from the original platform.

## 🎯 Quick Setup (Recommended)

### Option 1: Copy CSS Files
1. From your mapping platform source, copy the `src/css/` folder to your deployment
2. Your file structure should look like:
   ```
   second/
   ├── index.html          ✅ (already generated)
   ├── config.json         ✅ (already generated)
   ├── src/
   │   └── css/
   │       └── main.css    ⚠️ (copy from source)
   ├── package.json        ✅ (already generated)
   └── README.md           ✅ (already generated)
   ```

### Option 2: Use CDN CSS (Alternative)
If you can't copy the CSS files, update the CSS link in `index.html`:

Replace:
```html
<link href="src/css/main.css" rel="stylesheet" />
```

With:
```html
<link href="https://unpkg.com/maplibre-gl@^4.0.0/dist/maplibre-gl.css" rel="stylesheet" />
<style>
/* Basic styling for the deployment */
body { margin: 0; font-family: Arial, sans-serif; }
.app-main { display: flex; height: 100vh; }
.app-sidebar { width: 350px; background: #f8f9fa; border-right: 1px solid #dee2e6; overflow-y: auto; transition: width 0.3s ease; }
.app-sidebar.collapsed { width: 40px; overflow: hidden; }
.app-map-container { flex: 1; position: relative; }
.app-map { width: 100%; height: 100%; }
.sidebar-content { padding: 1rem; }
.sidebar-collapse-toggle { background: none; border: none; font-size: 1.2rem; cursor: pointer; margin-bottom: 1rem; }
.sidebar-section { margin-bottom: 2rem; }
.sidebar-section h3 { margin: 0 0 1rem 0; font-size: 1.1rem; color: #333; }
.layer-item { display: flex; align-items: center; padding: 0.5rem 0; border-bottom: 1px solid #eee; }
.layer-visibility { width: 16px; height: 16px; border: 2px solid #ccc; border-radius: 3px; margin-right: 0.5rem; cursor: pointer; }
.layer-visibility.visible { background: #28a745; border-color: #28a745; }
.layer-name { flex: 1; font-size: 0.9rem; }
.map-info p { margin: 0.25rem 0; font-size: 0.9rem; }
.no-layers { color: #666; font-style: italic; margin: 0; }
.app-header { background: #fff; border-bottom: 1px solid #dee2e6; padding: 1rem; }
.app-header.hidden { display: none; }
.header-title { margin: 0; color: #333; }
.app-footer { background: #f8f9fa; border-top: 1px solid #dee2e6; padding: 0.5rem 1rem; text-align: center; }
.app-footer.hidden { display: none; }
.footer-content p { margin: 0; font-size: 0.8rem; color: #666; }
</style>
```

## 🚀 Testing Your Deployment

1. **Local Testing**: Open `index.html` in your browser
2. **Server Testing**: Use `npm start` if you have the package.json
3. **GitHub Pages**: Upload files and enable Pages in repository settings

## 🔧 Customization

- **Edit Configuration**: Modify `config.json` to change map settings
- **Update Styling**: Edit the CSS in `index.html` or add external stylesheets
- **Add Features**: The HTML includes basic layer management and map controls

## 📞 Support

- Check the browser console for any errors
- Ensure all file paths are correct
- Verify that MapLibre GL JS is loading properly
- For advanced features, consider using the full platform source

## ✅ What's Working

Your deployment includes:
- ✅ Interactive map with MapLibre GL JS
- ✅ Layer visibility controls
- ✅ Sidebar with layer list and map information
- ✅ Navigation controls (zoom, pan, fullscreen)
- ✅ Responsive design
- ✅ Error handling and fallbacks

Enjoy your deployed mapping platform! 🗺️
