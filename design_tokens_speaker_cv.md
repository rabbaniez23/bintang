# Design Tokens
**Professional Speaker CV Landing Page**

---

## Color Tokens

### Primary Colors
```
--color-primary-blue: #0A66C2
--color-deep-blue: #003D82
--color-ocean-blue: #1E88E5
```

### Secondary Colors
```
--color-cyan-accent: #00BCD4
--color-navy-dark: #0D1B2A
--color-electric-blue: #2196F3
```

### Neutral Colors
```
--color-white: #FFFFFF
--color-light-gray: #F5F7FA
--color-medium-gray: #8B95A5
--color-dark-gray: #2D3748
--color-charcoal: #1A202C
```

### Accent Colors
```
--color-success-green: #10B981
--color-warning-amber: #F59E0B
--color-gradient-start: #0A66C2
--color-gradient-end: #1E88E5
```

---

## Typography Tokens

### Font Families
```
--font-primary: 'Inter', sans-serif
--font-display: 'Poppins', sans-serif
--font-mono: 'JetBrains Mono', monospace
```

### Font Sizes
```
--font-size-xs: 12px
--font-size-sm: 14px
--font-size-base: 16px
--font-size-lg: 18px
--font-size-xl: 20px
--font-size-2xl: 24px
--font-size-3xl: 30px
--font-size-4xl: 36px
--font-size-5xl: 48px
--font-size-6xl: 60px
--font-size-7xl: 72px
```

### Font Weights
```
--font-weight-light: 300
--font-weight-normal: 400
--font-weight-medium: 500
--font-weight-semibold: 600
--font-weight-bold: 700
--font-weight-extrabold: 800
```

### Line Heights
```
--line-height-tight: 1.25
--line-height-normal: 1.5
--line-height-relaxed: 1.625
--line-height-loose: 2
```

---

## Spacing Tokens

### Spacing Scale (8px base unit)
```
--spacing-0: 0px
--spacing-1: 4px
--spacing-2: 8px
--spacing-3: 12px
--spacing-4: 16px
--spacing-5: 20px
--spacing-6: 24px
--spacing-8: 32px
--spacing-10: 40px
--spacing-12: 48px
--spacing-16: 64px
--spacing-20: 80px
--spacing-24: 96px
--spacing-32: 128px
```

---

## Border Radius Tokens

### Radius Scale
```
--radius-none: 0px
--radius-sm: 2px
--radius-base: 4px
--radius-md: 6px
--radius-lg: 8px
--radius-xl: 12px
--radius-2xl: 16px
--radius-3xl: 24px
--radius-full: 9999px
```

---

## Shadow Tokens

### Shadow Scale
```
--shadow-sm: 0 1px 2px 0 rgba(0, 0, 0, 0.05)
--shadow-md: 0 4px 6px -1px rgba(0, 0, 0, 0.1), 0 2px 4px -1px rgba(0, 0, 0, 0.06)
--shadow-lg: 0 10px 15px -3px rgba(0, 0, 0, 0.1), 0 4px 6px -2px rgba(0, 0, 0, 0.05)
--shadow-xl: 0 20px 25px -5px rgba(0, 0, 0, 0.1), 0 10px 10px -5px rgba(0, 0, 0, 0.04)
--shadow-2xl: 0 25px 50px -12px rgba(0, 0, 0, 0.25)
--shadow-inner: inset 0 2px 4px 0 rgba(0, 0, 0, 0.06)
--shadow-none: 0 0 0 0 rgba(0, 0, 0, 0)
```

### Custom Shadows
```
--shadow-glow: 0 0 20px rgba(10, 102, 194, 0.3)
--shadow-blue-glow: 0 0 30px rgba(30, 136, 229, 0.4)
```

---

## Opacity Tokens

### Opacity Scale
```
--opacity-0: 0
--opacity-5: 0.05
--opacity-10: 0.1
--opacity-20: 0.2
--opacity-30: 0.3
--opacity-40: 0.4
--opacity-50: 0.5
--opacity-60: 0.6
--opacity-70: 0.7
--opacity-80: 0.8
--opacity-90: 0.9
--opacity-95: 0.95
--opacity-100: 1
```

---

## Animation Tokens

### Transition Durations
```
--duration-fast: 150ms
--duration-normal: 200ms
--duration-medium: 300ms
--duration-slow: 500ms
--duration-very-slow: 700ms
```

### Transition Timing Functions
```
--ease-linear: linear
--ease-in: cubic-bezier(0.4, 0, 1, 1)
--ease-out: cubic-bezier(0, 0, 0.2, 1)
--ease-in-out: cubic-bezier(0.4, 0, 0.2, 1)
```

---

## Breakpoint Tokens

### Responsive Breakpoints
```
--breakpoint-sm: 640px
--breakpoint-md: 768px
--breakpoint-lg: 1024px
--breakpoint-xl: 1280px
--breakpoint-2xl: 1536px
```

---

## Container Tokens

### Max Width
```
--container-max-width: 1280px
```

---

## Component-Level Tokens

### Button Tokens
```
--button-padding-x: 24px
--button-padding-y: 12px
--button-font-size: 16px
--button-font-weight: 600
--button-border-radius: 8px
--button-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1)
--button-shadow-hover: 0 10px 15px -3px rgba(0, 0, 0, 0.1)
--button-transform-hover: -4px
```

