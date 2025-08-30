# Kartikey Dwivedi - Data Engineer Portfolio

A modern, professional portfolio website showcasing Data Engineering expertise with dark/light mode themes, responsive design, and smooth animations.

## ✨ Features

- **Dark/Light Mode Toggle** - Seamless theme switching with persistent preferences
- **Responsive Design** - Optimized for all devices (mobile, tablet, desktop)
- **Interactive Sections** - Hero, About, Skills, Projects, Certifications, Resume, Contact
- **Smooth Animations** - Particle background, floating elements, and transition effects
- **Contact Form** - Functional contact form with validation
- **Resume Download** - Direct PDF download functionality
- **Modern UI/UX** - Clean, professional design with accessibility features

## 🛠️ Tech Stack

### Frontend
- **React 18** - Modern React with functional components and hooks
- **TypeScript** - Type-safe JavaScript for better development experience
- **Vite** - Fast build tool and development server
- **Tailwind CSS** - Utility-first CSS framework for rapid styling
- **Wouter** - Lightweight client-side routing
- **TanStack Query** - Data fetching and state management
- **React Hook Form** - Form handling with validation
- **Radix UI** - Accessible component primitives
- **Lucide React** - Beautiful, customizable icons

### Backend
- **Express.js** - Web application framework
- **Node.js** - JavaScript runtime
- **TypeScript** - Type safety on the backend

### UI Components
- **shadcn/ui** - Beautifully designed, accessible components
- **Framer Motion** - Animation library (via CSS animations)
- **Custom Particle System** - Animated background effects

## 📋 Prerequisites

Before running this project, make sure you have the following installed:

