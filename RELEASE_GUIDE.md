# Release Guide for the docs as system starterkit he Package

This document explains step by step how to publish a new version of the docs as system starterkit he package to npm, including basic checks and required Git actions.

## Before You Start

To publish a new version you need:

• An active npm account  
• Login from your local machine  
```
npm login  
```
• Permission to publish the package  
• A clean Git workspace  
git status  

If there are untracked files or pending changes, commit or clear them before continuing.

## Choosing a Version Number

The package uses Semantic Versioning in the format  
MAJOR.MINOR.PATCH

Summary:  
• PATCH for bug fixes  
• MINOR for added capabilities without breaking compatibility  
• MAJOR for changes that require modifications in existing projects

## Step 1: Update package.json

### Option A: Use npm version
```
npm version patch  
npm version minor  
npm version major  
```

This updates package.json and creates a Git tag.

### Option B: Update manually
Edit package.json and change the version field.

## Step 2: Local Tests Before Publishing

```
npm install  
node bin/das.cjs --help  
npm link  
das --help  
das create test-project  
```
## Step 3: Commit and Tag in Git
```
git add package.json  
git commit -m "Bump version"  
git tag v0.2.0  
git push origin main  
git push origin tags  
```
## Step 4: Publish to npm

```bash
npm login 
npm link 
npm publish --access public
```

Check published version:  
```
npm view docs-as-system-starterkit version
```
## Step 5: Test Like a Real User
```
npm install -g docs-as-system-starterkit  
das create my-project  
```

## Step 6: Update Documentation

Update CHANGELOG, README and any document that references commands or versions.

© 2025 Tomer Kedem.
Part of the official Docs as System template suite.
