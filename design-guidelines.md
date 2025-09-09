# Akksi Design System Guidelines

## Overview

This document outlines the comprehensive design system for the Akksi platform, establishing consistent visual and interaction patterns for optimal user experience. Our design system follows a **light-first approach** with optional dark mode support, featuring a modern and playful aesthetic while maintaining professionalism.

## Design Philosophy

**Refined and Space-Conscious**: Our design prioritizes readability and elegance through smaller text sizes, lighter font weights, and tighter spacing. This approach creates a more sophisticated and professional appearance while improving information density and user experience.

**Light Mode is Default**: Our primary design language is optimized for light mode, providing excellent readability, professional aesthetics, and optimal print quality. Dark mode serves as an enhancement for users who prefer darker interfaces.

## Core Design Principles

### 1. Clarity Through Hierarchy

-   **Primary elements** use bold typography and high contrast
-   **Secondary elements** use medium contrast and normal weight
-   **Tertiary elements** use low contrast and lighter weight

### 2. Consistent Spacing

-   Follow TailwindCSS spacing scale: `space-1` (4px), `space-2` (8px), `space-3` (12px), `space-4` (16px), `space-6` (24px), `space-8` (32px), `space-12` (48px), `space-16` (64px)
-   Use consistent spacing for similar elements across the interface

### 3. Accessible Color Contrast

-   Maintain WCAG AAA standards (7:1 ratio) for primary text
-   Maintain WCAG AA standards (4.5:1 ratio) for secondary text
-   All interactive elements meet accessibility requirements

### 4. Modern Layout Patterns

-   **Horizontal Layouts**: Prefer side-by-side content over stacked layouts for hero sections
-   **Compact Spacing**: Reduced vertical padding (py-20 instead of py-32) for better content density
-   **Refined Typography**: Light font weights (font-light) for headlines, medium (font-medium) for emphasis
-   **Smaller Icons**: 4px-6px range for refined, professional appearance
-   **Workflow Demonstrations**: Motion-style input→output showcases over abstract process flows

---

## Color System

### Brand Colors (Teal)

Our primary brand color is **Teal**, providing freshness, innovation, and trustworthiness:

```css
/* Available as bg-teal-[shade], text-teal-[shade], border-teal-[shade] */
teal-50:  #f0fdfa  /* Very light backgrounds */
teal-100: #ccfbf1  /* Light backgrounds */
teal-200: #99f6e4  /* Primary button background */
teal-300: #5eead4  /* Light accents */
teal-400: #2dd4bf  /* Medium accents */
teal-500: #14b8a6  /* Default teal */
teal-600: #0d9488  /* Medium brand color */
teal-700: #0f766e  /* Primary text & button text */
teal-800: #115e59  /* Dark accents */
teal-900: #134e4a  /* Darkest accents */
teal-950: #042f2e  /* Extreme dark */
```

### Light Mode Color Palette (Default)

#### Backgrounds

-   **Primary**: `bg-white` or `bg-background`
-   **Secondary**: `bg-gray-50` or `bg-gray-100`
-   **Card/Panel**: `bg-white` with `border border-gray-200`
-   **Accent**: `bg-teal-50` for subtle brand emphasis

#### Text Colors

-   **Primary Text**: `text-teal-700` or `text-foreground` (brand-forward primary text)
-   **Secondary Text**: `text-gray-600` or `text-muted-foreground`
-   **Tertiary Text**: `text-gray-500`
-   **Brand Text**: `text-teal-700` or `text-primary`

#### Interactive Elements

-   **Primary Button**: `bg-teal-100 text-teal-600 font-bold hover:bg-teal-200 hover:text-teal-700` (premium subtle approach)
-   **Secondary Button**: `border border-gray-300 bg-white text-gray-700 hover:bg-gray-50`
-   **Links**: `text-teal-700 hover:text-teal-800 font-medium`
-   **Focus Ring**: `ring-2 ring-teal-500 ring-offset-2`

#### Borders & Dividers

-   **Default**: `border-gray-200`
-   **Strong**: `border-gray-300`
-   **Subtle**: `border-gray-100`

### Dark Mode Color Palette

#### Backgrounds

-   **Primary**: `dark:bg-gray-900`
-   **Secondary**: `dark:bg-gray-800`
-   **Card/Panel**: `dark:bg-gray-800` with `dark:border-gray-700`
-   **Accent**: `dark:bg-teal-950/50`

#### Text Colors

-   **Primary Text**: `dark:text-teal-300` (softer teal for dark mode)
-   **Secondary Text**: `dark:text-gray-300`
-   **Tertiary Text**: `dark:text-gray-400`
-   **Brand Text**: `dark:text-teal-400`

#### Interactive Elements

-   **Primary Button**: `dark:bg-teal-700 dark:text-teal-100 font-bold dark:hover:bg-teal-600` (adjusted for dark mode)
-   **Secondary Button**: `dark:border-gray-600 dark:bg-gray-700 dark:text-gray-200 dark:hover:bg-gray-600`
-   **Links**: `dark:text-teal-400 dark:hover:text-teal-300 font-medium`
-   **Focus Ring**: `dark:ring-teal-400 dark:ring-offset-gray-900`

