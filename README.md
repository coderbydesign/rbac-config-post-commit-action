# RBAC Post-commit Action
A GitHub action to run post-commit for RBAC config

Usage:
```
on:
  push:
    branches:
      - master
name: Config conversion
jobs:
  convert_config:
    name: Converts config
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - name: Converting config to configmaps
        uses: coderbydesign/rbac-config-post-commit-action@main
        with:
          token: ${{ secrets.GITHUB_TOKEN }}
```