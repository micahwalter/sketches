# Sketches

A collection of creative coding experiments, interactive tools, and visualizations built with HTML, CSS, and JavaScript.

## Overview

This repository contains a variety of self-contained web-based sketches exploring different concepts in generative art, data visualization, and interactive tools. Each sketch is a single HTML file that can be opened directly in a browser.

## Featured Sketches

### Gradient Examples
- **Color Distance Gradient** - Interactive gradient based on color distance calculations
- **Distance Gradient** - Visualize gradients using distance-based algorithms
- **Inverse Distance Gradient** - Gradient effect with inverse distance weighting

### Test Patterns
- **Sinusoidal Test Pattern** - Generate customizable sine wave test patterns with adjustable frequency and amplitude

### Architecture Diagrams
- **API Gateway to ALB** - Visualize AWS architecture connecting API Gateway to Application Load Balancer

### Calculators
- **Growth Calculator** - Calculate and visualize business growth projections over time with interactive charts

### Animations
- **Aurora Animation** - Beautiful animated aurora borealis effect

### Tools
- **Electrical Panel Manager** - Interactive tool to manage and visualize electrical circuit breaker panels with shareable state

## Running Locally

1. Clone this repository:
   ```bash
   git clone https://github.com/micahwalter/sketches.git
   cd sketches
   ```

2. Start a local web server:
   ```bash
   # Using Python 3
   python3 -m http.server 8000

   # Or using Node.js
   npx http-server
   ```

3. Open your browser to `http://localhost:8000`

Alternatively, you can open any individual HTML file directly in your browser.

## Technologies Used

- **p5.js** - Creative coding library for generative art and animations
- **React** - UI components for interactive tools
- **Chart.js** - Data visualization for calculators
- **Tailwind CSS** - Utility-first CSS framework for styling
- **Vanilla JavaScript** - For simple interactions and DOM manipulation

## Adding New Sketches

To add a new sketch:

1. Create a new HTML file in the root directory
2. Add your sketch code as a self-contained HTML file
3. Update `index.html` to include a link to your new sketch:
   - Add the link in the appropriate category section
   - Include a data-title and data-description for search functionality
   - Use the pattern: `<a href="your-sketch.html">Your Sketch Title</a>`

## License

MIT License - feel free to use and modify these sketches for your own projects.

## Author

Created by Micah Walter

---

*Browse all sketches at [index.html](index.html)*
