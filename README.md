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

## File Location

```URL
https://example.com/agents.json
```

## Key Components

### Agent Guidelines

- Explicitly allowed and prohibited actions
- Rate limiting and concurrent connection limits
- Best practices for interaction
- Required headers or specific request formats
- Supported response formats (JSON, XML, etc.)

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

## Version Control

The manifest should include version information to help agents handle changes:

- Schema version
- API versions supported
- Deprecation notices
- Change log references

## Contributing

We welcome contributions! Please read our contributing guidelines and submit pull requests to help improve this specification.

## License

[MIT License](LICENSE)
