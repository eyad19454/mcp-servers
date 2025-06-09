# MCP Servers Collection

A comprehensive collection of Model Context Protocol (MCP) servers for integrating enterprise APIs with GenAI applications.

## Overview

This collection provides production-ready MCP servers for major enterprise platforms, enabling seamless integration with AI agents and GenAI applications. Each server is designed with enterprise requirements in mind: security, scalability, and reliability.

## Available Servers

### Cloud Platforms

| Server | Description | Status |
|--------|-------------|--------|
| [AWS MCP Server](https://github.com/asklokesh/aws-mcp-server) | Amazon Web Services - comprehensive cloud services integration | ✅ Ready |
| [GCP MCP Server](https://github.com/asklokesh/gcp-mcp-server) | Google Cloud Platform - complete GCP services integration | ✅ Ready |
| [Azure MCP Server](https://github.com/asklokesh/azure-mcp-server) | Microsoft Azure - full Azure services integration | ✅ Ready |

### CRM & Sales Platforms

| Server | Description | Status |
|--------|-------------|--------|
| [Salesforce MCP Server](https://github.com/asklokesh/salesforce-mcp-server) | Complete Salesforce CRM, Sales Cloud, Service Cloud integration | ✅ Ready |
| [HubSpot MCP Server](https://github.com/asklokesh/hubspot-mcp-server) | HubSpot CRM, Marketing, Sales, and Service Hub integration | ✅ Ready |
| [Zoho CRM MCP Server](https://github.com/asklokesh/zoho-crm-mcp-server) | Zoho CRM suite integration | ✅ Ready |

### DevOps & CI/CD

| Server | Description | Status |
|--------|-------------|--------|
| [Jenkins MCP Server](https://github.com/asklokesh/jenkins-mcp-server) | Jenkins CI/CD automation server integration | ✅ Ready |
| [GitLab MCP Server](https://github.com/asklokesh/gitlab-mcp-server) | GitLab DevOps platform integration | ✅ Ready |
| [ArgoCD MCP Server](https://github.com/asklokesh/argocd-mcp-server) | GitOps continuous delivery for Kubernetes | ✅ Ready |
| [Harness MCP Server](https://github.com/asklokesh/harness-mcp-server) | Continuous delivery and cloud cost management | ✅ Ready |
| [Rundeck MCP Server](https://github.com/asklokesh/rundeck-mcp-server) | Runbook automation and job scheduling | ✅ Ready |

### Container & Orchestration

| Server | Description | Status |
|--------|-------------|--------|
| [Rancher MCP Server](https://github.com/asklokesh/rancher-mcp-server) | Kubernetes management platform | ✅ Ready |

### Business Intelligence & Analytics

| Server | Description | Status |
|--------|-------------|--------|
| [Power BI MCP Server](https://github.com/asklokesh/powerbi-mcp-server) | Microsoft Power BI analytics and visualization | ✅ Ready |
| [Tableau MCP Server](https://github.com/asklokesh/tableau-mcp-server) | Tableau data visualization platform | ✅ Ready |

### Accounting & Finance

| Server | Description | Status |
|--------|-------------|--------|
| [QuickBooks MCP Server](https://github.com/asklokesh/quickbooks-mcp-server) | QuickBooks accounting software integration | ✅ Ready |
| [Xero MCP Server](https://github.com/asklokesh/xero-mcp-server) | Xero cloud accounting platform | ✅ Ready |
| [FreshBooks MCP Server](https://github.com/asklokesh/freshbooks-mcp-server) | FreshBooks small business accounting | ✅ Ready |

### Marketing & Communication

| Server | Description | Status |
|--------|-------------|--------|
| [Mailchimp MCP Server](https://github.com/asklokesh/mailchimp-mcp-server) | Email marketing and automation platform | ✅ Ready |
| [Hootsuite MCP Server](https://github.com/asklokesh/hootsuite-mcp-server) | Social media management platform | ✅ Ready |
| [Chanty MCP Server](https://github.com/asklokesh/chanty-mcp-server) | Team collaboration platform | ✅ Ready |

### IT Service Management & Automation

| Server | Description | Status |
|--------|-------------|--------|
| [ServiceNow MCP Server](https://github.com/asklokesh/servicenow-mcp-server) | IT service management platform | ✅ Ready |
| [UiPath MCP Server](https://github.com/asklokesh/uipath-mcp-server) | Robotic Process Automation (RPA) platform | ✅ Ready |

### Version Control

| Server | Description | Status |
|--------|-------------|--------|
| [Git MCP Server](https://github.com/asklokesh/git-mcp-server) | Git repository operations and management | ✅ Ready |

## Key Features

### Enterprise-Ready
- Production-grade error handling
- Comprehensive logging and monitoring
- Rate limiting and retry logic
- Multi-tenant/multi-account support

### Security First
- Multiple authentication methods (OAuth 2.0, API keys, JWT)
- Role-based access control (RBAC)
- Audit logging
- Encryption at rest and in transit

### Developer Friendly
- Consistent API design across all servers
- Comprehensive documentation
- Example code for common use cases
- Easy configuration via environment variables

### GenAI Optimized
- Designed for AI agent integration
- Structured tool definitions
- Context-aware responses
- Batch operation support

## Quick Start

### Installation

Each server can be installed via pip:

```bash
pip install salesforce-mcp-server
pip install aws-mcp-server
pip install hubspot-mcp-server
# ... etc
```

### Basic Usage

All servers follow a consistent pattern:

```python
from salesforce_mcp import SalesforceMCPServer

# Initialize with configuration
server = SalesforceMCPServer(
    instance_url="https://your-instance.salesforce.com",
    username="your-username",
    password="your-password",
    security_token="your-token"
)

# Start the server
server.start()
```

### Claude Desktop Integration

Add any server to your Claude Desktop configuration:

```json
{
  "mcpServers": {
    "salesforce": {
      "command": "python",
      "args": ["-m", "salesforce_mcp.server"],
      "env": {
        "SALESFORCE_INSTANCE_URL": "https://your-instance.salesforce.com",
        "SALESFORCE_USERNAME": "your-username",
        "SALESFORCE_PASSWORD": "your-password",
        "SALESFORCE_SECURITY_TOKEN": "your-token"
      }
    }
  }
}
```

## Architecture

All MCP servers in this collection follow a consistent architecture:

```
server-name-mcp-server/
├── src/
│   └── server_name_mcp/
│       ├── __init__.py
│       ├── server.py      # MCP server implementation
│       ├── client.py      # API client wrapper
│       ├── config.py      # Configuration management
│       ├── auth.py        # Authentication handlers
│       └── exceptions.py  # Custom exceptions
├── tests/
│   ├── test_server.py
│   ├── test_client.py
│   └── test_auth.py
├── examples/
│   ├── basic_usage.py
│   ├── genai_integration.py
│   └── advanced_scenarios.py
├── pyproject.toml
├── README.md
└── LICENSE
```

## Contributing

We welcome contributions! Please see our [Contributing Guide](CONTRIBUTING.md) for details.

### Development Setup

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Add tests
5. Submit a pull request

## Security

- Report security vulnerabilities to security@asklokesh.com
- See [SECURITY.md](SECURITY.md) for our security policy

## Support

- Documentation: Each server has comprehensive README
- Issues: Use GitHub Issues for bug reports and feature requests
- Discussions: Join our GitHub Discussions for community support

## License

All servers in this collection are released under the MIT License. See individual repositories for details.

## Author

**AskLokesh** - Cloud & Agentic AI Solutions Architect

- GitHub: [@asklokesh](https://github.com/asklokesh)
- LinkedIn: [AskLokesh](https://www.linkedin.com/in/iamlokesh/)

---

Built with focus on enterprise integration, security, and GenAI compatibility.