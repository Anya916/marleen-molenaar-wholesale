# Images Guide

## How to Update Images

### Adding New Images

1. **Naming Convention**: Use format `SKU_Brand_Size_Colour.jpg`
   - Example: `MM_0001_MarleenMolenaar_6T_Pink.jpg`
   - Keep filenames URL-safe (lowercase, hyphens instead of spaces)

2. **File Placement**:
   - Upload original images to `/images/` folder
   - The system will auto-generate optimized versions in `/images/thumbs/` and `/images/standard/`

3. **Supported Formats**: JPG, JPEG, PNG (will be converted to WebP + JPEG)

### Updating Existing Images

1. Replace the file in `/images/` with the same filename
2. Delete corresponding files in `/images/thumbs/` and `/images/standard/`
3. Re-run the optimization script (or they'll be regenerated automatically)

### Image Optimization

The system creates:
- **Thumbnails**: 400px max width in `/images/thumbs/`
- **Standard**: 1200px max width in `/images/standard/`
- **Formats**: WebP (modern browsers) + JPEG (fallback)

### Missing Images

- Missing images automatically use `images/placeholder.webp`
- Check `Missing_Images_Report.csv` for items needing photos
- The console logs missing images when they fail to load

### GitHub Pages Deployment

1. Upload new images to `/images/` folder
2. Commit and push to GitHub
3. GitHub Pages will update automatically (2-3 minutes)
4. Check the live site to verify images appear correctly

### Troubleshooting

- **Case sensitivity**: GitHub Pages is case-sensitive, ensure exact filename matches
- **File size**: Keep original images under 5MB for faster uploads
- **Browser cache**: Hard refresh (Ctrl+F5) to see new images immediately
