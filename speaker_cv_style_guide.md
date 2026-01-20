# UI Style Guide: Professional Speaker Landing Page

## Overview

This style guide defines the design system for a modern, interactive professional CV landing page tailored for public speakers. The design emphasizes credibility, engagement, and dynamic storytelling through a sophisticated blue-toned palette with interactive elements that showcase speaking expertise and personality.

**Design Principles:**
- Modern & Professional: Clean interfaces that convey authority and expertise
- Interactive & Engaging: Micro-animations and hover states that bring the page to life
- Blue-Centric Palette: Professional, trustworthy color scheme with strategic accent colors
- Content-First: Typography and spacing that prioritize readability and hierarchy
- Responsive & Accessible: Mobile-friendly with proper contrast ratios

---

## Color Palette

### Primary Colors
- **Primary Blue**: `#0A66C2` - Main brand color, CTAs, links
- **Deep Blue**: `#003D82` - Headers, important text, dark mode elements
- **Ocean Blue**: `#1E88E5` - Interactive states, highlights

### Secondary Colors
- **Cyan Accent**: `#00BCD4` - Secondary CTAs, badges, skill highlights
- **Navy Dark**: `#0D1B2A` - Background sections, footer
- **Electric Blue**: `#2196F3` - Hover states, active elements

### Neutral Colors
- **Pure White**: `#FFFFFF` - Backgrounds, cards
- **Light Gray**: `#F5F7FA` - Alternative backgrounds, subtle sections
- **Medium Gray**: `#8B95A5` - Secondary text, borders
- **Dark Gray**: `#2D3748` - Body text
- **Charcoal**: `#1A202C` - Headings, emphasis text

### Accent Colors
- **Success Green**: `#10B981` - Achievements, success indicators
- **Warning Amber**: `#F59E0B` - Highlights, featured items
- **Gradient Start**: `#0A66C2` - For gradient backgrounds
- **Gradient End**: `#1E88E5` - For gradient backgrounds

### Usage Guidelines
```
Backgrounds: White (#FFFFFF), Light Gray (#F5F7FA), Navy Dark (#0D1B2A)
Text: Charcoal (#1A202C), Dark Gray (#2D3748), Medium Gray (#8B95A5)
Interactive: Primary Blue (#0A66C2), Electric Blue (#2196F3)
Accents: Cyan (#00BCD4), Success Green (#10B981)
```

---

## Typography

### Font Families
- **Primary Font**: `Inter` - Clean, modern sans-serif for body text
- **Display Font**: `Poppins` - Bold, attention-grabbing for headings
- **Monospace**: `JetBrains Mono` - Code snippets, technical details

### Font Sizes
```
Hero/Display:   text-6xl (60px) - text-7xl (72px)
H1:             text-5xl (48px)
H2:             text-4xl (36px)
H3:             text-3xl (30px)
H4:             text-2xl (24px)
H5:             text-xl (20px)
H6:             text-lg (18px)
Body Large:     text-lg (18px)
Body:           text-base (16px)
Body Small:     text-sm (14px)
Caption:        text-xs (12px)
```

### Font Weights
```
Light:      font-light (300)
Regular:    font-normal (400)
Medium:     font-medium (500)
Semibold:   font-semibold (600)
Bold:       font-bold (700)
Extrabold:  font-extrabold (800)
```

### Typography Hierarchy
```
Hero Title:         text-6xl font-bold text-charcoal leading-tight
Section Heading:    text-4xl font-bold text-deep-blue mb-4
Subsection:         text-2xl font-semibold text-dark-gray mb-3
Body Text:          text-base font-normal text-dark-gray leading-relaxed
Emphasis:           text-lg font-medium text-primary-blue
Caption/Meta:       text-sm font-normal text-medium-gray
```

### Line Heights
```
Tight:      leading-tight (1.25)
Normal:     leading-normal (1.5)
Relaxed:    leading-relaxed (1.625)
Loose:      leading-loose (2)
```

---

## Spacing System

### Base Unit
8px base unit following the 8-point grid system

