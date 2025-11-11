# Integration Guide: Vector Field Animation

This guide explains how to export and integrate the vector field animations into your own projects as backgrounds.

## Export Options

The Vector Field Generator now offers **two export modes** to suit different use cases:

1. **Page Background** - Use the animation as a full-page fixed background
2. **Component Background** - Use the animation as a background for specific components (hero sections, cards, etc.)

## Quick Start

1. **Create or customize your animation** in the Vector Field Generator app
2. **Click the "Export Animation 📋" button**
3. **Choose your export mode** (Page Background or Component Background)
4. **Copy the HTML, CSS, and JavaScript code** provided
5. **Integrate into your project** following the instructions below

---

## Option 1: Page Background

Use this option when you want a **fixed, full-page background** that stays in place behind all your page content as users scroll.

### How it Works

- The canvas uses `position: fixed` with `z-index: -1` to stay behind all content
- It covers the entire viewport (100% width and height)
- The animation doesn't scroll with the page
- Your page content appears on top automatically

### Integration Steps

#### Step 1: Add the HTML

Add the canvas element anywhere in your `<body>` tag (typically right after the opening `<body>` tag):

```html
<canvas id="vectorCanvas"></canvas>
```

#### Step 2: Add the CSS

Add this CSS to your stylesheet or in a `<style>` tag in your `<head>`:

```css
/* Vector Animation - Page Background */
#vectorCanvas {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    z-index: -1;
    display: block;
}

/* Optional: Ensure body doesn't have overflow issues */
body {
    margin: 0;
    padding: 0;
}
```

#### Step 3: Add the JavaScript

Add the exported JavaScript code in a `<script>` tag before the closing `</body>` tag or in a separate `.js` file:

```html
<script>
    // Paste the exported JavaScript code here
</script>
```

### Complete Example

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Page with Animated Background</title>
    <style>
        /* Vector Animation - Page Background */
        #vectorCanvas {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: -1;
            display: block;
        }
        
        body {
            margin: 0;
            padding: 0;
            font-family: Arial, sans-serif;
        }
        
        .content {
            padding: 50px;
            color: white;
            max-width: 1200px;
            margin: 0 auto;
        }
    </style>
</head>
<body>
    <!-- Background Animation Canvas -->
    <canvas id="vectorCanvas"></canvas>
    
    <!-- Your Page Content -->
    <div class="content">
        <h1>Welcome to My Website</h1>
        <p>This content appears on top of the animated background.</p>
        <p>The background stays fixed as you scroll.</p>
        
        <!-- Add more content here -->
    </div>
    
    <script>
        // Paste the exported JavaScript code here
    </script>
</body>
</html>
```

---

## Option 2: Component Background

Use this option when you want the animation as a **background for specific components** like hero sections, cards, jumbotrons, or any container element.

### How it Works

- The animation is contained within a specific container
- Uses relative/absolute positioning
- Your content stays on top within the same container
- Perfect for hero sections, cards, and feature blocks
- The animation respects the component's boundaries

### Integration Steps

#### Step 1: Add the HTML Structure

Wrap your component content in the provided HTML structure:

```html
<div class="vector-bg-container">
    <!-- The canvas for the animation background -->
    <canvas class="vector-bg-canvas"></canvas>
    
    <!-- Your component content goes here -->
    <div class="vector-bg-content">
        <!-- Add your content (text, images, buttons, etc.) -->
        <h1>Your Content Here</h1>
        <p>This content appears on top of the animation.</p>
    </div>
</div>
```

#### Step 2: Add the CSS

Add this CSS to your stylesheet:

```css
/* Vector Animation - Component Background */
.vector-bg-container {
    position: relative;
    width: 100%;
    min-height: 400px; /* Adjust as needed */
    overflow: hidden;
}

.vector-bg-canvas {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    display: block;
}

