# VBS3 Project - Comprehensive API Documentation

## Table of Contents
- [Project Overview](#project-overview)
- [HTML Components](#html-components)
- [CSS Styling Components](#css-styling-components)
- [JavaScript Functions](#javascript-functions)
- [Assets and Resources](#assets-and-resources)
- [Usage Examples](#usage-examples)
- [File Structure](#file-structure)

## Project Overview

**TestVBS** is an HTML-based learning project focused on VBS3 (Virtual Battlespace 3) within the New Zealand Defence Force Royal New Zealand Artillery (NZDF RNZA). The project demonstrates basic web development concepts including responsive design, interactive elements, and multimedia integration.

### Purpose
- Educational tool for learning HTML, CSS, and JavaScript
- Showcase VBS3 military simulation system
- Interactive demonstration of web technologies

## HTML Components

### Main Document Structure

#### Document Type and Meta Information
```html
<!DOCTYPE html>
<html lang="en-US">
<title> "VBS3 lives On" </title>
<meta charset="UTF-8">
```

**Description**: Standard HTML5 document structure with UTF-8 encoding and English language specification.

**Usage**: This forms the foundation of the web page and ensures proper rendering across browsers.

### Header Component

#### Main Title
```html
<h1 style="text-align:center;color: black;font-size:60px;">
  VBS3 within <br> the NZDF RNZA  
</h1>
```

**Properties**:
- **Alignment**: Center-aligned
- **Color**: Black
- **Font Size**: 60px
- **Content**: Multi-line title with line break

**Usage**: Primary heading that introduces the VBS3 system within the military context.

### Interactive Components

#### Flex Container Grid
```html
<div class="flex-container">
  <div>1 <img src="Guns.PNG" alt="L119 is the Gun" width="46" height="34"></div>  
  <div>2</div>
  <!-- ... additional numbered divisions 3-8 -->
</div>
```

**Properties**:
- **Type**: Flexible grid layout
- **Items**: 8 numbered divisions
- **Special Content**: Division 1 contains an embedded image of military equipment

**API Methods**:
- Responsive layout adjustment based on screen size
- Automatic spacing and alignment

#### Text Display Element
```html
<p id="VBS3">VBS3</p>
```

**Properties**:
- **ID**: `VBS3`
- **Default Content**: "VBS3"
- **Functionality**: Target for JavaScript manipulation

#### Interactive Button
```html
<button type="button" onclick="myFunction()">Press</button>
```

**Properties**:
- **Type**: Button element
- **Event Handler**: `onclick="myFunction()"`
- **Label**: "Press"

**API Methods**:
- `click()`: Triggers the associated JavaScript function

#### External Link
```html
<a href="https://gaz-learning.w3spaces.com" 
   style="text-align:center;color: rgba(252, 250, 250, 0.602);font-size:30px;">
   Visit Gaz's Training Page
</a>
```

**Properties**:
- **Target URL**: https://gaz-learning.w3spaces.com
- **Style**: Center-aligned, light colored text, 30px font size
- **Purpose**: External navigation to training resources

## CSS Styling Components

### Typography Styles

#### Font Family Definition
```css
body, h1, h2, h3, h4, h5, h6 {
  font-family: Arial;
}
```

**Scope**: All body text and headings
**Font**: Arial sans-serif family

### Layout Components

#### Flex Container
```css
.flex-container {
  display: flex;
  flex-wrap: nowrap;
  background-color: rgba(100, 123, 138, 0);
}
```

**Properties**:
- **Display**: Flexible box layout
- **Wrap**: No wrapping (single line)
- **Background**: Transparent blue-gray

**Usage Example**:
```html
<div class="flex-container">
  <!-- Child elements will be arranged horizontally -->
</div>
```

#### Flex Items
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

**Properties**:
- **Background**: Semi-transparent light brown (#cab1b144)
- **Dimensions**: 100px width, 75px line height
- **Spacing**: 10px margin on all sides
- **Alignment**: Center-aligned text
- **Typography**: 30px font size

### Background Styling

#### Background Image Component
```css
body {
  background-image: url("maxresdefault.jpg");
  background-repeat: no-repeat;
  background-size: auto;
}
```

**Properties**:
- **Image Source**: maxresdefault.jpg
- **Repeat**: No repetition
- **Size**: Automatic sizing

**Usage**: Provides visual context with background imagery

## JavaScript Functions

### Primary Interactive Function

#### `myFunction()`
```javascript
function myFunction() {
  document.getElementById("VBS3").innerHTML = "Now VBS4." 
}
```

**Purpose**: Updates text content to demonstrate system evolution from VBS3 to VBS4

**Parameters**: None

**Return Value**: `undefined`

**Side Effects**: 
- Modifies the DOM element with ID "VBS3"
- Changes display text from "VBS3" to "Now VBS4."

**Usage Example**:
```html
<!-- HTML Setup -->
<p id="VBS3">VBS3</p>
<button type="button" onclick="myFunction()">Press</button>

<!-- Result after button click -->
<p id="VBS3">Now VBS4.</p>
```

**API Methods Called**:
- `document.getElementById(elementId)`: Retrieves DOM element by ID
- `element.innerHTML`: Sets or gets HTML content of element

## Assets and Resources

### Image Assets

#### Military Equipment Image
- **Filename**: `Guns.PNG`
- **Size**: 1.7MB
- **Dimensions in use**: 46px × 34px
- **Alt Text**: "L119 is the Gun"
- **Purpose**: Visual representation of L119 artillery piece
- **Usage**: Embedded in flex container division 1

#### Background Image
- **Filename**: `maxresdefault.jpg`
- **Size**: 85KB
- **Purpose**: Page background providing military/training context
- **Implementation**: CSS background-image property

### External JavaScript
- **Filename**: `VBS button.js`
- **Status**: Currently empty (2 lines, no content)
- **Purpose**: Intended for additional JavaScript functionality

## Usage Examples

### Complete Implementation Example

```html
<!DOCTYPE html>
<html lang="en-US">
<head>
    <title>"VBS3 lives On"</title>
    <meta charset="UTF-8">
    <style>
        /* Include all CSS components as documented above */
    </style>
</head>
<body>
    <!-- Main title -->
    <h1 style="text-align:center;color: black;font-size:60px;">
        VBS3 within <br> the NZDF RNZA  
    </h1>
    
    <!-- Interactive grid -->
    <div class="flex-container">
        <div>1 <img src="Guns.PNG" alt="L119 is the Gun" width="46" height="34"></div>
        <div>2</div>
        <!-- ... additional divisions -->
    </div>
    
    <!-- Interactive elements -->
    <p id="VBS3">VBS3</p>
    <button type="button" onclick="myFunction()">Press</button>
    
    <!-- External link -->
    <a href="https://gaz-learning.w3spaces.com">Visit Gaz's Training Page</a>
    
    <script>
        function myFunction() {
            document.getElementById("VBS3").innerHTML = "Now VBS4.";
        }
    </script>
</body>
</html>
```

### JavaScript API Usage

```javascript
// Accessing the text change function
myFunction(); // Changes "VBS3" to "Now VBS4."

// Alternative programmatic usage
document.getElementById("VBS3").innerHTML = "Custom text";

// Button click simulation
document.querySelector('button').click();
```

### CSS Customization Examples

```css
/* Modify flex container background */
.flex-container {
    background-color: rgba(200, 200, 200, 0.5);
}

/* Customize flex items */
.flex-container > div {
    background-color: #newcolor;
    width: 120px;
    font-size: 25px;
}

/* Alternative background styling */
body {
    background-image: url("custom-background.jpg");
    background-size: cover;
}
```

## File Structure

```
/workspace/
├── README.md                 # Basic project description
├── LICENSE                   # Project license (1.0KB)
└── VBS test/                 # Main project directory
    ├── VBS.htm              # Main HTML file (1.5KB, 91 lines)
    ├── VBS button.js        # JavaScript file (currently empty)
    ├── Guns.PNG             # Military equipment image (1.7MB)
    └── maxresdefault.jpg    # Background image (85KB)
```

## Browser Compatibility

- **HTML5**: Compatible with all modern browsers
- **CSS Flexbox**: Supported in IE 11+, Chrome, Firefox, Safari
- **JavaScript**: ES5 compatible, works in all browsers

## Dependencies

- **External Dependencies**: None
- **Font Dependencies**: Arial (system font)
- **Image Dependencies**: Local PNG and JPG files

## License

Please refer to the LICENSE file in the project root for licensing information.

---

*This documentation covers all public APIs, functions, and components available in the TestVBS project. For additional examples or clarification, refer to the source code in the VBS test directory.*