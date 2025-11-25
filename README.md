# Vector Animation - Interactive 2D Vector Field Visualizer

Animate your 2D vector-valued functions into cool 2D particle flow visualizations!

## 📹 Demo

**[Watch the Project Demo Video](https://www.linkedin.com/posts/umer-tariq-455b88294_gemini-ai-mathematics-activity-7399044329618575360-L-0K?utm_source=share&utm_medium=member_desktop&rcm=ACoAAEddhIEBkfsyaU_JGbF8-BR6uKav33MuAIw)** *(Video demonstration coming soon)*

**[Try it Live](https://umer-tariq77400.github.io/vector-animation)** - Experience the interactive vector field generator in action!

## 🌟 Features

### 🎨 Interactive Vector Field Generation
- **AI-Powered Generation**: Describe your desired animation in natural language and let Gemini AI generate the mathematical vector field
- **Real-time Visualization**: Watch 1500+ particles flow along your custom vector fields
- **Preset Animations**: Quick-start with 6 pre-configured patterns via dropdown menu:
  - 🌀 Central Vortex - Swirling rotational flow
  - 🌊 Complex Waves - Undulating wave patterns
  - ⚫ Central Sink - Converging attractor flow
  - 🌪️ Expanding Spiral - Outward spiral motion
  - 💨 Turbulence - Chaotic turbulent flow
  - 💫 Radial Expansion - Outward radial flow

### 🤖 AI Integration
- **Gemini AI-Powered**: Uses Google's Gemini 2.5 Flash model for intelligent field generation
- **Natural Language Input**: Simply describe what you want to see (e.g., "a swirling vortex", "flowing waves")
- **AI Explanations**: Get detailed mathematical explanations of what your vector field does and why

### 📋 Export Functionality
- **Self-Contained Export**: Export your animations as standalone HTML files
- **Multiple Export Options**:
  - Complete HTML file (ready to use immediately)
  - Separate HTML, CSS, and JavaScript files
  - Individual code sections for custom integration
- **One-Click Copy**: Copy any code section to your clipboard instantly
- **No Dependencies**: Exported animations work without any external libraries (pure JavaScript)

### 🎯 Educational Features
- **Interactive Descriptions**: Collapsible explanation of what vector fields are
- **Mathematical Visualization**: See the math come to life as particle flows
- **Real-time Equation Display**: Shows the current vector field equation being visualized

### 🎨 Customization
- **Color Customization**: 
  - Choose custom colors for particle gradient (start and end colors)
  - Customize background color with visual color pickers
  - See color codes displayed next to pickers
- **Particle Controls**:
  - Adjust particle speed with slider (0.1x to 3.0x)
  - Modify particle size with slider (1px to 5px)
  - Real-time updates as you adjust controls
- **Visual Enhancements**:
  - Beautiful particle system with customizable gradient colors
  - Smooth particle trails with configurable fade
  - Responsive canvas that adapts to any screen size
  - Dark theme UI with modern design

## 🚀 Getting Started

### Using the Live App

1. Open `vector_animation.html` in your browser
2. Try the preset animations or describe your own
3. Click "Generate New Field ✨" to create a custom animation
4. Click "Explain Current Field ✨" to understand the mathematics
5. Click "Export Animation 📋" to get the code for your project

### Exporting Your Animation

1. **Create or select** your desired animation
2. **Click** the "Export Animation 📋" button
3. **Choose** your preferred export method:
   - **Complete HTML**: Single file, ready to use
   - **Separate Files**: HTML, CSS, and JS organized separately
   - **Individual Sections**: Copy specific parts for custom integration
4. **Copy** the code using the convenient copy buttons
5. **Integrate** into your project (see [INTEGRATION.md](INTEGRATION.md) for detailed instructions)

## 📁 Project Structure

This project consists of the following files and directories:

### Main Application
- **`vector_animation.html`** - The core interactive application that allows you to create, customize, and export vector field animations. This single HTML file contains everything you need: the UI built with Tailwind CSS, the canvas-based particle system, AI integration with Google Gemini API for generating custom vector fields, and export functionality to package your animations for use in other projects.

### Documentation
- **`README.md`** (this file) - Complete project overview, feature list, and getting started guide
- **`docs/INTEGRATION.md`** - Comprehensive integration guide showing you how to use exported animations in your own websites. Covers both full-page background and component-specific background implementations with detailed examples.

### Example Files
The `examples/` directory contains three demonstration files showing different use cases:

- **`blackbg_whitetext.html`** - Example of a page background animation with a black background and white text/particles, demonstrating how to use the animation as a fixed background for a content-heavy page with good contrast.

- **`whitebg_blacktext.html`** - Example of a page background animation with a white/light background and dark particles, showing an alternative color scheme suitable for lighter-themed websites.

- **`component_animation.html`** - Comprehensive showcase demonstrating how to use vector animations as backgrounds for specific page components like hero sections, feature cards, and call-to-action blocks. This example shows multiple animated components on a single page.

### Additional Files
- **`.gitignore`** - Git configuration to exclude unnecessary files from version control

## 🛠️ Technical Details

### Technologies Used
- **HTML5 Canvas** - For rendering the particle system
- **Vanilla JavaScript** - No frameworks, pure JS
- **Tailwind CSS** - Modern, responsive UI styling (via CDN)
- **Google Gemini API** - AI-powered field generation and explanations

### How It Works
1. A vector field function `f(x,y) = P(x,y)î + Q(x,y)ĵ` defines the flow
2. Particles are spawned randomly across the canvas
3. Each particle follows the vector at its current position
4. The trail effect creates beautiful flow visualizations

### Particle System
- 1500 particles by default
- Dynamic respawning to maintain density
- Gradient coloring based on position
- Smooth motion with configurable speed

## 🎓 What is a Vector Field?

A 2D vector field is a mathematical function that assigns a vector (direction and magnitude) to every point in 2D space. It's represented as:

```
f(x,y) = P(x,y)î + Q(x,y)ĵ
```

Where:
- `P(x,y)` controls horizontal movement (x-component)
- `Q(x,y)` controls vertical movement (y-component)

In this visualizer, particles flow along the paths defined by these vectors, creating mesmerizing patterns!

## 📚 Additional Resources

For detailed integration instructions, see **[docs/INTEGRATION.md](docs/INTEGRATION.md)** which includes:
- Multiple integration methods (page background vs. component background)
- Complete code examples with copy-paste snippets
- Links to example implementations
- Customization options
- Troubleshooting tips

## 🌐 Browser Support

Works on all modern browsers:
- Chrome 60+
- Firefox 60+
- Safari 12+
- Edge 79+

## 📝 Examples

### Example Vector Fields

**Vortex (Rotation):**
```
f(x,y) = -(y - 4)î + (x - 4)ĵ
```

**Wave Pattern:**
```
f(x,y) = 2sin(y)î + 2cos(x)ĵ
```

**Central Sink:**
```
f(x,y) = -0.5(x-4)î - 0.5(y-4)ĵ
```

## 🤝 Contributing

Contributions are welcome! Feel free to:
- Report bugs
- Suggest new features
- Submit pull requests
- Share your cool vector field patterns

## 📄 License

Free to use and modify for your projects. Exported animations are yours to use however you like!

## 🎉 Have Fun!

Create beautiful mathematical art and share your creations! Each vector field tells a unique story through the dance of particles.