.vector-bg-content {
    position: relative;
    z-index: 1;
    /* Add padding/styling for your content */
    padding: 40px;
}
```

#### Step 3: Add the JavaScript

Add the exported JavaScript code. Unlike page background, this code supports **multiple instances** on the same page:

```html
<script>
    // Paste the exported JavaScript code here
</script>
```

### Example: Hero Section

Here's a complete example of a hero section with the animation as a background:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Hero Section with Animation</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: Arial, sans-serif;
        }
        
        /* Vector Animation - Component Background */
        .vector-bg-container {
            position: relative;
            width: 100%;
            min-height: 600px;
            overflow: hidden;
            background-color: #111827; /* Fallback color */
        }

        .vector-bg-canvas {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            display: block;
        }

        .vector-bg-content {
            position: relative;
            z-index: 1;
            display: flex;
            align-items: center;
            min-height: 600px;
            padding: 40px;
        }
        
        /* Hero Section Styling */
        .hero-inner {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            gap: 40px;
            align-items: center;
            width: 100%;
        }
        
        .hero-text {
            flex: 1;
            color: white;
        }
        
        .hero-text h1 {
            font-size: 48px;
            font-weight: bold;
            margin-bottom: 20px;
        }
        
        .hero-text p {
            font-size: 18px;
            margin-bottom: 30px;
            opacity: 0.9;
        }
        
        .hero-cta {
            background: #06b6d4;
            color: white;
            padding: 15px 30px;
            border: none;
            border-radius: 8px;
            font-size: 16px;
            font-weight: bold;
            cursor: pointer;
            transition: background 0.3s;
        }
        
        .hero-cta:hover {
            background: #0891b2;
        }
        
        .hero-visual {
            flex: 1;
        }
        
        .placeholder {
            background: rgba(255,255,255,0.1);
            border-radius: 12px;
            padding: 60px;
            text-align: center;
            backdrop-filter: blur(10px);
            color: white;
        }
        
        /* Regular content section */
        .content-section {
            padding: 80px 40px;
            max-width: 1200px;
            margin: 0 auto;
        }
    </style>
</head>
<body>
    <!-- Hero Section with Vector Animation Background -->
    <div class="vector-bg-container">
        <canvas class="vector-bg-canvas"></canvas>
        
        <div class="vector-bg-content">
            <div class="hero-inner">
                <!-- Left side: Text and CTA -->
                <div class="hero-text">
                    <h1>Welcome to Our Amazing Product</h1>
                    <p>Experience the future with our cutting-edge solution that transforms the way you work.</p>
                    <button class="hero-cta">Get Started Now</button>
                </div>
                
                <!-- Right side: Visual element -->
                <div class="hero-visual">
                    <div class="placeholder">
                        <p>Your Image or Video Here</p>
                    </div>
                </div>
            </div>
        </div>
    </div>
    
    <!-- Regular page content -->
    <div class="content-section">
        <h2>More Content Below</h2>
        <p>This is regular page content that appears below the hero section.</p>
    </div>
    
    <script>
        // Paste the exported JavaScript code here
    </script>
</body>
</html>
```

### Example: Card with Animation Background

```html
<style>
    .card {
        width: 400px;
        border-radius: 12px;
        overflow: hidden;
        box-shadow: 0 4px 6px rgba(0,0,0,0.1);
    }
    
    .vector-bg-container.card-bg {
        min-height: 300px;
        background-color: #1f2937;
    }
    
    .card-content {
        text-align: center;
        color: white;
    }
    
    .card-content h3 {
        font-size: 24px;
        margin-bottom: 10px;
    }
</style>

<div class="card">
    <div class="vector-bg-container card-bg">
        <canvas class="vector-bg-canvas"></canvas>
        
        <div class="vector-bg-content card-content">
            <h3>Feature Card</h3>
            <p>Beautiful animated background for your card component.</p>
        </div>
    </div>
</div>
```

---

## Customization Options

You can customize the animation by modifying these constants in the exported JavaScript code:

