# QUICK CUSTOMIZATION REFERENCE

This file shows exactly where to find and edit important information in your website.

---

## 🎨 BRAND COLORS (Easy Change!)

**File:** `assets/styles/style.css`

Find the `:root` section and update:

```css
:root {
    --primary: #E74C3C;           /* Main red - Change this! */
    --primary-dark: #C0392B;      /* Darker red */
    --primary-light: #EC7063;     /* Light red */
    --secondary: #2E86AB;         /* Blue */
    --secondary-dark: #1B4965;    /* Darker blue */
    --accent: #F39C12;            /* Gold/Orange */
    /* ... more colors ... */
}
```

**Popular Colors:** (Use hex code)
- Red: `#E74C3C` (current)
- Blue: `#3498DB`
- Green: `#27AE60`
- Orange: `#E67E22`
- Purple: `#8E44AD`
- Teal: `#1ABC9C`

---

## 📱 SHOP CONTACT DETAILS

### Phone Number
**File:** `index.html`
**Search:** `9953787727`
**Replace with:** Your actual phone number (keep without spaces or dashes)

Appears in:
- Navigation bar "Call Now" button
- Contact section
- WhatsApp links
- Footer

### Email Address
**File:** `index.html`
**Search:** `J264003@gmail.com`
**Replace with:** Your business email

Appears in:
- Contact section
- Footer

### WhatsApp Number (API)
**File:** `assets/js/script.js`
**Search:** `phone=919953787727`
**Replace with:** `phone=91YOUR_10_DIGIT_NUMBER` (keep 91 prefix for India)

### Shop Name
**File:** `index.html`
**Search:** `Jayshree Paints`
**Replace with:** Your shop name

Appears in:
- Logo/Header
- Hero section title
- Footer
- All WhatsApp messages

---

## 📍 LOCATION & ADDRESS

**File:** `index.html`

### Physical Address
```html
Find: 
<p>SH 15A, Main Road, Preetnagar<br>
Chopan, Near Baghel Katra<br>
Sonbhadra, Uttarpradesh</p>

Replace with: Your full address
```

### Google Maps Link
```html
Find: 
href="https://maps.google.com/?q=SH+15A+Main+Road+Preetnagar+Chopan+Sonbhadra+Uttarpradesh"

Replace with:
- Right-click on Google Maps location
- Select "Share"
- Copy Google Maps link
- Paste in place of current link
```

### Google Maps Embed
```html
Find: 
<iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12...">

To update:
1. Go to Google Maps
2. Find your shop location
3. Click "Share" → "Embed a map"
4. Copy the iframe code
5. Replace the entire iframe element
```

---

## ⏰ OPERATING HOURS

**File:** `index.html`
**Find:** `<table class="hours-table">`

Current:
```html
<tr>
    <td>Monday</td>
    <td>9:00 AM - 7:00 PM</td>
</tr>
```

Your hours work automatically - the website detects current time and shows "Open Now" or "Closed" in the navbar!

**To change hours:**
```html
<tr>
    <td>Monday</td>
    <td>YOUR_OPENING_TIME - YOUR_CLOSING_TIME</td>
</tr>
```

Also update in `assets/js/script.js`:
```javascript
const openTime = 9 * 60;      // 9:00 AM (in minutes)
const closeTime = 19 * 60;    // 7:00 PM (in minutes)
```

---

## 🏪 SHOP AMENITIES

**File:** `index.html`
**Find:** `<div class="amenities-list">`

Current amenities:
```html
<div class="amenity">
    <span class="amenity-icon">🚚</span>
    <span>Loading Assistance</span>
</div>
```

**To change/add amenities:**
1. Keep the structure
2. Change emoji to represent your amenity
3. Update the text

**Popular emoji for shops:**
- 🚚 Delivery
- 🎨 Paint/Color
- 💳 Payment/Cards
- 👥 Staff/People
- 🔧 Tools/Service
- ⭐ Quality
- 📞 Support
- 🅿️ Parking
- ♿ Wheelchair access
- 🌡️ Climate control

---

## 📦 PRODUCTS & SERVICES

**File:** `assets/js/script.js`
**Find:** `const productsData = [`

### Add New Product
```javascript
{
    id: 13,                                    // Unique number
    name: 'Product Name Here',                 // Product title
    category: 'paints',                        // paints, hardware, materials, or tools
    description: 'What the product does',      // Short description
    price: '₹450/L',                           // Price or price range
    stock: 'In Stock',                         // 'In Stock' or 'Low Stock'
    isNew: false,                              // true = shows "NEW" badge
    image: '🎨'                                // Emoji or image URL
}
```

### Edit Existing Product
Simply open the `productsData` array and update any field.

### Product Categories
- `paints` - Paint products
- `hardware` - Hinges, locks, nails, etc.
- `materials` - Tiles, putty, adhesive, etc.
- `tools` - Drills, brushes, ladders, etc.

### Stock Status
- `'In Stock'` - Shows green badge
- `'Low Stock'` - Shows yellow/warning badge

---

## ⭐ CUSTOMER REVIEWS

**File:** `assets/js/script.js`
**Find:** `const reviewsData = [`

### Add New Review
```javascript
{
    id: 7,                              // Unique number
    author: 'Customer Name',            // Person's name
    rating: 5,                          // 1-5 stars
    text: 'Their review/testimonial',   // Happy message
    date: '1 week ago'                  // When they reviewed
}
```

### Edit Reviews
- Update customer names with REAL customers
- Change ratings based on your experience
- Update text with actual testimonials
- Use dates like "2 weeks ago", "3 months ago"

---

## 🎯 HOMEPAGE TEXT

**File:** `index.html`

