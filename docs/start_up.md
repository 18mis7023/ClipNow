# ClipNow - Startup Guide

## Prerequisites

- **Node.js**: v17.0.0 or higher (tested with v24.11.0)
- **npm**: v8.0.0 or higher

## Installation

1. **Clone the repository** (if not already done):
   ```bash
   git clone <repository-url>
   cd Clipnow
   ```

2. **Install dependencies**:
   ```bash
   npm install --legacy-peer-deps
   ```
   
   > **Note**: The `--legacy-peer-deps` flag is required due to the `use-dark-mode` package having a peer dependency on React 16, while this project uses React 17.

## Running the Application

### Development Mode
```bash
npm start
```
This will start the development server at [http://localhost:3000](http://localhost:3000).

### Production Build
```bash
npm run build
```
This creates an optimized production build in the `build/` folder.

### Running Tests
```bash
npm test
```

## Troubleshooting

### Common Installation Issues

#### 1. Peer Dependency Conflicts
If you see errors about peer dependencies, use:
```bash
npm install --legacy-peer-deps
```

#### 2. `node-sass` Build Failures
The project uses `sass` (Dart Sass) instead of `node-sass`. If you encounter `node-sass` related errors:
- Ensure `node-sass` is not in your `package.json`
- The modern `sass` package is already included and works with all Node.js versions

#### 3. Python/distutils Errors
If you see `ModuleNotFoundError: No module named 'distutils'`:
- This is caused by `node-sass` which has been removed from this project
- Run `rm -rf node_modules package-lock.json` and reinstall

## Tech Stack

- **React**: v17.0.2
- **React Router**: v6.2.1
- **Firebase**: v9.17.2
- **Styling**: Sass, styled-components, MDB React UI Kit
- **Testing**: Jest, React Testing Library

## Project Structure

```
Clipnow/
├── public/          # Static assets
├── src/             # Source code
├── docs/            # Documentation
├── package.json     # Dependencies and scripts
└── README.md        # Project overview
```
