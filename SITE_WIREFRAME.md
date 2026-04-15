# Site Structure Wireframe
## Adam's Islandstyle Grill & Catering

**Version:** 1.0  
**Purpose:** Developer blueprint for visual design and implementation  
**Last Updated:** December 2024

---

## 1. Overview

### Purpose
Drive pickup orders and catering leads while showcasing authentic island cuisine and Adam's story.

### Primary CTAs
- **Order Pickup** → Toast ordering URL
- **Request Catering Quote** → Contact form
- **Call Adam** → (801) 252-5958

### Core Content Sources
- Embedded menu JSON (`#menu-data`)
- About copy (family story + Puleju teriyaki)
- JSON-LD Restaurant schema
- Toast ordering integration

---

## 2. Pages and Section Wireframes

### 2.1 Home Page (`/`)

#### Top Navigation
```
[Logo]  Home | Menu | Catering | About | Contact  [ORDER NOW Button]
```
- Logo: Left-aligned, links to home
- Nav links: Centered, smooth scroll to sections on home page
- Order button: Right-aligned, prominent coral background (#ff5a00)
- Mobile: Hamburger menu with sticky bottom CTA bar

#### Hero Section
- **Background:** Large hero image (grill action or plated teriyaki chicken)
- **H1:** "Taste of the Islands in Magna"
- **Tagline:** "Tender, smoky, and made with genuine aloha — Adam's Puleju‑style teriyaki and island plates bring family recipes and Pacific Island warmth to every plate."
- **CTAs (3 buttons):**
  - Primary: "Order Pickup" → Toast URL
  - Secondary: "Request Catering Quote" → /catering#contact-form
  - Tertiary: "Call Adam: (801) 252-5958" → tel:+18012525958

#### Quick Info Strip
- **Layout:** Horizontal flex row, 3 columns
- **Content:**
  - 📍 Address: 9071 W Magna Main Street, Magna, UT 84044
  - 📞 Phone: (801) 252-5958 (click-to-call)
  - ⏰ Opens: 11:00 AM (dynamic based on day)
- **Style:** Neutral dark surface (#121212), subtle border

#### Why We're Different (3-Card Grid)
- **Card 1: Secret Marinade**
  - Icon: 🔥
  - Title: "Secret Marinade"
  - Copy: "A proprietary blend perfected over years; every bite is uniquely Adam's."
- **Card 2: Puleju Teriyaki**
  - Icon: 🍗
  - Title: "Puleju-Style Teriyaki"
  - Copy: "Deeper, richer, and unmistakably authentic."
- **Card 3: Genuine Aloha**
  - Icon: 🌺
  - Title: "Genuine Aloha"
  - Copy: "Food prepared with intention, respect, and the spirit of family."
- **Footer note:** "Not a franchise. Not a formula. One man, one grill, and no shortcuts."

#### Must-Try Feature Block
- **Layout:** Two-column (image left, content right) on desktop; stacked on mobile
- **Image:** High-quality photo of Teriyaki Chicken plate
- **Content:**
  - Badge: "Most Popular"
  - H2: "Teriyaki Chicken, Puleju-Style"
  - Description: "Tender chicken marinated in Adam's secret blend, grilled to a smoky finish, and served with jasmine rice and creamy mac salad. One bite explains why locals keep coming back."
  - Price hint: "Single & Double plates available"
  - CTA: "Order Now" → Toast

#### Catering Snapshot
- **Background:** Elevated surface (#1a1a1a)
- **Headline:** "We Cater Events of Any Size"
- **Copy:** "From backyard birthdays to corporate lunches and large memorial services. Adam brings the same hands‑on care to events as he does at the grill — cooked to standard, never reheated, and presented to create the 'awe effect'."
- **Fast Facts (bullet list):**
  - Serves Magna, West Valley, and greater Salt Lake
  - Flexible packages for 10–500+ guests
  - Personal oversight by Adam
- **CTA:** "View Catering Packages" → /catering

#### Footer
- **Left:** Logo + NAP (Name, Address, Phone)
- **Center:** Hours note ("Mon–Sat 10am–8pm | Sun Closed")
- **Right:** Social links (Instagram, Facebook) + small text
- **Bottom:** Schema script inclusion, copyright
- **Style:** Dark background (#0a0a0a), subtle top border

---

### 2.2 Menu Page (`/menu`)

#### Hero Section
- **H1:** "Menu — Island Plates & Signature Teriyaki"
- **Intro:** "No Shortcuts. No Frozen Trays. Just Real Food, Made Right."
- **Quote:** "What taught me to make my signature dishes? Myself. Time. And definitely taste." — Adam
- **Subtext:** "Dine-In • Takeout • Catering | Call Adam: (801) 252-5958"
- **CTA:** "Order Online" button (links to Toast)

#### Menu Filters (Tabs)
- **Buttons:** Entrees | Apps & Snacks | Sides | Add-Ons | Beverages | Keiki
- **Behavior:** Filter grid below; active state uses brand glow
- **Mobile:** Horizontal scroll or dropdown

#### Menu Grid (Dynamic from JSON)
- **Data Source:** `#menu-data` embedded JSON
- **Item Card Structure:**
  ```html
  <div class="menu-item-card">
    <div class="item-header">
      <h3 class="item-name">Teriyaki Chicken, Puleju-Style</h3>
      <span class="item-price">$X.XX</span>
    </div>
    <p class="item-description">Tender chicken marinated...</p>
    <div class="item-tags">
      <span class="tag gf">GF</span>
      <span class="tag popular">Popular</span>
    </div>
  </div>
  ```
- **Fields Mapping:**
  - `name` → title
  - `price` / `price_range` → price display
  - `description` → subtitle
  - `tags` → badges (GF, vegan, shareable, popular)

#### Menu Notes Section
- **Sourcing Note:** "All proteins are fresh-grilled daily. Prices subject to change."
- **Toast Link:** "For live prices and availability, order via Toast."
- **Style:** Muted text, smaller font

#### Download / Catering Menu CTA
- **Box:** Elevated surface with brand border
- **Content:** "Planning an event? Download our full catering menu (PDF)"
- **CTA:** "Download PDF" + "View Catering Packages" button

---

### 2.3 Catering Page (`/catering`)

#### Hero Section
- **H1:** "We Cater Events of Any Size"
- **Subhead:** "You Don't Just Need Food at Your Event. You Need an Experience."
- **Quote:** "When people see the food set up, I want them to have the awe effect. And genuine aloha." — Adam
- **CTAs:**
  - Primary: "📞 Call Adam Directly" → tel:+18012525958
  - Subtext: "Prefer to write? Send a quick message" → anchor to form
- **Service Area:** "Serving Magna, West Valley, Salt Lake County & Beyond"

#### Why Adam's Catering (Differentiators)
- **Headline:** "Why Most Catering Falls Short (And Why Adam's Doesn't)"
- **Bullet List:**
  - ✅ Cooked to Standard, Not to Schedule
  - ✅ Secret Marinade, Every Time
  - ✅ Puleju-Style Teriyaki
  - ✅ Personal Oversight
- **Quote:** "The grill is my life. When I cater, I bring that same energy to your table."

#### What We Cater (Table/Grid)
| Event Type | Why It Works |
|------------|--------------|
| 🎉 Birthdays & Graduations | Crowd-pleasing plates that keep the party moving |
| 🤍 Funerals & Memorials | Comfort food that honors tradition |
| 🏢 Corporate & Company Lunches | Reliable, on-time, actually enjoyed |
| 🌺 Community & Cultural Gatherings | Authentic flavors that celebrate heritage |
| 🏠 Backyard & Private Parties | Flexible packages, homemade touch |

#### Catering Packages (3-Card Layout)
- **Package 1: The Aloha Package (Most Popular)**
  - Serves: 20–25 people
  - Price: $XXX
  - Includes: Teriyaki Chicken (10 lbs), Kalua Pork (10 lbs), Rice (5 lbs), Mac Salad (5 lbs), Gravy, Lupia (50 pcs), Supplies
  - CTA: "Request This Package"

- **Package 2: The Ohana Package**
  - Serves: 40–50 people
  - Price: $XXX
  - Includes: Double quantities + Huli Huli Chicken
  - CTA: "Request This Package"

- **Package 3: The Corporate Package**
  - Serves: 15–20 people
  - Price: $XXX
  - Includes: Choice of 2 proteins, individual plates, on-time guarantee
  - CTA: "Request This Package"

- **Custom Option:** "Got a specific vision? Build a custom menu."

#### Case Study: 500+ Guest Funeral
- **Style:** Testimonial block with quote
- **Story:** "When a local Magna family lost someone they loved, they didn't want generic catering. They wanted food that felt like home."
- **Result:** "Adam catered for 500+ guests—every plate marinated, grilled, and plated with the same care as a family dinner."
- **Quote:** "Food isn't just fuel at times like that. It's how we show up. How we say, 'I'm here.'"

#### Custom Quote Form
- **Form ID:** `#contact-form`
- **Fields:**
  - Name (required)
  - Email (required)
  - Phone (required)
  - Event Date (date picker)
  - Guest Count (number)
  - Venue/Location (text)
  - Preferred Package (dropdown: Aloha, Ohana, Corporate, Custom)
  - Notes (textarea)
- **Submit:** Triggers email to Adam via Web3 Forms
- **Validation:** Inline error messages, success confirmation modal
- **Note:** "Adam reviews messages daily and replies within 24 hours."

#### Logistics Section
- **Delivery:** "We deliver and set up buffet-style."
- **Setup:** "Coordinate with your venue's requirements."
- **Dietary:** "Modifications available—ask upfront."
- **Payment:** "Deposit to lock date, balance due before/day-of."
- **Minimums:**
  - Under 25 guests: No minimum
  - 25–100 guests: $X minimum
  - 100+ guests: Custom quote

---

### 2.4 About Page (`/about`)

#### Hero Section
- **H1:** "Rooted in Family, Seasoned with Time"
- **Mission Statement:** "Adam's Island Style Grill & Catering isn't just a restaurant—it's a labor of love, born from generations of Pacific Islander tradition."

#### Founder Story (Long Form)
- **Layout:** Text left, image right (Adam at grill)
- **Content:** Full narrative from About doc:
  - Learning from mother and grandmother
  - Journey into cooking as a kid
  - Refining techniques over time
  - Bringing heritage to Magna, Utah
- **Pull Quote:** "I journeyed into cooking as a kid, learning from my mother and my grandmother. What taught me to make my signature dishes? Myself. Time. And definitely taste."

#### Values Section (3 Columns)
- **Aloha:** Warmth, respect, intention in every dish
- **Family:** Ohana first—food is how we connect
- **Authenticity:** No shortcuts, no compromises

#### Press / Community
- **Photos:** Local events, community outreach
- **Mentions:** Any press coverage, partnerships
- **Callout:** "Proudly serving Magna, West Valley & Greater Salt Lake"

---

### 2.5 Contact Page (`/contact`)

#### Contact Card
- **NAP:** Name, Address, Phone (large, clickable)
- **Map Embed:** Google Maps iframe centered on 9071 W Magna Main Street
- **Hours:** Mon–Sat 10am–8pm | Sun Closed
- **Click-to-Call:** Prominent button

#### Contact Form (Quick Inquiry)
- **Fields:** Name, Email, Message
- **Submit:** General inquiries (not catering)
- **Link:** "Need catering? Go to Catering Page"

#### FAQ Section
- **Q1:** Do you deliver and set up?
- **Q2:** What about dietary restrictions?
- **Q3:** Is this the same food as the restaurant?
- **Q4:** How do payments work?
- **Q5:** What's the minimum order?
- **Format:** Accordion or expandable cards

---

## 3. Component Inventory

### Global Components
- **Header:** Logo, nav links, Order button, mobile hamburger
- **Footer:** NAP, hours, social links, schema script
- **Mobile Nav:** Full-screen overlay with sticky bottom CTA bar
- **Toast Order Link:** Reusable button component
- **JSON-LD Schema:** Injected in `<head>` on all pages

### Reusable UI Blocks
- **Hero Block:** Background image, H1, tagline, CTAs
- **Info Strip:** 3-column flex row (address, phone, hours)
- **Card:** Image + title + text + CTA (used for differentiators, packages)
- **MenuItem Card:** Name, price, description, tags, dynamic from JSON
- **Package Card:** Title, serves count, includes list, price, CTA
- **Contact Form:** Validated fields, Web3 Forms integration
- **Map Embed:** Responsive Google Maps iframe
- **Testimonial Block:** Quote, attribution, optional photo

### Microcopy Library
- **CTA Labels:** "Order Pickup", "Request Quote", "Call Adam", "Download Menu"
- **Confirmation Messages:** "Thanks! Adam will reply within 24 hours."
- **Form Validation:** "Please enter a valid email", "This field is required"
- **Loading States:** "Submitting...", "Checking availability..."

---

## 4. Content Mapping and Data Flow

### Menu Page → Menu JSON
```json
{
  "entrees": [
    {
      "name": "Teriyaki Chicken, Puleju-Style",
      "price": 12.99,
      "price_range": "Single $12.99 | Double $16.99",
      "description": "Tender chicken marinated...",
      "tags": ["popular", "gf-option"]
    }
  ],
  "apps_snacks": [...],
  "sides": [...],
  "add_ons": [...],
  "beverages": [...]
}
```

### Catering Packages → CMS/JSON
- Store package definitions in editable JSON or lightweight CMS
- Fields: name, serves_min, serves_max, price, items[], cta_text

### Schema → JSON-LD in `<head>`
```json
{
  "@context": "https://schema.org",
  "@type": "Restaurant",
  "name": "Adam's Islandstyle Grill & Catering",
  "telephone": "+18012525958",
  "address": {
    "streetAddress": "9071 W Magna Main Street",
    "addressLocality": "Magna",
    "addressRegion": "UT",
    "postalCode": "84044"
  },
  "servesCuisine": "Hawaiian, Pacific Islander",
  "hasMenu": "https://adamsislandstyle.com/menu",
  "openingHoursSpecification": [
    {
      "dayOfWeek": ["Monday", "Tuesday", "Wednesday", "Thursday", "Friday", "Saturday"],
      "opens": "10:00",
      "closes": "20:00"
    }
  ]
}
```

### Order Flow
- All "Order" buttons → Toast ordering URL (external)
- Menu page remains canonical source for SEO
- Toast is authoritative for live pricing/availability

---

## 5. SEO and Schema Implementation

### Meta Title Template
```
Adam's Islandstyle Grill & Catering — [Page-Specific Keyword] in Magna UT
```
- Home: "Adam's Islandstyle Grill & Catering — Teriyaki, Lumpia, Catering in Magna UT"
- Menu: "Menu — Island Plates & Signature Teriyaki | Adam's Magna UT"
- Catering: "Event Catering — Birthdays, Funerals, Corporate | Adam's Magna UT"
- About: "Our Story — Family Recipes & Genuine Aloha | Adam's Magna UT"
- Contact: "Contact & Location — 9071 W Magna Main St | Adam's Grill"

### Meta Description (155 chars)
"Adam's Islandstyle Grill & Catering — Homegrown island plates in Magna, UT. Try the signature Puleju Teriyaki Chicken. Full‑service catering for events large and small."

### H1 Strategy
- Home: "Taste of the Islands in Magna"
- Menu: "Menu — Island Plates & Signature Teriyaki"
- Catering: "We Cater Events of Any Size"
- About: "Rooted in Family, Seasoned with Time"
- Contact: "Visit Us or Get in Touch"

### Structured Data
- **JSON-LD Restaurant:** Name, telephone, address, servesCuisine, hasMenu, openingHoursSpecification
- **AggregateRating:** Add when reviews available
- **LocalBusiness Citations:** Ensure NAP consistency across directories
- **sameAs:** Link to social profiles, Toast ordering page

### Local SEO Tactics
- Embed Google Map on Contact page
- Dedicated pages for Catering and Menu (keyword targeting)
- Keywords naturally integrated:
  - "Hawaiian food in Magna, Utah"
  - "Island style catering West Valley"
  - "Teriyaki chicken Salt Lake Valley"
  - "Authentic Hawaiian BBQ near me"
  - "Event catering Magna UT"
  - "Lupia and island plates Utah"

---

## 6. Accessibility and Responsive Notes

### Contrast Requirements
- All text on dark backgrounds must meet WCAG AA (4.5:1 ratio)
- Use token palette: text.primary (#ffffff), text.secondary (rgba(255,255,255,0.75))
- Verify gold (#ffb700) on dark surfaces passes contrast checks

### Keyboard Navigation
- All CTAs, form fields, menu filters must be focusable
- Visible focus styles: use `border.focus` token (rgba(255, 90, 0, 0.6))
- Skip-to-content link for screen readers

### ARIA Labels
- `aria-label="Order pickup via Toast"` on order buttons
- `role="navigation"` on header nav
- `aria-live="polite"` on form submission messages
- `aria-expanded` on mobile menu toggle

### Responsive Layout Breakpoints
- **Desktop (≥1024px):**
  - Two-column hero layouts
  - Three-column card grids
  - Full navigation visible
- **Tablet (768px–1023px):**
  - Stacked hero content
  - Two-column menu grid
  - Hamburger menu
- **Mobile (≤767px):**
  - Single column throughout
  - Sticky bottom CTA bar (Order + Call)
  - Collapsible accordion for FAQs
  - Horizontal scroll for menu filters

### Performance Optimizations
- Lazy load hero images and menu item photos
- Inline critical CSS for hero and nav (above-the-fold)
- Defer non-critical JS (form validation, map embed)
- Compress images to WebP format
- Use `loading="lazy"` on below-fold images

---

## 7. Deliverables Checklist

### Pre-Launch
- [ ] Finalize Toast ordering URL and test all order links
- [ ] Confirm weekly hours for accurate schema (`openingHoursSpecification`)
- [ ] Export menu JSON to CMS or keep as embedded `#menu-data`
- [ ] Implement JSON-LD in `<head>` on all pages
- [ ] Update schema after hours confirmation

### Design & Development
- [ ] Apply design token CSS variables (colors, typography, shadows)
- [ ] Build responsive header/footer components
- [ ] Implement menu grid with JSON rendering
- [ ] Create catering quote form with Web3 Forms integration
- [ ] Embed Google Map on Contact page
- [ ] Add smooth scroll for anchor links

### Quality Assurance
- [ ] Accessibility audit (contrast, keyboard nav, ARIA)
- [ ] Color contrast verification using token palette
- [ ] Cross-browser testing (Chrome, Firefox, Safari, Edge)
- [ ] Mobile responsiveness check (iOS, Android)
- [ ] Form submission testing (success/error states)
- [ ] Schema validation (Google Rich Results Test)

### Content & SEO
- [ ] Write meta titles/descriptions for all pages
- [ ] Optimize images with alt text
- [ ] Verify internal linking structure
- [ ] Submit sitemap to Google Search Console
- [ ] Set up Google Business Profile with menu

### Post-Launch
- [ ] Monitor analytics for CTA click-through rates
- [ ] Track form submissions and catering leads
- [ ] Gather customer reviews for aggregateRating schema
- [ ] Plan quarterly content updates (seasonal menus, events)

---

## 8. Technical Stack Recommendations

### Frontend
- **Framework:** Next.js or Astro (static generation + ISR for menu updates)
- **Styling:** CSS custom properties (design tokens) + Tailwind CSS utility classes
- **Animations:** Framer Motion or CSS transitions (subtle hover effects)
- **Forms:** Web3 Forms (serverless, no backend required)

### Integrations
- **Ordering:** Toast POS (external link)
- **Maps:** Google Maps Embed API
- **Analytics:** Google Analytics 4 + Google Tag Manager
- **SEO:** Next.js Head component or Astro `<head>` for meta tags

### Hosting
- **Platform:** Vercel or Netlify (edge deployment, automatic HTTPS)
- **Domain:** adamsislandstyle.com (or client-provided)
- **SSL:** Auto-provisioned via hosting platform

---

## Appendix A: Menu JSON Structure Example

```json
{
  "lastUpdated": "2024-12-01",
  "categories": {
    "entrees": [
      {
        "id": "tc-puleju",
        "name": "Teriyaki Chicken, Puleju-Style",
        "description": "Tender chicken marinated in Adam's secret blend, grilled to perfection, finished with a glaze that balances sweet, savory, and smoky.",
        "price_single": 12.99,
        "price_double": 16.99,
        "tags": ["popular", "signature"],
        "allergens": ["soy"],
        "image": "/images/teriyaki-chicken.jpg"
      },
      {
        "id": "kalua-pork",
        "name": "Kalua Pork Plate",
        "description": "Slow-roasted until it falls apart, smoky and tender. The way it's been made in the islands for generations.",
        "price_single": 13.99,
        "price_double": 17.99,
        "tags": ["traditional"],
        "allergens": [],
        "image": "/images/kalua-pork.jpg"
      }
    ],
    "apps_snacks": [
      {
        "id": "lumpia",
        "name": "Lupia (Lumpia)",
        "description": "Crispy, golden rolls stuffed with seasoned meat and vegetables. A Pacific Islander staple done right.",
        "price": 8.99,
        "quantity": "6 pieces",
        "tags": ["shareable", "popular"],
        "allergens": ["gluten"],
        "image": "/images/lumpia.jpg"
      }
    ],
    "sides": [
      {
        "id": "rice",
        "name": "Steamed Rice",
        "price": 2.99,
        "tags": ["vegan", "gf"],
        "allergens": []
      },
      {
        "id": "mac-salad",
        "name": "Macaroni Salad",
        "price": 3.99,
        "tags": ["vegetarian"],
        "allergens": ["eggs", "dairy"]
      }
    ],
    "beverages": [
      {
        "id": "hawaiian-sun",
        "name": "Hawaiian Sun Juice",
        "flavors": ["Li Hing Mui", "Guava", "Passion Orange"],
        "price": 2.49,
        "tags": ["local-favorite"]
      }
    ]
  }
}
```

---

## Appendix B: Quick Reference — Token Usage by Component

| Component | Background | Text | Border | Shadow/Glow |
|-----------|-----------|------|--------|-------------|
| Header | `bg.surface` | `text.primary` | `border.subtle` | `shadow.base` |
| Hero CTA (Primary) | `brand.primary` (coral) | `text.inverse` | `border.brand` | `glow.brand` (hover) |
| Menu Item Card | `bg.elevated` | `text.primary` | `border.default` | `shadow.base` |
| Form Input | `bg.surface` | `text.primary` | `border.default` | `glow.brand` (focus) |
| Footer | `bg.page` | `text.secondary` | `border.subtle` | none |
| Badge (Popular) | `brand.secondary` (gold) | `text.inverse` | none | `glow.secondary` |

---

**End of Wireframe Document**

*For questions or clarifications, contact the design/development lead.*