### Spacing Scale
```
0:    0px
1:    4px    (0.5 × base)
2:    8px    (1 × base)
3:    12px   (1.5 × base)
4:    16px   (2 × base)
5:    20px   (2.5 × base)
6:    24px   (3 × base)
8:    32px   (4 × base)
10:   40px   (5 × base)
12:   48px   (6 × base)
16:   64px   (8 × base)
20:   80px   (10 × base)
24:   96px   (12 × base)
32:   128px  (16 × base)
```

### Common Spacing Patterns
```
Component Internal Padding:  p-6 (24px)
Section Padding:             py-16 px-6 (64px vertical, 24px horizontal)
Card Padding:                p-8 (32px)
Button Padding:              px-6 py-3 (24px horizontal, 12px vertical)
Element Margins:             mb-4, mb-6, mb-8
Grid Gaps:                   gap-6, gap-8
Container Max Width:         max-w-7xl (1280px)
```

### Responsive Spacing
```
Mobile:     p-4, py-8, gap-4
Tablet:     p-6, py-12, gap-6
Desktop:    p-8, py-16, gap-8
```

---

## Component Styles

### Buttons

**Primary Button**
```
Classes: px-6 py-3 bg-primary-blue text-white rounded-lg font-semibold 
         hover:bg-deep-blue transition-all duration-300 shadow-md 
         hover:shadow-lg hover:-translate-y-0.5
```

**Secondary Button**
```
Classes: px-6 py-3 bg-transparent border-2 border-primary-blue 
         text-primary-blue rounded-lg font-semibold hover:bg-primary-blue 
         hover:text-white transition-all duration-300
```

**Ghost Button**
```
Classes: px-6 py-3 text-primary-blue font-semibold hover:bg-light-gray 
         rounded-lg transition-colors duration-200
```

### Cards

**Standard Card**
```
Classes: bg-white rounded-xl shadow-md hover:shadow-xl transition-shadow 
         duration-300 p-8 border border-gray-100
```

**Featured Card**
```
Classes: bg-gradient-to-br from-primary-blue to-ocean-blue text-white 
         rounded-xl shadow-lg p-8 transform hover:scale-105 
         transition-transform duration-300
```

**Testimonial Card**
```
Classes: bg-light-gray rounded-lg p-6 border-l-4 border-cyan-accent 
         shadow-sm hover:shadow-md transition-shadow duration-200
```

### Input Fields

**Text Input**
```
Classes: w-full px-4 py-3 border-2 border-gray-300 rounded-lg 
         focus:border-primary-blue focus:ring-2 focus:ring-primary-blue/20 
         focus:outline-none transition-all duration-200
```

**Textarea**
```
Classes: w-full px-4 py-3 border-2 border-gray-300 rounded-lg 
         focus:border-primary-blue focus:ring-2 focus:ring-primary-blue/20 
         focus:outline-none transition-all duration-200 resize-none
```

### Badges

**Skill Badge**
```
Classes: inline-block px-4 py-2 bg-cyan-accent/10 text-primary-blue 
         rounded-full text-sm font-medium border border-cyan-accent/30
```

**Status Badge**
```
Classes: inline-flex items-center px-3 py-1 bg-success-green/10 
         text-success-green rounded-full text-xs font-semibold
```

### Navigation

**Nav Link**
```
Classes: text-dark-gray font-medium hover:text-primary-blue 
         transition-colors duration-200 relative after:absolute 
         after:bottom-0 after:left-0 after:w-0 after:h-0.5 
         after:bg-primary-blue after:transition-all after:duration-300 
         hover:after:w-full
```

**Mobile Menu**
```
Classes: fixed inset-0 bg-navy-dark text-white z-50 p-6 
         transform transition-transform duration-300
```

---

## Shadows & Elevation

### Shadow Scale
```
sm:     shadow-sm     - Subtle lift (0 1px 2px rgba(0,0,0,0.05))
base:   shadow-md     - Standard cards (0 4px 6px rgba(0,0,0,0.1))
md:     shadow-lg     - Elevated elements (0 10px 15px rgba(0,0,0,0.1))
lg:     shadow-xl     - Modal, dropdown (0 20px 25px rgba(0,0,0,0.1))
xl:     shadow-2xl    - Highest elevation (0 25px 50px rgba(0,0,0,0.25))
```

