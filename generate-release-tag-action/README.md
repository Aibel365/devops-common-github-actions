# Generate Release Tag Action

Github action for generating release tag, following semantic versioning, based on pull request labels.




## Usage

Below is a simple example of using the action. 

```yaml

name: Main

on: push

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout
        uses: actions/checkout@v3
      - name: Release
        uses: Aibel365/devops-common-github-actions/generate-release-tag-action
        with:
          github_token: ${{ secrets.GITHUB_TOKEN }}
          prefix: "v"
```
