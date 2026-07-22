# Load and Geaux — Site Fixes & Patches

## Fixed: Footer Google Map Not Displaying (2026-07-22)

**Issue:** The embedded Google Map in the footer (Visit section) was not displaying. The iframe had `src="about:blank"` with the real map URL in a `data-src` attribute, which relied on WP Smush's lazy-loading library to move the URL to the `src` attribute. However, WP Smush's lazy-loader doesn't process iframes, only images.

**Root Cause:** 
- Bricks theme configured the iframe with lazy-loading
- WP Smush lazy-loader doesn't support iframe lazy-loading
- The `data-src` → `src` transfer never happened
- Map iframe remained blank

**Fix Applied:**
- Edited the footer iframe in Bricks builder
- Replaced lazy-loaded version with direct `src` attribute
- Removed `data-load-mode="0"` and `data-src` attributes

**Code Changed:**
```html
<!-- BEFORE (Not working) -->
<iframe style="border: 0;" data-src="https://www.google.com/maps/embed?pb=..." src="about:blank" data-load-mode="0">

<!-- AFTER (Fixed) -->
<iframe style="border: 0;" src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3273.151593810182!2d-91.14522422475427!3d30.469419698311256!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x8626a1ee80bd9ad9%3A0xea835d45c58cbecb!2sLoad%20and%20Geaux%20Portable%20Storage!5e1!3m2!1sen!2s!4v1755066250049!5m2!1sen!2s" width="529px" height="270px" allowfullscreen="allowfullscreen">
```

**Location:** WordPress → Bricks Footer Template → Visit Section → Google Maps Iframe

**Status:** ✅ Fixed and live at https://loadandgeaux.com/

**Future Prevention:** 
- When adding iframes to Bricks, avoid lazy-loading attributes
- Use direct `src` URLs for iframes (lazy-loading doesn't work reliably with iframes)
- Test all embedded content (maps, videos, etc.) after theme updates
