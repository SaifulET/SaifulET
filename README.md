name: Generate Snake

on:
  schedule:
    # Every 12 hours
    - cron: "0 */12 * * *"
  workflow_dispatch:
  push:
    branches:
      - main
      - master

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - name: Generate contribution snake SVG
        uses: Platane/snk@v3
        with:
          github_user_name: SaifulET
          outputs: |
            dist/github-contribution-grid-snake.svg
            dist/github-contribution-grid-snake-dark.svg?palette=github-dark
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}

      - name: Push SVG to output branch
        uses: crazy-max/ghaction-github-pages@v3.1.0
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
