# npm-oidc-test

Test repo for debugging OIDC trusted publishing to npm.

## Purpose

Minimal setup to isolate and debug npm publish with OIDC authentication:
- No build tooling (Nx, webpack, etc.)
- Single package.json + index.js
- GitHub Actions workflow with `NPM_CONFIG_PROVENANCE=true`
- Environment: `npm-publish` with `id-token: write` permission

## Setup

1. Package created on npmjs.com by org owner
2. Trusted publisher configured at npmjs.com/package/@redhat-cloud-services/npm-oidc-test/access:
   - Org: RedHatInsights
   - Repo: tmp-npm-oidc-test
   - Workflow: publish.yaml
   - Environment: npm-publish

## Usage

Push to master branch → CI publishes to npm via OIDC.
