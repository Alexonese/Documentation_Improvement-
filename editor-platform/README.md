# PrintVis Documentation Editor

This folder contains the custom documentation editing platform.

## Applications

- `apps/web`: React and TypeScript frontend
- `apps/api`: Azure Functions and TypeScript backend

## Requirements

- Node.js 22
- npm
- Azure Functions Core Tools 4
- Python and the existing MkDocs dependencies

## Start the frontend

```powershell
npm install --prefix apps/web
npm run dev:web