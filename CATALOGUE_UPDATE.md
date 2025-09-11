# Catalogue Update Guide

## How to Add/Edit Items

### Adding New Items

1. **Update CSV**: Add new row to `detailed_inventory.csv`
   - Required fields: SKU, Item_Name, Brand, Corrected_Category, Corrected_Subcategory, Qty
   - Optional: Size, Colour, Anchor_Price_AUD, Wholesale_Price_AUD, Image_URL

2. **Add Image**: Upload image to `/images/` folder using naming convention

3. **Deploy**: Commit and push to GitHub Pages

### Editing Existing Items

1. **Edit CSV**: Modify the relevant row in `detailed_inventory.csv`
2. **Categories**: Use these exact categories:
   - Children's Sleepwear
   - Ladies' Sleepwear  
   - Bathrobes
   - Pajama Sets
   - Other/Accessories

3. **Pricing**: Update Anchor_Price_AUD and Wholesale_Price_AUD as needed

### Dynamic Totals

The page automatically calculates:
- **Total Pieces**: Sum of all Qty values
- **Total SKUs**: Count of rows with Qty > 0
- **Category Breakdown**: Pieces per category

**No need to update HTML manually** - totals update automatically from CSV.

### Categories & Filtering

Items are automatically categorized based on:
- Product name and description keywords
- Manual Corrected_Category field (takes priority)

The filter dropdown and stats update automatically when categories change.

### Deployment Process

1. **Edit Files**: Update CSV and/or add images
2. **Commit**: `git add .` and `git commit -m "Update catalogue"`
3. **Push**: `git push origin main`
4. **Wait**: 2-3 minutes for GitHub Pages to update
5. **Verify**: Check live site at your GitHub Pages URL

### Quality Checks

- Verify all images load correctly
- Check totals match your expectations
- Test filters and search functionality
- Ensure mobile responsiveness

### Backup

- Keep a backup copy of `detailed_inventory.csv`
- GitHub maintains version history automatically
- Can revert to previous versions if needed
