# Video Script Generator

A simple, embeddable video script generator for creating engaging video scripts quickly.

## Features

- 📝 Simple form-based interface
- 🎨 Modern, gradient design
- 📱 Fully responsive
- 🔗 iframe-ready
- 📋 One-click copy to clipboard
- ⚡ No dependencies - pure HTML/CSS/JavaScript

## Usage

### Standalone
Simply open `index.html` in your browser.

### As an iframe
Embed in your website:

```html
<iframe 
  src="https://your-domain.com/index.html" 
  width="100%" 
  height="900px" 
  frameborder="0"
  style="border: none; border-radius: 8px;">
</iframe>
```

### Deployment Options

1. **GitHub Pages**: Push to a repo and enable GitHub Pages
2. **Netlify**: Drag and drop the file
3. **Vercel**: Deploy with `vercel`
4. **Any web server**: Upload `index.html` to your hosting

## How It Works

The generator creates structured video scripts based on:
- **Topic**: The main subject of your video
- **Duration**: Target length in seconds (15-600s)
- **Tone**: Professional, Casual, Enthusiastic, Educational, or Storytelling
- **Audience**: Who you're targeting
- **Key Points**: Optional specific points to cover

## Customization

The script is self-contained in a single HTML file for easy customization:
- **Colors**: Modify the CSS gradient values
- **Fonts**: Change the font-family in the CSS
- **Script Logic**: Edit the `createScript()` function
- **Form Fields**: Add or remove input fields as needed

## Browser Support

Works in all modern browsers:
- Chrome/Edge 90+
- Firefox 88+
- Safari 14+
- Mobile browsers

## License

Free to use and modify for your projects.

