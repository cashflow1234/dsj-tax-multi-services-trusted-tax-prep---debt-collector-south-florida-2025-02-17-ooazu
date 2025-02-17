# DSJ Tax Landing Page - Maintenance Guide

This guide will help you maintain and customize the DSJ Tax landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates safely and effectively.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the company logo and navigation menu. To update:

```html
<!-- Located at the top of the page -->
<div class="text-2xl font-bold text-blue-500">DSJ Tax</div>
```

To change the company name:
1. Locate this div in the header section
2. Replace "DSJ Tax" with your desired text
3. Maintain the existing classes to preserve styling

### Hero Section
The main headline and subheading can be updated here:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-6 bg-gradient-to-r from-blue-400 to-blue-600 bg-clip-text text-transparent">
    DSJ Tax Multi-Services
</h1>
<p class="text-xl md:text-2xl text-gray-300 mb-12 max-w-3xl mx-auto">
    Trusted tax preparation & Expert Debt Collection Agency in South Florida
</p>
```

To modify:
1. Replace the text between the `<h1>` tags for the main headline
2. Update the text between the `<p>` tags for the subheading
3. Keep all classes intact to maintain responsive design

### Understanding Tailwind Classes
Common classes used in this page:
- `text-[size]`: Controls text size (e.g., `text-xl`, `text-2xl`)
- `md:text-[size]`: Applies styles at medium screen sizes
- `bg-[color]`: Sets background color
- `px-[number]`: Adds horizontal padding
- `py-[number]`: Adds vertical padding
- `mb-[number]`: Adds bottom margin

## Managing Links

### Navigation Menu Links
Current navigation links are located in the header:

```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="hover:text-blue-500 transition-colors duration-300">Features</a>
    <a href="#benefits" class="hover:text-blue-500 transition-colors duration-300">Benefits</a>
    <a href="#faq" class="hover:text-blue-500 transition-colors duration-300">FAQ</a>
    <a href="#contact" class="hover:text-blue-500 transition-colors duration-300">Contact</a>
</div>
```

To update links:
1. Locate the `href` attribute in each `<a>` tag
2. Replace the value with your new link
   - For same-page sections, use `#section-id`
   - For external links, use complete URLs (e.g., `https://example.com`)

### Call-to-Action Buttons
The main CTA button currently links to a JotForm:

```html
<a href="https://form.jotform.com/250476421727054" class="inline-block bg-blue-600 hover:bg-blue-700 px-8 py-4 rounded-full">
    Start Your Tax Journey
</a>
```

To update:
1. Replace the `href` value with your form or landing page URL
2. Update the button text between the `<a>` tags
3. Maintain all classes for consistent styling

## Adding Privacy and Terms Pages

### Footer Links
Located at the bottom of the page:

```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-blue-500 transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-blue-500 transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To link privacy and terms pages:
1. Create your privacy.html and terms.html files
2. Update the href attributes:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-blue-500 transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-blue-500 transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

Common issues and solutions:

1. **Broken Layout**
   - Check that all Tailwind classes remain intact
   - Verify the Tailwind CDN link is working
   - Ensure closing tags match opening tags

2. **Links Not Working**
   - Confirm file paths are correct
   - Check for typos in URLs
   - Verify section IDs match href values for internal links

3. **Responsive Issues**
   - Keep all `md:` and `lg:` prefixed classes
   - Test on different screen sizes
   - Don't remove the viewport meta tag

Need additional help? Contact your web developer or refer to the [Tailwind CSS documentation](https://tailwindcss.com/docs).