# Mysterious Catalyst Landing Page - Maintenance Guide

This guide will help you maintain and customize the Mysterious Catalyst landing page. It's written for beginners who are new to HTML and Tailwind CSS.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the logo and navigation menu. To update:

1. **Logo Text**: Find this line and modify the text between the `<a>` tags:
```html
<a href="/" class="text-2xl font-bold bg-gradient-to-r from-purple-600 to-blue-600 bg-clip-text text-transparent">
    Mysterious Catalyst
</a>
```

2. **Navigation Menu Items**: Located in the `<nav>` section:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

### Hero Section
The main headline and subheading are in the first `<section>` after `<main>`:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-8 bg-gradient-to-r from-purple-600 to-blue-600 bg-clip-text text-transparent">
    Igniting Creative Futures By Empowering Entrepreneurs
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12">
    Mysterious Catalyst empowers first-generation college aspirants from low-income backgrounds
</p>
```

### Understanding Tailwind Classes
Common classes used in this page:
- `text-[size]`: Controls text size (e.g., `text-xl`, `text-2xl`)
- `font-[weight]`: Controls text weight (e.g., `font-bold`, `font-medium`)
- `mb-[size]`: Adds margin bottom (e.g., `mb-8`, `mb-12`)
- `py-[size]`: Adds padding top and bottom
- `px-[size]`: Adds padding left and right

## Managing Links

### Current Link Structure
The page contains several types of links:

1. **Navigation Links**:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```
To update these:
- Keep the `#` prefix for internal page sections
- Ensure the href matches the section's ID exactly

2. **Call-to-Action Links**:
```html
<a href="https://mysterious.wtf/" class="inline-flex items-center justify-center px-8 py-3...">
    Get Started Now
</a>
```
To update:
- Replace `https://mysterious.wtf/` with your desired URL
- Maintain the full class list for consistent styling

### Fixing Broken Links
1. Check all `href` attributes in the HTML
2. Update external links (starting with `https://`)
3. Verify internal links match their section IDs
4. Test all links after updating

## Adding Privacy and Terms Pages

### Footer Link Setup
Locate the footer's legal section:
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To link to new pages:
1. Create `privacy.html` and `terms.html` in your project folder
2. Update the href attributes:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
- Check that section IDs match exactly with href attributes
- Example: `href="#features"` must match `id="features"`

2. **Responsive Design Issues**
- Look for classes starting with `md:` or `lg:`
- These control appearance at different screen sizes
- Don't remove these classes unless you understand their purpose

3. **Gradient Text Not Showing**
- Ensure these classes stay together:
```html
bg-gradient-to-r from-purple-600 to-blue-600 bg-clip-text text-transparent
```

4. **Button Styling Problems**
- Keep all classes in button elements
- Don't remove transition classes (`transition-all`, `duration-300`)

### Need More Help?
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Verify HTML syntax using the [W3C Validator](https://validator.w3.org/)
- Test responsiveness using browser developer tools

Remember to always backup your files before making changes, and test on multiple devices and browsers after updates.