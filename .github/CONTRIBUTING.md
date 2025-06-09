# Contributing to LokiMCPUniverse

Thank you for your interest in contributing to our MCP servers collection! We welcome contributions from the community.

## How to Contribute

### Reporting Issues
- Use our issue templates for bug reports and feature requests
- Provide detailed information about your environment
- Include steps to reproduce any bugs

### Requesting New Platforms
- Use the "New Platform Request" template
- Provide API documentation links
- Explain the business use case

### Code Contributions

#### Getting Started
1. Fork the repository
2. Clone your fork locally
3. Create a feature branch
4. Make your changes
5. Test thoroughly
6. Submit a pull request

#### Development Setup
```bash
git clone https://github.com/LokiMCPUniverse/[server-name]
cd [server-name]
pip install -e ".[dev]"
pytest
```

#### Code Standards
- Follow existing code style
- Add comprehensive tests
- Update documentation
- Use type hints where applicable
- Follow security best practices

#### Commit Message Format
```
type(scope): brief description

Detailed explanation if needed

Fixes #issue-number
```

Types: feat, fix, docs, style, refactor, test, chore

### New MCP Server Development

#### Architecture Requirements
All MCP servers must follow our standard architecture:

```
server-name-mcp-server/
├── src/server_name_mcp/
│   ├── __init__.py
│   ├── server.py          # MCP protocol implementation
│   ├── client.py          # Platform API client
│   ├── auth.py            # Authentication handlers
│   ├── config.py          # Configuration management
│   └── exceptions.py      # Custom error types
├── tests/                 # Comprehensive test suite
├── examples/              # Integration examples
├── pyproject.toml         # Project configuration
├── README.md             # Detailed documentation
└── LICENSE               # MIT License
```

#### Security Requirements
- Use secure authentication methods (OAuth 2.0, JWT)
- Implement rate limiting
- Add comprehensive error handling
- Follow least privilege principles
- Sanitize all inputs

#### Testing Requirements
- Unit tests for all components
- Integration tests with mock APIs
- Error handling tests
- Performance tests for bulk operations
- Security tests for authentication

#### Documentation Requirements
- Comprehensive README with examples
- API documentation
- Configuration guide
- Troubleshooting section
- Claude Desktop integration example

### Review Process
1. All submissions require review
2. Maintainers will provide feedback
3. Address review comments
4. Tests must pass
5. Documentation must be updated

### Code of Conduct
- Be respectful and professional
- Focus on constructive feedback
- Help others learn and improve
- Follow GitHub's community guidelines

### Getting Help
- Open a discussion for questions
- Join our community discussions
- Check existing issues and documentation
- Reach out to maintainers for guidance

### Recognition
Contributors will be recognized in:
- Repository contributors list
- Release notes for significant contributions
- Project documentation
- Community showcases

## Development Workflow

### Branch Naming
- feature/platform-name-integration
- fix/issue-description
- docs/section-update
- refactor/component-name

### Testing Locally
```bash
# Run tests
pytest

# Run linting
ruff check .

# Run type checking
mypy src/

# Test installation
pip install -e .
```

### Submitting Changes
1. Ensure all tests pass
2. Update documentation
3. Follow pull request template
4. Link related issues
5. Request review from maintainers

Thank you for contributing to the future of enterprise AI integration!