- **Node.js** (version 18 or higher) - [Download here](https://nodejs.org/)
- **npm** or **yarn** package manager
- **VS Code** - [Download here](https://code.visualstudio.com/)

### Recommended VS Code Extensions

Install these extensions for the best development experience:

1. **ES7+ React/Redux/React-Native snippets** - Provides helpful React snippets
2. **TypeScript Importer** - Auto imports for TypeScript
3. **Tailwind CSS IntelliSense** - Intelligent autocomplete for Tailwind classes
4. **Prettier** - Code formatter
5. **ESLint** - JavaScript linter
6. **Auto Rename Tag** - Automatically renames paired HTML/JSX tags
7. **Bracket Pair Colorizer** - Makes matching brackets easier to identify
8. **GitLens** - Enhanced Git capabilities

## 🚀 Getting Started

### 1. Download/Clone the Project

#### Option A: Download from Replit
1. In Replit, click on the menu (three dots) next to your repl name
2. Select "Download as zip"
3. Extract the zip file to your desired location

#### Option B: Clone from Git (if available)
```bash
git clone <repository-url>
cd kartikey-portfolio
```

### 2. Open in VS Code
```bash
cd path/to/your/project
code .
```

### 3. Install Dependencies
```bash
npm install
```

### 4. Environment Setup
Create a `.env` file in the root directory (optional for basic functionality):
```env
NODE_ENV=development
PORT=5000
```

### 5. Start Development Server
```bash
npm run dev
```

The application will start on `http://localhost:5000`

## 📁 Project Structure

```
kartikey-portfolio/
├── client/                 # Frontend React application
│   ├── src/
│   │   ├── components/     # Reusable UI components
│   │   │   ├── ui/         # shadcn/ui components
│   │   │   ├── about-section.tsx
│   │   │   ├── certifications-section.tsx
│   │   │   ├── contact-section.tsx
│   │   │   ├── footer.tsx
│   │   │   ├── hero-section.tsx
│   │   │   ├── navigation.tsx
│   │   │   ├── particles-background.tsx
│   │   │   ├── projects-section.tsx
│   │   │   ├── resume-section.tsx
│   │   │   ├── skills-section.tsx
│   │   │   └── theme-provider.tsx
│   │   ├── hooks/          # Custom React hooks
│   │   ├── lib/            # Utilities and configurations
│   │   ├── pages/          # Page components
│   │   ├── App.tsx         # Main App component
│   │   ├── main.tsx        # React app entry point
│   │   └── index.css       # Global styles
│   └── index.html          # HTML template
├── server/                 # Backend Express server
│   ├── index.ts            # Server entry point
│   ├── routes.ts           # API routes
│   ├── storage.ts          # Data storage interface
│   └── vite.ts             # Vite integration
├── shared/                 # Shared types and schemas
│   └── schema.ts           # Zod schemas and types
├── attached_assets/        # Static assets (images, resume)
├── components.json         # shadcn/ui configuration
├── package.json            # Dependencies and scripts
├── tailwind.config.ts      # Tailwind CSS configuration
├── tsconfig.json           # TypeScript configuration
├── vite.config.ts          # Vite configuration
└── README.md              # Project documentation
```

## 🖥️ VS Code Development Setup

### 1. Open Integrated Terminal
- Press `Ctrl + `` (backtick) to open terminal
- Or go to `Terminal > New Terminal`

### 2. Recommended Workspace Settings
Create `.vscode/settings.json`:
```json
{
  "editor.formatOnSave": true,
  "editor.defaultFormatter": "esbenp.prettier-vscode",
  "editor.codeActionsOnSave": {
    "source.fixAll.eslint": true
  },
  "emmet.includeLanguages": {
    "typescript": "html",
    "typescriptreact": "html"
  },
  "tailwindCSS.includeLanguages": {
    "typescript": "html",
    "typescriptreact": "html"
  }
}
```

### 3. Debugging Configuration
Create `.vscode/launch.json`:
```json
{
  "version": "0.2.0",
  "configurations": [
    {
      "name": "Debug Server",
      "type": "node",
      "request": "launch",
      "program": "${workspaceFolder}/server/index.ts",
      "outFiles": ["${workspaceFolder}/dist/**/*.js"],
      "runtimeArgs": ["-r", "tsx/cjs"]
    }
  ]
}
```

## 📦 Available Scripts

```bash
# Start development server (both frontend and backend)
npm run dev

# Build for production
npm run build

# Start production server
npm start

# Type checking
npm run type-check

# Lint code
npm run lint

# Format code with Prettier
npm run format
```

## 🎨 Customization Guide

### Changing Colors
Edit `client/src/index.css` to modify the color palette:
```css
:root {
  --dark-primary: hsl(0, 0%, 0%);           /* Black */
  --dark-secondary: hsl(207, 47%, 35%);     /* Deep Blue */
  --dark-accent: hsl(204, 36%, 67%);        /* Light Blue */
  --light-primary: hsl(210, 17%, 98%);      /* White/Light Gray */
  --light-secondary: hsl(207, 47%, 35%);    /* Deep Blue */
  --light-accent: hsl(204, 36%, 67%);       /* Light Blue */
}
```

### Adding New Sections
1. Create a new component in `client/src/components/`
2. Import and add to `client/src/pages/home.tsx`
3. Add navigation link in `client/src/components/navigation.tsx`

### Modifying Content
- **Personal Info**: Update `client/src/components/about-section.tsx`
- **Skills**: Edit `client/src/components/skills-section.tsx`
- **Projects**: Modify `client/src/components/projects-section.tsx`
- **Certifications**: Update `client/src/components/certifications-section.tsx`

## 🚀 Deployment Options

### Vercel (Recommended)
1. Push code to GitHub
2. Connect to Vercel
3. Deploy with zero configuration

### Netlify
1. Build the project: `npm run build`
2. Upload `dist` folder to Netlify

### Traditional Hosting
1. Run `npm run build`
2. Upload contents of `dist` folder to your web server

## 🔧 Troubleshooting

### Common Issues

**Node.js Version Issues**
```bash
# Check Node version
node --version

# Should be 18.x or higher
# Use nvm to manage Node versions
```

**Port Already in Use**
```bash
# Kill process on port 5000
npx kill-port 5000

# Or change port in package.json scripts
```

**TypeScript Errors**
```bash
# Clear TypeScript cache
npx tsc --build --clean

# Restart TypeScript service in VS Code
Ctrl+Shift+P > "TypeScript: Restart TS Server"
```

**Styling Issues**
```bash
# Regenerate Tailwind styles
npm run build:css
```

## 📱 Browser Support

- Chrome (latest)
- Firefox (latest)  
- Safari (latest)
- Edge (latest)
- Mobile browsers (iOS Safari, Chrome Mobile)

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch: `git checkout -b feature-name`
3. Commit changes: `git commit -am 'Add feature'`
4. Push to branch: `git push origin feature-name`
5. Submit a pull request

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

## 📞 Support

For questions or issues:
- Email: kartikeydwivedi55@gmail.com
- Create an issue in the repository
- Check the troubleshooting section above

---

**Built with ❤️ by Kartikey Dwivedi**

*Data Engineer • Python • SQL • Big Data • Cloud Technologies*