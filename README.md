# 🚀 Release Automation POC

A React TypeScript application demonstrating automated CI/CD pipeline with semantic versioning and release automation.

## ✨ Features

- **React 18** with **TypeScript** and **Vite**
- **Automated Testing** with Vitest and React Testing Library
- **CI/CD Pipeline** with GitHub Actions
- **Semantic Versioning** and automated releases
- **Automated Changelog** generation
- **Conventional Commits** enforcement
- **Code Quality** checks with ESLint and TypeScript

## 🏗️ Project Structure

```
├── .github/workflows/     # GitHub Actions workflows
├── src/                   # Source code
│   ├── test/             # Test setup and utilities
│   └── App.tsx           # Main application component
├── public/                # Static assets
├── .husky/               # Git hooks
├── vitest.config.ts      # Vitest configuration
├── .releaserc.json       # Semantic release configuration
├── commitlint.config.js  # Commit message validation rules
└── package.json          # Dependencies and scripts
```

## 🚀 Getting Started

### Prerequisites

- Node.js 18+
- npm or yarn

### Installation

```bash
git clone <your-repo-url>
cd release-automation-poc
npm install
npm run dev
```

## 🧪 Testing

```bash
npm run test          # Run tests in watch mode
npm run test:ci       # Run tests with coverage
npm run test:ui       # Run tests with UI
```

## 🔧 Development Scripts

```bash
npm run dev          # Start development server
npm run build        # Build for production
npm run preview      # Preview production build
npm run lint         # Run ESLint
npm run type-check   # Run TypeScript type checking
npm run commit       # Interactive conventional commit
```

## 📝 Conventional Commits

This project enforces [Conventional Commits](https://www.conventionalcommits.org/) for automated versioning and releases.

### Commit Format

```
<type>[optional scope]: <description>

[optional body]

[optional footer(s)]
```

### Commit Types

- `feat` - New features (minor version)
- `fix` - Bug fixes (patch version)
- `docs` - Documentation changes
- `style` - Code style changes
- `refactor` - Code refactoring
- `perf` - Performance improvements
- `test` - Adding or updating tests
- `build` - Build system changes
- `ci` - CI/CD changes
- `chore` - Other changes
- `revert` - Reverts a previous commit

### Making Commits

**Interactive (Recommended):**

```bash
npm run commit
```

**Manual:**

```bash
git commit -m "feat: add new feature"
git commit -m "fix(auth): resolve login issue"
git commit -m "BREAKING CHANGE: remove deprecated API"
```

### Enforcement

- **Commitizen**: Interactive commit creation
- **Commitlint**: Validates commit message format
- **Husky**: Git hooks that run automatically

## 🚀 CI/CD Pipeline

### Continuous Integration

- Multi-Node testing (18.x, 20.x, 22.x)
- Type checking and linting
- Test coverage reporting
- Build verification

### Release Automation

- Analyzes commits for version bump type
- Generates changelog and release notes
- Creates GitHub release and npm package
- Optional GitHub Pages deployment

## 📋 GitHub Actions Workflows

- **CI Workflow**: Runs on push/PR with testing and building
- **Release Workflow**: Triggers after successful CI for semantic releases
  asdasd

## 🔐 Environment Variables

- `GITHUB_TOKEN`: Automatically provided by GitHub Actions
- `NPM_TOKEN`: For npm package publishing (if public package)

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make changes with conventional commits
4. Push and create a pull request

## 📝 License

This project is licensed under the MIT License.

## 🔗 Useful Links

- [React Documentation](https://react.dev/)
- [Vite Documentation](https://vitejs.dev/)
- [Semantic Release](https://semantic-release.gitbook.io/)
- [Conventional Commits](https://www.conventionalcommits.org/)
- [GitHub Actions](https://docs.github.com/en/actions)
