# Timeline Viewer

A beautiful, mobile-friendly timeline viewer for Mahavir Mannat property transactions.

## 🚀 Quick Start

### Step 1: Export Data from MongoDB

```bash
npm run export-timeline-data
```

This will create `output/timeline-data.json` with all the property data.

### Step 2: View the Timeline

The timeline reads data from `timeline-data.json` in the same folder.

**Important**: Due to browser security (CORS), you need to run a local web server:

```bash
cd output/report
python3 -m http.server 8000
```

Then open in your browser:
```
http://localhost:8000/timeline.html
```

## 📁 Files

- `timeline.html` - The timeline viewer (HTML/CSS/JS)
- `timeline-data.json` - Property data (auto-generated)

## 🎨 Features

- ✅ Accordion for each shop
- ✅ Timeline view with all transactions
- ✅ Sort by purchase date (ascending)
- ✅ "Show More" modal with full details
- ✅ Mobile-friendly responsive design
- ✅ Beautiful animations and gradients

## 🔄 Updating Data

Whenever you update your MongoDB data, just re-export:

```bash
npm run export-timeline-data
```

Then refresh the browser - the timeline will show the updated data!

## 💡 Alternative: Python Server

If you don't have Python 3, use Python 2:

```bash
cd output/report
python -m SimpleHTTPServer 8000
```

Or use Node.js:

```bash
cd output/report
npx http-server -p 8000
```

## 🌐 Deploy to Web

To deploy to a website, simply upload both files to your web server:
- timeline.html
- timeline-data.json

They must be in the same folder!
