# Pura Loss Lead Capture Page - Implementation Instructions

## Project Overview

Build a high-converting, SEO-optimized lead capture page for Pura Loss that collects visitor information (First Name, Last Name, Email) in exchange for a free ebook: **"The Ultimate Weight Loss Program – 100 Tips to Achieve the Best Version of Yourself."**

The page will bridge seamlessly into the affiliate offer (All Day Slimming Tea) by suggesting the free training supports results that many enhance with a daily tea ritual.

## Technical Stack

- **Framework**: HTML5 with Tailwind CSS (already configured in project)
- **Fonts**: Inter font family (already loaded)
- **Form Handling**: Formspree or similar service
- **SEO**: Complete meta tags, Open Graph, Twitter Cards, JSON-LD schema
- **Responsive**: Mobile-first design using Tailwind utilities

## File Structure

```
/
├── index.html (existing All Day Slimming Tea page)
├── free-weight-loss-program.html (NEW - Pura Loss lead capture)
├── privacy.html (existing)
├── terms.html (existing)
├── instructions.md (this file)
└── assets/
    └── ebook-cover.jpg (placeholder needed)
```

## Page Sections & Content

### 1. Hero Section (Above the Fold)
- **Headline**: "100 Proven Weight Loss Tips — Free Guide from Pura Loss"
- **Subheadline**: "Get your FREE copy of 'The Ultimate Weight Loss Program – 100 Tips to Achieve the Best Version of Yourself' and start your transformation today."
- **Form Fields**: First Name, Last Name, Email Address
- **CTA Button**: "Send Me My Free Program Now!"
- **Privacy Line**: "Instant access. Pura Loss respects your privacy. No spam — ever."
- **Visual**: Ebook cover mockup

### 2. Benefits Section
- **Headline**: "What You'll Discover Inside the Program"
- **Benefits List**:
  - 100 actionable tips for natural weight loss and steady progress
  - Daily routines to boost energy and support digestion
  - Strategies for sustainable results without fad diets
  - Simple nutrition & movement hacks for busy people
  - Motivation tools to stay consistent and become your best self
- **Secondary CTA**: "Yes, I Want Instant Access"

### 3. Trust Section
- **Headline**: "Trusted Tips for Real People"
- **Copy**: "At Pura Loss, we focus on real-life solutions, not gimmicks. Our free program gives you a clear path to better habits, stronger routines, and lasting results."

### 4. Final CTA Section
- **Headline**: "Start Your Transformation Today"
- **Form**: Repeat lead capture form
- **CTA Button**: "Send Me the Free Program Now"

### 5. Bridge Section (Affiliate Introduction)
- **Headline**: "Want Faster, Natural Results?"
- **Copy**: "Your free program is designed to give you sustainable weight loss strategies you can use right away. Many people also find that combining these lifestyle tips with a simple daily ritual — like enjoying a gentle slimming tea — helps them stay consistent and feel their best. One option loved by thousands is All Day Slimming Tea, a natural formula that supports energy, fat metabolism, and digestion."
- **CTA Button**: "Discover All Day Slimming Tea →"
- **Disclosure**: "We may earn a commission if you purchase through this link — at no extra cost to you."

### 6. FAQ Section
- **Questions & Answers**:
  - Is the guide really free? → Yes — just enter your name and email to get instant access from Pura Loss.
  - Do I need to follow a strict diet? → No — this program focuses on simple, practical changes you can actually stick with.
  - How fast will I see results? → Everyone is different. The key is consistency. The tips are designed for gradual, sustainable change.
  - Can I use All Day Slimming Tea with the program? → Yes. Many people combine it with the program to support their results. The tea is optional but recommended.
  - Will you spam me? → No. We respect your inbox. You can unsubscribe at any time.

## SEO Implementation

### Meta Tags
```html
<title>Free Weight Loss Program | Pura Loss – 100 Proven Tips</title>
<meta name="description" content="Download Pura Loss' FREE guide: 100 weight loss tips to burn fat naturally, boost energy, and maintain results. Start your transformation today!">
<link rel="canonical" href="https://slimming-tea.puraloss.com/free-weight-loss-program/">
```

### Open Graph Tags
```html
<meta property="og:type" content="website">
<meta property="og:url" content="https://slimming-tea.puraloss.com/free-weight-loss-program/">
<meta property="og:title" content="Free Weight Loss Program by Pura Loss – 100 Proven Tips">
<meta property="og:description" content="Download your free guide with 100 tips for natural weight loss, energy, and healthy habits. Start today.">
<meta property="og:image" content="https://slimming-tea.puraloss.com/assets/ebook-cover.jpg">
```

