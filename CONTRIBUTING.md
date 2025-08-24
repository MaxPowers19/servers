# Contributing to RemoteMCPList

Thank you for your interest in contributing to RemoteMCPList! This guide will help you add new MCP servers to our directory.

## 🚀 How to Contribute

The best way to add a new MCP server is by submitting a Pull Request with your server's YAML file. Don't worry if you're new to Git - we'll guide you through it!

## 📝 Step-by-Step Guide

### 1️⃣ Fork this Repository
Click the "Fork" button at the top right of this page to create your own copy.

### 2️⃣ Create Your Server File
1. Copy `example-server.yaml` as a template
2. Name it `servers/your-server-name.yaml` (use lowercase and hyphens)
3. Fill in all the required fields with your server's information

### 3️⃣ Validate Your File
```bash
python scripts/validate.py servers/your-server-name.yaml
```

### 4️⃣ Submit a Pull Request
1. Commit your changes: `git commit -m "Add [Your Server Name] MCP server"`
2. Push to your fork: `git push origin main`
3. Click "Create Pull Request" on GitHub
4. Fill out the PR template

## 💡 Need Help?

If you're not comfortable with Git or need assistance:
1. [Open an issue](https://github.com/remotemcplist/servers/issues/new) describing your server
2. Include as much information as possible
3. We'll help you create the YAML file and guide you through the PR process

Remember: Pull Requests are the fastest way to get your server added!

## 📝 Contribution Guidelines

### Before You Submit

Please ensure your MCP server:
- ✅ Is publicly accessible (not private/internal)
- ✅ Follows the Model Context Protocol standards
- ✅ Has documentation available
- ✅ Is actively maintained
- ✅ Has a valid HTTP endpoint (MCP uses SSE/streaming HTTP)

### Submission Requirements

1. **Unique ID**: Use lowercase letters and hyphens only (e.g., `github-mcp`)
2. **Accurate Information**: All fields should be current and correct
3. **Working Endpoints**: Test that the HTTP/SSE endpoint is accessible
4. **Clear Description**: Explain what the server does in 50-200 characters
5. **Proper Category**: Choose the most appropriate category

## 📄 File Format

Create a YAML file in the `servers/` directory:

```yaml
id: your-server-mcp
name: Your Server Name
category: development  # Choose appropriate category
description: Brief description (50-200 chars)
# ... see README.md for full format
```

## 🏷️ Valid Categories

- `development` - Version control, CI/CD, code tools
- `data-analysis` - Data processing, analytics
- `communication` - Chat, email, messaging
- `payments` - Payment processing, billing
- `cloud` - Cloud services, infrastructure
- `productivity` - Task management, notes
- `security` - Auth, monitoring, compliance
- `database` - Database connections
- `ai-ml` - AI/ML services
- `monitoring` - Observability, logging

## ✅ Validation

Before submitting, validate your YAML:

```bash
# Install dependencies
pip install pyyaml jsonschema

# Validate your file
python scripts/validate.py servers/your-server-mcp.yaml
```

## 🔄 Pull Request Process

1. **Fork** this repository
2. **Create** a new branch: `git checkout -b add-servername`
3. **Add** your server YAML file
4. **Test** validation locally
5. **Commit** with message: `Add [Server Name] MCP server`
6. **Push** to your fork
7. **Submit** a pull request

## 📋 PR Checklist

Your PR should:
- [ ] Add only one server per PR
- [ ] Pass all validation checks
- [ ] Include a meaningful commit message
- [ ] Not modify other server files
- [ ] Not include generated files

## 🤝 Code of Conduct

- Be respectful and constructive
- Help others with their submissions
- Report issues professionally
- Follow GitHub's community guidelines

## ❓ Getting Help

- **Questions**: Use [GitHub Discussions](https://github.com/remotemcplist/servers/discussions)
- **Issues**: Report bugs via [GitHub Issues](https://github.com/remotemcplist/servers/issues)
- **Website**: Visit [remotemcplist.com](https://remotemcplist.com)

## 🏆 Recognition

Contributors are acknowledged:
- On the website's contributors page
- In release notes
- With a contributors badge

## 📜 License

By contributing, you agree that your contributions will be licensed under the MIT License.

---

Thank you for helping make RemoteMCPList the best resource for MCP servers! 🎉