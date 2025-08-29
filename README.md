# Landing Page Maintenance Guide

This guide will help you maintain and customize your landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates safely and effectively.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Text Content Updates

The landing page contains several key sections where you might need to update text:

1. **Header (Logo and Navigation)**
```html
<!-- Find this near the top of the page -->
<a href="#" class="text-2xl font-bold">Logo</a>
```
To change the logo text, simply replace "Logo" with your company name.

2. **Hero Section**
```html
<h1 class="text-4xl sm:text-5xl lg:text-6xl font-extrabold">Lorem ipsum dolor</h1>
<p class="text-xl sm:text-2xl text-gray-600">Lorem ipsum dolor</p>
```
Replace both instances of "Lorem ipsum dolor" with your actual headline and subheading.

3. **Features Section**
```html
<h3 class="text-xl font-semibold mb-4">Lorem ipsum dolor</h3>
<p class="text-gray-600">Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
```
Update each feature card's heading and description text.

### Tailwind CSS Classes Explained

Key styling classes used in this landing page:

1. **Responsive Text Sizes**
- `text-4xl sm:text-5xl lg:text-6xl`: Text starts at extra large (4xl) on mobile, increases at small (sm) and large (lg) breakpoints
- To make text smaller/larger, adjust the number (e.g., `text-3xl` for smaller, `text-5xl` for larger)

2. **Colors**
```html
<!-- Example of gradient background -->
<div class="bg-gradient-to-r from-purple-600 to-pink-600">
```
To change colors:
- Replace `purple-600` with colors like `blue-600`, `green-600`, etc.
- Numbers range from 50-900 (lighter to darker)

3. **Spacing**
- `px-4`: Adds horizontal padding (left/right)
- `py-4`: Adds vertical padding (top/bottom)
- `mb-4`: Adds margin bottom
- Numbers range from 1-16, representing 0.25rem to 4rem

## Managing Links

### Navigation Menu Links

Current navigation links:
```html
<div class="hidden md:flex items-center space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#contact">Contact Us</a>
</div>
```

To update internal links:
1. Identify the section ID you want to link to
2. Update the `href` attribute with `#` followed by the section ID
3. Example: `<a href="#new-section">New Section</a>`

To add external links:
1. Replace the `#` with your full URL
2. Example: `<a href="https://yourwebsite.com/page">Page</a>`

### Footer Links

Current footer links structure:
```html
<div class="grid grid-cols-1 md:grid-cols-4 gap-8">
    <!-- Company Links -->
    <ul class="space-y-2">
        <li><a href="#">About</a></li>
        <li><a href="#">Careers</a></li>
    </ul>
    <!-- Legal Links -->
    <ul class="space-y-2">
        <li><a href="#">Privacy</a></li>
        <li><a href="#">Terms</a></li>
    </ul>
</div>
```

To update footer links:
1. Locate the appropriate section (Company, Legal, or Social)
2. Replace the `#` with your desired URL
3. Update the link text as needed

## Adding Privacy and Terms Pages

### Step 1: Create New Pages
1. Create two new files in your website directory:
   - `privacy.html`
   - `terms.html`

### Step 2: Update Footer Links
```html
<!-- Find this in the footer section -->
<div>
    <h4 class="text-sm font-semibold text-gray-900 uppercase mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="privacy.html" class="text-gray-600 hover:text-gray-900">Privacy Policy</a></li>
        <li><a href="terms.html" class="text-gray-600 hover:text-gray-900">Terms of Service</a></li>
    </ul>
</div>
```

### Step 3: Maintain Consistent Styling
Copy these classes to maintain consistent link styling:
```html
class="text-gray-600 hover:text-gray-900 transition-colors duration-300"
```

## Troubleshooting

Common issues and solutions:

1. **Links Not Working**
- Verify file names match exactly (case-sensitive)
- Ensure files are in the correct directory
- Check for typos in `href` attributes

2. **Styling Issues**
- Make sure Tailwind CSS is properly linked
- Check for missing closing tags
- Verify class names are spelled correctly

3. **Responsive Design Problems**
- Test at different screen sizes
- Ensure responsive classes (sm:, md:, lg:) are properly ordered
- Check for conflicting classes

Need more help? Consult the [Tailwind CSS documentation](https://tailwindcss.com/docs) or reach out to your development team.