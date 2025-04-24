# Armadale Landing Page Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the Armadale Accounting Services landing page. Whether you're new to web development or need a quick reference, follow these steps to make common updates safely and effectively.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the company name and navigation menu. To update:

1. **Company Name**
```html
<!-- Located in the header section -->
<a href="/" class="text-2xl font-bold bg-gradient-to-r from-purple-500 to-pink-500 bg-clip-text text-transparent">
    Armadale  <!-- Change this text -->
</a>
```

2. **Navigation Menu Items**
```html
<div class="hidden md:flex space-x-8">
    <a href="#services">Services</a>  <!-- Update text here -->
    <a href="#benefits">Benefits</a>  <!-- Update text here -->
    <a href="#contact">Contact</a>    <!-- Update text here -->
</div>
```

### Hero Section
The main headline and subheading are in the hero section:

```html
<h1 class="text-5xl md:text-6xl lg:text-7xl font-bold leading-tight">
    Building financial clarity in a complex world  <!-- Main headline -->
</h1>
<p class="text-xl md:text-2xl text-gray-300 mb-8">
    Professional accounting services tailored to your business needs  <!-- Subheading -->
</p>
```

### Styling Tips for Beginners
- The `md:` prefix means the style applies to medium-sized screens and larger
- For text sizes, larger numbers mean bigger text (e.g., `text-xl` is larger than `text-lg`)
- Color classes use this format: `text-{color}-{shade}` (e.g., `text-purple-500`)
- The `hover:` prefix adds styles when users mouse over elements

## Managing Links

### Navigation Menu Links
Current links in the navigation:
```html
<a href="#services">Services</a>
<a href="#benefits">Benefits</a>
<a href="#contact">Contact</a>
<a href="https://theaccountants.com">Get Started</a>
```

To update:
1. For internal page sections, keep the `#` symbol followed by the section ID
2. For external links, use the full URL including `https://`
3. Example:
```html
<a href="https://your-new-domain.com">Get Started</a>
```

### Footer Links
The footer contains multiple link sections. To update:

```html
<!-- Company Links -->
<ul class="space-y-2 text-gray-400">
    <li><a href="/about">About Us</a></li>
    <li><a href="/blog">Blog</a></li>
    <li><a href="/careers">Careers</a></li>
</ul>
```

Replace the href values with your actual page URLs.

## Adding Privacy and Terms Pages

### Step 1: Update Footer Links
Locate the Legal section in the footer:
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2 text-gray-400">
        <li><a href="/privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="/terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

### Step 2: Create New Pages
1. Create `privacy.html` and `terms.html` in your root directory
2. Copy the header and footer from `index.html` to maintain consistent styling
3. Add your policy content between the header and footer

### Step 3: Maintain Consistent Styling
Apply these classes to maintain consistent link styling:
```html
class="hover:text-white transition-colors duration-300"
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Links**
   - Check for typos in URLs
   - Ensure files exist in the correct directory
   - Verify that external URLs include `https://`

2. **Responsive Design Issues**
   - Keep the `md:` and `lg:` prefixed classes
   - Test on different screen sizes
   - Don't remove the viewport meta tag in the header

3. **Gradient Text Not Showing**
   - Ensure these classes stay together:
     ```html
     bg-gradient-to-r from-purple-500 to-pink-500 bg-clip-text text-transparent
     ```

### Need Help?
- Validate your HTML at [W3C Validator](https://validator.w3.org/)
- Check Tailwind CSS documentation for class references
- Test all links before deploying changes
- Keep a backup of the original file before making changes

Remember to test all changes in a development environment before pushing to production.