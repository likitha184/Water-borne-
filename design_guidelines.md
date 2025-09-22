# Smart Community Health Monitoring - Design Guidelines

## Design Approach
**Reference-Based Approach**: Drawing inspiration from health-focused platforms like WHO dashboards and emergency response systems, combined with clean utility interfaces like Linear and Notion for optimal usability in health monitoring scenarios.

## Core Design Elements

### A. Color Palette
**Primary Colors:**
- Blue: 215 85% 45% (trust, healthcare reliability)
- Green: 142 75% 50% (safety, health positive indicators)
- Dark mode backgrounds: 220 15% 8%
- Light mode backgrounds: 0 0% 98%

**Supporting Colors:**
- Alert red: 0 75% 55% (outbreak warnings)
- Warning amber: 35 85% 55% (moderate risk)
- Text primary: 220 25% 15% (light) / 220 15% 85% (dark)
- Text secondary: 220 15% 45% (light) / 220 10% 65% (dark)

### B. Typography
**Primary Font**: Inter (Google Fonts)
- Headers: 600-700 weight, sizes from text-lg to text-4xl
- Body: 400-500 weight, text-sm to text-base
- Data/numbers: 500-600 weight for emphasis

### C. Layout System
**Spacing Primitives**: Tailwind units 2, 4, 6, 8, 12, 16
- Card padding: p-6
- Section spacing: py-12 or py-16
- Element gaps: gap-4 or gap-6
- Container max-width: max-w-7xl

### D. Component Library

**Cards**: Rounded corners (rounded-xl), subtle shadows (shadow-sm), clean borders. Health status cards use color-coded left borders.

**Forms**: Clean input styling with focus states, multi-select dropdowns for symptoms, clear validation states.

**Navigation**: Sticky header with logo, clean link styling, mobile hamburger menu.

**Buttons**: 
- Primary: Blue background, white text
- Secondary: Outline variant with blue border
- CTA: Prominent sizing with subtle animations

**Data Visualization**: Card-based heatmap style for dashboard metrics, color-coded status indicators.

### E. Interactive Elements
**Hover Effects**: Subtle scale transforms (scale-105) on cards, smooth transitions (transition-all duration-200).

**Loading States**: Spinner component for form submissions, skeleton loading for dashboard data.

**Icons**: Lucide React icons (alert-triangle, droplet, activity, bell) with consistent sizing (w-5 h-5 for inline, w-6 h-6 for emphasis).

## Page-Specific Design Notes

**Homepage**: Hero section with background image overlay, prominent "Report Now" CTA, three feature cards in responsive grid.

**Dashboard**: Map placeholder with clean container, metric cards with large numbers and descriptive labels, villages at risk as a clean list component.

**Awareness**: Card grid layout (3 columns desktop, 1-2 mobile), language toggle in header, clear iconography for health tips.

**Report Form**: Single column layout, grouped form sections, clear progress indication, success/error states.

## Images
**Hero Background**: Use the provided health monitoring background image with a dark overlay (bg-black/40) to ensure text readability. Place hero content over this background with proper contrast.

**Map Placeholder**: Static image or Leaflet integration showing regional view with health data points.

**Awareness Cards**: Simple health-related icons or illustrations to support text content.

## Responsiveness
Mobile-first approach with breakpoints at sm (640px), md (768px), lg (1024px). Ensure touch-friendly interactive elements (min 44px tap targets) and readable text sizes across devices.