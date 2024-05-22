# Smooth Back-to-Top Button

This is a simple and customizable back-to-top button for your website. It appears as you scroll down the page and smoothly scrolls back to the top when clicked.

## Features

- Smooth scrolling animation for a better user experience.
- Customizable appearance (position, color, icon, etc.).
- Easy to integrate into any website using HTML, CSS, and JavaScript.

## Demo

You can see a live demo of this button in action here: [https://leartme.com] and [https://www.blockchainlegals.com/]

## How to Use

1. **HTML:** Copy the following code and paste it into your HTML (preferably before the closing `</body>` tag):

```html
<button id="backToTopBtn" class="back-to-top-btn">
  <span class="arrow-up"></span> 
</button>
```
**Note:** if you are using Elementor, add an Element like an icon or icon box then use custom css and an HTML widget

2. **CSS:** Add this CSS to your stylesheet or using a `<style>` tag in your HTML:

```css
/* Initial state: hidden and below its normal position */
.your-sticky-icon {
  opacity: 0;
  transform: translateY(20px); /* Adjust the distance as needed */
  transition: opacity 1.0s ease-in-out, transform 0.5s ease-in-out; 
  position: fixed;
  bottom: 20px;
  right: 20px;
  cursor: pointer;
}

/* Trigger animation after scrolling a bit */
.your-sticky-icon.show {
  opacity: 1;
  transform: translateY(0);
}
```
3. **Javascript:** Add this JavaScript code to a `<script>` tag in your HTML:
```javascrip
window.addEventListener('scroll', function() {
  var stickyIcon = document.querySelector('.your-sticky-icon');
  if (window.scrollY > 1000) { // Adjust the scroll threshold as needed
    stickyIcon.classList.add('show');
  } else {
    stickyIcon.classList.remove('show');
  }
});

// Handle click event for smooth scrolling
document.querySelector('.your-sticky-icon').addEventListener('click', function() {
  window.scrollTo({
    top: 0,
    behavior: 'smooth' 
  });
});
```


