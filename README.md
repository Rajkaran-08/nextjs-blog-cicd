# Next.js Blog – CI/CD Demo Project

## Overview
This repository demonstrates a production-style CI/CD pipeline
for an existing Next.js application using GitHub Actions and Vercel.

The application code is intentionally kept minimal; the focus
is on CI/CD design, control, and reliability.

## Application
- Framework: Next.js
- Source: Official Next.js blog starter template
- Purpose: Sample application used to demonstrate CI/CD workflows

## CI – Pull Request Validation
- Triggered on pull requests to `main`
- Installs dependencies in a clean environment
- Runs a production build (`npm run build`)
- Prevents broken code from being merged

## CD – Controlled Deployment
- Triggered only on pushes to `main`
- Automatic Vercel deployments are disabled
- Deployment is executed explicitly via GitHub Actions
- Uses Vercel CLI with production-scoped secrets

## Deployment Flow
Pull Request → CI validation → Merge to main → CD deployment → Production

## Security & Secrets
- Secrets are scoped to a `production` environment
- No secrets are stored in the repository
- Production deployments require verified commits

## Why this project exists
This project exists to demonstrate how an existing web application
can be operationalized with clean, auditable CI/CD pipelines.
