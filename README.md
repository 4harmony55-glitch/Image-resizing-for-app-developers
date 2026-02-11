DropCart Asset Resizer

🚀 The Ultimate Image Resizing Tool for App Developers

A zero-dependency, privacy-first browser tool that generates perfect app icons and assets at all required resolutions. Built for developers who need to quickly resize their app icons for manifests, stores, and platforms.

https://via.placeholder.com/800x400/0F172A/0EA5A4?text=DropCart+Asset+Resizer

✨ Why DropCart Asset Resizer?

You've just finished designing your app icon. Now you need it in 8 different sizes for your PWA manifest, iOS app store, Android launcher, and favicons.

Stop manually resizing in Photoshop. Stop using sketchy online converters. Stop writing scripts.

DropCart Asset Resizer handles everything in your browser, locally, instantly.

🎯 Features

· 🖼️ Drag & Drop Interface – Upload any PNG, JPEG, or WebP image
· 📏 8 Essential Sizes – 72, 96, 128, 144, 152, 192, 384, 512 pixels
· 🎯 Smart Aspect Ratio – Automatically centers and fits your image perfectly
· 📁 Asset-Ready Naming – Downloads with assets/ prefix – ready to drop into your project
· 🔒 100% Private – No server uploads, your image never leaves your device
· ⚡ Blazing Fast – Pure browser-side processing, no waiting
· 🌐 Works Offline – Save the HTML file and use it anywhere
· 📱 Responsive Design – Works on desktop, tablet, and mobile

🎨 Perfect For

· PWA Developers – Generate all manifest icons instantly
· Indie Hackers – Quick app store assets without design tools
· React Native / Flutter – Launcher icons at every density
· Web Developers – Favicon sets and touch icons
· Game Developers – App store screenshots and icons
· Anyone who just wants their icon to work everywhere

📋 Supported Platforms & Requirements

Platform Required Sizes Generated
PWA Manifest 72, 96, 128, 144, 152, 192, 384, 512 ✅ All
iOS App Store 1024 (we do 512) ⚠️ Scale up
Android Launcher 48, 72, 96, 144, 192, 512 ✅ Covered
macOS Icons 16-1024 ✅ Most sizes
Windows Tiles 70-620 ✅ Compatible
Favicon 16-512 ✅ Included

🚦 Quick Start

1. Download the Tool

```bash
# Clone the repo
git clone https://github.com/yourusername/dropcart-asset-resizer.git

# Or just download the HTML file
curl -O https://raw.githubusercontent.com/yourusername/dropcart-asset-resizer/main/index.html
```

2. Open in Browser

```bash
# Simply double-click the HTML file
open index.html

# Or serve locally
npx serve .
```

3. Upload & Generate

1. Drag your PNG icon into the upload area
2. Click any size button
3. Save to your /assets folder

That's it. No installation, no dependencies, no accounts.

💻 Usage Examples

Web Developer – PWA Manifest

```json
{
  "icons": [
    { "src": "/assets/my-icon-72x72.png", "sizes": "72x72", "type": "image/png" },
    { "src": "/assets/my-icon-96x96.png", "sizes": "96x96", "type": "image/png" },
    { "src": "/assets/my-icon-128x128.png", "sizes": "128x128", "type": "image/png" },
    { "src": "/assets/my-icon-144x144.png", "sizes": "144x144", "type": "image/png" },
    { "src": "/assets/my-icon-152x152.png", "sizes": "152x152", "type": "image/png" },
    { "src": "/assets/my-icon-192x192.png", "sizes": "192x192", "type": "image/png" },
    { "src": "/assets/my-icon-384x384.png", "sizes": "384x384", "type": "image/png" },
    { "src": "/assets/my-icon-512x512.png", "sizes": "512x512", "type": "image/png" }
  ]
}
```

React Developer – Vite/Parcel Setup

