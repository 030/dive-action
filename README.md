# dive-action

Create a `.github/workflows/dive.yml file:

```yaml
---
name: Dive
"on": push
jobs:
  docker:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - uses: 030/dive-action@v0.1.0
        with:
          image: some/image:${{ github.sha }}
```
