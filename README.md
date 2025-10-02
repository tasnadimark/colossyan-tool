# Video Tools - Script & Transcript Generator

A simple, embeddable tool for creating video scripts and generating transcripts from video files.

## Features

### Script Generator
- 📝 Simple form-based interface for creating video scripts
- 🎯 Customizable tone, duration, audience, and key points
- 🎨 Multiple tone options (Professional, Casual, Enthusiastic, Educational, Storytelling)
- 📋 One-click copy to clipboard

### Transcript Generator
- 🎙️ Upload video/audio files for automatic transcription
- 🤖 Uses OpenAI Whisper API for accurate transcription
- 📁 Supports multiple formats: MP4, MOV, AVI, MP3, WAV, M4A
- 🔒 API key stored locally in your browser

### General Features
- 🎨 Modern, gradient design with tab interface
- 📱 Fully responsive
- 🔗 iframe-ready
- ⚡ Pure HTML/CSS/JavaScript (no build step required)

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

### Script Generator
The generator creates structured video scripts based on:
- **Topic**: The main subject of your video
- **Duration**: Target length in seconds (15-600s)
- **Tone**: Professional, Casual, Enthusiastic, Educational, or Storytelling
- **Audience**: Who you're targeting
- **Key Points**: Optional specific points to cover

### Transcript Generator
Converts video/audio to text transcripts:
- **Requirements**: OpenAI API key (get one at [platform.openai.com](https://platform.openai.com/api-keys))
- **File Support**: Video and audio files up to 25MB
- **Processing**: Uses OpenAI's Whisper model for high-quality transcription
- **Privacy**: Your API key is stored locally in your browser
- **Cost**: ~$0.006 per minute of audio (see [OpenAI pricing](https://openai.com/api/pricing/))

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

