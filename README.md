# Engazwell - Advanced Online Code Editor & Compiler

A modern, fully responsive online code editor and compiler built with React, TypeScript, and Tailwind CSS. Execute code in multiple programming languages with real-time feedback, intelligent code analysis, and comprehensive testing capabilities.

## 🚀 Features

### 💻 **Multi-Language Support**
- **Python** - Interactive programming with full I/O support
- **JavaScript** - Browser-based execution environment
- **C++** - Compiled language with performance metrics
- **C** - System programming capabilities
- **Java** - Object-oriented programming support

### 🎨 **Modern Responsive UI/UX**
- **Fully Responsive Design** - Optimized for mobile, tablet, and desktop
- **Adaptive Layouts** - Smart layout switching based on screen size
- **Dark Theme** - Professional dark interface with syntax highlighting
- **Monaco Editor** - VS Code-like editing experience with IntelliSense
- **Touch Optimized** - Enhanced mobile and tablet interactions

### ⚡ **Smart Development Features**
- **Real-time Code Analysis** - Instant error detection and suggestions
- **Auto-completion** - Language-specific code suggestions and snippets
- **Intelligent Warnings** - Code quality improvements and best practices
- **Problem-Based Learning** - Structured coding challenges with test cases
- **Custom Test Cases** - Add your own test scenarios

### 📱 **Mobile-First Experience**
- **Touch-friendly Interface** - Optimized for mobile devices
- **Tabbed Navigation** - Easy switching between problem, editor, and results
- **Responsive Text Sizing** - Proper font scaling across devices
- **Mobile Menu** - Collapsible action menu for small screens
- **Gesture Support** - Natural touch scrolling and selection

### 🧪 **Advanced Testing System**
- **Automated Test Cases** - Pre-built test scenarios for each problem
- **Custom Test Creation** - Add personalized test cases
- **Detailed Results** - Comprehensive test execution feedback
- **Performance Metrics** - Execution time and memory usage tracking
- **Batch Testing** - Run multiple test cases simultaneously

## 🛠️ Tech Stack

- **Frontend**: React 18 + TypeScript
- **Styling**: Tailwind CSS with custom responsive utilities
- **Editor**: Monaco Editor (VS Code engine)
- **Icons**: Lucide React
- **Build Tool**: Vite with optimized bundling
- **Code Execution**: Judge0 API integration
- **Linting**: ESLint + TypeScript ESLint
- **Error Handling**: React Error Boundaries

## 🚀 Getting Started

### Prerequisites
- Node.js 18+ 
- npm or yarn
- Modern web browser

### Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd engazwell
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Start development server**
   ```bash
   npm run dev
   ```

4. **Open in browser**
   ```
   http://localhost:5173
   ```

### Available Scripts

- `npm run dev` - Start development server with hot reload
- `npm run build` - Build optimized production bundle
- `npm run preview` - Preview production build locally
- `npm run lint` - Run ESLint with TypeScript support

## 📁 Project Structure

```
src/
├── components/              # React components
│   ├── Header.tsx          # Navigation and actions
│   ├── LanguageSelector.tsx # Language dropdown
│   ├── ProblemSelector.tsx  # Problem selection
│   ├── CodeEditor.tsx      # Monaco editor wrapper
│   ├── ProblemDescription.tsx # Problem details
│   ├── TestResults.tsx     # Test execution results
│   ├── AddTestCaseModal.tsx # Custom test creation
│   └── ErrorBoundary.tsx   # Error handling
├── constants/              # Static configurations
│   ├── languages.ts        # Supported languages
│   └── problems.ts         # Coding problems
├── services/               # API integrations
│   ├── judge0.ts          # Code execution service
│   └── testRunner.ts      # Test management
├── types/                 # TypeScript definitions
│   └── index.ts           # Type definitions
├── utils/                 # Utility functions
│   └── codeAnalyzer.ts    # Code analysis logic
├── App.tsx                # Main application
├── main.tsx              # Application entry point
└── index.css             # Global styles & responsive utilities
```

## 🎯 Usage Guide

### Getting Started
1. **Select a Problem** - Choose from available coding challenges
2. **Pick Your Language** - Select from Python, JavaScript, C++, C, or Java
3. **Write Your Solution** - Use the Monaco editor with syntax highlighting
4. **Test Your Code** - Run individual tests or full test suites
5. **Add Custom Tests** - Create additional test cases for thorough validation

