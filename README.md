# Houston Web Landing Page Maintenance Guide

This README provides guidance for maintaining and customizing the Houston Web landing page. It focuses on three key areas: updating text and Tailwind CSS classes, fixing broken links, and linking privacy and terms pages.

## Table of Contents

1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Updating Text Content

To update text content, locate the specific section in the HTML file and modify the text within the appropriate tags. Here are some key sections:

1. Header (Navigation):
   ```html
   <header class="bg-white shadow-md fixed top-0 left-0 right-0 z-50">
     <nav class="container mx-auto px-4 sm:px-6 lg:px-8 py-4">
       <div class="flex justify-between items-center">
         <a href="#" class="text-2xl font-bold text-blue-600">Houston Web</a>
         <!-- Navigation links -->
       </div>
     </nav>
   </header>
   ```
   To change the logo text, update "Houston Web" within the `<a>` tag.

2. Hero Section:
   ```html
   <section class="bg-gradient-to-r from-blue-500 to-blue-600 text-white py-24">
     <div class="container mx-auto px-4 sm:px-6 lg:px-8">
       <h1 class="text-4xl md:text-5xl lg:text-6xl font-bold mb-6">Best Websites In Houston</h1>
       <p class="text-xl md:text-2xl mb-8">Custom Websites For Your Business</p>
       <!-- CTA button -->
     </div>
   </section>
   ```
   Update the main heading in the `<h1>` tag and the subheading in the `<p>` tag.

3. Features Section:
   ```html
   <section id="features" class="py-24 bg-gray-50">
     <div class="container mx-auto px-4 sm:px-6 lg:px-8">
       <h2 class="text-3xl md:text-4xl font-bold mb-12 text-center">Our Features</h2>
       <!-- Feature items -->
     </div>
   </section>
   ```
   Modify the section title in the `<h2>` tag and individual feature titles and descriptions within each feature item.

### Modifying Tailwind CSS Classes

Tailwind CSS uses utility classes to style elements. Here's how to modify some key classes:

1. Changing colors:
   - Background colors use classes like `bg-blue-500`. To change, replace "blue" with another color (e.g., `bg-red-500`).
   - Text colors use classes like `text-gray-600`. Change "gray" to another color as needed.

2. Adjusting spacing:
   - Padding uses classes like `py-24` (vertical padding) or `px-4` (horizontal padding). Increase or decrease the number to adjust spacing.
   - Margins use classes like `mb-6` (margin-bottom). Modify the number to change the margin size.

3. Responsive design:
   - Classes with `md:` or `lg:` prefixes apply to medium and large screens respectively.
   - Example: `text-4xl md:text-5xl lg:text-6xl` sets font size for different screen sizes.

Remember to maintain responsiveness by keeping or adjusting these prefixed classes appropriately.

## Fixing Broken Links

To fix broken links, update the `href` attribute of `<a>` tags. Here's how to update links in different sections:

1. Navigation Menu:
   ```html
   <div class="hidden md:flex space-x-6">
     <a href="#features" class="text-gray-600 hover:text-blue-600 transition duration-300">Features</a>
     <a href="#benefits" class="text-gray-600 hover:text-blue-600 transition duration-300">Benefits</a>
     <a href="#faq" class="text-gray-600 hover:text-blue-600 transition duration-300">FAQ</a>
     <a href="#contact" class="text-gray-600 hover:text-blue-600 transition duration-300">Contact</a>
   </div>
   ```
   These are internal links. Ensure the `href` values match the `id` attributes of corresponding sections.

2. CTA Buttons:
   ```html
   <a href="https://sigmaseo.io" class="bg-white text-blue-600 py-3 px-8 rounded-full font-semibold hover:bg-blue-100 transition duration-300 transform hover:scale-105">Get Started</a>
   ```
   Replace "https://sigmaseo.io" with the correct URL for your call-to-action.

3. Logo Link:
   ```html
   <a href="#" class="text-2xl font-bold text-blue-600">Houston Web</a>
   ```
   Replace "#" with your homepage URL or desired landing page.

To ensure proper linking:
- For internal links (within the same page), use "#section-id" format.
- For external links, use the full URL including "https://".
- Double-check all URLs to ensure they're correct and functional.

## Linking Privacy and Terms Pages

To add links to privacy and terms pages:

1. Create a footer section if not already present:
   ```html
   <footer class="bg-gray-100 py-8">
     <div class="container mx-auto px-4 sm:px-6 lg:px-8">
       <!-- Footer content -->
     </div>
   </footer>
   ```

2. Add links to the footer:
   ```html
   <footer class="bg-gray-100 py-8">
     <div class="container mx-auto px-4 sm:px-6 lg:px-8">
       <div class="flex justify-center space-x-6">
         <a href="privacy.html" class="text-gray-600 hover:text-blue-600 transition duration-300">Privacy Policy</a>
         <a href="terms.html" class="text-gray-600 hover:text-blue-600 transition duration-300">Terms of Service</a>
       </div>
     </div>
   </footer>
   ```

3. Ensure you have created `privacy.html` and `terms.html` files in the same directory as your `index.html`.

4. Style consistency:
   - Use the same Tailwind CSS classes as other links for consistent styling.
   - The `hover:text-blue-600` class creates a blue color on hover, matching the existing design.

## Troubleshooting

If you encounter issues:

1. Broken layout:
   - Check for unclosed HTML tags.
   - Ensure Tailwind CSS is properly linked in the `<head>` section.

2. Links not working:
   - Verify file names and paths are correct.
   - For internal links, confirm that section IDs match the href values.

3. Styles not applying:
   - Check for typos in Tailwind class names.
   - Ensure the Tailwind CSS file is correctly linked and not blocked by browser extensions.

4. Responsive design issues:
   - Test the page at different screen sizes using browser developer tools.
   - Review and adjust responsive Tailwind classes (e.g., `md:`, `lg:` prefixes) as needed.

If problems persist, consider using browser developer tools to inspect elements and identify CSS conflicts or HTML structure issues.

Remember to test all changes thoroughly across different devices and browsers to ensure a consistent user experience.