### Custom Shadows
```
Glow Effect:        shadow-[0_0_20px_rgba(10,102,194,0.3)]
Blue Glow:          shadow-[0_0_30px_rgba(30,136,229,0.4)]
Inset:              shadow-inner
None:               shadow-none
```

### Elevation Levels
```
Level 0: Base page - shadow-none
Level 1: Cards, inputs - shadow-md
Level 2: Hover states - shadow-lg
Level 3: Dropdowns, tooltips - shadow-xl
Level 4: Modals, dialogs - shadow-2xl
```

---

## Animations & Transitions

### Transition Durations
```
Fast:       duration-150  (150ms) - Micro-interactions
Normal:     duration-200  (200ms) - Hover states
Medium:     duration-300  (300ms) - Standard transitions
Slow:       duration-500  (500ms) - Page transitions
Very Slow:  duration-700  (700ms) - Special effects
```

### Transition Properties
```
All:        transition-all
Colors:     transition-colors
Transform:  transition-transform
Opacity:    transition-opacity
Shadow:     transition-shadow
```

### Easing Functions
```
Linear:     ease-linear
In:         ease-in
Out:        ease-out
In-Out:     ease-in-out
```

### Common Animations

**Fade In Up**
```
Classes: opacity-0 translate-y-4 animate-[fadeInUp_0.5s_ease-out_forwards]
Keyframe: @keyframes fadeInUp { to { opacity: 1; transform: translateY(0); } }
```

**Scale on Hover**
```
Classes: transform hover:scale-105 transition-transform duration-300
```

**Slide In from Left**
```
Classes: -translate-x-full animate-[slideIn_0.4s_ease-out_forwards]
Keyframe: @keyframes slideIn { to { transform: translateX(0); } }
```

**Pulse Effect**
```
Classes: animate-pulse
```

**Smooth Scroll**
```
Classes: scroll-smooth (applied to html/body)
```

**Interactive Card**
```
Classes: hover:shadow-xl hover:-translate-y-1 transition-all duration-300
```

---

## Border Radius

### Radius Scale
```
None:       rounded-none   (0px)
Small:      rounded-sm     (2px)
Base:       rounded        (4px)
Medium:     rounded-md     (6px)
Large:      rounded-lg     (8px)
XL:         rounded-xl     (12px)
2XL:        rounded-2xl    (16px)
3XL:        rounded-3xl    (24px)
Full:       rounded-full   (9999px)
```

### Component Usage
```
Buttons:            rounded-lg
Cards:              rounded-xl
Input Fields:       rounded-lg
Badges:             rounded-full
Images (Avatar):    rounded-full
Images (Content):   rounded-lg
Modals:             rounded-2xl
Containers:         rounded-xl
Pills/Tags:         rounded-full
```

---

## Opacity & Transparency

### Opacity Scale
```
0:      opacity-0     (0%)
5:      opacity-5     (5%)
10:     opacity-10    (10%)
20:     opacity-20    (20%)
30:     opacity-30    (30%)
40:     opacity-40    (40%)
50:     opacity-50    (50%)
60:     opacity-60    (60%)
70:     opacity-70    (70%)
80:     opacity-80    (80%)
90:     opacity-90    (90%)
95:     opacity-95    (95%)
100:    opacity-100   (100%)
```

### Background Opacity
```
Classes: bg-primary-blue/10  (10% opacity)
         bg-navy-dark/95     (95% opacity)
         bg-white/80         (80% opacity - glass effect)
```

### Common Use Cases
```
Overlay:                bg-navy-dark/70
Glass Effect:           bg-white/80 backdrop-blur-lg
Disabled State:         opacity-50
Hover Overlay:          bg-primary-blue/10
Loading State:          opacity-60
Subtle Background:      bg-light-gray/50
```

---

## Common Tailwind CSS Usage

### Layout Utilities
```
Container:          max-w-7xl mx-auto px-6
Section:            py-16 md:py-24
Grid 2-column:      grid grid-cols-1 md:grid-cols-2 gap-8
Grid 3-column:      grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6
Flex Center:        flex items-center justify-center
Flex Between:       flex items-center justify-between
Sticky Header:      sticky top-0 z-50 bg-white/95 backdrop-blur-sm
```

