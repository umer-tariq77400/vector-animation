# Integration Guide: Vector Field Animation

This guide explains how to export and integrate the vector field animations into your own projects as backgrounds.

## 📂 Live Examples

Before diving into the integration details, check out these working examples in the `examples/` folder:

- **[blackbg_whitetext.html](../examples/blackbg_whitetext.html)** - Full-page background with dark theme and white particles
- **[whitebg_blacktext.html](../examples/whitebg_blacktext.html)** - Full-page background with light theme and dark particles  
- **[component_animation.html](../examples/component_animation.html)** - Multiple component backgrounds (hero section, cards, etc.) on a single page

You can view these examples live at:
- [Black Background Example](https://umer-tariq77400.github.io/vector-animation/examples/blackbg_whitetext.html)
- [White Background Example](https://umer-tariq77400.github.io/vector-animation/examples/whitebg_blacktext.html)
- [Component Background Example](https://umer-tariq77400.github.io/vector-animation/examples/component_animation.html)

## ⚠️ Important Limitation

**You cannot use two different animations on a single page.** Due to the technical implementation, each page can only run one vector field function at a time. However, you can use the same animation as a background for multiple components on the same page (as demonstrated in `component_animation.html`).

If you need different animations on different pages of your website, that works perfectly fine - just use a different animation on each page. The limitation only applies to having multiple *different* animations on the *same* page simultaneously.

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

**See it in action:** Check out [blackbg_whitetext.html](../examples/blackbg_whitetext.html) and [whitebg_blacktext.html](../examples/whitebg_blacktext.html) for live examples of this approach.

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

**See it in action:** Check out [component_animation.html](../examples/component_animation.html) for a complete showcase with multiple animated components on one page.

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

For a complete, styled hero section example, see [component_animation.html](../examples/component_animation.html).

Basic structure:

```html
<div class="vector-bg-container" style="min-height: 600px;">
    <canvas class="vector-bg-canvas"></canvas>
    
    <div class="vector-bg-content" style="display: flex; align-items: center; min-height: 600px; padding: 40px;">
        <div style="max-width: 1200px; margin: 0 auto; color: white;">
            <h1 style="font-size: 48px; font-weight: bold; margin-bottom: 20px;">
                Welcome to Our Amazing Product
            </h1>
            <p style="font-size: 18px; margin-bottom: 30px;">
                Experience the future with our cutting-edge solution.
            </p>
            <button style="background: #06b6d4; color: white; padding: 15px 30px; border: none; border-radius: 8px;">
                Get Started Now
            </button>
        </div>
    </div>
</div>

<script>
    // Paste the exported JavaScript code here
</script>
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
        padding: 40px;
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

<script>
    // Paste the exported JavaScript code here
</script>
```

**For more complete examples, see [component_animation.html](../examples/component_animation.html)**

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

Change the color gradient by modifying `HUE_START` and `HUE_END` (values 0-360):
Red: 0 | Orange: 30 | Yellow: 60 | Green: 120 | Cyan: 180 | Blue: 240 | Purple: 280 | Pink: 320

### Performance Tuning

- **Better performance:** Reduce `NUM_PARTICLES` (500-1000)
- **Denser animation:** Increase `NUM_PARTICLES` (2000-3000)  
- **Slower devices:** Reduce both `NUM_PARTICLES` and `PARTICLE_SPEED`

---

## Multiple Instances

### Page Background
- Only one page background animation per page
- Uses ID selector (`#vectorCanvas`)
- **Cannot have two different animations on the same page**

### Component Background
- Supports **multiple instances** on the same page
- Each component gets its own canvas with the **same animation**
- Simply add more `.vector-bg-container` elements
- The JavaScript automatically handles all instances
- **All instances use the same vector field function** - you cannot mix different animations

**Important Note:** The same animation can be used across multiple components on a page (see [component_animation.html](../examples/component_animation.html) for an example), but you cannot have different vector field animations running simultaneously. This is because all animations share the same vector field function. If you need different animations, use them on different pages of your website.

---

## Browser Compatibility

Works in all modern browsers supporting HTML5 Canvas, ES6 JavaScript, and RequestAnimationFrame API.

**Supported:** Chrome 60+, Firefox 60+, Safari 12+, Edge 79+

---

## Troubleshooting

### Animation doesn't appear
- **Page Background:** Check canvas ID (`vectorCanvas`), z-index (-1), and JS loads after DOM
- **Component Background:** Verify container class (`vector-bg-container`), canvas class (`vector-bg-canvas`), and container has min-height

### Animation is too slow
- Reduce `NUM_PARTICLES` (try 500-800) or adjust devicePixelRatio
- Ensure browser hardware acceleration is enabled

### Content not visible on top
- Content needs `position: relative` and `z-index: 1` or higher
- For page background, canvas must have `z-index: -1`
- Check text color contrasts with animation

### Animation doesn't fit the container
- Set explicit height on component container with `min-height`
- Apply `overflow: hidden` to container
- Check for conflicting CSS rules

### Multiple instances not working
- Only supported for Component Background mode
- Use class selectors (`.vector-bg-canvas`), not IDs
- Ensure consistent HTML structure across containers

---

## Tips and Best Practices

1. **Choose the right mode:** Use **Page Background** for full-page experiences, **Component Background** for sections/cards
2. **Optimize for mobile:** Consider reducing particle count on mobile devices and test performance
3. **Color coordination:** Match animation colors to your brand and ensure text readability
4. **Content readability:** Add semi-transparent overlays or use backdrop-filter for better text contrast
5. **Accessibility:** Provide sufficient color contrast and consider a "reduce motion" option

---

## Need Help?

1. Check the troubleshooting section above
2. Review the [example files](../examples/) 
3. Verify your code matches the exported format
4. Create an issue on the GitHub repository

## License

The exported animations are yours to use freely in your projects!
