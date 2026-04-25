# Grunge/Distressed Style Prompt Guide

## Based on Your Project's Noir Texture Mode

Your bodycam FPS game already implements excellent grunge/distressed effects through CSS overlays. Here's a comprehensive guide for creating AI-generated assets that match your game's aesthetic.

## Core Prompt Keywords

### ✅ **USE THESE** (Distressed/Worn Effects):
- `distressed texture`
- `grunge overlay`
- `scratched surface`
- `eroded edges`
- `worn out`
- `texture damage`
- `weathered`
- `faded`
- `chipped`
- `torn paper`
- `dirty`
- `aged`
- `cracked surface`
- `corroded`
- `rust`
- `water stains`
- `dust`

### ❌ **AVOID THESE** (Not True Distressing):
- `noise` (unless you want pure grain)
- `film grain` (separate from surface wear)
- `blur`
- `low contrast`
- `smooth`
- `clean vector`
- `realistic photo`
- `3d render`
- `extra noise`

## Ready-Made Prompts

### 1. **For Game Posters/Key Art**
```
distressed texture, grunge overlay, scratched surface, eroded edges, worn out, texture damage, weathered, faded, chipped, torn paper, dirty, aged, high contrast monochrome, bodycam footage aesthetic

negative prompt: color, blur, low contrast, smooth, clean vector, realistic photo, 3d render, extra noise, film grain
```

### 2. **For Logo/Title Treatment**
```
distressed texture, grunge overlay, scratched metal, eroded edges, worn out, rust, corrosion, weathered paint, chipped, cracked surface, aged metal, industrial decay

negative prompt: color, blur, low contrast, smooth, clean vector, realistic photo, 3d render, extra noise, film grain, perfect edges
```

### 3. **For UI Elements/Backgrounds**
```
distressed texture, grunge overlay, scratched surface, eroded edges, worn out, texture damage, faded, dirty, aged paper, water stains, dust particles, subtle wear patterns

negative prompt: color, blur, low contrast, smooth, clean vector, realistic photo, 3d render, extra noise, film grain, vibrant colors
```

### 4. **For Character/Weapon Textures**
```
distressed texture, grunge overlay, scratched metal, worn leather, eroded edges, battle damage, weathered, dirty, aged, rust spots, chipped paint, use wear

negative prompt: color, blur, low contrast, smooth, clean vector, realistic photo, 3d render, extra noise, film grain, pristine condition
```

## Implementation in Your Project

Your current implementation uses multiple CSS layers to achieve the distressed effect:

### **Menu.html Implementation:**
```css
/* Base film grain */
url('data:image/svg+xml,<svg>...</svg>')

/* Scratched surface effect */
repeating-linear-gradient(45deg, transparent 0px, transparent 2px, rgba(255,255,255,0.01) 2px, rgba(255,255,255,0.01) 3px)

/* Eroded edges and worn texture */
radial-gradient(ellipse at 20% 50%, rgba(0,0,0,0.15) 0%, transparent 50%)

/* Texture damage and wear patterns */
radial-gradient(circle at 10% 20%, rgba(0,0,0,0.08) 0%, transparent 3%)

/* Weathered and faded effect */
linear-gradient(135deg, rgba(0,0,0,0.05) 0%, transparent 25%, rgba(255,255,255,0.02) 50%, transparent 75%, rgba(0,0,0,0.03) 100%)
```

### **Index.html Implementation:**
Similar layered approach with:
- Film grain base
- Scratched surfaces (horizontal and vertical lines)
- Wear patterns (radial gradients at specific points)
- Weathered gradients (diagonal fade effects)

## Tips for Better Results

1. **Layer Multiple Effects**: Combine scratches, dust, wear patterns, and erosion for realistic distress
2. **Use Radial Gradients**: Place wear marks at natural stress points (edges, corners, high-contact areas)
3. **Vary Opacity**: Keep distress subtle (0.01-0.15 opacity) for realistic worn look
4. **Direction Matters**: Use different angles for scratches (45°, 90°, 135°) to avoid patterns
5. **Edge Erosion**: Darken edges with radial gradients to simulate worn borders

## Style Consistency

To maintain consistency with your game's noir mode:
- Keep everything monochrome (grayscale)
- Use high contrast (300%+ contrast ratio)
- Maintain low brightness (60% brightness)
- Add scanlines for CRT/bodycam effect
- Include vignette for lens distortion

## Example Asset Generation Workflow

1. **Base Layer**: Generate with `distressed texture, grunge overlay`
2. **Add Details**: Refine with `scratched surface, eroded edges, worn out`
3. **Enhance Wear**: Add `texture damage, weathered, faded, chipped`
4. **Final Touches**: Include `dirty, aged` for complete look
5. **Post-Process**: Apply your CSS filters (grayscale, contrast, brightness)

## Negative Prompt Strategy

Always include these to avoid unwanted effects:
```
color, blur, low contrast, smooth, clean vector, realistic photo, 3d render, extra noise, film grain
```

This ensures you get true surface distress rather than just noise or blur effects.

---

*This guide is based on the successful implementation in your DYING LIGHT bodycam FPS game's noir texture mode.*