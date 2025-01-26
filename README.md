# agents-manifest

Agent Manifest — A specification for machine-readable service descriptions designed for AI agents. Similar to robots.txt but for the agentic era, providing structured information about APIs, authentication, payment methods, and more.

## Overview

Agent Manifest allows developers to describe the key capabilities and entry points of a service for intelligent agents. Instead of leaving these agents clueless about how to interact with your web application or website, you provide a structured file containing information about APIs, response formats, authentication methods, and (if necessary) payment instructions.

## Analogy with robots.txt

The robots.txt file is used by search engine crawlers to understand which pages or sections of a site should be indexed or ignored. In a similar way, an "agent manifest" (for example, a file named agents.json) works as a guide for AI-driven agents, indicating which actions they can perform, which resources are available, and how authentication or payment should be handled.

## Usage for Regular Websites

You can think of an agent manifest as an expanded version of a site map, offering additional metadata specifically for AI agents. Alongside a list of pages or services, you can specify:

- Detailed endpoints (e.g., /api/users, /api/products)
- Recommended usage scenarios (e.g., "Use this endpoint for user onboarding")
- Authentication workflows (e.g., OAuth2 or API tokens)
- Payment options (e.g., stripe api, or crypto payment)

This approach lets agents understand both the structure of your website and the specifics of each endpoint, reducing guesswork and making automated interactions more reliable.

## Key Technical Requirements

- Must be a UTF-8 encoded plain text file in JSON format
- Must be located at a well-known location:
  - Primary: `/agents.json` at the root directory (e.g., `example.com/agents.json`)
  - Alternative: Can be specified via HTTP header `X-Agent-Manifest: <URL>`
- File size should not exceed 2MB
- Must return content-type `application/json`
- Must be publicly accessible without authentication (the manifest file itself)
- Can use HTTP caching headers (e.g., `Cache-Control`, `ETag`)
- Should handle conditional requests (If-Modified-Since, If-None-Match)
- Must maintain backwards compatibility within major versions
- Should be served over HTTPS
- Can reference additional files for detailed documentation (similar to sitemap.xml references)
- Must be valid JSON and parseable by standard JSON parsers
- Should include a required minimal set of fields:
  - version
  - last_modified
  - supported_agent_versions

## Key Components

### Agent Guidelines

- Explicitly allowed and prohibited actions
- Rate limiting and concurrent connection limits
- Best practices for interaction
- Required headers or specific request formats

### Authentication

- Authentication methods supported (OAuth2, API keys, JWT)
- Token endpoints and scopes
- Registration process for new agents
- Session management guidelines
- Security requirements and best practices

### Navigation & Structure

- Site structure and main sections
- Important entry points and landing pages
- Search functionality details
- Dynamic content handling
- Sitemap references and relationships

### API Documentation

- Endpoint descriptions and purposes
- Required parameters and expected responses
- Rate limiting information
- Example requests and responses
- Error handling and status codes
- Versioning information

### Payment Integration

- Supported payment processors and methods
- Pricing models (usage-based, subscription, pay-per-call)
- Currency and rate information
- Payment endpoint specifications
- Trial or free tier details
- Billing cycle information

### Compliance & Policies

- Terms of service reference
- Privacy policy guidelines
- Data usage restrictions
- Regional availability
- Required legal disclaimers

## Contributing

We welcome contributions! Please read our [contributing guidelines](CONTRIBUTING.md) and submit pull requests to help improve this specification.

## License

[MIT License](LICENSE)
