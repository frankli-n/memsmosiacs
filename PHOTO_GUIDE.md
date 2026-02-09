# MemsMosaics Website - Photo Guide

## How to Add Your Photos

This guide explains exactly where and how to add your photos to the new MemsMosaics website.

---

## GALLERY PHOTOS

### Step 1: Prepare Your Gallery Photos
- Save your mosaic artwork photos in a folder (e.g., "images")
- Recommended format: JPG or PNG
- Recommended size: 1200px x 1200px (square format works best)
- Name them clearly: mosaic1.jpg, mosaic2.jpg, etc.

### Step 2: Upload Photos
Place all your gallery images in the same folder as your HTML file, or create an "images" subfolder.

### Step 3: Replace Photo Placeholders in the Code

Find this section in the HTML (around line 450-480):

```html
<!-- PHOTO SLOT 1 -->
<div class="gallery-item" onclick="openModal(this)">
    <div class="photo-placeholder">Your Photo Here</div>
    <div class="overlay">
        <span class="title">Artwork Title 1</span>
    </div>
</div>
```

**Replace it with:**

```html
<!-- PHOTO SLOT 1 -->
<div class="gallery-item" onclick="openModal(this)">
    <img src="images/mosaic1.jpg" alt="Description of this mosaic">
    <div class="overlay">
        <span class="title">Name of This Piece</span>
    </div>
</div>
```

### What to Change:
1. **Delete** the line: `<div class="photo-placeholder">Your Photo Here</div>`
2. **Add** instead: `<img src="images/mosaic1.jpg" alt="Description of this mosaic">`
3. **Update** the title: Change "Artwork Title 1" to your actual piece name
4. **Update** the alt text: Describe the piece for accessibility

### Example - If your photo is in the same folder as HTML:
```html
<img src="mosaic1.jpg" alt="Blue and gold geometric mosaic">
```

### Example - If your photo is in an "images" subfolder:
```html
<img src="images/mosaic1.jpg" alt="Blue and gold geometric mosaic">
```

### Repeat for All Gallery Items
Do this for PHOTO SLOT 2, 3, 4, 5, 6, etc.

---

## ABOUT SECTION PHOTO

### Step 1: Prepare Your About Photo
- This should be a photo of you (the artist) or your studio
- Recommended format: JPG or PNG
- Recommended size: 800px x 1000px (portrait orientation works best)
- Name it: artist.jpg or studio.jpg

### Step 2: Find the About Photo Section
Look for this code (around line 495):

```html
<div class="about-image">
    <!-- ABOUT PHOTO SLOT -->
    <div class="photo-placeholder">Your Photo Here</div>
</div>
```

**Replace it with:**

```html
<div class="about-image">
    <img src="images/artist.jpg" alt="Artist photo">
</div>
```

---

## ADDING MORE GALLERY PHOTOS

To add more than 6 gallery photos, copy this entire block:

```html
<!-- PHOTO SLOT 7 -->
<div class="gallery-item" onclick="openModal(this)">
    <img src="images/mosaic7.jpg" alt="Description of mosaic">
    <div class="overlay">
        <span class="title">Artwork Title 7</span>
    </div>
</div>
```

Paste it inside the `<div class="gallery-grid">` section, after the last photo slot.

You can add as many as you want - they'll automatically arrange in a responsive grid!

---

## CUSTOMIZING TEXT

### About Section
Find these lines (around line 505-515) and replace the placeholder text:

```html
<h3>Creating Art, Piece by Piece</h3>
<p>
    [Replace this text with your artist biography...]
</p>
```

### Contact Email
Find this line (around line 530):

```html
<a href="mailto:your.email@example.com" class="contact-button">
```

**Change to your actual email:**

```html
<a href="mailto:memsmosaics@gmail.com" class="contact-button">
```

---

## FOLDER STRUCTURE

Recommended setup:

```
your-website-folder/
│
├── memsmosaics.html (the main website file)
│
└── images/
    ├── mosaic1.jpg
    ├── mosaic2.jpg
    ├── mosaic3.jpg
    ├── mosaic4.jpg
    ├── mosaic5.jpg
    ├── mosaic6.jpg
    └── artist.jpg
```

---

## QUICK REFERENCE CHECKLIST

☐ Prepare and resize all photos
☐ Create "images" folder
☐ Upload all photos to images folder
☐ Replace each photo placeholder with `<img src="images/yourphoto.jpg" alt="description">`
☐ Update artwork titles in the overlays
☐ Replace About section text with your bio
☐ Add your artist/studio photo
☐ Update contact email address
☐ Test the website by opening memsmosaics.html in your browser

---

## TIPS

1. **Image sizes**: Keep photos under 2MB each for fast loading
2. **Square format**: Gallery photos look best as squares (1:1 ratio)
3. **Consistent naming**: Use simple names without spaces (use-hyphens-instead)
4. **Alt text**: Always describe your images - it helps with accessibility and SEO
5. **Test locally**: Open the HTML file in your browser to see changes before uploading to your server

---

## Need Help?

Common issues:
- **Image not showing?** Check the file path matches exactly (including folder name and file extension)
- **Image stretched?** Make sure it's approximately square for gallery, portrait for about section
- **Want different layout?** The grid automatically adjusts - just add more photos!

---

**That's it! Your modern MemsMosaics website is ready to showcase your beautiful work.**
