# Vector Animation - Interactive 2D Vector Field Visualizer

Animate your 2D vector-valued functions into cool 2D particle flow visualizations!

## 🌟 Features

### 🎨 Interactive Vector Field Generation
- **AI-Powered Generation**: Describe your desired animation in natural language and let Gemini AI generate the mathematical vector field
- **Real-time Visualization**: Watch 1500+ particles flow along your custom vector fields
- **Preset Animations**: Quick-start with pre-configured patterns:
  - 🌀 Central Vortex - Swirling rotational flow
  - 🌊 Complex Waves - Undulating wave patterns
  - ⚫ Central Sink - Converging attractor flow

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
- Beautiful particle system with gradient colors (cyan to blue)
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

## 📚 Documentation

- **[INTEGRATION.md](INTEGRATION.md)** - Complete guide for integrating animations into your projects
  - Multiple integration methods
  - Customization options
  - Code examples
  - Troubleshooting tips

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

