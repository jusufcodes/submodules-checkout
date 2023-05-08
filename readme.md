# Submodule Checkout Action

This GitHub Action allows you to checkout a repository and its submodules, with optional SSH key support.

## Usage

To use this action in your workflow, you can include the following steps:

```yaml
name: My Workflow

on:
  push:
    branches:
      - main

jobs:
  build:
    runs-on: ubuntu-latest

    steps:
      - name: 'Checkout repository and submodules'
        uses: jusufcodes/submodules-checkout@v1
        with:
          token: ${{ secrets.GITHUB_TOKEN }}
          ssh-key: ${{ secrets.SSH_KEY }}

      # Add more steps for your workflow here
```

## In the above example:

The token input is passed to the action, allowing it to access the repository and its submodules.

Ensure that the ssh-key input is set to the appropriate secret for your repository (e.g., secrets.SSH_KEY).

You can omit the ssh-key input if you don't need to provide an SSH key.

## Outputs

This action does not provide any outputs.
