---
name: humble-brand-guidelines
description: Applies Humble Robotics' official brand colors and typography to any artifact that may benefit from having Humble's look-and-feel. Use when brand colors, style guidelines, visual formatting, or company design standards apply.
license: Complete terms in LICENSE.txt
---

# Humble Robotics Brand Styling

## Overview

To apply Humble Robotics' official brand identity and style resources, use this skill.

**Keywords**: branding, corporate identity, visual identity, post-processing, styling, brand colors, typography, Humble brand, Humble Robotics, visual formatting, visual design

## Brand Guidelines

### Primary Colors

| Name             | Hex       | Usage                                      |
|------------------|-----------|---------------------------------------------|
| White            | `#FFFFFF` | Heading text on dark backgrounds, icons     |
| Optimist Neutral | `#FAFFF2` | Body text alternative on dark backgrounds    |
| Humble Green     | `#81F2B2` | Primary brand accent, highlights, CTAs      |
| Rich Black       | `#030101` | Default background, dark surfaces           |

### Secondary Colors

| Name             | Primary Hex | Dark Hex  | Usage                                          |
|------------------|-------------|-----------|------------------------------------------------|
| Sage Green       | `#173A31`   | `#0C1F1A` | Elevated surface panels, card backgrounds, navbars |
| Highlight Lime   | `#EDFD9A`   | `#C8D67E` | Attention callouts, tags, highlight overlays    |
| Electric Blue    | `#83ECFF`   | `#55A7B6` | Secondary accent, links, data visualizations    |
| Freight Orange   | `#EF6B2C`   | `#A33200`  | Warnings, emphasis, tertiary accent             |

### Neutrals (Gray Scale)

| Name    | Hex       | Usage                                    |
|---------|-----------|------------------------------------------|
| Gray 1  | `#F5F4F1` | Reserved for high-contrast text elements  |
| Gray 2  | `#EEECE8` | Reserved for secondary text elements      |
| Gray 3  | `#D6D4D1` | Body text on dark backgrounds             |
| Gray 4  | `#BEBDBA` | Secondary body text, descriptions         |
| Gray 5  | `#A7A5A2` | Muted/placeholder text                   |
| Gray 6  | `#8F8E8B` | Icon fills, tertiary text                |
| Gray 7  | `#777674` | Disabled text, subtle labels             |
| Gray 8  | `#5F5E5D` | Borders, dividers on dark backgrounds    |
| Gray 9  | `#302F2E` | Elevated card/panel surfaces             |
| Gray 10 | `#181817` | Alternate dark background, near Rich Black|

### Gradients

| Name                 | Definition                                                |
|----------------------|-----------------------------------------------------------|
| Optimist Green Light | Light gradient blending Highlight Lime → Humble Green     |
| Optimist Green Dark  | Dark gradient blending Sage Green → a mid-teal            |

Use CSS: `linear-gradient(to right, #EDFD9A, #81F2B2)` for Light, `linear-gradient(to right, #173A31, #55A7B6)` for Dark.

### Typography

- **Headings**: Poppins (with Arial fallback)
- **Body Text**: Inter (with Helvetica Neue / sans-serif fallback)
- **Monospace / Code**: JetBrains Mono (with monospace fallback)

## Features

### Smart Color Application

- Default background: Rich Black (`#030101`) or Sage Green (`#173A31`). Dark mode is the default — never use White or Optimist Neutral as a page/artifact background.
- Default text on dark backgrounds: White (`#FFFFFF`) for headings, Gray 3 (`#D6D4D1`) for body text
- Primary accent: Humble Green (`#81F2B2`) for buttons, highlights, CTAs, progress indicators
- Cards and surface panels use Gray 10 (`#181817`) or Gray 9 (`#302F2E`) to create subtle depth on dark backgrounds
- Subtle borders/dividers on dark backgrounds: Gray 8 (`#5F5E5D`)
- Charts and data visualizations cycle through: Humble Green → Electric Blue → Freight Orange → Highlight Lime
- Warning/alert states use Freight Orange (`#EF6B2C`)
- Optimist Neutral (`#FAFFF2`) and White (`#FFFFFF`) are reserved for text and small UI elements — never as backgrounds

### Smart Font Application

- Applies Poppins to headings (H1–H3, 24pt+)
- Applies Inter to body text and UI labels
- Automatically falls back to system fonts if custom fonts are unavailable
- Preserves readability across all systems

### Shape and Accent Colors

- Non-text shapes and decorative elements use Secondary colors
- Cycles through Humble Green, Electric Blue, Freight Orange, Highlight Lime
- Maintains visual interest while staying on-brand
- Use Sage Green (`#173A31`) or Gray 9 (`#302F2E`) for card/panel surfaces against the Rich Black background

## Technical Details

### Font Management

- Uses system-installed Poppins, Inter, and JetBrains Mono when available
- Provides automatic fallback to Arial (headings), Helvetica Neue (body), monospace (code)
- No font installation required — works with existing system fonts
- For best results, pre-install Poppins, Inter, and JetBrains Mono

### Color Application

- Uses hex color values for precise brand matching
- In Python (python-pptx), apply via `RGBColor` class
- In CSS/HTML, use hex values directly or define as CSS custom properties:

```css
:root {
  --hum-white: #FFFFFF;
  --hum-neutral: #FAFFF2;
  --hum-green: #81F2B2;
  --hum-black: #030101;
  --hum-sage: #173A31;
  --hum-sage-dark: #0C1F1A;
  --hum-lime: #EDFD9A;
  --hum-lime-dark: #C8D67E;
  --hum-blue: #83ECFF;
  --hum-blue-dark: #55A7B6;
  --hum-orange: #EF6B2C;
  --hum-orange-dark: #A33200;
  --hum-gray-1: #F5F4F1;
  --hum-gray-2: #EEECE8;
  --hum-gray-3: #D6D4D1;
  --hum-gray-4: #BEBDBA;
  --hum-gray-5: #A7A5A2;
  --hum-gray-6: #8F8E8B;
  --hum-gray-7: #777674;
  --hum-gray-8: #5F5E5D;
  --hum-gray-9: #302F2E;
  --hum-gray-10: #181817;
}
```

### Gradient Application

- Optimist Green Light: `linear-gradient(135deg, #EDFD9A, #81F2B2)`
- Optimist Green Dark: `linear-gradient(135deg, #173A31, #55A7B6)`
- Use gradients sparingly for hero sections, banners, and feature highlight backgrounds — they pop against the dark default
