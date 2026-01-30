# HRV Website - Premium Night Recovery Supplements

A production-ready Next.js marketing website for HRV, a premium supplement brand focused on nighttime recovery for disciplined athletes and purpose-driven leaders.

## Brand Overview

**Domain:** livehrv.com  
**Flagship Product:** HRV Dusk - Night Recovery Ritual  
**Brand Message:** "Sleep is worship. Recovery is stewardship. Strength is service."  
**Visual Style:** Luxury wellness + elite performance minimalism

## Tech Stack

- **Framework:** Next.js 14 (App Router)
- **Styling:** Tailwind CSS
- **Language:** TypeScript
- **Animations:** Framer Motion
- **Deployment:** Vercel (recommended)

## Project Structure

```
hrv-website/
├── app/
│   ├── layout.tsx              # Root layout with navigation
│   ├── page.tsx                # Homepage
│   ├── globals.css             # Global styles
│   ├── products/
│   │   └── dusk/
│   │       └── page.tsx        # Product page
│   ├── science/
│   │   └── page.tsx            # Science & ingredients
│   ├── about/
│   │   └── page.tsx            # Brand story
│   ├── protocol/
│   │   └── page.tsx            # Night recovery protocol
│   ├── faq/
│   │   └── page.tsx            # FAQ
│   ├── contact/
│   │   └── page.tsx            # Contact form
│   ├── privacy-policy/
│   │   └── page.tsx            # Privacy policy
│   ├── terms/
│   │   └── page.tsx            # Terms of service
│   ├── disclaimer/
│   │   └── page.tsx            # Medical disclaimer
│   ├── sitemap.ts              # SEO sitemap
│   └── robots.ts               # Robots.txt
├── components/
│   ├── Navigation.tsx          # Header navigation
│   ├── Footer.tsx              # Footer
│   ├── Button.tsx              # Reusable button
│   └── EmailCapture.tsx        # Email signup form
├── data/
│   └── content.ts              # Product data, FAQs, testimonials
├── public/                     # Static assets (add images here)
└── package.json
```

## Getting Started

### Prerequisites

- Node.js 18+ installed
- npm or yarn package manager

### Installation

1. **Navigate to the project directory:**
   ```bash
   cd hrv-website
   ```

2. **Install dependencies:**
   ```bash
   npm install
   ```

3. **Run the development server:**
   ```bash
   npm run dev
   ```

4. **Open your browser:**
   Navigate to [http://localhost:3000](http://localhost:3000)

### Development Commands

```bash
npm run dev      # Start development server
npm run build    # Build for production
npm run start    # Start production server
npm run lint     # Run ESLint
```

## Deployment

### Deploy to Vercel (Recommended)

1. **Install Vercel CLI:**
   ```bash
   npm install -g vercel
   ```

2. **Deploy:**
   ```bash
   vercel
   ```

3. **For production deployment:**
   ```bash
   vercel --prod
   ```

### Alternative: Deploy via Vercel Dashboard

1. Push your code to GitHub
2. Go to [vercel.com](https://vercel.com)
3. Import your repository
4. Vercel will auto-detect Next.js and configure everything
5. Click "Deploy"

### Environment Variables

Currently, no environment variables are required for the basic site. When integrating with services, add them to `.env.local`:

```env
# Example for future integrations
NEXT_PUBLIC_STRIPE_KEY=your_stripe_key
EMAIL_SERVICE_API_KEY=your_email_key
```

## Content Management

### Editing Product Information

All product data is centralized in `/data/content.ts`. To update:

1. Open `data/content.ts`
2. Modify the relevant section:
   - `productData.dusk` - Product info, pricing, formula
   - `faqData` - FAQ questions and answers
   - `testimonials` - Customer reviews
   - `brandValues` - Brand messaging

### Adding Images

1. Add images to the `/public` folder
2. Reference them in components: `/image-name.jpg`
3. For product images, update the placeholder divs in components

Example:
```jsx
<Image 
  src="/product-dusk.jpg" 
  alt="HRV Dusk"
  width={600}
  height={600}
/>
```

## Key Features

### ✅ Complete Page Set
- Homepage with hero, benefits, ingredients, testimonials
- Product page with detailed formula, subscription options
- Science page explaining HRV and research
- Protocol page with comprehensive night recovery guide
- About page with founder story
- FAQ, Contact, and all legal pages

### ✅ Conversion Optimized
- Sticky mobile CTA on product page
- Email capture with benefits
- Subscribe & Save option
- Trust badges and quality indicators
- Clear value propositions

### ✅ Professional Design
- Premium black/white minimalist aesthetic
- Custom Crimson Pro font for headers
- Responsive mobile-first layout
- Smooth animations and transitions
- Accessible semantic HTML

### ✅ SEO Ready
- Metadata and OpenGraph tags
- Sitemap.xml generation
- Robots.txt configuration
- Semantic HTML structure
- Fast loading performance

## Customization Guide

### Changing Colors

Edit `tailwind.config.ts`:
```typescript
colors: {
  'hrv-black': '#0A0A0A',    // Main black
  'hrv-white': '#FAFAFA',    // Main white
  'hrv-gray': { ... }         // Gray scale
}
```

### Updating Typography

The site uses:
- **Display font:** Crimson Pro (serif, for headers)
- **Body font:** System font stack (sans-serif)

To change fonts, update `app/globals.css`:
```css
@import url('https://fonts.googleapis.com/css2?family=Your+Font&display=swap');

:root {
  --font-display: 'Your Font', serif;
}
```

### Modifying Animations

Global animations are in `app/globals.css`. Component-specific animations use Framer Motion in individual components.

## Integration Checklist

Before going live, integrate:

- [ ] **E-commerce Platform** (Shopify, WooCommerce, or custom)
- [ ] **Payment Processing** (Stripe recommended)
- [ ] **Email Marketing** (Klaviyo, ConvertKit, or Mailchimp)
- [ ] **Analytics** (Google Analytics, Plausible)
- [ ] **Customer Support** (Intercom, Zendesk)
- [ ] **Product Images** (Professional photos)
- [ ] **SSL Certificate** (Auto via Vercel)
- [ ] **Domain Setup** (Point livehrv.com to deployment)

## Future Enhancements

Consider adding:
- Shopping cart functionality
- User account dashboard
- Subscription management portal
- Blog/content section
- Product reviews system
- Referral program
- Wholesale/bulk ordering

## Brand Voice Guidelines

**Tone:** Calm authority, masculine restraint, premium minimalism  
**Avoid:** Hype, cringe, medical claims, clichés ("biohack", "crush it")  
**Use:** Supportive language ("supports", "promotes", "helps")  
**Phrases:**
- "Sleep is worship"
- "Recovery is stewardship"
- "Strength is service"
- "Night recovery ritual"

## Legal Compliance

All pages include appropriate disclaimers:
- Medical disclaimer on all product pages
- FDA statement: "These statements have not been evaluated..."
- Clear "not intended to diagnose, treat, cure, or prevent"
- Proper legal pages (Privacy, Terms, Disclaimer)

## Support

For questions or issues:
- Email: support@livehrv.com
- Review FAQ page
- Check component documentation

## License

Proprietary - All rights reserved by HRV

---

**Built with discipline. Optimized for recovery. Designed for performance.**
