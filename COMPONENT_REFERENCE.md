# Component Reference Guide

## Overview
This document provides detailed technical specifications for all reusable components in the VBS3 project.

## HTML Components

### FlexContainer Component

#### Description
A responsive container that arranges child elements in a horizontal layout using CSS Flexbox.

#### Specification
```html
<div class="flex-container">
  <!-- Child elements -->
</div>
```

#### Properties
| Property | Type | Default | Description |
|----------|------|---------|-------------|
| `display` | string | `flex` | Defines the container as a flex container |
| `flex-wrap` | string | `nowrap` | Prevents child elements from wrapping |
| `background-color` | color | `rgba(100, 123, 138, 0)` | Transparent background |

#### Child Element Specifications
```css
.flex-container > div {
  background-color: #cab1b144;
  width: 100px;
  margin: 10px;
  text-align: center;
  line-height: 75px;
  font-size: 30px;
}
```

#### Usage Example
```html
<div class="flex-container">
  <div>Item 1</div>
  <div>Item 2</div>
  <div>Item 3</div>
</div>
```

#### API Methods
- **Responsive Behavior**: Automatically adjusts spacing based on container width
- **Child Alignment**: Centers content both horizontally and vertically
- **Overflow Handling**: Maintains single-line layout regardless of content

---

### InteractiveButton Component

#### Description
A button component that triggers JavaScript functions and provides user interaction.

#### Specification
```html
<button type="button" onclick="functionName()">Button Text</button>
```

#### Properties
| Property | Type | Required | Description |
|----------|------|----------|-------------|
| `type` | string | Yes | Must be "button" for non-form buttons |
| `onclick` | function | Yes | JavaScript function to execute on click |
| `textContent` | string | Yes | Display text for the button |

#### Events
- **click**: Triggered when button is pressed
- **focus**: Triggered when button receives focus
- **blur**: Triggered when button loses focus

#### Usage Example
```html
<!-- Basic button -->
<button type="button" onclick="myFunction()">Press</button>

<!-- Button with custom styling -->
<button type="button" 
        onclick="customFunction()" 
        style="background-color: blue; color: white;">
  Custom Button
</button>
```

#### Accessibility Features
- Keyboard navigation support (Tab, Enter, Space)
- Screen reader compatible
- Focus indicators

---

### TextDisplay Component

#### Description
A paragraph element that serves as a target for dynamic content updates.

#### Specification
```html
<p id="uniqueId">Initial Text</p>
```

#### Properties
| Property | Type | Required | Description |
|----------|------|----------|-------------|
| `id` | string | Yes | Unique identifier for JavaScript targeting |
| `textContent` | string | No | Initial display text |

#### API Methods
- `getElementById(id)`: Access element by ID
- `innerHTML`: Get/set HTML content
- `textContent`: Get/set plain text content

#### Usage Example
```html
<!-- HTML -->
<p id="status">Ready</p>

<!-- JavaScript manipulation -->
<script>
document.getElementById("status").innerHTML = "Processing...";
document.getElementById("status").textContent = "Complete";
</script>
```

---

### NavigationLink Component

#### Description
External link component with custom styling for navigation to external resources.

#### Specification
```html
<a href="url" style="styling">Link Text</a>
```

#### Properties
| Property | Type | Required | Description |
|----------|------|----------|-------------|
| `href` | URL | Yes | Target URL for navigation |
| `style` | CSS | No | Inline styling properties |
| `target` | string | No | Window/frame target (_blank, _self, etc.) |

#### Default Styling
```css
style="text-align:center;
       color: rgba(252, 250, 250, 0.602);
       font-size:30px;"
```

#### Usage Example
```html
<!-- Basic external link -->
<a href="https://example.com">Visit Example</a>

<!-- Styled external link -->
<a href="https://training.site.com" 
   style="color: white; font-size: 24px;">
   Training Resources
</a>

<!-- Link opening in new tab -->
<a href="https://docs.site.com" target="_blank">
   Documentation
</a>
```

---

### ImageDisplay Component

#### Description
Image component for displaying visual content with accessibility features.

#### Specification
```html
<img src="filename" alt="description" width="number" height="number">
```

#### Properties
| Property | Type | Required | Description |
|----------|------|----------|-------------|
| `src` | string | Yes | Image file path or URL |
| `alt` | string | Yes | Alternative text for accessibility |
| `width` | number | No | Display width in pixels |
| `height` | number | No | Display height in pixels |

#### Usage Example
```html
<!-- Basic image -->
<img src="image.png" alt="Description">

<!-- Sized image -->
<img src="equipment.PNG" 
     alt="L119 Artillery Piece" 
     width="46" 
     height="34">

<!-- Responsive image -->
<img src="background.jpg" 
     alt="Training Environment" 
     style="max-width: 100%; height: auto;">
```

#### Best Practices
- Always include meaningful `alt` text
- Use appropriate file formats (PNG for graphics, JPG for photos)
- Consider loading performance for large images
- Implement responsive sizing when needed