### Twitter Cards
```html
<meta name="twitter:card" content="summary_large_image">
<meta name="twitter:title" content="Free Weight Loss Program by Pura Loss – 100 Proven Tips">
<meta name="twitter:description" content="Get instant access to 100 proven tips for sustainable weight loss and energy. Free from Pura Loss.">
<meta name="twitter:image" content="https://slimming-tea.puraloss.com/assets/ebook-cover.jpg">
```

### JSON-LD Schema
Complete structured data including:
- Organization schema for Pura Loss
- WebSite schema
- WebPage schema
- Book schema for the ebook
- FAQPage schema
- SubscribeAction schema

## Form Integration

### Recommended: Formspree Setup
1. Create account at formspree.io
2. Create new form endpoint
3. Configure form action: `action="https://formspree.io/f/YOUR_FORM_ID"`
4. Add honeypot protection
5. Set up email notifications
6. Configure thank you page redirect

### Form HTML Structure
```html
<form action="https://formspree.io/f/YOUR_FORM_ID" method="POST" class="space-y-4">
  <input type="text" name="firstName" placeholder="First Name" required>
  <input type="text" name="lastName" placeholder="Last Name" required>
  <input type="email" name="email" placeholder="Email Address" required>
  <input type="hidden" name="_next" value="https://slimming-tea.puraloss.com/thank-you">
  <input type="hidden" name="_subject" value="New Free Program Download">
  <button type="submit">Send Me My Free Program Now!</button>
</form>
```

## Design Guidelines

### Color Scheme
- Primary: Emerald/Green (#059669, #10b981)
- Secondary: Gray tones (#374151, #6b7280)
- Background: White with subtle green gradients
- CTA Buttons: Emerald with hover effects

### Typography
- Font Family: Inter (already loaded)
- Headings: Bold, large sizes (text-4xl to text-6xl)
- Body: Regular weight, readable sizes (text-lg, text-xl)
- Consistent spacing and hierarchy

### Layout
- Max width containers (max-w-7xl)
- Responsive grid systems
- Generous padding and margins
- Mobile-first approach

## Implementation Steps

1. **Create HTML file**: `free-weight-loss-program.html`
2. **Set up basic structure**: HTML5 doctype, head section, body
3. **Add SEO elements**: All meta tags, Open Graph, Twitter Cards
4. **Implement header**: Consistent with existing site navigation
5. **Build hero section**: Form, headline, subheadline, CTA
6. **Add benefits section**: Bullet points, secondary CTA
7. **Create trust section**: Social proof copy
8. **Implement final CTA**: Repeat form for conversion
9. **Add bridge section**: Affiliate link introduction
10. **Build FAQ section**: Structured Q&A with schema
11. **Create footer**: Consistent with existing site
12. **Add JSON-LD schema**: Complete structured data
13. **Set up form handling**: Formspree integration
14. **Test responsiveness**: Mobile, tablet, desktop
15. **Validate HTML/SEO**: Check all elements work correctly

## Testing Checklist

- [ ] Form submission works correctly
- [ ] All links function properly
- [ ] Mobile responsiveness verified
- [ ] SEO meta tags present and correct
- [ ] Schema markup validates
- [ ] Page loads quickly
- [ ] Images display correctly
- [ ] CTA buttons have proper hover effects
- [ ] Privacy/Terms links work
- [ ] Email notifications configured

## Development & Deployment Workflow

### Local Development
1. **Development**: Build and test on localhost
2. **Git workflow**: Commit changes to GitHub repository
3. **Deployment**: Coolify automatically deploys from GitHub to slimming-tea.puraloss.com
4. **Testing**: Verify deployment on live domain

### Launch Requirements
1. **Domain setup**: Already configured at slimming-tea.puraloss.com/free-weight-loss-program/
2. **SSL certificate**: Handled by Coolify deployment
3. **Analytics**: Add Google Analytics/GTM if needed
4. **Form testing**: Verify email delivery works on live site
5. **Mobile testing**: Test on actual devices
6. **Performance**: Check page speed scores
7. **SEO validation**: Use Google Search Console

## Maintenance Notes

- Monitor form submissions regularly
- Update ebook cover image when available
- A/B test different headlines/CTAs
- Track conversion rates
- Update FAQ section based on common questions
- Ensure affiliate links remain active

## Contact Information

- Support Email: support@puraloss.com
- Brand: © Pura Loss, All Rights Reserved
- Privacy Policy: Link to existing privacy.html
- Terms: Link to existing terms.html