#### Borders & Dividers

-   **Default**: `dark:border-gray-700`
-   **Strong**: `dark:border-gray-600`
-   **Subtle**: `dark:border-gray-800`

---

## Typography System

### Font Family

```css
/* Primary font with system fallbacks */
font-family: "Lexend", ui-sans-serif, system-ui, sans-serif;
```

### Font Scale

Use TailwindCSS text utilities:

#### Headings

-   **Hero Title**: `text-3xl sm:text-4xl lg:text-5xl font-light` (48px-60px, 300 weight)
-   **Section Title**: `text-2xl sm:text-3xl font-normal` (24px-30px, 400 weight)
-   **Card Title**: `text-lg font-medium` (18px, 500 weight)
-   **Subsection**: `text-base font-medium` (16px, 500 weight)

#### Body Text

-   **Hero Description**: `text-lg` (18px)
-   **Section Description**: `text-lg` (18px)
-   **Default Body**: `text-base` (16px)
-   **Small Text**: `text-sm` (14px)
-   **Caption**: `text-xs text-gray-500` (12px, muted)

#### Font Weights

-   **Light**: `font-light` (300) - For hero titles and large headings
-   **Normal**: `font-normal` (400) - For section titles and body text
-   **Medium**: `font-medium` (500) - For emphasis and card titles
-   **Bold**: `font-bold` (700) - Sparingly used for important numbers/CTAs

### Line Heights

-   **Tight**: `leading-tight` - For headings
-   **Normal**: `leading-normal` - For body text
-   **Relaxed**: `leading-relaxed` - For long-form content

---

## Layout & Spacing

### Container Widths

-   **Full Width**: `w-full`
-   **Large Container**: `max-w-6xl mx-auto` (1152px)
-   **Medium Container**: `max-w-4xl mx-auto` (896px)
-   **Small Container**: `max-w-2xl mx-auto` (672px)

### Common Spacing Patterns

-   **Section Padding**: `py-20` (reduced from py-32 for tighter spacing)
-   **Component Padding**: `p-6` or `p-8`
-   **Content Spacing**: `mb-16` (reduced from mb-20 for sections)
-   **Element Gaps**: `gap-4` for medium, `gap-2` for tight, `gap-6` for loose
-   **Icon Sizes**: `w-4 h-4` to `w-6 h-6` (smaller, refined icons)
-   **Container Max Width**: `max-w-6xl` (reduced from max-w-7xl for better readability)

### Grid Systems

```css
/* 12-column responsive grid */
grid-cols-1 md:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4

/* Common layouts */
grid-cols-1 lg:grid-cols-2  /* Two-column on large screens */
grid-cols-1 md:grid-cols-3  /* Three-column on medium+ */
```

---

## Component Guidelines

### Buttons

#### Primary Button

```css
/* Light mode - Refined approach with medium font weight */
bg-teal-100 text-teal-600 font-medium px-8 py-4 rounded-xl text-base hover:bg-teal-200 hover:text-teal-700 focus:ring-2 focus:ring-teal-500 focus:ring-offset-2

/* Dark mode - Adjusted for better contrast */
dark:bg-teal-700 dark:text-teal-100 dark:hover:bg-teal-600 dark:focus:ring-teal-400 dark:ring-offset-gray-900
```

#### Secondary Button

```css
/* Light mode */
border border-gray-300 bg-white text-gray-700 px-4 py-2 rounded-md font-medium hover:bg-gray-50 focus:ring-2 focus:ring-teal-500 focus:ring-offset-2

/* Dark mode additions */
dark:border-gray-600 dark:bg-gray-700 dark:text-gray-200 dark:hover:bg-gray-600 dark:focus:ring-teal-400 dark:ring-offset-gray-900
```

### Cards

```css
/* Standard card */
bg-white border border-gray-200 rounded-lg p-6 shadow-sm

/* Dark mode additions */
dark:bg-gray-800 dark:border-gray-700
```

### Input Fields

```css
/* Standard input */
border border-gray-300 rounded-md px-3 py-2 text-sm focus:ring-2 focus:ring-teal-500 focus:border-teal-500

/* Dark mode additions */
dark:border-gray-600 dark:bg-gray-700 dark:text-gray-200 dark:focus:ring-teal-400 dark:focus:border-teal-400
```

### Navigation

```css
/* Active nav item */
bg-teal-50 text-teal-700 border-r-2 border-teal-700 font-medium

/* Dark mode active nav */
dark:bg-teal-950/50 dark:text-teal-400 dark:border-teal-400

/* Inactive nav item */
text-gray-600 hover:text-teal-700 hover:bg-teal-50

/* Dark mode inactive nav */
dark:text-gray-400 dark:hover:text-teal-300 dark:hover:bg-teal-950/30
```

---

## Interactive States

### Hover States

