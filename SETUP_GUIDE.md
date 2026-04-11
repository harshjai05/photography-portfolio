# Photography Portfolio Setup Guide

## How It Works

Your portfolio now uses a **dynamic image management system** powered by `data.json`. All images, categories, and featured selections are controlled through this single JSON file.

---

## Quick Start

### Step 1: Create Photos Folder
```
📁 Your project folder
├── index.html
├── data.json
└── 📁 photos/
    ├── street_01.jpg
    ├── portrait_01.jpg
    ├── landscape_01.jpg
    └── ...
```

### Step 2: Add Images to data.json
Open `data.json` and add entries to the `images` array:

```json
{
  "images": [
    {
      "id": 1,
      "src": "photos/street_01.jpg",
      "title": "Morning Rush",
      "caption": "Street, Chennai",
      "category": "street",
      "date": "2025-04-05",
      "featured": true
    }
  ]
}
```

### Step 3: That's It!
The gallery auto-loads, filters, and displays everything.

---

## Understanding data.json Fields

| Field | Purpose | Example |
|-------|---------|---------|
| `id` | Unique number | `1`, `2`, `3` |
| `src` | Image file path | `"photos/street_01.jpg"` |
| `title` | Image title (shown in overlay) | `"Morning Rush"` |
| `caption` | Short description | `"Street, Chennai"` |
| `category` | For filtering | `"street"` \| `"portrait"` \| `"landscape"` \| `"architecture"` \| `"mixed"` |
| `date` | YYYY-MM-DD format | `"2025-04-05"` |
| `featured` | Show in hero carousel? | `true` or `false` |

---

## How Sorting Works

### ✓ Latest Images First
Images are **automatically sorted by date** (newest first). Just update the date field when you add new photos.

```json
{
  "date": "2025-04-05"  // This appears first
},
{
  "date": "2025-04-01"  // This appears later
}
```

### ✓ Category Filtering
Click a category (Street, Portrait, etc.) to filter the gallery. Counts auto-update.

### ✓ Featured Carousel
Set `"featured": true` to include an image in the hero carousel. It rotates every 6 seconds and shows at the top of the page.

```json
{
  "featured": true  // Shows in carousel
},
{
  "featured": false  // Only in gallery
}
```

---

## Complete Example

Here's a sample `data.json` with multiple images:

```json
{
  "images": [
    {
      "id": 1,
      "src": "photos/street_01.jpg",
      "title": "Morning Rush",
      "caption": "Street, Chennai",
      "category": "street",
      "date": "2025-04-05",
      "featured": true
    },
    {
      "id": 2,
      "src": "photos/portrait_01.jpg",
      "title": "Urban Portrait",
      "caption": "Portrait Session",
      "category": "portrait",
      "date": "2025-04-04",
      "featured": true
    },
    {
      "id": 3,
      "src": "photos/landscape_02.jpg",
      "title": "Monsoon Light",
      "caption": "Landscape Study",
      "category": "landscape",
      "date": "2025-04-03",
      "featured": false
    },
    {
      "id": 4,
      "src": "photos/architecture_01.jpg",
      "title": "Geometric Forms",
      "caption": "Architecture Detail",
      "category": "architecture",
      "date": "2025-04-02",
      "featured": false
    }
  ]
}
```

---

## Tips

- **Photo Size**: Keep JPGs/WebP under 1MB for fast loading
- **Naming**: Use simple names like `street_01.jpg`, `portrait_02.jpg`
- **Dates**: Always use `YYYY-MM-DD` format (e.g., `2025-04-05`)
- **Categories**: Only use: street, portrait, landscape, architecture, mixed
- **Featured**: Pick 2-3 of your best shots for the hero carousel
- **Update Order**: Change dates if you want to reorder photos (latest=highest date)

---

## Features Included

✓ **Dynamic Gallery** - Renders from JSON  
✓ **Auto-Sorting** - Newest photos first  
✓ **Category Filtering** - Click to filter by type  
✓ **Live Counts** - Category counts update automatically  
✓ **Featured Carousel** - Rotating hero images (6 sec intervals)  
✓ **Lightbox** - Click to view full-size  
✓ **Responsive** - Works on mobile/tablet  
✓ **Staggered Animation** - Smooth gallery reveal  

---

## Troubleshooting

**Images not showing?**
- Check file paths in `data.json` match actual files in `photos/` folder
- Verify JSON syntax is valid (use [JSONLint.com](https://jsonlint.com))
- Check browser console for errors (F12 → Console tab)

**Categories not filtering?**
- Make sure category name matches exactly (case-sensitive)
- Refresh page after editing JSON

**Carousel not rotating?**
- Set at least one image to `"featured": true`
- Check browser console for errors

---

## Next Steps

1. **Create the `photos/` folder** next to `index.html`
2. **Export your images** (JPG or WebP)
3. **Add entries to `data.json`** for each photo
4. **Open `index.html`** in a browser to test
5. **Adjust featured status** and dates as needed

You're all set! 📸
