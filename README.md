# Essendon Accounting Landing Page - Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the Essendon Accounting landing page. Whether you're new to web development or need a quick reference, follow these steps to make common updates safely and effectively.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the company logo and navigation menu. To update:

1. **Company Logo**
```html
<!-- Find this section in the header -->
<a href="/" class="text-2xl font-bold text-white hover:text-blue-400 transition-colors duration-300">
    Essendon<span class="text-blue-500">.</span>
</a>
```
- Replace "Essendon" with your company name
- The blue dot can be removed by deleting the `<span>` element

2. **Navigation Menu Items**
```html
<div class="hidden md:flex space-x-8">
    <a href="#services" class="text-gray-300 hover:text-white transition-colors duration-300">Services</a>
    <a href="#benefits" class="text-gray-300 hover:text-white transition-colors duration-300">Benefits</a>
    <a href="#contact" class="text-gray-300 hover:text-white transition-colors duration-300">Contact</a>
</div>
```
- Change text between `<a>` tags to update menu items
- Keep the `class` attributes unchanged to maintain styling

### Hero Section
Located at the top of the page:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight tracking-tight mb-6">
    Essendon accounting services
</h1>
<p class="text-xl md:text-2xl text-gray-400 mb-8 leading-relaxed">
    Trusted advisors for your financial future
</p>
```
- Update heading text between `<h1>` tags
- Modify subheading text between `<p>` tags
- The responsive text sizes (`text-4xl`, `md:text-5xl`, `lg:text-6xl`) ensure proper scaling on different devices

### Understanding Tailwind Classes
Common classes used in this page:
- `text-{size}`: Controls text size (xl, 2xl, 4xl, etc.)
- `bg-{color}-{shade}`: Sets background color
- `p-{number}`: Sets padding
- `m-{number}`: Sets margin
- `rounded-{size}`: Controls border radius

Example:
```html
<!-- Original button -->
<a href="#" class="bg-blue-600 text-white px-8 py-4 rounded-full">
    Start Your Journey
</a>

<!-- To modify styling -->
<a href="#" class="bg-green-600 text-white px-6 py-3 rounded-lg">
    Start Your Journey
</a>
```

## Fixing Broken Links

### Navigation Links
Current placeholder links that need updating:
```html
<!-- Main navigation -->
<a href="https://theaccountants.com" class="bg-blue-600 text-white px-6 py-2 rounded-full">
    Get Started
</a>

<!-- Contact section -->
<a href="mailto:support@example.com" class="text-lg text-blue-400">
    support@example.com
</a>
```

To update:
1. Replace `https://theaccountants.com` with your actual website URL
2. Change `support@example.com` to your actual email address

### Footer Links
The footer contains multiple sections of links:
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Services</h4>
    <ul class="space-y-2 text-gray-400">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Tax Optimization</a></li>
        <!-- More links -->
    </ul>
</div>
```

To update:
1. Replace `href="#"` with actual page URLs
2. For internal links, use format: `href="#section-id"`
3. For external links, use complete URLs: `href="https://example.com/page"`

## Linking Privacy and Terms Pages

### Adding Privacy and Terms Links
Locate the legal section in the footer:
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2 text-gray-400">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To link to privacy and terms pages:
1. Create privacy.html and terms.html in your root directory
2. Update the href attributes:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

Common issues and solutions:

1. **Broken Responsive Design**
- If elements look wrong on mobile, check for `md:` prefixed classes
- Ensure you haven't removed any responsive class variations

2. **Missing Styles**
- Verify the Tailwind CDN link is present in the head section
- Check for typos in class names

3. **Links Not Working**
- Ensure IDs match exactly for internal links (e.g., `href="#services"` needs matching `id="services"`)
- Test all URLs in a private browser window

For additional help, refer to:
- [Tailwind CSS Documentation](https://tailwindcss.com/docs)
- [HTML Links Guide](https://www.w3schools.com/html/html_links.asp)