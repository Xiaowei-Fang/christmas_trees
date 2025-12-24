## Project Overview

This is a Three.js-based interactive Christmas tree visualization with luxury design elements. The project features:
- A 3D Christmas tree with dynamic foliage and ornaments
- Dual-state animation system (FORMED vs CHAOS modes)
- Photo integration system allowing users to add personal photos to the tree
- Cinematic bloom effects and post-processing
- Responsive design with mobile support

## Key Commands

### Development
- `npm install` - Install dependencies
- `npm run dev` - Start development server on port 3000
- `npm run build` - Build production version
- `npm run preview` - Preview production build

### Environment Setup
1. Set the `GEMINI_API_KEY` in `.env.local` to your Gemini API key

## Architecture

### Core Technologies
- Three.js (3D graphics library)
- Vite (build tool)
- TypeScript
- Tailwind CSS (styling)
- HTML/CSS/JavaScript

### File Structure
- `index.html` - Main HTML file containing all Three.js code and UI
- `vite.config.ts` - Vite configuration
- `package.json` - Dependencies and scripts
- `tsconfig.json` - TypeScript configuration
- `dist/single-file-build.html` - Production build output

### Key Components

1. **Tree System**
   - Dynamic foliage using particle system with custom shaders
   - Instanced ornaments with physics-based animations
   - Animated ribbon/tinsel wrapped around the tree
   - Golden star topper with rotation effects

2. **Animation System**
   - Dual-state transitions between FORMED (tree shape) and CHAOS (scattered particles)
   - Smooth interpolation using lerp functions
   - Custom easing functions for natural movement

3. **Photo Integration**
   - Up to 8 photos can be added to the tree
   - Automatic positioning in predefined slots
   - Click-to-zoom functionality
   - Responsive sizing based on image aspect ratios

4. **Visual Effects**
   - Post-processing with UnrealBloomPass for glow effects
   - Custom shaders for foliage rendering
   - Dynamic lighting with multiple light sources
   - Starfield background for depth

### State Management
The application uses a central state object to manage:
- Current mode (FORMED/CHAOS)
- Animation progress
- Photo collection
- Time-based animations

### UI Components
- Mode toggle button (UNLEASH CHAOS / ASSEMBLE TREE)
- Photo management controls (+ PHOTO / - REMOVE)
- File input for photo uploads
- Photo counter display

## Development Notes

- All 3D logic is contained within the `<script type="module">` tag in index.html
- The project uses ES modules for Three.js imports via CDN
- Custom shaders are defined inline for foliage rendering
- Physics-based animations use mathematical interpolation rather than external libraries
- Mobile touch events are disabled via touch-action: none for better 3D control
