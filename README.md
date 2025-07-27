# VBS3 Project - TestVBS

An interactive HTML/CSS/JavaScript project showcasing VBS3 (Virtual Battlespace 3) within the New Zealand Defence Force Royal New Zealand Artillery (NZDF RNZA).

## Project Overview

This educational project demonstrates fundamental web development concepts including responsive design, interactive elements, and multimedia integration. Built as a learning tool for HTML, CSS, and JavaScript development.

## Features

- 🎯 **Interactive UI**: Button-driven content updates
- 📱 **Responsive Design**: Flexbox-based layout system  
- 🖼️ **Media Integration**: Military equipment imagery and backgrounds
- 🔗 **External Navigation**: Links to training resources
- 📊 **Modular Architecture**: 8-module grid display system

## Quick Start

1. Navigate to the `VBS test` directory
2. Open `VBS.htm` in your web browser
3. Click the "Press" button to see the interactive functionality
4. Explore the modular grid layout

## Documentation

📚 **Complete documentation is available in the following files:**

- **[API Documentation](API_DOCUMENTATION.md)** - Comprehensive API reference for all components, functions, and styling
- **[Component Reference](COMPONENT_REFERENCE.md)** - Detailed specifications for reusable components
- **[Developer Guide](DEVELOPER_GUIDE.md)** - Setup instructions, usage examples, and best practices

## File Structure

```
VBS3 Project/
├── README.md                    # This file
├── LICENSE                      # Project license
├── API_DOCUMENTATION.md         # Complete API documentation
├── COMPONENT_REFERENCE.md       # Component specifications  
├── DEVELOPER_GUIDE.md          # Development guide
└── VBS test/                   # Main project directory
    ├── VBS.htm                 # Main HTML file (1.5KB)
    ├── VBS button.js           # JavaScript file
    ├── Guns.PNG               # Military equipment image (1.7MB)
    └── maxresdefault.jpg      # Background image (85KB)
```

## Technology Stack

- **HTML5**: Semantic markup and structure
- **CSS3**: Flexbox layouts and responsive design
- **Vanilla JavaScript**: Interactive functionality and DOM manipulation
- **No external dependencies**: Pure web technologies

## Browser Support

- ✅ Chrome (latest)
- ✅ Firefox (latest) 
- ✅ Safari (latest)
- ✅ Edge (latest)
- ✅ IE 11+ (legacy support)

## Key Components

### Interactive Elements
- **Text Display**: Dynamic content updates (`VBS3` → `VBS4`)
- **Action Button**: Triggers system upgrade functionality
- **Flex Grid**: 8-module responsive layout system
- **External Link**: Navigation to training resources

### Styling Features
- **Typography**: Arial-based font system
- **Layout**: CSS Flexbox container with 8 divisions
- **Background**: Military training environment imagery
- **Color Scheme**: Semi-transparent overlays with military aesthetic

### JavaScript Functionality
- **DOM Manipulation**: Element content updates
- **Event Handling**: Button click interactions
- **Error Handling**: Robust element targeting

## Getting Started for Developers

### Prerequisites
- Web browser (any modern browser)
- Text editor or IDE
- Basic knowledge of HTML/CSS/JavaScript

### Development Setup
```bash
# Clone the repository
git clone [repository-url]

# Navigate to project directory  
cd "VBS test"

# Open in browser
open VBS.htm  # macOS
xdg-open VBS.htm  # Linux
start VBS.htm  # Windows
```

### Making Changes
1. Edit `VBS.htm` for structure and content
2. Modify CSS within `<style>` blocks for styling
3. Update JavaScript in `<script>` blocks for functionality
4. Refresh browser to see changes

## API Usage Examples

### Basic Function Call
```javascript
// Trigger system upgrade
myFunction(); // Updates display from "VBS3" to "Now VBS4."
```

### DOM Element Access
```javascript
// Access display element
const element = document.getElementById("VBS3");
element.innerHTML = "Custom content";
```

### Flex Container Usage
```html
<div class="flex-container">
    <div>Module 1</div>
    <div>Module 2</div>
    <!-- Additional modules -->
</div>
```

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test across browsers
5. Submit a pull request

## Performance Notes

- **Image Optimization**: Large images (1.7MB PNG) may benefit from compression
- **CSS Efficiency**: Inline styles used for simplicity, consider external stylesheets for larger projects
- **JavaScript Performance**: Minimal DOM manipulation ensures fast execution

## Educational Value

This project serves as an excellent learning resource for:
- HTML5 semantic structure
- CSS3 flexbox layouts
- Vanilla JavaScript DOM manipulation
- Responsive web design principles
- Military simulation system interfaces

## License

See [LICENSE](LICENSE) file for details.

## Support

For technical documentation, refer to:
- [API_DOCUMENTATION.md](API_DOCUMENTATION.md) for complete API reference
- [COMPONENT_REFERENCE.md](COMPONENT_REFERENCE.md) for component details
- [DEVELOPER_GUIDE.md](DEVELOPER_GUIDE.md) for development guidance

---

*Built as an educational project demonstrating web development fundamentals with military simulation system theming.*