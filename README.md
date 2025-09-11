# All Day Slimming Tea Landing Page - Maintenance Guide

This guide will help you maintain and customize the All Day Slimming Tea landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions for common updates.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the main navigation and logo. To update:

1. **Logo Text**
```html
<a href="/" class="text-2xl font-bold text-emerald-600">AllDaySlimming</a>
```
- Replace "AllDaySlimming" with your desired text
- Adjust size using `text-2xl` (options: text-sm, text-lg, text-3xl, etc.)
- Change color using `text-emerald-600` (options: text-blue-600, text-red-600, etc.)

### Hero Section
Located at the top of the page with main heading and subtitle:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 tracking-tight mb-6">
    All Day Slimming Tea
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12 max-w-3xl mx-auto">
    Your natural companion for losing weight effectively and safely
</p>
```

Tailwind CSS Class Explanation:
- `text-4xl`: Base text size
- `md:text-5xl`: Text size on medium screens
- `lg:text-6xl`: Text size on large screens
- `mb-6`: Margin bottom spacing
- `mx-auto`: Center alignment

### Features Section
To add or modify feature cards:

1. Copy the existing feature card structure:
```html
<div class="bg-white rounded-xl p-8 shadow-lg hover:shadow-xl transition-all duration-300 transform hover:scale-105">
    <div class="w-12 h-12 bg-emerald-100 rounded-full flex items-center justify-center mb-6">
        <!-- Icon SVG here -->
    </div>
    <h3 class="text-xl font-semibold mb-4">Quick Results</h3>
    <p class="text-gray-600">Experience the power of our fast-acting formula...</p>
</div>
```

2. Paste within the grid container:
```html
<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
    <!-- Paste new feature cards here -->
</div>
```

## Managing Links

### Navigation Menu Links
Current navigation links are:

```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-emerald-600 transition-colors duration-300">Features</a>
    <a href="#benefits" class="text-gray-600 hover:text-emerald-600 transition-colors duration-300">Benefits</a>
    <a href="#contact" class="text-gray-600 hover:text-emerald-600 transition-colors duration-300">Contact</a>
</div>
```

To update:
1. Locate the `href` attribute
2. Replace `#features` with your new link destination
3. Update the link text between `<a>` tags

### Call-to-Action Links
Currently pointing to "https://puraloss.com". To update:

```html
<a href="https://puraloss.com" class="inline-flex items-center px-8 py-4 border border-transparent text-lg font-medium rounded-full text-white bg-emerald-600 hover:bg-emerald-700">
    Start Your Journey Today
</a>
```

Replace `https://puraloss.com` with your new URL.

## Adding Privacy and Terms Pages

### Footer Link Setup
Current footer links structure:

```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To link privacy and terms pages:

1. Create new HTML files:
   - `privacy.html`
   - `terms.html`

2. Update the href attributes:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Links**
- Check for typos in `href` attributes
- Ensure file names match exactly (case-sensitive)
- Verify file locations relative to index.html

2. **Styling Problems**
- Make sure Tailwind CSS is properly loaded:
```html
<script src="https://cdn.tailwindcss.com"></script>
```
- Check for missing or mistyped classes
- Verify responsive classes (md:, lg:) are properly formatted

3. **Layout Issues**
- Check container classes: `max-w-7xl mx-auto px-4`
- Verify grid classes: `grid grid-cols-1 md:grid-cols-2`
- Ensure proper nesting of elements

### Need Help?
- Review the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Check HTML syntax at [W3C Validator](https://validator.w3.org/)
- Test responsive design using browser developer tools

Remember to always test changes across different screen sizes and browsers before deploying to production.