```bash
# After generating assets/
assets/
├── my-icon-72x72.png
├── my-icon-96x96.png
├── my-icon-128x128.png
├── my-icon-144x144.png
├── my-icon-152x152.png
├── my-icon-192x192.png
├── my-icon-384x384.png
└── my-icon-512x512.png

# Copy to public folder
cp -r assets/* public/assets/
```

App Developer – Capacitor/Cordova

```xml
<!-- config.xml -->
<platform name="ios">
    <icon src="assets/my-icon-72x72.png" width="72" height="72"/>
    <icon src="assets/my-icon-144x144.png" width="144" height="144"/>
    <!-- etc -->
</platform>
```

🎨 Design Tips

For Best Results:

· ✅ Use square images (1:1 aspect ratio)
· ✅ Export at 512×512 or higher for crisp upscaling
· ✅ Leave padding around your logo (10-15%)
· ✅ Use transparent PNGs for professional results
· ❌ Avoid tiny source images (<256px)
· ❌ Don't use JPEGs with backgrounds

📊 Size Guide

Size Use Case
72×72 Android launcher, older PWA
96×96 Google TV, some PWAs
128×128 Chrome Web Store
144×144 IE10/11 pinned sites
152×152 iPad touch icon
192×192 PWA home screen, Android
384×384 High-res PWA, some stores
512×512 PWA large, app stores

🔧 Advanced Usage

Batch Download All Sizes

Click each button once, or use this bookmarklet:

```javascript
javascript:(function(){document.querySelectorAll('.dl-btn').forEach((btn,i)=>setTimeout(()=>btn.click(),i*200))})();
```

Custom Size Addition

Edit the SIZES array in the script:

```javascript
const SIZES = [72, 96, 128, 144, 152, 192, 384, 512, 1024]; // Add 1024px
```

Change Output Format

Modify the toBlob call to use 'image/jpeg' or 'image/webp'.

🚨 Troubleshooting

Q: My image looks stretched!
A: The tool preserves aspect ratio automatically. If it still looks off, your source image might be extremely wide/tall.

Q: Downloaded file has no assets/ folder
A: Your browser might block folder creation. Just create the folder manually – the filename still has the prefix.

Q: Can I use SVG files?
A: Yes! Upload SVG – it rasterizes perfectly at any size.

Q: Is this really free?
A: 100% free, open source, no hidden costs.

📦 Project Structure

```
dropcart-asset-resizer/
├── index.html          # The entire tool (single file)
├── README.md           # This documentation
├── LICENSE            # MIT License
├── screenshot.png     # Preview image
└── assets/            # Your generated icons go here
```

🤝 Contributing

This tool is intentionally minimal. Found a bug? Want a feature?

1. Fork the repository
2. Create your feature branch (git checkout -b feature/amazing)
3. Commit changes (git commit -m 'Add amazing feature')
4. Push to branch (git push origin feature/amazing)
5. Open a Pull Request

Ideas for contributions:

· Add WebP/AVIF output support
· Add ZIP batch download
· Add favicon .ico generation
· Add iOS adaptive icon masks
· Add dark/light theme toggle

📄 License

MIT License – do literally whatever you want with this code. Use it in your projects, modify it, sell it, print it out and frame it.

🙏 Acknowledgments

· Inspired by every developer who's ever had to manually resize icons at 2 AM
· Built with vanilla JS because dependencies are overrated
· Color scheme: #0F172A (dark) and #0EA5A4 (teal) – the DropCart brand

💬 Community & Support

· Issues: GitHub Issues
· Discussions: GitHub Discussions
· Twitter: @dropcart

🎉 Success Stories

"Went from designing my icon to having all PWA assets in under 30 seconds. This tool saved me an hour." – @frontendjoe

"Finally, a resizer that doesn't upload my unreleased app icons to some random server." – @indiedev

"I keep this HTML file in every project repo. It's my secret weapon." – @webdevmike

---

Made with ❤️ for developers who just want things to work.

Stop resizing. Start shipping.