### Card Tokens
```
--card-padding: 32px
--card-border-radius: 12px
--card-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1)
--card-shadow-hover: 0 20px 25px -5px rgba(0, 0, 0, 0.1)
--card-border-width: 1px
--card-border-color: rgba(0, 0, 0, 0.05)
```

### Input Tokens
```
--input-padding-x: 16px
--input-padding-y: 12px
--input-border-width: 2px
--input-border-radius: 8px
--input-border-color: #D1D5DB
--input-border-color-focus: #0A66C2
--input-ring-width: 2px
--input-ring-color: rgba(10, 102, 194, 0.2)
```

### Badge Tokens
```
--badge-padding-x: 16px
--badge-padding-y: 8px
--badge-font-size: 14px
--badge-font-weight: 500
--badge-border-radius: 9999px
--badge-border-width: 1px
```

### Section Tokens
```
--section-padding-y-mobile: 32px
--section-padding-y-tablet: 48px
--section-padding-y-desktop: 64px
--section-padding-x: 24px
```

### Grid Tokens
```
--grid-gap-mobile: 16px
--grid-gap-tablet: 24px
--grid-gap-desktop: 32px
```

### Navigation Tokens
```
--nav-link-font-weight: 500
--nav-underline-height: 2px
--nav-underline-color: #0A66C2
```

### Hero Tokens
```
--hero-min-height: 100vh
--hero-overlay-opacity: 0.1
```

### Testimonial Tokens
```
--testimonial-padding: 24px
--testimonial-border-radius: 8px
--testimonial-border-left-width: 4px
--testimonial-border-color: #00BCD4
--testimonial-avatar-size: 64px
```

### Statistics Tokens
```
--stat-number-font-size: 48px
--stat-number-font-weight: 700
--stat-label-font-size: 18px
--stat-divider-width: 80px
--stat-divider-height: 4px
```

---

## Usage Notes

### Naming Convention
All tokens follow the pattern: `--{category}-{property}-{variant}`

Examples:
- `--color-primary-blue`
- `--spacing-8`
- `--font-size-2xl`
- `--shadow-lg`
- `--button-padding-x`

### CSS Custom Properties Implementation
```css
:root {
  /* Colors */
  --color-primary-blue: #0A66C2;
  --color-deep-blue: #003D82;
  
  /* Typography */
  --font-primary: 'Inter', sans-serif;
  --font-size-base: 16px;
  --font-weight-semibold: 600;
  
  /* Spacing */
  --spacing-6: 24px;
  --spacing-8: 32px;
  
  /* Shadows */
  --shadow-md: 0 4px 6px -1px rgba(0, 0, 0, 0.1);
  
  /* Animation */
  --duration-medium: 300ms;
  --ease-in-out: cubic-bezier(0.4, 0, 0.2, 1);
}
```

### Tailwind Config Integration
```javascript
module.exports = {
  theme: {
    extend: {
      colors: {
        'primary-blue': '#0A66C2',
        'deep-blue': '#003D82',
        'ocean-blue': '#1E88E5',
        'cyan-accent': '#00BCD4',
        'navy-dark': '#0D1B2A',
        'electric-blue': '#2196F3',
        'light-gray': '#F5F7FA',
        'medium-gray': '#8B95A5',
        'dark-gray': '#2D3748',
        'charcoal': '#1A202C',
        'success-green': '#10B981',
        'warning-amber': '#F59E0B',
      },
      fontFamily: {
        primary: ['Inter', 'sans-serif'],
        display: ['Poppins', 'sans-serif'],
        mono: ['JetBrains Mono', 'monospace'],
      },
      spacing: {
        '1': '4px',
        '2': '8px',
        '3': '12px',
        '4': '16px',
        '5': '20px',
        '6': '24px',
        '8': '32px',
        '10': '40px',
        '12': '48px',
        '16': '64px',
        '20': '80px',
        '24': '96px',
        '32': '128px',
      },
      borderRadius: {
        'none': '0px',
        'sm': '2px',
        'DEFAULT': '4px',
        'md': '6px',
        'lg': '8px',
        'xl': '12px',
        '2xl': '16px',
        '3xl': '24px',
        'full': '9999px',
      },
      boxShadow: {
        'sm': '0 1px 2px 0 rgba(0, 0, 0, 0.05)',
        'DEFAULT': '0 4px 6px -1px rgba(0, 0, 0, 0.1)',
        'md': '0 4px 6px -1px rgba(0, 0, 0, 0.1)',
        'lg': '0 10px 15px -3px rgba(0, 0, 0, 0.1)',
        'xl': '0 20px 25px -5px rgba(0, 0, 0, 0.1)',
        '2xl': '0 25px 50px -12px rgba(0, 0, 0, 0.25)',
        'inner': 'inset 0 2px 4px 0 rgba(0, 0, 0, 0.06)',
        'glow': '0 0 20px rgba(10, 102, 194, 0.3)',
        'blue-glow': '0 0 30px rgba(30, 136, 229, 0.4)',
      },
      transitionDuration: {
        '150': '150ms',
        '200': '200ms',
        '300': '300ms',
        '500': '500ms',
        '700': '700ms',
      },
    },
  },
}
```

---

**Token Version**: 1.0  
**Extracted From**: Professional Speaker CV Style Guide v1.0  
**Total Tokens**: 150+