### Responsive Patterns
```
Mobile First:       text-2xl md:text-4xl lg:text-6xl
Hide on Mobile:     hidden md:block
Show on Mobile:     block md:hidden
Responsive Grid:    grid-cols-1 sm:grid-cols-2 lg:grid-cols-3
Responsive Padding: px-4 md:px-6 lg:px-8
```

### Text Utilities
```
Heading:            text-4xl font-bold text-charcoal leading-tight
Body:               text-base text-dark-gray leading-relaxed
Subtext:            text-sm text-medium-gray
Truncate:           truncate
Multi-line Clamp:   line-clamp-3
Text Gradient:      bg-gradient-to-r from-primary-blue to-ocean-blue 
                    bg-clip-text text-transparent
```

### Interactive States
```
Hover Lift:         hover:shadow-lg hover:-translate-y-1
Active State:       active:scale-95
Focus Ring:         focus:ring-2 focus:ring-primary-blue focus:ring-offset-2
Disabled:           disabled:opacity-50 disabled:cursor-not-allowed
Group Hover:        group-hover:text-primary-blue
```

### Backgrounds
```
Gradient:           bg-gradient-to-br from-primary-blue to-ocean-blue
Solid:              bg-white
Pattern:            bg-light-gray
Dark Section:       bg-navy-dark text-white
Glass:              bg-white/80 backdrop-blur-lg
```

### Common Combinations
```
Card:               bg-white rounded-xl shadow-md p-8 hover:shadow-xl 
                    transition-shadow duration-300

CTA Button:         px-6 py-3 bg-primary-blue text-white rounded-lg 
                    font-semibold hover:bg-deep-blue shadow-md 
                    hover:shadow-lg hover:-translate-y-0.5 
                    transition-all duration-300

Section Container:  max-w-7xl mx-auto px-6 py-16

Feature Grid:       grid grid-cols-1 md:grid-cols-3 gap-8

Image Container:    rounded-lg overflow-hidden shadow-md
```

---

## Example Component Reference

### Hero Section
```jsx
<section className="relative min-h-screen flex items-center justify-center bg-gradient-to-br from-navy-dark via-deep-blue to-primary-blue text-white overflow-hidden">
  <div className="absolute inset-0 bg-[url('/grid-pattern.svg')] opacity-10"></div>
  <div className="relative max-w-7xl mx-auto px-6 py-24 text-center">
    <h1 className="text-6xl md:text-7xl font-bold mb-6 animate-[fadeInUp_0.6s_ease-out]">
      John Anderson
    </h1>
    <p className="text-2xl md:text-3xl font-light mb-4 text-cyan-accent animate-[fadeInUp_0.6s_ease-out_0.2s_both]">
      International Keynote Speaker
    </p>
    <p className="text-lg md:text-xl text-white/80 max-w-2xl mx-auto mb-8 animate-[fadeInUp_0.6s_ease-out_0.4s_both]">
      Inspiring leaders and teams to achieve extraordinary results through innovation and authentic communication
    </p>
    <div className="flex flex-col sm:flex-row gap-4 justify-center animate-[fadeInUp_0.6s_ease-out_0.6s_both]">
      <button className="px-8 py-4 bg-white text-primary-blue rounded-lg font-semibold hover:bg-light-gray shadow-lg hover:shadow-xl hover:-translate-y-1 transition-all duration-300">
        Book a Speaking Engagement
      </button>
      <button className="px-8 py-4 bg-transparent border-2 border-white text-white rounded-lg font-semibold hover:bg-white hover:text-primary-blue transition-all duration-300">
        Watch Showreel
      </button>
    </div>
  </div>
</section>
```

### Speaking Topics Card
```jsx
<div className="bg-white rounded-xl shadow-md hover:shadow-xl transition-all duration-300 p-8 border border-gray-100 group">
  <div className="w-16 h-16 bg-gradient-to-br from-primary-blue to-ocean-blue rounded-lg flex items-center justify-center mb-6 group-hover:scale-110 transition-transform duration-300">
    <svg className="w-8 h-8 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
      <path strokeLinecap="round" strokeLinejoin="round" strokeWidth={2} d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z" />
    </svg>
  </div>
  <h3 className="text-2xl font-bold text-charcoal mb-3 group-hover:text-primary-blue transition-colors duration-200">
    Leadership Excellence
  </h3>
  <p className="text-base text-dark-gray leading-relaxed mb-4">
    Empowering leaders to navigate change, build resilient teams, and drive organizational transformation in the modern workplace.
  </p>
  <a href="#" className="inline-flex items-center text-primary-blue font-semibold hover:text-ocean-blue transition-colors duration-200">
    Learn More
    <svg className="w-4 h-4 ml-2 group-hover:translate-x-1 transition-transform duration-200" fill="none" stroke="currentColor" viewBox="0 0 24 24">
      <path strokeLinecap="round" strokeLinejoin="round" strokeWidth={2} d="M9 5l7 7-7 7" />
    </svg>
  </a>
</div>
```

