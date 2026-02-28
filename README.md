# NFI Clear Documentation

This directory contains the documentation for NFI Clear API, built with [Mintlify](https://mintlify.com/).

## Structure

```
docs/
├── mint.json              # Mintlify configuration
├── README.md              # This file
├── introduction.mdx       # Landing page
├── quickstart.mdx         # Quick start guide
├── authentication.mdx     # Authentication guide
├── api-reference/
│   ├── overview.mdx       # API overview
│   ├── verifications/
│   │   ├── create.mdx     # Create verification
│   │   ├── list.mdx       # List verifications
│   │   ├── get.mdx        # Get verification
│   │   └── details.mdx    # Get full details
│   └── errors/
│       ├── codes.mdx      # Error codes
│       └── handling.mdx   # Error handling
└── concepts/
    ├── verifications.mdx  # Verification lifecycle
    ├── kyc-flow.mdx       # KYC process
    └── kyb-flow.mdx       # KYB process
```

## Available Features

### API Endpoints
- `POST /api/v1/verifications` - Create verification
- `GET /api/v1/verifications` - List verifications
- `GET /api/v1/verifications/:id` - Get verification status
- `GET /api/v1/verifications/:id/details` - Get full details

### Verification Types
- **KYC** - 5-step individual verification
- **KYB** - 8-step business verification

### Authentication
- API Key based authentication via `X-API-Key` header

## Local Development

Install the [Mintlify CLI](https://www.npmjs.com/package/mint):

```bash
npm install -g mint
```

Run the documentation locally:

```bash
cd docs
mint dev
```

The documentation will be available at `http://localhost:3333`.

## Deployment

This documentation is automatically deployed when pushed to the main branch.

### Manual Deployment

```bash
mint deploy
```
