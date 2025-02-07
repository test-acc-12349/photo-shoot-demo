# Photo-Shoot Landing Page Maintenance Guide

This guide will help you maintain and customize the Photo-Shoot landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates safely and effectively.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the site name and navigation menu. To update:

```html
<!-- Located at the top of the page -->
<div class="flex-shrink-0">
    <h1 class="text-2xl font-bold">Photo-Shoot</h1> <!-- Change site name here -->
</div>
```

**Key Tailwind Classes Explained:**
- `text-2xl`: Sets large text size
- `font-bold`: Makes text bold
- `flex-shrink-0`: Prevents text from shrinking in flexible layouts

### Hero Section
The main banner section with large text and call-to-action:

```html
<div class="text-center">
    <h2 class="text-4xl md:text-6xl font-bold text-white mb-6 tracking-tight">Photo-Shoot</h2>
    <p class="text-xl md:text-2xl text-gray-200 mb-8">Get the ultimate product photography lightbox</p>
</div>
```

**Responsive Design Tips:**
- `md:text-6xl`: Text becomes larger on medium screens
- `text-4xl`: Default size for mobile
- `mb-6`: Adds margin bottom spacing

### Features Section
To modify feature cards:

```html
<div class="bg-white p-8 rounded-xl shadow-lg hover:shadow-xl transition-shadow duration-300">
    <div class="w-12 h-12 bg-blue-100 rounded-full flex items-center justify-center mb-6">
        <i class="fas fa-usb text-blue-600 text-xl"></i>
    </div>
    <h3 class="text-xl font-semibold mb-4">USB Powered</h3> <!-- Feature title -->
    <p class="text-gray-600">Connect to any USB port for consistent, reliable power supply</p> <!-- Feature description -->
</div>
```

## Fixing Broken Links

### Navigation Menu Links
Current navigation links are:

```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Features</a>
    <a href="#benefits" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Benefits</a>
    <a href="#faq" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">FAQ</a>
</div>
```

To update:
1. Locate the `href` attribute
2. Replace `#section-name` with your desired link
3. For external links, use complete URLs (e.g., `https://example.com`)
4. For internal links, use relative paths (e.g., `./about.html`)

### Buy Now Links
The current Stripe payment link appears multiple times:

```html
<a href="https://buy.stripe.com/14k5mM58ObjBbRK000" class="inline-flex items-center px-4 py-2 border border-transparent text-sm font-medium rounded-md text-white bg-blue-600 hover:bg-blue-700">
    Buy Now
</a>
```

To update:
1. Replace the Stripe URL with your new payment link
2. Ensure you update ALL instances (there are multiple throughout the page)

## Linking Privacy and Terms Pages

### Footer Policy Links
Located in the footer section:

```html
<div>
    <h4 class="text-white text-lg font-semibold mb-4">Policies</h4>
    <ul class="space-y-2">
        <li><a href="./privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="./terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
        <li><a href="./shipping.html" class="hover:text-white transition-colors duration-300">Shipping Policy</a></li>
    </ul>
</div>
```

To add new policy pages:
1. Create your policy HTML files (e.g., `privacy.html`, `terms.html`)
2. Place them in the same directory as `index.html`
3. Update the `href` attributes to point to your new files
4. Maintain the same class structure for consistent styling

## Troubleshooting

### Common Issues:

1. **Broken Images**
   - Ensure image paths are correct
   - Verify image files exist in the specified location
   - Check image URLs are accessible

2. **Responsive Design Issues**
   - Don't remove `md:` prefixes from classes
   - Maintain the existing grid structure
   - Test on multiple screen sizes

3. **Link Problems**
   - Verify all URLs start with `http://` or `https://` for external links
   - Use `./` for files in the same directory
   - Check for typos in file names and paths

### Need Help?
If you encounter issues:
1. Check the browser's developer tools (F12) for errors
2. Verify all files are in the correct locations
3. Ensure Tailwind CSS CDN is loading properly
4. Contact support at admin@photoshoot.site

Remember to always test your changes across different devices and browsers before pushing to production.