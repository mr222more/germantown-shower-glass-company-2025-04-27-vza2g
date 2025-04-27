# Custom Euro Glass Landing Page - Maintenance Guide

This guide will help you maintain and customize the Custom Euro Glass landing page. It's designed for beginners with no prior coding experience.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your company name and navigation menu. To update:

1. **Company Name:**
```html
<a href="/" class="text-2xl font-bold text-gray-900">Custom Euro Glass</a>
```
- Replace "Custom Euro Glass" with your desired company name
- The `text-2xl` class controls size (options: text-xl, text-3xl, text-4xl)

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-gray-900">Features</a>
    <!-- Additional menu items -->
</div>
```
- Update text between `<a>` tags
- `space-x-8` controls spacing between items (adjust using space-x-4, space-x-6, etc.)

### Hero Section
Located at the top of the page:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold">
    Germantown Shower Glass Company
</h1>
<p class="text-xl md:text-2xl text-gray-600">
    Walk-in shower glass - open design for modern living
</p>
```
- Update text between the tags
- Size classes explained:
  - `text-4xl`: Default size
  - `md:text-5xl`: Size on medium screens
  - `lg:text-6xl`: Size on large screens

### Styling Tips
- Color modifications:
  - Background colors use `bg-{color}-{shade}` (e.g., `bg-blue-600`)
  - Text colors use `text-{color}-{shade}` (e.g., `text-gray-900`)
- Common colors in use:
  - Blue: `blue-600` (buttons)
  - Gray: `gray-900` (dark text), `gray-600` (lighter text)
  - White: `white` (light backgrounds)

## Managing Links

### Navigation Menu Links
Current internal links:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```
To update:
1. The `#` symbol indicates an internal page section
2. Ensure the href matches the section's ID attribute
3. Example updating Features link to a new page:
```html
<a href="/features.html">Features</a>
```

### External Links
The main call-to-action button:
```html
<a href="http://www.customeuroglass.com" class="inline-block bg-blue-600">
    Get Your Custom Design
</a>
```
To update:
1. Replace the URL with your website
2. Always include `http://` or `https://`
3. Test the link after updating

### Email Links
Located in the contact section:
```html
<a href="mailto:office@customeuroglass.com">
```
To update:
1. Replace `office@customeuroglass.com` with your email
2. Keep the `mailto:` prefix

## Adding Privacy and Terms Pages

### Current Footer Links
```html
<div>
    <h4 class="text-white text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white">Terms of Service</a></li>
    </ul>
</div>
```

### Steps to Add Policy Pages
1. Create new files:
   - `privacy.html`
   - `terms.html`

2. Update the footer links:
```html
<li><a href="/privacy.html" class="text-gray-400 hover:text-white">Privacy Policy</a></li>
<li><a href="/terms.html" class="text-gray-400 hover:text-white">Terms of Service</a></li>
```

3. Maintain consistent styling by copying these classes:
   - `text-gray-400`: Default text color
   - `hover:text-white`: Hover effect
   - `transition-colors duration-300`: Smooth transition

## Troubleshooting

Common Issues:
1. **Broken Internal Links**
   - Ensure section IDs match href attributes
   - Check for typos in IDs
   - IDs are case-sensitive

2. **Responsive Design Issues**
   - Check media query classes (md:, lg:)
   - Test on different screen sizes
   - Common breakpoints:
     - md: 768px
     - lg: 1024px

3. **Style Changes Not Working**
   - Verify Tailwind CSS is properly loaded
   - Check class name spelling
   - Ensure classes are in the correct order

For additional help, consult the [Tailwind CSS documentation](https://tailwindcss.com/docs) or contact your web developer.