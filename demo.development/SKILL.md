---
name: demo.development
description: Demo project development (project)
---

# Demo Project Development

Introduction to developing the Demo project - a multi-stack Hello World showcase for Xedant Code.

## Project Overview

**Demo** is a Hello World project showcasing multiple technology stacks working together. It demonstrates Xedant Code's capabilities with servers in ASP.NET Core, Python Flask, and Node.js Express, plus clients in SvelteKit 5 and React.

## Architecture

### Directory Structure
- `server-netcore/` - ASP.NET Core 9.0 minimal API server
- `server-python/` - Python Flask API server
- `server-node/` - Node.js Express API server
- `client-svelte/` - SvelteKit 5 static client
- `client-react/` - React static client with Vite

### Technology Stack
- **server-netcore**: ASP.NET Core 9.0 minimal API
- **server-python**: Python 3.8+ with Flask 3.0
- **server-node**: Node.js 18+ with Express 4.18
- **client-svelte**: Svelte 5.0 with SvelteKit 2.0, adapter-static
- **client-react**: React 19 with Vite 6.0, TypeScript 5.6

## Prerequisites

This project contains source files only. No runtime dependencies are included or installed automatically.
Only install prerequisites for sub-projects the user actually plans to use.

- **.NET (server-netcore)**: .NET 9.0 SDK - https://dotnet.microsoft.com/download/dotnet/9.0
- **Python (server-python)**: Python 3.8+ - https://www.python.org/downloads/ (check "Add to PATH" during install)
- **Node.js (server-node, client-svelte, client-react)**: Node.js 18+ LTS - https://nodejs.org/ (includes npm)

## Key Components

### Servers
All three servers expose `/api/hello` returning JSON: `{ message, server, timestamp }`.

### Clients
Both clients have big "Test" buttons on the home page to connect to each server individually.
No auto-fetch on page load - user clicks to test.

## Development Rules

### Hot Reload
- Builds are done automatically via build.yml - never do them manually
- NEVER run `dotnet build` or `dotnet run` or manual builds
- NEVER run `npm run build` or `npm run dev` or manual builds
- NEVER attempt to test your changes, better ask the user to do that
- NEVER create test files or test documentation if not explicitly asked by the user

### Code Practices
- Keep code minimal - this is a demo project
- Use Svelte 5 runes (`$state`, `$effect`) for reactivity - never use legacy `$:` or `export let`
- Use functional components with hooks in React
- All Svelte files must be in `client-svelte/src/`
- Never enable nullable reference types
- Delete unused code, don't comment out

# Important!
- Whenever I ask you to check what's done according to a plan and implement the rest, NEVER skip stages when checking
- You must NOT start with the last stage of the plan and assume all the rest was successfully done
- Whenever you finish implementing a stage of a plan, you must append a notice into the main plan file about that
