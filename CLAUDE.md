# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Purpose

This is a Postman collection repository for Harness FME (formerly Split) public Admin APIs. It contains no buildable code — only Postman collection and environment JSON files used for testing and documenting API endpoints.

## Key Files

- `public Admin APIs.postman_collection.json` — Original Split Admin API collection (internal v2 endpoints)
- `Before and After - APIs for Split Admins.postman_collection.json` — Migration guide collection showing Split (BEFORE) and Harness (AFTER) API equivalents for five admin endpoints being replaced during Split-to-Harness migration
- Environment files: `prod.postman_environment.json`, `staging.postman_environment.json`, `local.postman_environment.json`

## Architecture

The "Before and After" collection is organized by endpoint category (Users, Groups, Workspaces, Restrictions, Projects), each containing "Split (BEFORE)" and "Harness (AFTER)" subfolders with working API examples.

### Environment Variables

- `auth-token` / `apikey-auth` / `jwt-auth` — Authentication tokens
- `base-url` — API base URL (defaults: prod uses Split API, staging uses `api.split-stage.io`, local uses `localhost:8080`)
- `workspace-id`, `org-id`, `environment-id`, `traffictype-id` — Resource identifiers

## Working With This Repo

- Changes are made by editing JSON files directly or exporting from Postman
- To test: import collection and environment files into Postman, fill in auth tokens and resource IDs
- API reference: https://docs.split.io/reference
- Harness API key info: created under Account Settings > Access Control > Service Accounts in Harness
