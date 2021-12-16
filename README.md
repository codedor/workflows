# Workflows

## Usage

### Style

```yaml
name: Check & fix styling

on: [pull_request, workflow_dispatch]

jobs:
  call-style:
    uses: codedor/workflows/.github/workflows/style.yml@v0
```

### PHPUnit

There is only a workflow to run PHPUnit on PHP 7.4 & PHP 8.0 with Laravel 8.

```yaml
name: PHPUnit

on: [pull_request]

jobs:
  call-style:
    uses: codedor/workflows/.github/workflows/phpunit-l8.yml@v0
    secrets:
      REPMAN_TOKEN: ${{ secrets.REPMAN_TOKEN }}
      NOVA_USERNAME: ${{ secrets.NOVA_USERNAME }}
      NOVA_PASSWORD: ${{ secrets.NOVA_PASSWORD }}
```
