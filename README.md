# Kubernetes Manifests

Kubernetes configuration for our applications managed via GitOps.

## Structure

- `apps/`: Application manifests
  - `demo-nodejs-gitops/`: Express.js application manifests
    - `base/`: Base configuration
    - `overlays/`: Environment-specific configurations
      - `staging/`: Staging environment
      - `production/`: Production environment

## GitOps Workflow

Application images are updated automatically by the CI/CD pipeline.
ArgoCD syncs these manifests to the Kubernetes cluster.
