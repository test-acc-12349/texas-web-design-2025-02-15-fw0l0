# Texas Web Design Landing Page - Maintenance Guide

This guide will help you maintain and customize the Texas Web Design landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates safely and effectively.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the company logo and navigation menu. To modify:

1. **Company Logo**
```html
<a href="/" class="text-2xl font-bold text-blue-600">TWD</a>
```
- Replace "TWD" with your company name
- Adjust size using `text-2xl` (options: text-sm, text-lg, text-3xl, etc.)
- Change color using `text-blue-600` (options: text-red-600, text-green-600, etc.)

2. **Navigation Menu Items**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-blue-600">Features</a>
    <!-- Other menu items -->
</div>
```
- Replace text between `<a>` tags
- Maintain the `hidden md:flex` class for mobile responsiveness
- `space-x-8` controls spacing between items (adjust number as needed)

### Hero Section
Located at the top of the page:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6">
    Texas Web Design
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12">
    Best Websites In Texas
</p>
```
- Update text between tags
- Size classes explained:
  - `text-4xl`: Default size
  - `md:text-5xl`: Size on medium screens
  - `lg:text-6xl`: Size on large screens

### Features Section
To modify feature cards:
```html
<div class="bg-white p-8 rounded-2xl shadow-lg">
    <h3 class="text-xl font-bold mb-4">Free Hosting</h3>
    <p class="text-gray-600">Premium hosting included...</p>
</div>
```
- Update headings and descriptions
- Maintain padding (`p-8`) and margin (`mb-4`) classes for consistent spacing
- Keep `shadow-lg` for visual depth

## Managing Links

### Navigation Links
Current navigation structure:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```
To update:
1. Internal links (same page):
   - Use `#section-id` format
   - Ensure IDs match section identifiers
2. External links:
   - Replace `#` with full URL
   - Example: `href="https://yoursite.com/page"`

### Call-to-Action Buttons
```html
<a href="https://twd.com" class="inline-block px-8 py-4 bg-blue-600">
    Start Your Project Today
</a>
```
- Replace `https://twd.com` with your actual URL
- Maintain classes for consistent styling
- Test links after updating

## Adding Privacy and Terms Pages

### Footer Link Updates
Locate the legal section in the footer:
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white">Terms of Service</a></li>
    </ul>
</div>
```

To link privacy and terms pages:
1. Create new HTML files:
   - `privacy.html`
   - `terms.html`
2. Update href attributes:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Links**
- Check for typos in URLs
- Verify file names match exactly
- Ensure files are in the correct directory

2. **Styling Problems**
- Maintain all Tailwind classes when copying/pasting
- Check for missing closing tags
- Verify class names are spelled correctly

3. **Responsive Design Issues**
- Keep `md:` and `lg:` prefixed classes for proper scaling
- Test on multiple screen sizes
- Don't remove `container` classes from section wrappers

### Need Help?
- Review the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Check browser developer tools (F12) for errors
- Maintain a backup copy of the original file before making changes

Remember to test all changes across different devices and browsers before publishing updates to your live site.