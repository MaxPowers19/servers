# RemoteMCPList Servers Directory

[![Website](https://img.shields.io/badge/website-remotemcplist.com-blue)](https://remotemcplist.com)
[![Servers](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fremotemcplist.com%2Fapi%2Fservers.json&query=%24.count&label=MCP%20Servers&color=green)](https://remotemcplist.com/servers)
[![License](https://img.shields.io/badge/license-MIT-purple)](LICENSE)
[![Contribute](https://img.shields.io/badge/contribute-welcome-orange)](CONTRIBUTING.md)

🚀 **The premier community-driven directory of remote Model Context Protocol (MCP) servers**

This repository contains the data that powers [RemoteMCPList.com](https://remotemcplist.com), the #1 directory for discovering and learning about remote MCP servers.

## 🎯 Quick Links

- 🌐 **Browse Servers**: [remotemcplist.com](https://remotemcplist.com)
- 📚 **API Access**: [remotemcplist.com/api/servers.json](https://remotemcplist.com/api/servers.json)
- 🤖 **AI Discovery**: [remotemcplist.com/llms.txt](https://remotemcplist.com/llms.txt)
- 📋 **Submit Server**: [Contributing Guide](https://github.com/remotemcplist/servers/blob/main/CONTRIBUTING.md)

## 🤝 Contributing a New Server

### Option 1: For Technical Users (Direct PR)
1. Fork this repository
2. Copy `example-server.yaml` to `servers/your-server.yaml`
3. Fill in your server details
4. Run validation: `python scripts/validate.py servers/your-server.yaml`
5. Submit a pull request

### Option 2: For Everyone (Request Form)
1. [Open a server request issue](https://github.com/remotemcplist/servers/issues/new/choose)
2. Fill out the structured form
3. We'll help you create the YAML and PR

📖 **[Full guide in CONTRIBUTING.md](CONTRIBUTING.md)**

## 📄 Server YAML Format

Each server must have a YAML file in the `servers/` directory following this structure:

```yaml
id: github-mcp                    # Unique identifier (lowercase, hyphens)
name: GitHub MCP Server           # Display name
category: development             # One of: development, data-analysis, communication, 
                                 # payments, cloud, productivity, security, database, 
                                 # ai-ml, monitoring
description: Complete GitHub integration for MCP  # 20-200 characters
long_description: |               # Detailed description (must be longer than description)
  The GitHub MCP Server provides comprehensive access to GitHub's API,
  enabling AI assistants to manage repositories, issues, pull requests,
  and automate development workflows through the Model Context Protocol.

maintainer:
  name: Anthropic                 # Your name or organization
  github: anthropic               # GitHub username
  website: anthropic.com          # Optional (domain or full URL)

authentication:
  type: oauth2                    # One of: oauth2, api-key, none
  provider: github                # e.g., github, google, custom
  instructions: |                 # How to get credentials
    1. Go to GitHub Settings > Developer settings
    2. Create a personal access token
    3. Configure in your MCP client

endpoints:
  production: https://github-mcp.example.com      # Required
  sandbox: https://sandbox.github-mcp.example.com # Optional

capabilities:                     # List what the server can do
  - id: repository.read
    name: Read Repositories
    description: Access repository contents and metadata
  - id: issues.manage
    name: Manage Issues  
    description: Create, update, and close issues

tags:                            # For search/filtering
  - github
  - version-control
  - development
  - mcp
  - remote

verification:
  status: pending                # verified, pending, or unverified
  tested_date: "2024-12-10T00:00:00Z"
  security_audit: false

featured: false                  # Show on homepage (only one should be true)
```

## 📁 Repository Structure

```
servers/
├── github-mcp.yaml      # Individual server files
├── stripe-mcp.yaml
├── slack-mcp.yaml
└── ...

scripts/
├── validate.py          # Validation script
└── check_urls.py        # URL checker

.github/
├── ISSUE_TEMPLATE/
│   └── new-server.yml   # Issue template for submissions
└── workflows/
    └── validate.yml     # Auto-validation on PRs
```

## ✅ Validation

All submissions are automatically validated for:
- Valid YAML syntax
- Required fields present
- Correct category values
- Valid URLs
- Proper date formats

Run validation locally:
```bash
python scripts/validate.py
```

## 🏷️ Categories

- **development** - Version control, CI/CD, code tools
- **data-analysis** - Data processing, analytics, BI tools
- **communication** - Chat, email, messaging platforms
- **payments** - Payment processing, billing, invoicing
- **cloud** - Cloud services, hosting, infrastructure
- **productivity** - Task management, notes, calendars
- **security** - Authentication, monitoring, compliance
- **database** - Database connections and management
- **ai-ml** - AI/ML services and model providers
- **monitoring** - Observability, logging, metrics

## 🔍 How It Works

1. **Submit** - Create a YAML file for your MCP server
2. **Validate** - Automatic checks ensure quality
3. **Review** - Community members review submissions
4. **Merge** - Approved servers are added
5. **Deploy** - Changes appear on remotemcplist.com within minutes

## 📊 API Access

Access the data programmatically:

```bash
# Get all servers
curl https://remotemcplist.com/api/servers.json

# Get specific server
curl https://remotemcplist.com/api/servers/github-mcp.json

# Search servers
curl "https://remotemcplist.com/api/search?q=github"
```

## 🤖 For AI Assistants

AI assistants can discover MCP servers via:
- **llms.txt**: https://remotemcplist.com/llms.txt
- **API**: Structured JSON data
- **Sitemap**: https://remotemcplist.com/sitemap.xml

## 📜 License

This repository is licensed under the MIT License. See [LICENSE](LICENSE) for details.

## 🙏 Acknowledgments

Inspired by awesome-lists and the MCP community. Special thanks to all contributors!

## 🔗 Links

- **Website**: [remotemcplist.com](https://remotemcplist.com)
- **API Docs**: [remotemcplist.com/api/docs](https://remotemcplist.com/api/docs)
- **Submit Server**: [New Issue](https://github.com/remotemcplist/servers/issues/new?template=new-server.yml)
- **Discussion**: [GitHub Discussions](https://github.com/remotemcplist/servers/discussions)

---

<p align="center">
  Made with ❤️ for the MCP community
  <br>
  <a href="https://remotemcplist.com">remotemcplist.com</a>
</p>