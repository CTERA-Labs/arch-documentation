# Arch Documentation Apps

A collection of interactive tools and presentations for architecture documentation, deployed as a Vercel page.

## Structure

```
├── index.html                    # Main landing page
├── vercel.json                   # Vercel deployment configuration
├── Insight-calculator/
│   └── index.html               # Cloud Data Architecture Cost Calculator
├── Insight-presentation/
│   └── index.html               # Insight Architecture Presentation
└── portal-modernization-presentation/
    └── index.html               # AI-Enhanced Modernization Roadmap
```

## Features

- **Dynamic App Discovery**: The main index.html automatically scans directories and creates clickable tiles
- **Modern UI**: Beautiful, responsive design with hover effects and animations
- **App Metadata**: Each app has custom icons, descriptions, and categories
- **Mobile Responsive**: Optimized for all device sizes

## Deployment

### Deploy to Vercel

1. **Connect your repository to Vercel**:
   - Go to [vercel.com](https://vercel.com)
   - Import your GitHub repository
   - Vercel will automatically detect the configuration

2. **Manual deployment**:
   ```bash
   npm i -g vercel
   vercel
   ```

3. **Environment Variables**: No environment variables required for basic functionality

### Local Development

1. **Simple HTTP Server**:
   ```bash
   # Python 3
   python -m http.server 8000
   
   # Python 2
   python -m SimpleHTTPServer 8000
   
   # Node.js
   npx serve .
   ```

2. **Open in browser**: Navigate to `http://localhost:8000`

## Adding New Apps

To add a new application:

1. **Create a new directory** with your app name (use hyphens for spaces)
2. **Add an `index.html` file** in that directory
3. **Update the app configuration** in the main `index.html`:
   ```javascript
   const appConfigs = {
       'your-new-app': {
           icon: '🎨',  // Choose an appropriate emoji
           description: 'Your app description here',
           category: 'Category'
       }
   };
   ```

## App Categories

- **Calculator**: Interactive calculation tools
- **Presentation**: Slide-based presentations
- **Tool**: General purpose utilities
- **Demo**: Proof of concept applications

## Customization

### Styling
The main page uses CSS custom properties for easy theming:
- `--primary-color`: Main brand color
- `--secondary-color`: Accent color
- `--background-color`: Page background
- `--surface-color`: Card backgrounds

### Icons
Use emoji icons for simplicity and universal compatibility. Popular choices:
- 📊 Calculator/Tools
- 🎯 Presentations
- 🚀 Modernization/Architecture
- 📈 Analytics
- 🔧 Utilities

## Browser Support

- Chrome/Edge: Full support
- Firefox: Full support
- Safari: Full support
- Mobile browsers: Responsive design optimized

## License

This project is open source and available under the MIT License.