### Hero Title
```html
<h1 class="hero-title">
    Transform Your Space with Premium Paint & Hardware Solutions
</h1>
```
Change to highlight your shop's specialty.

### Hero Subtitle
```html
<p class="hero-subtitle">
    100% Genuine Products | Expert Advice | Custom Color Matching | Local Delivery Available
</p>
```
Update with your actual selling points.

### About Us Title
```html
<h3>Our Story</h3>
<p>For over a decade, Jayshree Paints and Hardware has been serving...</p>
```
Tell your actual business story!

---

## 💬 TRUST MARKERS

**File:** `index.html`
**Find:** `<div class="trust-markers">`

Current markers:
1. 100% Genuine Products
2. Expert Consultation
3. Fast Local Delivery
4. Custom Color Matching

**Update to match your business:**
```html
<div class="trust-item">
    <span class="icon">✓</span>
    <h4>Your Trust Marker</h4>
    <p>Why customers trust you</p>
</div>
```

---

## 📧 CONTACT FORM

**File:** `index.html` and `assets/js/script.js`

The form automatically sends messages via WhatsApp. No backend needed!
Just make sure your WhatsApp number is correct (see Phone Number section above).

**Form fields:**
- Name (validated: min 2 characters)
- Phone (validated: must be 10 digits)
- Message (validated: min 5 characters)

Users click "Send Inquiry on WhatsApp" → Automatic redirect to WhatsApp chat.

---

## 🔗 SOCIAL MEDIA LINKS

**File:** `index.html` and Footer

### Facebook
```html
<a href="https://www.facebook.com/jayshreepaints" target="_blank">
```
Replace URL with your Facebook page link.

### Instagram
```html
<a href="https://www.instagram.com/jayshreepaints" target="_blank">
```
Replace URL with your Instagram profile link.

### WhatsApp (Footer)
Already configured to your phone number (see Contact Details above).

---

## 🎨 LOGO & BRANDING

Current: Emoji 🎨

**To use your actual logo:**

1. **Save your logo image** in `assets/images/` folder
2. **In index.html, find:**
```html
<span class="logo-icon">🎨</span>
<span class="logo-text">Jayshree Paints</span>
```
3. **Replace with:**
```html
<img src="assets/images/your-logo.png" alt="Jayshree Paints Logo" class="logo-img">
<span class="logo-text">Jayshree Paints</span>
```

4. **In assets/styles/style.css, add:**
```css
.logo-img {
    height: 40px;
    width: auto;
    margin-right: 10px;
}
```

---

## 📄 SEO OPTIMIZATION

**File:** `index.html` (in `<head>`)

### Page Title
```html
<title>Jayshree Paints and Hardware | Paints, Hardware & Building Materials in Sonbhadra</title>
```
Update this for search engines.

### Meta Description
```html
<meta name="description" content="Jayshree Paints and Hardware - Your trusted source for premium paints, hardware, and building materials in Sonbhadra, Uttarpradesh.">
```
Update this for Google search results.

### Keywords
```html
<meta name="keywords" content="paints, hardware, building materials, Sonbhadra, Chopan">
```
Update with your relevant keywords.

---

## 🎯 CALL-TO-ACTION (CTA) BUTTONS

**File:** `index.html`

Current CTAs:
- "Browse Our Catalog" → Scroll to products
- "Get Directions" → Google Maps
- "Call Now" → Direct phone call
- "Inquire on WhatsApp" → WhatsApp chat

**These are perfect!** Just make sure your phone number and shop address are correct.

---

## 📊 STATISTICS CARDS

**File:** `index.html`
**Find:** `<div class="about-stats">`

Current:
- 10+ Years of Service
- 5000+ Happy Customers
- 500+ Product Variants
- 24/7 WhatsApp Support

**Update with your actual stats:**
```html
<div class="stat-card">
    <h4>YOUR_NUMBER+</h4>
    <p>Your Description</p>
</div>
```

---

## 🔄 NEWSLETTER SUBSCRIPTION

**File:** `assets/js/script.js`

Newsletter form automatically sends via WhatsApp. Currently uses your business WhatsApp number.

**To use email instead:**
1. Set up backend service (Firebase, Formspree, etc.)
2. Replace WhatsApp logic with email API
3. Store emails in database

(Advanced feature - contact developer if needed)

---

## 🌍 GOOGLE MAPS EMBED COORDINATES

Current location in embed:
```
Latitude: 23.8321
Longitude: 82.3449
```

**To update:**
1. Go to Google Maps
2. Find your exact shop location
3. Right-click → Copy coordinates
4. Replace in `index.html` map embed code

---

## ✅ FINAL CHECKLIST BEFORE LAUNCH

- [ ] Shop name updated everywhere
- [ ] Phone number verified (10 digits)
- [ ] Email address updated
- [ ] Address updated and coordinates verified
- [ ] Operating hours set correctly
- [ ] Products added or updated
- [ ] Real customer reviews added
- [ ] Social media links verified
- [ ] Logo/branding updated
- [ ] Colors customized (optional)
- [ ] All links tested (clicking works)
- [ ] Mobile view tested (responsive)
- [ ] Form tested (messages work)
- [ ] WhatsApp links tested (open app)

---

## 🚀 AFTER LAUNCH

1. **Collect Reviews:** Ask customers to leave Google reviews
2. **Update Products:** Add new items monthly
3. **Monitor Analytics:** Check Google Analytics weekly
4. **Respond Quickly:** Reply to WhatsApp within 1 hour
5. **Add Content:** Blog posts, tips, tutorials
6. **Promote:** Share on social media regularly

---

**Everything is ready to customize! Pick what you need and follow the examples above.** ✨

**If stuck, contact:** J264003@gmail.com or +91 9953787727