### Code Analysis Features
- **🟢 Green Checkmark**: No issues detected
- **🟡 Yellow Warning**: Potential improvements suggested
- **🔴 Red Error**: Syntax or logic errors found
- **🔵 Blue Lightbulb**: Helpful coding tips and best practices

### Responsive Breakpoints
- **Mobile**: < 768px (stacked tabbed layout)
- **Tablet**: 768px - 1024px (adaptive side-by-side)
- **Desktop**: > 1024px (full three-panel layout)
- **Large Desktop**: > 1440px (expanded problem panel)

### Mobile Features
- **Tabbed Interface** - Problem, Editor, and Results tabs
- **Collapsible Menu** - Action buttons in mobile menu
- **Touch Optimized** - 44px minimum touch targets
- **Auto-switching** - Smart tab switching after code execution

## 🔧 Configuration

### Adding New Languages
Edit `src/constants/languages.ts`:

```typescript
{
  id: 999,              // Judge0 language ID
  name: 'New Language', // Display name
  extension: 'ext',     // File extension
  template: `// Default code template`
}
```

### Creating New Problems
Add to `src/constants/problems.ts`:

```typescript
'problem-id': {
  id: 'problem-id',
  title: 'Problem Title',
  description: 'Detailed problem description...',
  inputFormat: 'Input specification',
  outputFormat: 'Output specification',
  examples: [{ input: '...', output: '...', explanation: '...' }],
  testCases: [{ input: '...', expectedOutput: '...', description: '...' }],
  sampleSolutions: { [languageId]: 'solution code...' }
}
```

### Customizing Responsive Behavior
Modify breakpoints in `src/index.css`:

```css
/* Custom responsive utilities */
@media (max-width: 767px) { /* Mobile styles */ }
@media (min-width: 768px) and (max-width: 1023px) { /* Tablet styles */ }
@media (min-width: 1024px) { /* Desktop styles */ }
```

## 🌐 API Integration

### Judge0 Configuration
The application uses Judge0 API for code execution. Configure in `src/services/judge0.ts`:

```typescript
const JUDGE0_API_BASE = 'https://judge0-ce.p.rapidapi.com';
const RAPIDAPI_KEY = 'your_api_key_here';
```

**Production Setup**: Use environment variables:
```bash
VITE_JUDGE0_API_KEY=your_api_key_here
VITE_JUDGE0_API_BASE=https://your-judge0-instance.com
```

### Supported Judge0 Language IDs
- Python: 71
- JavaScript: 63
- C++: 54
- C: 50
- Java: 62

## 📱 Mobile Optimization Features

### Performance Optimizations
- **Lazy Loading** - Components loaded on demand
- **Optimized Scrolling** - Smooth scrolling with momentum
- **Touch Gestures** - Native touch interactions
- **Viewport Management** - Proper mobile viewport handling

### Accessibility Features
- **Keyboard Navigation** - Full keyboard support
- **Screen Reader Support** - ARIA labels and descriptions
- **High Contrast** - Accessible color combinations
- **Focus Management** - Proper focus indicators

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Follow the coding standards and responsive design principles
4. Test on multiple devices and screen sizes
5. Commit your changes (`git commit -m 'Add amazing responsive feature'`)
6. Push to the branch (`git push origin feature/amazing-feature`)
7. Open a Pull Request

### Development Guidelines
- **Mobile-First**: Design for mobile, enhance for desktop
- **Performance**: Optimize for slower mobile connections
- **Accessibility**: Ensure WCAG 2.1 compliance
- **Testing**: Test across different devices and browsers

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- [Judge0](https://judge0.com/) - Robust code execution API
- [Monaco Editor](https://microsoft.github.io/monaco-editor/) - Powerful code editor
- [Tailwind CSS](https://tailwindcss.com/) - Utility-first CSS framework
- [Lucide](https://lucide.dev/) - Beautiful icon library
- [React](https://reactjs.org/) - Modern UI library
- [Vite](https://vitejs.dev/) - Fast build tool

---

**Built with ❤️ using modern web technologies and responsive design principles**

### Recent Updates
- ✅ Fully responsive design across all devices
- ✅ Enhanced mobile experience with tabbed navigation
- ✅ Improved tablet layout with adaptive panels
- ✅ Advanced code analysis and suggestions
- ✅ Custom test case creation
- ✅ Performance optimizations for mobile devices
- ✅ Accessibility improvements
- ✅ Touch-optimized interactions