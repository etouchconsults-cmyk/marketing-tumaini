# Tumaini Cyber - Animated Business Card

An HTML5 Canvas animation that brings the Tumaini Cyber brand identity to life. This animation recreates the detailed storyboard sequence: orbital rings assembly, lettermark composition, and complete business card reveal.

## Features

✨ **Dynamic Animations:**
- Orbital rings sweeping into position
- Lettermark (T and C) assembly with elastic easing
- Pulse light effect on assembly
- Logo rise and wordmark appearance
- Cascading contact details
- Continuous orbital rotation in background

🎨 **Brand Colors:**
- Navy gradient background (#0f1b3c to #1a2d5c)
- Blue orbital rings and lettermarks (#3399ff, #0066cc)
- Red accent orbital and lettermarks (#cc0000)
- Grey tagline text (#999999)
- Professional, modern color scheme

🎬 **Playback Controls:**
- Play / Pause functionality
- Reset animation to start
- Download as video file (WebM format)

## Quick Start

### Option 1: View in Browser
1. Open `animations/business-card.html` in any modern web browser
2. Animation plays automatically in a 1920x1080px canvas

### Option 2: Browser Support
Works on:
- Chrome/Edge (recommended for video export)
- Firefox
- Safari 14.1+
- Opera

## Controls

| Button | Function |
|--------|----------|
| **▶ Play** | Start/resume animation |
| **⏸ Pause** | Pause at current frame |
| **↻ Reset** | Jump back to frame 0 |
| **⬇ Download Video** | Export animation as WebM video (10 seconds) |

## Animation Timeline

| Phase | Duration | Description |
|-------|----------|-------------|
| Blue Orbital | 0-1s | Outer blue ring sweeps in from left |
| Red Orbital | 0.75-1.75s | Red ring sweeps from opposite direction |
| T Drop | 1.5-2.5s | T lettermark slides in from above |
| C Rotate | 2s-3s | C lettermark rotates in from below-right |
| Pulse | 2.83-3.33s | Light pulse effect at center |
| Logo Rise | 3.33-5s | Complete logo rises upward |
| Wordmark | 4.17-5.33s | "Tumaini Cyber" text appears |
| Tagline | 5-6s | "Perfect prints Guaranteed" fades in |
| Contact Details | 5.83-8s | Phone, email, website, LinkedIn cascade |
| Idle | 8-10s | Final frame with voiceover callout |

## Technical Specifications

- **Resolution:** 1920x1080px (Full HD)
- **Frame Rate:** 60fps
- **Duration:** 10 seconds (600 frames total)
- **Canvas Rendering:** HTML5 2D Context
- **Animation Loop:** Continuous (restarts after 10s)
- **Export Format:** WebM video

## File Structure

```
animations/
├── business-card.html   # Main HTML with canvas and controls
├── animation.js         # Core animation engine (~500 lines)
└── README.md           # This documentation
```

## Customization

### Colors
Edit the `colors` object in `animation.js`:
```javascript
this.colors = {
    darkBlue: '#0f1b3c',
    blue: '#0066cc',
    lightBlue: '#3399ff',
    red: '#cc0000',
    grey: '#999999',
    white: '#ffffff',
};
```

### Timeline
Adjust frame timing in the `timeline` object:
```javascript
this.timeline = {
    blueOrbital: { start: 0, end: 60 },      // 1 second
    redOrbital: { start: 45, end: 105 },     // 1 second (overlapping)
    // ... edit other phases
};
```

### Font & Text
Modify font sizes in the `animate()` method:
- Wordmark font: 120px (default)
- Tagline font: 60px (default)
- Contact details: 45px (default)

### Duration
Change total animation length:
```javascript
this.totalFrames = 600; // 10 seconds at 60fps
// Change to 300 for 5 seconds, 900 for 15 seconds, etc.
```

## Browser Compatibility

| Browser | Support | Video Export |
|---------|---------|--------------|
| Chrome 76+ | ✅ Full | ✅ Yes |
| Firefox 29+ | ✅ Full | ✅ Yes |
| Safari 14.1+ | ✅ Full | ⚠️ Limited |
| Edge 79+ | ✅ Full | ✅ Yes |
| Opera 63+ | ✅ Full | ✅ Yes |

## Animation Classes & Methods

**TumainiAnimation**
- `drawGradientBackground()` - Navy gradient fill
- `drawOrbitalRing()` - Render complete rotating rings
- `drawBlueOrbitalArc()` - Sweep blue orbital from left
- `drawRedOrbitalArc()` - Sweep red orbital from right
- `drawLetterT()` - Render T lettermark
- `drawLetterC()` - Render C lettermark with rotation
- `drawText()` - Render text with opacity/easing
- `easeInOutCubic()` - Smooth cubic easing function
- `easeOutElastic()` - Bouncy elastic easing function
- `animate()` - Main render loop
- `play()`, `pause()`, `reset()` - Playback controls
- `recordVideo()` - Export as video file

## Notes

- Animation loops continuously when in play mode
- All animations use professional easing functions (cubic, elastic)
- Background orbital rings rotate throughout entire sequence
- Video export records at 60fps with high bitrate (8.5Mbps)
- Contact details cascade with 35-frame delays
- Lettermarks use overlapping animations for organic assembly

## Troubleshooting

**Video doesn't download:**
- Ensure browser supports MediaRecorder API
- Try Chrome, Firefox, or Edge
- Check browser console for errors

**Animation stutters:**
- Close other tabs/applications
- Check system CPU usage
- Try a different browser

**Colors look wrong:**
- Check display color profile
- Colors calibrated for dark navy (#0f1b3c) background

## Contact

**Tumaini Cyber**
- 📱 Phone: +254 759607619
- 📧 Email: info@tumainicyber.com
- 🌐 Website: TumainiCyber.com
- 💼 LinkedIn: Tumaini Cyber

---

**Perfect prints Guaranteed** 🎨

Created with HTML5 Canvas Animation