## CSS Component Classes

### .flex-container

#### Purpose
Creates a horizontal layout container using CSS Flexbox.

#### CSS Definition
```css
.flex-container {
  display: flex;
  flex-wrap: nowrap;
  background-color: rgba(100, 123, 138, 0);
}
```

#### Modifiers
```css
/* Add spacing */
.flex-container.spaced {
  gap: 20px;
}

/* Vertical alignment */
.flex-container.centered {
  align-items: center;
  justify-content: center;
}

/* Responsive wrap */
.flex-container.responsive {
  flex-wrap: wrap;
}
```

#### Browser Support
- Chrome 29+
- Firefox 28+
- Safari 9+
- IE 11+

### Typography Classes

#### Global Font Styling
```css
body, h1, h2, h3, h4, h5, h6 {
  font-family: Arial;
}
```

#### Custom Typography
```css
/* Large headers */
.main-title {
  text-align: center;
  color: black;
  font-size: 60px;
}

/* Navigation links */
.nav-link {
  text-align: center;
  color: rgba(252, 250, 250, 0.602);
  font-size: 30px;
}
```

## JavaScript Component Functions

### myFunction()

#### Purpose
Updates the content of the VBS3 text display to show system evolution.

#### Function Signature
```javascript
function myFunction(): void
```

#### Implementation
```javascript
function myFunction() {
  document.getElementById("VBS3").innerHTML = "Now VBS4.";
}
```

#### Parameters
None

#### Return Value
`undefined`

#### Side Effects
- Modifies DOM element with ID "VBS3"
- Changes display text to "Now VBS4."

#### Error Handling
```javascript
function myFunction() {
  const element = document.getElementById("VBS3");
  if (element) {
    element.innerHTML = "Now VBS4.";
  } else {
    console.error("Element with ID 'VBS3' not found");
  }
}
```

#### Usage Examples
```javascript
// Direct function call
myFunction();

// Event-driven call
document.querySelector('button').addEventListener('click', myFunction);

// Conditional call
if (userAction === 'upgrade') {
  myFunction();
}
```

## Component Integration Examples

### Complete Interactive Section
```html
<section class="interactive-demo">
  <!-- Status display -->
  <p id="systemStatus">VBS3</p>
  
  <!-- Action button -->
  <button type="button" onclick="upgradeSystem()">
    Upgrade System
  </button>
  
  <!-- Visual feedback -->
  <div class="flex-container">
    <div class="status-indicator">Ready</div>
    <div class="system-version">3.0</div>
  </div>
  
  <!-- External resources -->
  <a href="https://training.example.com" 
     class="resource-link">
     Access Training Materials
  </a>
</section>

<script>
function upgradeSystem() {
  // Update status
  document.getElementById("systemStatus").innerHTML = "VBS4";
  
  // Update visual indicators
  document.querySelector('.system-version').textContent = "4.0";
  document.querySelector('.status-indicator').textContent = "Upgraded";
  
  // Provide feedback
  console.log("System upgraded successfully");
}
</script>

<style>
.interactive-demo {
  padding: 20px;
  text-align: center;
}

.status-indicator, .system-version {
  background-color: #4CAF50;
  color: white;
  padding: 10px;
  margin: 5px;
  border-radius: 5px;
}

.resource-link {
  display: block;
  margin-top: 20px;
  color: #007BFF;
  text-decoration: none;
}
</style>
```

## Performance Considerations

### Image Optimization
- **Large images**: Consider compression for files > 1MB
- **Loading strategy**: Implement lazy loading for non-critical images
- **Format selection**: Use WebP where supported, fallback to PNG/JPG

### CSS Performance
- **Flexbox**: Minimal performance impact, excellent browser support
- **Inline styles**: Consider moving to external stylesheets for better caching
- **Selector efficiency**: Current selectors are optimized

### JavaScript Performance
- **DOM manipulation**: Current implementation is efficient for small-scale changes
- **Event handling**: Consider event delegation for multiple similar elements
- **Memory management**: No memory leaks in current implementation

## Testing Guidelines

### Component Testing
```javascript
// Test button functionality
function testButtonInteraction() {
  const initialText = document.getElementById("VBS3").innerHTML;
  myFunction();
  const updatedText = document.getElementById("VBS3").innerHTML;
  
  console.assert(updatedText === "Now VBS4.", "Text update failed");
}

// Test flex container layout
function testFlexLayout() {
  const container = document.querySelector('.flex-container');
  const computedStyle = window.getComputedStyle(container);
  
  console.assert(computedStyle.display === 'flex', "Flex display not applied");
}
```

### Browser Testing Matrix
- Chrome (latest 2 versions)
- Firefox (latest 2 versions)
- Safari (latest 2 versions)
- Edge (latest 2 versions)
- IE 11 (legacy support)

---

*This component reference provides detailed specifications for all reusable components in the VBS3 project. Use this guide for implementation, customization, and testing.*