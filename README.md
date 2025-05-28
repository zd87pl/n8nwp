# AI Automated WordPress Agency

This repository contains documentation and example n8n workflows for running a fully automated WordPress creative agency using WP Engine as the hosting provider. The goal is to take a customer's requirements, generate content with AI, and deploy a WordPress site with minimal manual effort.

## Repository Structure

- `workflows/` – Example n8n workflow JSON exports.
- `docs/` – Additional documentation and roadmaps.

## Quick Start

1. Set up n8n (self‑hosted or cloud) and import the workflow from `workflows/automated-agency.json`.
2. Configure credentials for WP Engine, email, Stripe, and any AI providers (OpenAI, Whisper, etc.).
3. Trigger the workflow via the provided webhook URL or connected form.
4. Follow the automated steps as the workflow gathers requirements, creates a staging site, and deploys it to production.

The workflow provided here is a template. Adapt it to your specific plugins, design templates, and business processes.

## Documentation

See `docs/roadmap.md` for a high-level overview of the business process and automation phases.

