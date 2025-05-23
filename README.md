# k8s-tools-setup
Reusable Github Actions Runner workflow that sets up standard set of tools for interfacing with Kubernetes

## Usage
How to use this in your own Github Actions Workflow


```yaml
name: Deploy to Kubernetes
on:
  push:
    branches:
      - main
jobs:
  setup-tools:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout code
        uses: actions/checkout@v4
      - name: Set up Kubernetes Tools
        uses: bps-cloudops/k8s-tools-setup@v2

```