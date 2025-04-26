# Landing Page Maintenance Guide

This guide will help you maintain and customize the Koala Knuffel landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your logo and navigation menu. To update:

1. **Logo Text:**
```html
<a href="#" class="text-2xl font-bold bg-gradient-to-r from-purple-600 to-pink-600 bg-clip-text text-transparent">
    Koala Knuffel <!-- Change this text -->
</a>
```

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>  <!-- Change menu item text here -->
    <a href="#benefits">Voordelen</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

### Hero Section
Located at the top of the page:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold mb-6">
    Ademende Koala Knuffel <!-- Main headline -->
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12">
    🔥 Nog maar enkele stuks beschikbaar! <!-- Subheadline -->
</p>
```

### Understanding Tailwind Classes
Common classes used in this page:
- `text-[size]`: Controls text size (e.g., `text-4xl`)
- `font-[weight]`: Controls text weight (e.g., `font-bold`)
- `mb-[size]`: Adds margin bottom (e.g., `mb-6`)
- `py-[size]`: Adds padding top and bottom
- `px-[size]`: Adds padding left and right

Example of modifying responsive text:
```html
<!-- Original -->
<h1 class="text-4xl md:text-5xl lg:text-6xl">

<!-- Make text smaller -->
<h1 class="text-3xl md:text-4xl lg:text-5xl">
```

## Managing Links

### Navigation Menu Links
Current internal links in the navigation:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Voordelen</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

To update:
1. Find the `href` attribute
2. Replace the value with your new link
3. For internal sections, use `#section-name`
4. For external links, use the full URL

Example:
```html
<!-- Internal link -->
<a href="#new-section">New Section</a>

<!-- External link -->
<a href="https://your-website.com/page">External Page</a>
```

### Call-to-Action Links
The main product link appears twice:
```html
<a href="https://amzn.to/4iwZ7dH" class="inline-block px-8 py-4...">
    Bestel Nu Met Korting
</a>
```

To update:
1. Locate both CTA buttons (one in hero section, one in bottom section)
2. Replace the `href` value with your new product link
3. Update the button text if needed

## Adding Privacy and Terms Pages

### Current Footer Links
```html
<ul class="space-y-2">
    <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
</ul>
```

To link to new pages:

1. Create your privacy.html and terms.html files
2. Update the footer links:
```html
<ul class="space-y-2">
    <li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
</ul>
```

3. Ensure consistent styling by copying these classes to new page links:
```html
class="text-gray-400 hover:text-white transition-colors duration-300"
```

## Troubleshooting

### Common Issues

1. **Broken Internal Links**
   - Ensure section IDs match the href values
   - Check for typos in IDs
   - IDs should not contain spaces

2. **Responsive Design Issues**
   - Keep the `md:` and `lg:` prefixes when modifying classes
   - Don't remove the `container` class from main sections
   - Maintain the existing grid structure in features and benefits sections

3. **Styling Problems**
   - Don't remove the `font-['Poppins']` class from the body
   - Keep the gradient classes intact for consistent branding
   - Maintain the existing padding and margin rhythm

### Need Help?
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Validate your HTML at [W3C Validator](https://validator.w3.org/)
- Test responsiveness using browser developer tools

Remember to always test your changes across different screen sizes before publishing updates.