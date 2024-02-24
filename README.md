# Turborepo with Next.js (standalone build), Docker, and Tailwind

This project is a monorepo using Turborepo, Next.js, Docker, and Tailwind CSS. It includes two Next.js applications: app and landing-page. This guide provides instructions for installation, development, and building for both development and production environments.

## Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/tokmo/turborepo-next14-docker.git
    ```

2. Install dependencies:
    ```bash
    pnpm install
    ```

## Development

Development with Docker:

- Start the development environment with both Next.js applications:
    ```bash
    pnpm docker:dev
    ```

- Start the development environment for a specific Next.js application:
    ```bash
    # For app:
    pnpm docker:dev:app

    # For landing-page:
    pnpm docker:dev:landing-page
    ```

## Building and Deploying

Building for production:

- Build both Next.js applications:
    ```bash
    pnpm docker:build
    ```

- Build a specific Next.js application:
    ```bash
    # For app:
    pnpm docker:build:app

    # For landing-page:
    pnpm docker:build:landing-page
    ```

Deploying to production with Docker:

- Deploy both Next.js applications:
    ```bash
    # Replace "prod-app" and "prod-landing-page" with your desired service names
    pnpm docker:prod:app
    pnpm docker:prod:landing-page
    ```

- Deploy a specific Next.js application:
    ```bash
    # Replace "prod-app" or "prod-landing-page" with the desired service name
    pnpm docker:prod:app
    ```

## Additional notes

- This guide assumes you have Docker and Docker Compose installed.
- You can customize the scripts in package.json to fit your specific needs.
- Refer to the documentation for Turborepo, Next.js, Docker, and Tailwind CSS for further details on each technology.
