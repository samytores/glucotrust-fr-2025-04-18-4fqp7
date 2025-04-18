# GlucoTrust Landing Page Maintenance Guide

This guide will help you maintain and customize the GlucoTrust landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions for common maintenance tasks.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the site logo and navigation menu. To update:

```html
<!-- Original header text -->
<a href="#" class="text-2xl font-bold text-gray-800">GlucoTrust FR</a>

<!-- To change the logo text, modify it like this: -->
<a href="#" class="text-2xl font-bold text-gray-800">Your New Brand Name</a>
```

#### Navigation Menu Items
To modify navigation links:
```html
<div class="hidden md:flex items-center space-x-8">
    <!-- Update text between <a> tags -->
    <a href="#features" class="text-gray-600 hover:text-gray-900 transition-colors">Caractéristiques</a>
</div>
```

### Hero Section
The main banner section can be customized:

```html
<div class="relative z-10 text-center text-white max-w-4xl mx-auto px-4">
    <!-- Update main heading -->
    <h1 class="text-4xl md:text-6xl font-bold mb-6">GlucoTrust FR</h1>
    <!-- Update subheading -->
    <p class="text-xl md:text-2xl mb-8">Le TOP Supplément Régulateur de Glycémie</p>
</div>
```

#### Tailwind CSS Class Guide
Common classes explained:
- `text-4xl`: Large text size
- `md:text-6xl`: Larger text on medium screens
- `font-bold`: Bold text weight
- `mb-6`: Margin bottom spacing
- `px-4`: Horizontal padding
- `py-4`: Vertical padding

## Fixing Broken Links

### Navigation Menu Links
Current links in the navigation:
```html
<div class="hidden md:flex items-center space-x-8">
    <a href="#features">Caractéristiques</a>
    <a href="#benefits">Avantages</a>
    <a href="#faq">FAQ</a>
    <a href="https://glucotrustfr.co/decouverte/#aff=MichaelMica&cam=GithuB">Acheter maintenant</a>
</div>
```

To update:
1. Internal links (starting with #) point to section IDs
2. External links need full URLs
3. Replace the purchase link with your affiliate link:
```html
<a href="your-new-link-here" class="bg-blue-600 text-white px-6 py-2 rounded-full">
    Acheter maintenant
</a>
```

### Footer Links
Update social media links:
```html
<div class="flex space-x-4">
    <a href="your-facebook-url" class="text-gray-400 hover:text-white">
        <i class="fab fa-facebook"></i>
    </a>
    <!-- Repeat for Twitter and Instagram -->
</div>
```

## Linking Privacy and Terms Pages

### Adding Policy Links
In the footer section, locate:
```html
<ul class="space-y-2 text-gray-400">
    <!-- Original links -->
    <li><a href="#" class="hover:text-white transition-colors">Politique de confidentialité</a></li>
    <li><a href="#" class="hover:text-white transition-colors">Conditions d'utilisation</a></li>

    <!-- Update to: -->
    <li><a href="privacy.html" class="hover:text-white transition-colors">Politique de confidentialité</a></li>
    <li><a href="terms.html" class="hover:text-white transition-colors">Conditions d'utilisation</a></li>
</ul>
```

### Creating New Policy Pages
1. Create new files named `privacy.html` and `terms.html`
2. Use the same header and footer as `index.html`
3. Add policy content between header and footer
4. Maintain consistent styling using Tailwind classes

## Troubleshooting

### Common Issues and Solutions

1. **Broken Layout**
   - Check for missing closing tags
   - Verify Tailwind CSS classes are spelled correctly
   - Ensure responsive classes (md:, lg:) are properly formatted

2. **Missing Images**
   - Verify image URLs are correct
   - Check file paths for local images
   - Ensure images are uploaded to the correct directory

3. **Non-Working Links**
   - Confirm all href attributes have valid URLs
   - Check that section IDs match their corresponding links
   - Test all external links in a browser

### Need Help?
If you encounter issues:
1. Check the browser console for errors (F12 key)
2. Verify all CDN links are working
3. Ensure all required files are in the correct directory
4. Double-check spelling in class names and attributes

Remember to always test changes in multiple browsers and screen sizes before publishing updates to the live site.