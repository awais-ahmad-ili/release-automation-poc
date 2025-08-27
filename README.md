# 🚀 Release Automation POC

A React TypeScript application demonstrating automated CI/CD pipeline with semantic versioning and release automation.

## ✨ Features

- **React 18** with **TypeScript** and **Vite**
- **Automated Testing** with Vitest and React Testing Library
- **CI/CD Pipeline** with GitHub Actions
- **Semantic Versioning** and automated releases
- **Automated Changelog** generation
- **Release Notes** generation
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

1. Clone the repository:
```bash
git clone <your-repo-url>
cd release-automation-poc
```

2. Install dependencies:
```bash
npm install
```

3. Start development server:
```bash
npm run dev
```

## 🧪 Testing

### Run Tests
```bash
# Run tests in watch mode
npm run test

# Run tests once with coverage
npm run test:ci

# Run tests with UI
npm run test:ui
```

### Test Coverage
The project includes comprehensive test coverage for:
- Component rendering
- User interactions
- State management
- Component behavior

## 🔧 Development Scripts

```bash
npm run dev          # Start development server
npm run build        # Build for production
npm run preview      # Preview production build
npm run lint         # Run ESLint
npm run type-check   # Run TypeScript type checking
npm run test         # Run tests
npm run test:ci      # Run tests with coverage
npm run commit       # Interactive conventional commit
```

## 🚀 CI/CD Pipeline

### Continuous Integration (CI)
The CI pipeline runs on every push and pull request:

1. **Multi-Node Testing**: Tests against Node.js 18.x, 20.x, and 22.x
2. **Type Checking**: Ensures TypeScript compilation
3. **Linting**: Code quality checks with ESLint
4. **Testing**: Comprehensive test suite execution
5. **Coverage**: Code coverage reporting
6. **Build**: Production build verification

### Release Automation
The release pipeline automatically:

1. **Analyzes Commits**: Determines version bump type
2. **Generates Changelog**: Creates detailed release notes
3. **Creates Release**: Publishes to GitHub and npm
4. **Updates Version**: Bumps package version
5. **Deploys**: Optional GitHub Pages deployment

### Commit Message Convention
Follow [Conventional Commits](https://www.conventionalcommits.org/) for automatic versioning:

- `feat:` - New features (minor version)
- `fix:` - Bug fixes (patch version)
- `BREAKING CHANGE:` - Breaking changes (major version)
- `docs:` - Documentation changes
- `style:` - Code style changes
- `refactor:` - Code refactoring
- `test:` - Test additions/changes
- `chore:` - Build/tooling changes

### Commit Enforcement
This project enforces conventional commit format using:

- **Commitizen**: Interactive commit creation (`npm run commit`)
- **Commitlint**: Validates commit message format
- **Husky**: Git hooks to enforce rules

#### Commit Types
- `feat` - New features
- `fix` - Bug fixes
- `docs` - Documentation changes
- `style` - Code style changes
- `refactor` - Code refactoring
- `perf` - Performance improvements
- `test` - Adding or updating tests
- `build` - Build system changes
- `ci` - CI/CD changes
- `chore` - Other changes

#### Examples
```bash
feat: add user authentication
fix(auth): resolve login button issue
docs: update README with new features
BREAKING CHANGE: remove deprecated API
```

## 📋 GitHub Actions Workflows

### CI Workflow (`.github/workflows/ci.yml`)
- Triggers: Push to main/develop, Pull requests
- Jobs: Testing, Building, Coverage reporting
- Matrix testing across Node.js versions
- Uploads build artifacts for release workflow

### Release Workflow (`.github/workflows/release.yml`)
- Triggers: After successful CI workflow completion
- Jobs: Semantic release automation
- Downloads build artifacts from CI
- Creates GitHub release and tags

## 🔐 Environment Variables

The following secrets are required in your GitHub repository:

- `GITHUB_TOKEN`: Automatically provided by GitHub Actions
- `NPM_TOKEN`: For npm package publishing (if public package)

## 📊 Code Quality

### ESLint Configuration
- React-specific rules
- TypeScript support
- Hooks rules
- Consistent code style

### TypeScript Configuration
- Strict mode enabled
- Modern ES features
- React JSX support
- Type checking in CI

## 🎯 Git Hooks

### Pre-commit Hook
Automatically runs before each commit:
- Linting
- Type checking
- Tests

### Commit-msg Hook
- Validates conventional commit format
- Enforces commit message rules

## 🚀 Deployment

### GitHub Pages
The application can be automatically deployed to GitHub Pages on each release.

### Build Artifacts
Build artifacts are uploaded to GitHub Actions for each CI run.

## 📈 Monitoring and Metrics

- **Test Coverage**: Automated coverage reporting
- **Build Status**: GitHub Actions status checks
- **Release Tracking**: Automated changelog generation
- **Performance**: Web Vitals monitoring

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes with conventional commits
4. Follow commit message conventions
5. Push and create a pull request

## 📝 License

This project is licensed under the MIT License.

## 🔗 Useful Links

- [React Documentation](https://react.dev/)
- [Vite Documentation](https://vitejs.dev/)
- [Vitest Documentation](https://vitest.dev/)
- [Semantic Release](https://semantic-release.gitbook.io/)
- [Conventional Commits](https://www.conventionalcommits.org/)
- [GitHub Actions](https://docs.github.com/en/actions)
