# Integration Guide: Vector Field Animation

This guide explains how to export and integrate the vector field animations into your own projects.

## Quick Start

1. **Create your animation** in the Vector Field Generator app
2. **Click the "Export Animation 📋" button**
3. **Choose your integration method** (see below)
4. **Copy and paste** the code into your project

## Integration Methods

### Method 1: Complete HTML File (Easiest)

This is the simplest method - you get a complete, standalone HTML file that you can use immediately.

**Steps:**
1. Click the **"Export Animation 📋"** button in the app
2. Scroll to the **"Complete HTML File"** section
3. Click **"Copy Complete"**
4. Create a new file (e.g., `animation.html`) in your project
5. Paste the copied code
6. Open the HTML file in your browser

**That's it!** The animation will work immediately with no additional dependencies.

### Method 2: Separate HTML, CSS, and JS Files

If you want to organize your code into separate files, follow these steps:

#### Step 1: Create the HTML file

Create an `index.html` file with this structure:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Vector Field Animation</title>
    <link rel="stylesheet" href="animation.css">
</head>
<body>
    <!-- Paste the exported HTML code here -->
    <canvas id="vectorCanvas"></canvas>
    
    <script src="animation.js"></script>
</body>
</html>
```

#### Step 2: Create the CSS file

Create an `animation.css` file and paste the exported CSS code:

1. Click **"Copy CSS"** in the export modal
2. Create `animation.css`
3. Paste the copied CSS

#### Step 3: Create the JavaScript file

Create an `animation.js` file and paste the exported JavaScript code:

1. Click **"Copy JS"** in the export modal
2. Create `animation.js`
3. Paste the copied JavaScript

### Method 3: Embed in Existing HTML Page

If you want to add the animation to an existing page:

#### Step 1: Add the HTML

In your existing HTML file, add the canvas element where you want the animation:

```html
<div class="animation-container">
    <canvas id="vectorCanvas"></canvas>
</div>
```

#### Step 2: Add the CSS

Add the exported CSS to your existing stylesheet or in a `<style>` tag:

```html
<style>
    /* Your existing styles */
    
    /* Vector Animation Styles */
    .animation-container {
        width: 100%;
        height: 500px; /* Adjust as needed */
        position: relative;
    }
    
    /* Paste the exported CSS here */
</style>
```

#### Step 3: Add the JavaScript

Add the exported JavaScript in a `<script>` tag before the closing `</body>` tag:

```html
<script>
    // Paste the exported JavaScript here
</script>
```

## Customization Options

You can customize the animation by modifying these constants in the JavaScript code:

```javascript
const NUM_PARTICLES = 1500;      // Number of particles (more = denser, but slower)
const PARTICLE_SPEED = 1;        // Speed multiplier (higher = faster)
const FIELD_SCALE = 8;           // Scale of the mathematical field
const FADE_OPACITY = 0.05;       // Trail fade speed (lower = longer trails)
const HUE_START = 180;           // Starting color hue (0-360)
const HUE_END = 240;             // Ending color hue (0-360)
```

### Color Customization

Change the color gradient by modifying `HUE_START` and `HUE_END`:
- Red: 0
- Orange: 30
- Yellow: 60
- Green: 120
- Cyan: 180
- Blue: 240
- Purple: 280
- Pink: 320

### Size and Performance

- **For better performance:** Reduce `NUM_PARTICLES` (e.g., 500-1000)
- **For denser animation:** Increase `NUM_PARTICLES` (e.g., 2000-3000)
- **For specific canvas size:** Modify the CSS for the canvas element

## Browser Compatibility

The animation works in all modern browsers that support:
- HTML5 Canvas
- ES6 JavaScript
- RequestAnimationFrame API

**Supported browsers:**
- Chrome 60+
- Firefox 60+
- Safari 12+
- Edge 79+

## Troubleshooting

### Animation doesn't appear
- Make sure the canvas element has a visible size (width and height)
- Check the browser console for JavaScript errors
- Ensure the JavaScript is loaded after the DOM is ready

### Animation is too slow
- Reduce `NUM_PARTICLES`
- Reduce canvas resolution
- Check if hardware acceleration is enabled in your browser

### Colors look different
- Different displays may show colors differently
- Adjust `HUE_START` and `HUE_END` values to your preference

### Canvas is blank
- Check that the canvas has the correct ID (`vectorCanvas`)
- Ensure the JavaScript is running (check for errors in console)
- Verify the background color isn't hiding the particles

## Examples

### Full-screen Background Animation

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Page with Vector Animation</title>
    <style>
        /* Vector animation as full-screen background */
        #vectorCanvas {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: -1;
        }
        
        /* Your content on top */
        .content {
            position: relative;
            z-index: 1;
            padding: 50px;
            color: white;
        }
    </style>
</head>
<body>
    <canvas id="vectorCanvas"></canvas>
    
    <div class="content">
        <h1>Welcome to My Page</h1>
        <p>The vector field animation is in the background!</p>
    </div>
    
    <script>
        // Paste exported JavaScript here
    </script>
</body>
</html>
```

### Card/Section Animation

```html
<style>
    .animation-card {
        width: 600px;
        height: 400px;
        border-radius: 12px;
        overflow: hidden;
        box-shadow: 0 4px 6px rgba(0,0,0,0.1);
    }
</style>

<div class="animation-card">
    <canvas id="vectorCanvas"></canvas>
</div>
```

## Need Help?

If you encounter any issues or have questions:
1. Check the troubleshooting section above
2. Review the exported code for any modifications you made
3. Create an issue on the GitHub repository

## License

The exported animations are yours to use freely in your projects!