```javascript
const NUM_PARTICLES = 1500;      // Number of particles (more = denser, but slower)
const PARTICLE_SPEED = 1;        // Speed multiplier (higher = faster)
const PARTICLE_SIZE = 1;         // Size of each particle in pixels
const FIELD_SCALE = 8;           // Scale of the mathematical field
const FADE_OPACITY = 0.05;       // Trail fade speed (lower = longer trails)
const HUE_START = 180;           // Starting color hue (0-360)
const HUE_END = 240;             // Ending color hue (0-360)
const BG_COLOR_R = 17;           // Background color - Red component (0-255)
const BG_COLOR_G = 24;           // Background color - Green component (0-255)
const BG_COLOR_B = 39;           // Background color - Blue component (0-255)
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

### Performance Tuning

- **For better performance:** Reduce `NUM_PARTICLES` (e.g., 500-1000)
- **For denser animation:** Increase `NUM_PARTICLES` (e.g., 2000-3000)
- **For slower devices:** Reduce both `NUM_PARTICLES` and `PARTICLE_SPEED`

---

## Multiple Instances

### Page Background
- Only one page background animation per page
- Uses ID selector (`#vectorCanvas`)

### Component Background
- Supports **multiple instances** on the same page
- Each component gets its own animation
- Simply add more `.vector-bg-container` elements
- The JavaScript automatically handles all instances

Example with multiple components:

```html
<!-- Hero Section -->
<div class="vector-bg-container">
    <canvas class="vector-bg-canvas"></canvas>
    <div class="vector-bg-content">
        <h1>Hero Section</h1>
    </div>
</div>

<!-- Features Section -->
<div class="content">
    <h2>Some regular content</h2>
</div>

<!-- Another Animated Section -->
<div class="vector-bg-container">
    <canvas class="vector-bg-canvas"></canvas>
    <div class="vector-bg-content">
        <h2>Another Animated Section</h2>
    </div>
</div>
```

---

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

---

## Troubleshooting

### Animation doesn't appear

**For Page Background:**
- Make sure the canvas has the correct ID (`id="vectorCanvas"`)
- Check that the JavaScript is loaded after the DOM is ready
- Verify the z-index is negative (`z-index: -1`)

**For Component Background:**
- Ensure the container has the class `vector-bg-container`
- Verify the canvas has the class `vector-bg-canvas`
- Check that the container has a height (set `min-height`)

### Animation is too slow
- Reduce `NUM_PARTICLES` (try 500-800)
- Reduce canvas resolution by adjusting devicePixelRatio
- Check if hardware acceleration is enabled in your browser

### Content not visible on top
- Ensure content has `position: relative` and `z-index: 1` or higher
- For page background, verify the canvas has `z-index: -1`
- Check that your text color contrasts with the animation

### Animation doesn't fit the container
- For component background, ensure the container has an explicit height
- Check that `overflow: hidden` is applied to the container
- Verify there are no conflicting CSS rules

### Multiple instances not working
- This is only supported for Component Background mode
- Ensure you're using class selectors (`.vector-bg-canvas`), not IDs
- Make sure each container follows the same HTML structure

---

## Tips and Best Practices

1. **Choose the right mode:**
   - Use **Page Background** for full-page experiences
   - Use **Component Background** for sections, cards, and hero areas

2. **Optimize for mobile:**
   - Consider reducing particle count on mobile devices
   - Test performance on various devices

3. **Color coordination:**
   - Match the animation colors to your brand palette
   - Ensure text remains readable against the animation

4. **Content readability:**
   - Consider adding a semi-transparent overlay for better text readability
   - Use backdrop-filter for modern browsers

5. **Accessibility:**
   - Provide sufficient color contrast for text
   - Consider adding a "reduce motion" option for users with motion sensitivity

---

## Need Help?

If you encounter any issues or have questions:
1. Check the troubleshooting section above
2. Review the complete examples provided
3. Verify your code matches the exported format
4. Create an issue on the GitHub repository

## License

The exported animations are yours to use freely in your projects!
