

## Prompt

I have intentionally added controls (H-10/...) to have more precise contril over animation stages, like "please do the same as for H-10 but for H-13 except more yelllow". .

![Halftone Inspiration](https://raw.githubusercontent.com/hutsul/Frame/main/2543.jpg)

```
Create an interactive gradient morphing demo with these requirements:

1. CANVAS SETUP
   - 277px × 311px (4:3 aspect ratio)
   - 9 vertical strips with specific widths: 23px, 33px, 33px, 33px, 33px, 33px, 33px, 33px, 23px
   - Black background (#000000)

2. GRADIENT 
 Please follow exactly the attached image.
 
Please follow for H-13 and H-16 the same pattern as H-10, but use the colors:
   - H-13: Magenta (#FF3CE2), bright oranges (#FFD699, #FFB366)
   - H-16: Light pinks (#FFB8E8, #E8A8FF), purples (#2C1947)

3. HALFTONE DITHERING EFFECT
   Apply halftone dissolve using:
   - Brightness threshold: 0.75 (colors above stay solid)
   - 3px dot grid spacing
   - Dot size based on darkness: darker = larger dots
   - Process: Check each pixel's brightness, if below threshold, calculate distance from 
     dot center and dissolve pixels outside dot radius to black

4. ANIMATION
   - Automatic cycling every 2 seconds
   - 1000ms smooth morphing between sets, "ambient effect".
   - Staggered start: 80ms delay between strips
   - Color interpolation with easeInOutCubic easing

5. TECHNICAL IMPLEMENTATION
   - Use canvas for rendering and pixel manipulation
   - Parse CSS gradients to extract color stops
   - Interpolate between current and target gradients
   - Apply halftone effect via getImageData/putImageData
   - Use performance.now() for precise timing

6. STYLING
   - Fira Code font
   - Controls with backdrop blur and white active state
   - Subtle label fade during transitions
```


