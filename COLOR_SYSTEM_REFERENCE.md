# Premium Cinematic Color System - Quick Reference

## 🎨 Color Palette Overview

### Implementation Method: CSS Variables + Tailwind

All colors use **CSS variables** defined in `globals.css` and mapped to **Tailwind classes** in `tailwind.config.ts`. This approach ensures consistency, maintainability, and easy theme switching.

---

## 📋 Complete Color Reference

### Background Colors (Cinema Blacks)

| Purpose | Hex | CSS Variable | Tailwind Class | Usage |
|---------|-----|--------------|----------------|-------|
| **Deepest Black** | `#0A0A0A` | `--background` | `bg-bg-deepest` | Main page background, nav background |
| **Darker Black** | `#111111` | `--background-darker` | `bg-bg-darker` | Gradient transitions, alternate sections |
| **Dark Black** | `#171717` | `--background-dark` | `bg-bg-dark` | Hover states, elevated surfaces |
| **Surface** | `#1A1A1A` | `--background-surface` | `bg-bg-surface` | Card backgrounds, panels |
| **Elevated** | `#202020` | `--background-elevated` | `bg-bg-elevated` | Modal overlays, tooltips |

---

### Accent Colors (Luxury Gold System)

| Purpose | Hex | CSS Variable | Tailwind Class | Usage |
|---------|-----|--------------|----------------|-------|
| **Primary Gold** | `#D4AF37` | `--primary` | `text-gold` / `bg-gold` / `border-gold` | Main accent, headings, icons, active states |
| **Light Gold** | `#F5C86B` | `--primary-light` | `text-gold-light` / `bg-gold-light` | Highlights, hover states, bright accents |
| **Dark Gold** | `#B8941F` | `--primary-dark` | `text-gold-dark` / `bg-gold-dark` | Gradient ends, subtle accents, shadows |

---

### Text Hierarchy

| Purpose | Hex | CSS Variable | Tailwind Class | Usage |
|---------|-----|--------------|----------------|-------|
| **Primary Text** | `#FFFFFF` | `--text-primary` | `text-text-primary` | Headings, important text, primary content |
| **Secondary Text** | `#E5E5E5` | `--text-secondary` | `text-text-secondary` | Body copy, descriptions, paragraphs |
| **Tertiary Text** | `#A3A3A3` | `--text-tertiary` | `text-text-tertiary` | Supporting text, labels, metadata |
| **Muted Text** | `#737373` | `--text-muted` | `text-text-muted` | Placeholders, disabled text, timestamps |

---

## 🎬 Usage Examples

### Navigation
```tsx
<nav className="bg-bg-deepest/95 border-b border-gold/10">
  <span className="text-gold">AK</span>
  <button className="text-text-secondary hover:text-white">About</button>
</nav>
```

### Buttons
```tsx
{/* Primary CTA - Gold gradient */}
<button className="bg-gradient-to-b from-gold-light via-gold to-gold-dark text-bg-deepest">
  View Portfolio
</button>

{/* Secondary CTA - Outlined */}
<button className="bg-white/5 border border-gold/30 hover:border-gold/50 text-white">
  Get In Touch
</button>
```

### Cards
```tsx
<div className="bg-bg-surface/80 border border-gold/10 hover:border-gold/40">
  <h3 className="text-white group-hover:text-gold-light">Title</h3>
  <p className="text-text-tertiary">Description</p>
</div>
```

### Progress Bars
```tsx
<div className="bg-bg-surface/50 border border-gold/10">
  <div className="bg-gradient-to-r from-gold-dark via-gold to-gold-light" 
       style={{ width: '85%' }}>
  </div>
</div>
```

### Form Inputs
```tsx
<input 
  className="bg-bg-surface/60 border border-white/10 
             text-white placeholder-text-muted
             focus:border-gold/40 focus:ring-2 focus:ring-gold/20"
  placeholder="Your name"
/>
```

---

## 🎯 Opacity Guidelines

### Gold Accent Opacity Levels

| Opacity | Usage | Example |
|---------|-------|---------|
| `/3-5` | Decorative elements, very subtle hints | Blur orbs, ambient glow |
| `/10-15` | Default borders, resting states | Card borders, dividers |
| `/20-30` | Medium emphasis, hover borders | Hovered card borders |
| `/40-50` | Strong emphasis, active states | Focus borders, active navigation |
| `/100` (solid) | Primary accents, text, icons | Headings, numbers, CTA gradients |

### Background Opacity Levels

| Opacity | Usage | Example |
|---------|-------|---------|
| `/30-40` | Very subtle backgrounds | Portfolio video cards (let videos shine) |
| `/50-60` | Light backgrounds | Form inputs, secondary cards |
| `/70-80` | Standard backgrounds | Main cards, panels |
| `/90-95` | Solid backgrounds | Navigation, modals |
| `/100` (solid) | Page backgrounds | Body, main container |

---

## 🌈 Gradient Patterns

### Gold Gradients (Metallic Effect)

```css
/* Three-stop metallic gradient */
bg-gradient-to-b from-gold-light via-gold to-gold-dark

/* Horizontal progress bar */
bg-gradient-to-r from-gold-dark via-gold to-gold-light

/* Left accent bar */
bg-gradient-to-b from-gold-light via-gold to-gold-dark

/* Card hover glow */
bg-gradient-to-br from-gold/12 to-bg-surface
```

### Background Gradients (Depth)

```css
/* Main page background */
bg-gradient-to-br from-bg-deepest via-bg-darker to-bg-deepest

/* Card backgrounds (light to dark) */
bg-gradient-to-br from-gold/8 to-bg-surface
```

