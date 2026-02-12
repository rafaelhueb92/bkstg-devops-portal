# Backstage DevOps Portal

![Backstage](https://backstage.io/assets/logo-light.svg)

A powerful developer portal built with [Backstage](https://backstage.io), providing a unified platform for managing microservices, catalogs, and DevOps workflows.

## Quick Start

### Prerequisites

- **Node.js**: 22 or 24
- **Yarn**: Latest version

### Installation & Setup

1. **Install dependencies:**

   ```sh
   yarn install
   ```

2. **Configure required libraries:**

   Before running the project, you need to install GitHub-related plugins and integrations. Run the configuration script:

   ```sh
   bash configs.sh
   ```

   This script installs the following packages:

   - `@backstage/plugin-catalog-backend-module-github` - GitHub catalog backend module for fetching repository metadata
   - `@backstage/plugin-auth-backend-module-github-provider` - GitHub authentication provider
   - `@backstage-community/plugin-github-actions` - GitHub Actions integration for CI/CD workflows

3. **Start the development server:**

   ```sh
   yarn start
   ```

   The app will be available at `http://localhost:3000`

## Project Structure

- **`packages/app/`** - Frontend React application
- **`packages/backend/`** - Backend Node.js server
- **`plugins/`** - Custom plugin extensions
- **`examples/`** - Example entities and templates for the catalog

## Available Scripts

| Command               | Purpose                                             |
| --------------------- | --------------------------------------------------- |
| `yarn start`          | Start both frontend and backend in development mode |
| `yarn build:all`      | Build all packages                                  |
| `yarn test`           | Run tests across the project                        |
| `yarn test:e2e`       | Run end-to-end tests with Playwright                |
| `yarn lint`           | Lint the codebase                                   |
| `yarn prettier:check` | Check code formatting                               |
| `yarn new`            | Create a new plugin or package                      |

## Configuration

- **`app-config.yaml`** - Main application configuration
- **`app-config.local.yaml`** - Local development overrides
- **`app-config.production.yaml`** - Production-specific configuration

## Integration Features

### GitHub Integration

- Automatically discover and catalog repositories
- Authenticate users via GitHub OAuth
- Display GitHub Actions workflows and build status
- Link components to GitHub repositories

## Next Steps

1. Update `app-config.yaml` with your GitHub organization and credentials
2. Add your services to `examples/entities.yaml`
3. Customize the Root component in `packages/app/src/components/Root/`
4. Create custom plugins in the `plugins/` directory

## Learn More

- [Backstage Documentation](https://backstage.io/docs)
- [GitHub Plugin Documentation](https://backstage.io/docs/integrations/github/discovery)
- [Backstage Community](https://github.com/backstage/backstage)