-   **Buttons**: Primary buttons go from `teal-100` → `teal-200` (background) and `teal-600` → `teal-700` (text)
-   **Links**: Darken and optionally underline
-   **Cards**: Add subtle shadow `hover:shadow-md`

### Focus States

-   **All interactive elements**: `focus:ring-2 focus:ring-teal-500 focus:ring-offset-2`
-   **Dark mode**: `dark:focus:ring-teal-400 dark:ring-offset-gray-900`

### Active States

-   **Buttons**: `active:scale-95` for subtle press effect
-   **Navigation**: Use brand color background with appropriate text color

### Disabled States

```css
/* Disabled button */
disabled:opacity-50 disabled:cursor-not-allowed

/* Disabled input */
disabled:bg-gray-100 disabled:text-gray-500 dark:disabled:bg-gray-800 dark:disabled:text-gray-400
```

---

## Shadows & Elevation

### Shadow Scale

-   **Subtle**: `shadow-sm` - For cards and panels
-   **Medium**: `shadow-md` - For dropdowns and modals
-   **Large**: `shadow-lg` - For important overlays
-   **Extra Large**: `shadow-xl` - For major modals

### Usage Guidelines

-   Use shadows sparingly to maintain clean aesthetic
-   Consistent elevation throughout similar components
-   Higher shadows for elements that appear "closer" to user

---

## Dark Mode Implementation

### CSS Class Strategy

```css
/* Use dark: prefix for all dark mode styles */
<div class="bg-white text-gray-900 dark:bg-gray-900 dark:text-gray-100">
```

### JavaScript Theme Toggle

```javascript
// Toggle between light and dark mode
function toggleTheme() {
    document.documentElement.classList.toggle("dark");
}
```

### Component Pattern

Always define both light and dark styles:

```css
/* ✅ Good - Both modes defined */
<button class="bg-teal-100 text-teal-600 font-bold border border-teal-200 dark:bg-teal-700 dark:text-teal-100 dark:border-teal-600">

/* ❌ Bad - Only light mode */
<button class="bg-teal-100 text-teal-600 font-bold border border-teal-200">
```

---

## Accessibility Guidelines

### Color Contrast

-   **Primary text**: Minimum 7:1 ratio (WCAG AAA)
-   **Secondary text**: Minimum 4.5:1 ratio (WCAG AA)
-   **Interactive elements**: Minimum 3:1 ratio for large elements

### Focus Management

-   All interactive elements must have visible focus indicators
-   Tab order should be logical and predictable
-   Focus should be trapped in modals and dialogs

### Screen Reader Support

-   Use semantic HTML elements
-   Provide alt text for images
-   Use ARIA labels where appropriate
-   Ensure color is not the only way information is conveyed

---

## Implementation Checklist

### For New Components

-   [ ] Light mode styles defined
-   [ ] Dark mode styles defined
-   [ ] Hover states implemented
-   [ ] Focus states implemented
-   [ ] Disabled states (if applicable)
-   [ ] Accessible color contrast verified
-   [ ] Responsive design considered
-   [ ] Typography scale followed
-   [ ] Spacing system used consistently

### Testing

-   [ ] Test in both light and dark modes
-   [ ] Verify keyboard navigation
-   [ ] Check color contrast ratios
-   [ ] Test with screen readers
-   [ ] Validate responsive behavior
-   [ ] Ensure print styles work (light mode)

---

## Migration Notes

### From Hardcoded Values to TailwindCSS Classes

```css
/* ❌ Old approach */
font-size: 16px;
margin-top: 24px;
color: #0f766e;

/* ✅ New approach */
class="text-base mt-6 text-teal-700"
```

### Teal Color Migration & Refined Button Approach

-   Replace any previous brand color references with TailwindCSS teal scale
-   Primary buttons use the refined approach: `bg-teal-100 text-teal-600 font-medium px-8 py-4 rounded-xl`
-   Primary text uses `text-teal-700` for brand-forward typography
-   Use `text-primary` or `bg-primary` for theme-aware brand colors
-   Ensure all teal usage works in both light and dark modes with proper contrast
-   The refined approach emphasizes elegance and professionalism through appropriate sizing and spacing

### Layout Migration Guidelines

-   **Hero Sections**: Convert vertical stacked layouts to horizontal (flex-col lg:flex-row)
-   **Section Padding**: Reduce from `py-32` to `py-20` for better content density
-   **Text Sizing**: Reduce heading sizes by 1-2 levels (text-6xl → text-3xl, text-4xl → text-2xl)
-   **Font Weights**: Replace font-bold with font-light for headlines, font-medium for emphasis
-   **Container Width**: Use `max-w-6xl` instead of `max-w-7xl` for better readability
-   **Icon Sizing**: Use `w-4 h-4` to `w-6 h-6` range instead of `w-8 h-8` to `w-12 h-12`

This refined design system ensures consistency, accessibility, and maintainability across the entire Akksi platform while providing an elegant, space-conscious user experience that feels modern and professional.
