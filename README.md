# Project Setup Commands - npm/npx/yarn

A comprehensive guide to create different types of projects using both npm/npx and yarn package managers.

## Prerequisites Installation

### Installing Node.js and npm

Node.js comes with npm (Node Package Manager) included.

#### Direct Installation
```bash
# Download from official website
# Visit: https://nodejs.org/
# Choose LTS version for stability

# Verify installation
node --version
npm --version
```

#### Package Manager Installation
```bash
# macOS with Homebrew
brew install node

# Ubuntu/Debian
sudo apt update
sudo apt install nodejs npm

# CentOS/RHEL/Fedora
sudo dnf install nodejs npm

# Windows with Chocolatey
choco install nodejs

# Windows with Winget
winget install OpenJS.NodeJS
```

### Installing NVM (Node Version Manager)

NVM allows you to install and switch between multiple Node.js versions.

#### Install NVM (Linux/macOS)
```bash
# Install NVM
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.0/install.sh | bash

# Reload your shell configuration
source ~/.bashrc
# or
source ~/.zshrc

# Verify installation
nvm --version
```

#### Install NVM for Windows
```bash
# Download and install from:
# https://github.com/coreybutler/nvm-windows/releases

# Or use Chocolatey
choco install nvm

# Or use Scoop
scoop install nvm
```

#### Using NVM
```bash
# List available Node.js versions
nvm list-remote     # Linux/macOS
nvm list available  # Windows

# Install latest LTS version
nvm install --lts

# Install specific version
nvm install 18.17.0

# Use specific version
nvm use 18.17.0

# Set default version
nvm alias default 18.17.0

# List installed versions
nvm list
```

### Installing Yarn

Before using yarn commands, you need to install yarn globally:

```bash
# Install yarn globally with npm
npm install -g yarn

# Verify installation
yarn --version
```

#### Alternative Yarn Installation Methods
```bash
# Using npm (recommended)
npm install -g yarn

# Using Corepack (Node.js 16.10+)
corepack enable
corepack prepare yarn@stable --activate

# Using Homebrew (macOS)
brew install yarn

# Using Chocolatey (Windows)
choco install yarn
```

## Web Frameworks

### React with Vite
```bash
# npm/npx
npx create-vite@latest my-react-app --template react

# yarn
yarn create vite my-react-app --template react
```

### React with Create React App (CRA)
```bash
# npm/npx
npx create-react-app my-react-app

# yarn
yarn create react-app my-react-app
```

### Next.js
```bash
# npm/npx
npx create-next-app@latest my-nextjs-app

# yarn
yarn create next-app my-nextjs-app
```

### Vue.js
```bash
# npm/npx
npx create-vue@latest my-vue-app

# yarn
yarn create vue my-vue-app
```

### Angular
```bash
# npm (requires global installation)
npm install -g @angular/cli
ng new my-angular-app

# yarn (requires global installation)
yarn global add @angular/cli
ng new my-angular-app
```

### Svelte with SvelteKit
```bash
# npm/npx
npx sv create my-svelte-app

# yarn
yarn create svelte my-svelte-app
```

## Backend Frameworks

### NestJS
```bash
# npm (requires global installation)
npm i -g @nestjs/cli
nest new my-nestjs-app

# yarn
yarn create nest my-nestjs-app
# or with global installation
yarn global add @nestjs/cli
nest new my-nestjs-app
```

### Express.js (with TypeScript)
```bash
# npm/npx
npx express-generator-typescript my-express-app

# yarn
yarn create express-generator-typescript my-express-app
```

### Fastify
```bash
# npm/npx
npx create-fastify my-fastify-app

# yarn
yarn create fastify my-fastify-app
```

## Mobile Development

### React Native CLI
```bash
# npm (requires global installation)
npm install -g @react-native-community/cli
npx react-native init MyReactNativeApp

# yarn (requires global installation)
yarn global add @react-native-community/cli
npx react-native init MyReactNativeApp
```

### React Native with Expo
```bash
# npm/npx
npx create-expo-app@latest MyExpoApp

# yarn
yarn create expo-app MyExpoApp
```

### Expo with specific template
```bash
# npm/npx
npx create-expo-app@latest MyExpoApp --template blank-typescript

# yarn
yarn create expo-app MyExpoApp --template blank-typescript
```

## Desktop Applications

### Electron
```bash
# npm/npx
npx create-electron-app my-electron-app

# yarn
yarn create electron-app my-electron-app
```

### Tauri
```bash
# npm/npx
npx create-tauri-app my-tauri-app

# yarn
yarn create tauri-app my-tauri-app
```

## Full-Stack Frameworks

### T3 Stack (Next.js + TypeScript + Tailwind + tRPC)
```bash
# npm/npx
npx create-t3-app@latest my-t3-app

# yarn
yarn create t3-app my-t3-app
```

### Remix
```bash
# npm/npx
npx create-remix@latest my-remix-app

# yarn
yarn create remix my-remix-app
```

## Static Site Generators

### Gatsby
```bash
# npm (requires global installation)
npm install -g gatsby-cli
gatsby new my-gatsby-site

# yarn (requires global installation)
yarn global add gatsby-cli
gatsby new my-gatsby-site
```

### Astro
```bash
# npm/npx
npx create-astro@latest my-astro-app

# yarn
yarn create astro my-astro-app
```

## Other Frameworks & Tools

### Flutter (requires Flutter SDK)
```bash
# Flutter CLI (same for both npm and yarn users)
flutter create my_flutter_app
```

### Vite (vanilla projects)
```bash
# npm/npx
npx create-vite@latest my-vite-app --template vanilla

# yarn
yarn create vite my-vite-app --template vanilla
```

### Storybook
```bash
# npm/npx (in existing project)
npx storybook@latest init

# yarn (in existing project)
yarn dlx storybook@latest init
```

## Package Manager Commands

### Installing Dependencies
```bash
# npm
npm install
npm install package-name
npm install -D package-name  # dev dependency

# yarn
yarn install
yarn add package-name
yarn add -D package-name     # dev dependency
```

### Running Scripts
```bash
# npm
npm run dev
npm start
npm run build

# yarn
yarn dev
yarn start
yarn build
```

## Notes

- **Global installations**: Some tools require global installation of CLI tools
- **Template options**: Many create commands accept `--template` or similar flags for different starting templates
- **Package managers**: Projects created with yarn commands will use yarn by default, while npm/npx commands typically use npm
- **Flutter**: Requires Flutter SDK to be installed separately from Node.js package managers

## Quick Reference

Most modern frameworks follow these patterns:
- **npm/npx**: `npx create-[framework]@latest project-name`
- **yarn**: `yarn create [framework] project-name`

Always check the official documentation for the most up-to-date commands and available templates.
