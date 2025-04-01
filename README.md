# NachtBril Landing Page Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the NachtBril landing page. Whether you're new to web development or need a quick reference, follow these step-by-step instructions.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Text Content Updates

#### Header Section
```html
<!-- Original -->
<a href="/" class="text-2xl font-bold">NachtBril</a>

<!-- How to modify -->
<a href="/" class="text-2xl font-bold">Your Brand Name</a>
```

#### Hero Section
The main headline and subheading are located in the hero section:
```html
<h1 class="text-4xl md:text-6xl font-bold leading-tight mb-6">
    Auto NachtBril - Beter Zicht - Veiliger In Het Verkeer
</h1>
<p class="text-xl md:text-2xl mb-8">
    Met De Antireflectie Auto Nachtbril - Veiliger De Weg Op
</p>
```

### Tailwind CSS Classes Explained

#### Responsive Design Classes
- `md:` prefix: Applies styles on medium screens (768px+)
- `lg:` prefix: Applies styles on large screens (1024px+)

Example:
```html
<!-- This text is smaller on mobile, larger on medium screens -->
<h1 class="text-4xl md:text-6xl">
```

#### Common Classes Used
- Layout: `container`, `mx-auto`, `px-4`, `py-4`
- Flexbox: `flex`, `items-center`, `justify-between`
- Spacing: `mb-4`, `mt-8`, `space-x-4`
- Colors: `bg-black`, `text-white`, `hover:bg-gray-800`

## Fixing Broken Links

### Navigation Menu Links
Current navigation links are:
```html
<div class="hidden md:flex items-center space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="https://nachtbril.com/shop/">Shop Now</a>
</div>
```

To update:
1. Internal links (starting with #) point to section IDs
2. External links need full URLs
3. Replace `https://nachtbril.com/shop/` with your actual shop URL

### Footer Links
Located in the footer section:
```html
<ul class="space-y-2">
    <li><a href="#" class="hover:text-gray-300">About Us</a></li>
    <li><a href="#" class="hover:text-gray-300">Shop</a></li>
    <li><a href="#" class="hover:text-gray-300">FAQ</a></li>
    <li><a href="#" class="hover:text-gray-300">Contact</a></li>
</ul>
```

To update:
1. Replace `#` with actual page URLs
2. Example: `<a href="/about.html">About Us</a>`

## Linking Privacy and Terms Pages

### Adding Policy Links
Locate the Policies section in the footer:
```html
<div>
    <h3 class="text-xl font-bold mb-4">Policies</h3>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-gray-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-gray-300">Terms of Service</a></li>
    </ul>
</div>
```

Update the links:
```html
<li><a href="/privacy.html" class="hover:text-gray-300">Privacy Policy</a></li>
<li><a href="/terms.html" class="hover:text-gray-300">Terms of Service</a></li>
```

### Creating New Policy Pages
1. Create `privacy.html` and `terms.html` in your root directory
2. Use the same header and footer as `index.html`
3. Maintain consistent styling:
```html
<div class="container mx-auto px-4 py-16">
    <h1 class="text-4xl font-bold mb-8">Privacy Policy</h1>
    <!-- Add your policy content here -->
</div>
```

## Troubleshooting

### Common Issues

1. **Broken Images**
   - Check image paths in `src` attributes
   - Ensure images are in the correct directory
   - Verify image URLs are accessible

2. **Responsive Design Issues**
   - Test different screen sizes using browser dev tools
   - Verify `md:` and `lg:` classes are working
   - Check for overflow issues on mobile

3. **Link Problems**
   - Ensure all `href` attributes have valid URLs
   - Test internal links (#) point to correct IDs
   - Verify external links include `https://`

### Need Help?
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Validate your HTML at [W3C Validator](https://validator.w3.org/)
- Test responsive design using Chrome DevTools

Remember to always test your changes across different devices and browsers before pushing to production.