### Statistics Counter
```jsx
<div className="bg-gradient-to-br from-primary-blue to-ocean-blue rounded-xl shadow-lg p-8 text-center text-white">
  <div className="text-5xl font-bold mb-2">500+</div>
  <div className="text-lg font-medium text-white/90">Speaking Engagements</div>
  <div className="mt-4 h-1 w-20 bg-cyan-accent mx-auto rounded-full"></div>
</div>
```

### Testimonial Component
```jsx
<div className="bg-light-gray rounded-lg p-6 border-l-4 border-cyan-accent shadow-sm hover:shadow-md transition-shadow duration-200">
  <div className="flex items-start gap-4">
    <img src="/avatar.jpg" alt="Client" className="w-16 h-16 rounded-full shadow-md" />
    <div className="flex-1">
      <p className="text-base text-dark-gray italic leading-relaxed mb-4">
        "John's keynote transformed our leadership team's approach to innovation. His insights were practical, inspiring, and immediately actionable."
      </p>
      <div>
        <p className="font-semibold text-charcoal">Sarah Mitchell</p>
        <p className="text-sm text-medium-gray">CEO, TechVision Inc.</p>
      </div>
    </div>
  </div>
</div>
```

### Contact Form
```jsx
<form className="max-w-2xl mx-auto space-y-6">
  <div>
    <label className="block text-sm font-semibold text-charcoal mb-2">Full Name</label>
    <input 
      type="text"
      className="w-full px-4 py-3 border-2 border-gray-300 rounded-lg focus:border-primary-blue focus:ring-2 focus:ring-primary-blue/20 focus:outline-none transition-all duration-200"
      placeholder="Enter your name"
    />
  </div>
  <div>
    <label className="block text-sm font-semibold text-charcoal mb-2">Email Address</label>
    <input 
      type="email"
      className="w-full px-4 py-3 border-2 border-gray-300 rounded-lg focus:border-primary-blue focus:ring-2 focus:ring-primary-blue/20 focus:outline-none transition-all duration-200"
      placeholder="your@email.com"
    />
  </div>
  <div>
    <label className="block text-sm font-semibold text-charcoal mb-2">Message</label>
    <textarea 
      rows={5}
      className="w-full px-4 py-3 border-2 border-gray-300 rounded-lg focus:border-primary-blue focus:ring-2 focus:ring-primary-blue/20 focus:outline-none transition-all duration-200 resize-none"
      placeholder="Tell us about your event..."
    ></textarea>
  </div>
  <button className="w-full px-6 py-4 bg-primary-blue text-white rounded-lg font-semibold hover:bg-deep-blue shadow-md hover:shadow-lg hover:-translate-y-0.5 transition-all duration-300">
    Send Message
  </button>
</form>
```

---

## Implementation Notes

### Best Practices
1. Always maintain minimum 4.5:1 contrast ratio for accessibility
2. Use consistent spacing from the 8px grid system
3. Implement smooth transitions for all interactive elements
4. Optimize images and use lazy loading
5. Test animations on lower-end devices
6. Ensure mobile responsiveness across all components

### Performance Considerations
- Use `will-change` sparingly for frequently animated elements
- Implement intersection observers for scroll animations
- Lazy load images below the fold
- Minimize use of `backdrop-blur` on mobile devices

### Accessibility
- Include focus states for all interactive elements
- Use semantic HTML elements
- Provide alt text for all images
- Ensure keyboard navigation works smoothly
- Test with screen readers

---

**Version**: 1.0  
**Last Updated**: January 2026  
**Design System**: Tailwind CSS v3.4+