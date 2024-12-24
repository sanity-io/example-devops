# Setup Node.js Environment

A composite action that sets up Node.js environment for GitHub Actions workflows.

## What it does

1. Sets up Node.js LTS with npm caching
2. Installs dependencies using `npm ci`

## Usage

```yaml
steps:
  # Requires checking out the repo, since this is a local action
  - uses: actions/checkout@v4
  - uses: ./.github/actions/setup

  - name: Your next step
    run: npm run your-script