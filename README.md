# Indexely Landing Page - Maintenance Guide

This guide will help you maintain and customize the Indexely landing page. Whether you're new to web development or just getting started with HTML and CSS, we'll walk through the essential updates you might need to make.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the main navigation and logo. To update:

1. **Logo Text**: Find this line and change "Indexely" to your brand name:
```html
<a href="/" class="text-2xl font-bold text-blue-500">Indexely</a>
```

2. **Navigation Items**: Locate the navigation menu:
```html
<div class="hidden md:flex items-center space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
</div>
```
To modify text, simply change the text between `<a>` tags.

### Hero Section
Find the main headline and subtitle:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-8">
    Indexely - Index Your Pages Fast in Google and AI Search
</h1>
<p class="text-xl md:text-2xl text-gray-300 mb-12">
    Get traffic fast to your website with instant indexing
</p>
```

To modify:
- Change the text between the tags
- Keep the classes intact to maintain responsive design
- The `md:` and `lg:` prefixes control how text appears on different screen sizes

### Tailwind CSS Classes Explained
Common classes used throughout:
- `text-[size]`: Controls text size (xl, 2xl, etc.)
- `mb-[number]`: Adds margin bottom (mb-8, mb-12, etc.)
- `py-[number]`: Adds padding top and bottom
- `px-[number]`: Adds padding left and right
- `bg-[color]`: Sets background color

## Managing Links

### Current Links Overview
1. Navigation Menu Links:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="https://laptoplifepro.com/speedyindex">Get Started</a>
```

2. Call-to-Action Links:
```html
<a href="https://laptoplifepro.com/speedyindex" class="inline-block bg-blue-600...">
    Start Free Trial
</a>
```

### Updating Links
To update any link:
1. Locate the `<a>` tag
2. Change the `href` attribute value
3. For internal links (same page sections):
   - Use `#section-id` format
   - Ensure the section has matching `id` attribute
4. For external links:
   - Use complete URLs starting with `https://`

Example:
```html
<!-- Before -->
<a href="https://laptoplifepro.com/speedyindex">Get Started</a>

<!-- After -->
<a href="https://your-domain.com/signup">Get Started</a>
```

## Adding Privacy and Terms Pages

### Footer Links Setup
Locate the footer section with legal links:
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
1. Create your privacy.html and terms.html files
2. Update the href attributes:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

Common Issues and Solutions:

1. **Broken Internal Links**
   - Check that section IDs match exactly with href values
   - IDs are case-sensitive
   - Example: `href="#FAQ"` won't link to `id="faq"`

2. **Responsive Design Issues**
   - Don't remove `md:` or `lg:` prefixes from classes
   - These ensure proper display on different devices
   - Test on mobile, tablet, and desktop views

3. **Style Changes Not Working**
   - Verify Tailwind CSS is properly loaded
   - Check for typos in class names
   - Maintain spacing between multiple classes

4. **Links Not Working**
   - Ensure full URLs include `https://`
   - Check for typos in URLs
   - Verify file paths for internal pages

Need more help? Contact support@indexely.com for assistance.