---

## 🎨 Shadow System

### Shadow with Gold Tint

```tsx
/* Subtle card shadow */
hover:shadow-[0_8px_16px_-4px_rgba(212,175,55,0.15)]

/* Medium button shadow */
hover:shadow-[0_12px_24px_-8px_rgba(212,175,55,0.2)]

/* Strong CTA shadow */
hover:shadow-[0_20px_40px_-12px_rgba(212,175,55,0.4)]
```

**Pattern:** `[y-offset_blur_spread_rgba(212,175,55,opacity)]`

**Rules:**
- Always use gold RGB: `212, 175, 55`
- Keep opacity low: 0.15-0.4
- Use negative spread for tighter glow
- Layer with black shadows for depth

---

## 🔄 Color Relationships

### Primary UI Flow

```
Default State:      border-gold/10
Hover State:        border-gold/30 → border-gold/40
Active/Focus:       border-gold/50
```

### Text Hierarchy

```
Heading:            text-white or text-gold
Body:               text-text-secondary (#E5E5E5)
Supporting:         text-text-tertiary (#A3A3A3)
Metadata:           text-text-muted (#737373)
```

### Background Layers

```
Page:               bg-bg-deepest (#0A0A0A)
Section:            bg-bg-darker (#111111)
Card:               bg-bg-surface (#1A1A1A)
Elevated:           bg-bg-elevated (#202020)
```

---

## ♿ Accessibility (WCAG)

### Contrast Ratios

| Combination | Ratio | Standard | Status |
|-------------|-------|----------|--------|
| Gold on Black | 8.2:1 | AAA | ✅ Pass |
| White on Black | 21:1 | AAA | ✅ Pass |
| Light Gold on Black | 9.4:1 | AAA | ✅ Pass |
| Dark text on Gold | 8.2:1 | AAA | ✅ Pass |
| Tertiary on Surface | 5.8:1 | AA | ✅ Pass |

**Result:** All color combinations exceed WCAG AA standards, most achieve AAA.

---

## 🎬 Psychology Quick Reference

| Color | Psychological Association | Industry Connection |
|-------|---------------------------|---------------------|
| **Gold** | Luxury, prestige, excellence, achievement | Oscar awards, golden hour, premium branding |
| **Deep Black** | Sophistication, power, cinematic quality | Cinema screens, OLED displays, high-end cameras |
| **Warm Tones** | Creativity, human touch, approachable expertise | Film lighting, studio warmth, artistic mastery |

**vs. Previous Blue:**
- Blue = Technology, trust, corporate, digital
- Gold = Luxury, creativity, premium, cinematic

---

## 🔧 Maintenance & Theme Switching

### Change Theme Colors (One Place)

Edit `globals.css`:

```css
:root {
  /* Change these values to switch theme */
  --primary: #D4AF37;        /* Main gold */
  --primary-light: #F5C86B;  /* Bright gold */
  --primary-dark: #B8941F;   /* Deep gold */
}

/* Example: Blue theme variant */
[data-theme="blue"] {
  --primary: #3b82f6;
  --primary-light: #60a5fa;
  --primary-dark: #2563eb;
}
```

**All components update automatically!**

---

## 📱 Responsive Considerations

### Mobile
- Gold remains visible on all screen types
- Increase touch targets (min 44x44px)
- Test form focus states on mobile
- Verify video embeds work on iOS/Android

### Tablet
- Same color system applies
- Layout adjusts, colors stay consistent
- Test hover states (some tablets support hover)

### Desktop
- Full gradient effects visible
- Hover states fully functional
- Shadow effects render properly
- 4K/Retina: Colors look richer

---

## 🎯 Quick Decision Matrix

**When to use which gold:**

| Element Type | Gold Variant | Reasoning |
|--------------|--------------|-----------|
| Large headings | `text-gold` | Standard gold for main accents |
| Hover highlights | `text-gold-light` | Brighter draws attention |
| Gradient ends | `gold-dark` | Creates depth in gradients |
| CTA buttons | All three (gradient) | Metallic luxury effect |
| Borders (default) | `/10-15` | Subtle brand presence |
| Borders (hover) | `/30-40` | Clear interaction feedback |

---

## 🚀 Implementation Priority

**Start with these (highest impact):**

1. ✅ Navigation accent
2. ✅ Hero name and CTAs
3. ✅ Section heading accents
4. ✅ Progress bars
5. ✅ Button gradients

**Then complete:**

6. ✅ Card borders
7. ✅ Hover states
8. ✅ Form elements
9. ✅ Footer accents
10. ✅ Decorative elements

---

## 💡 Pro Tips

1. **Use CSS variables** - Change theme instantly
2. **Keep gold strategic** - 15-20% of UI, not 50%
3. **Let videos pop** - Portfolio cards should be subtle
4. **Test on real devices** - Colors vary by screen
5. **Slower transitions** - 500ms feels more premium
6. **Subtle shadows** - /15-25 opacity, not /50
7. **Semantic naming** - `text-tertiary` beats `text-gray-400`

---

**Quick Copy-Paste:**

```css
/* globals.css */
--primary: #D4AF37;
--primary-light: #F5C86B;
--primary-dark: #B8941F;
--background: #0A0A0A;
--background-surface: #1A1A1A;
--text-tertiary: #A3A3A3;
```

```tsx
/* Common patterns */
className="text-gold"
className="bg-gold/10"
className="border-gold/20 hover:border-gold/40"
className="bg-gradient-to-b from-gold-light via-gold to-gold-dark"
```

---

**Reference this document while implementing for quick color lookups! 🎨✨**

