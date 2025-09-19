# Engine Meta

[![License](https://img.shields.io/badge/License-MIT-green.svg)](https://opensource.org/licenses/MIT)

**Engine Framework Meta Repository** - Coordination, releases, and cross-repository management for the AI Agent Orchestration System.

## 🎯 Purpose

This meta-repository coordinates the Engine Framework multirepo architecture, managing:
- Release coordination across all repositories
- Cross-repository documentation
- Development workflow automation
- Community and contribution management

## 📁 Structure

```
engine-meta/
├── scripts/             # Automation scripts
│   ├── release.sh      # Release coordination
│   ├── test-all.sh     # Cross-repo testing
│   ├── setup-dev.sh    # Development setup
│   └── deploy.sh       # Deployment automation
├── docs/               # Cross-repository docs
│   ├── architecture/   # System architecture
│   ├── contributing/   # Contribution guidelines
│   ├── migration/      # Migration guides
│   └── roadmap/        # Product roadmap
├── .github/            # GitHub automation
│   ├── workflows/      # Meta-repo CI/CD
│   └── ISSUE_TEMPLATE/ # Issue templates
└── docker-compose.yml  # Development environment
```

## 🚀 Quick Start

### Development Setup

```bash
# Clone meta repository
git clone https://github.com/engine-agi/engine-meta.git
cd engine-meta

# Setup development environment
./scripts/setup-dev.sh

# Start all services
docker-compose up -d
```

### Release Coordination

```bash
# Coordinate release across all repos
./scripts/release.sh --version 1.1.0

# Run tests across all repositories
./scripts/test-all.sh
```

## 📊 Release Management

### Version Coordination

Engine Framework uses coordinated versioning across all repositories:

```
engine-core:     v1.1.0
engine-cli:      v1.1.0
engine-web:      v1.1.0
engine-examples: v1.1.0
engine-infra:    v1.1.0
```

### Release Process

1. **Planning**: Create release issue with changelog
2. **Testing**: Run cross-repository test suite
3. **Release**: Coordinate releases in dependency order
4. **Communication**: Update documentation and announce

### Dependency Order

```
1. engine-core     (no dependencies)
2. engine-cli      (depends on core)
3. engine-web      (depends on core)
4. engine-examples (depends on core + cli)
5. engine-infra    (depends on all)
```

## 🔧 Automation Scripts

### Release Script

```bash
# Full release process
./scripts/release.sh --version 1.1.0 --repos "core,cli,web"

# Patch release
./scripts/release.sh --version 1.0.1 --patch
```

### Testing Script

```bash
# Test all repositories
./scripts/test-all.sh

# Test specific repositories
./scripts/test-all.sh --repos "core,cli"
```

### Development Setup

```bash
# Setup complete development environment
./scripts/setup-dev.sh

# Setup specific components
./scripts/setup-dev.sh --components "core,web"
```

## 📚 Documentation

### Architecture Documentation
- [System Architecture](docs/architecture/overview.md)
- [API Contracts](docs/architecture/contracts.md)
- [Data Models](docs/architecture/data-models.md)

### Development Guides
- [Contributing](docs/contributing/overview.md)
- [Development Setup](docs/contributing/setup.md)
- [Code Standards](docs/contributing/standards.md)

### Migration Guides
- [Monorepo to Multirepo](docs/migration/overview.md)
- [Upgrading Versions](docs/migration/upgrading.md)
- [Breaking Changes](docs/migration/breaking-changes.md)

## 🎯 Roadmap

### Q4 2025
- [ ] Release v1.1.0 with enhanced workflows
- [ ] Community documentation improvements
- [ ] Performance optimizations

### Q1 2026
- [ ] Plugin system architecture
- [ ] Advanced monitoring capabilities
- [ ] Enterprise features

## 🤝 Community Management

### Contribution Workflow
1. **Issue Creation**: Use appropriate repository
2. **Development**: Follow contribution guidelines
3. **Review**: Cross-repository review process
4. **Release**: Coordinated release process

### Communication Channels
- **GitHub Issues**: Repository-specific issues
- **GitHub Discussions**: General discussions
- **Discord**: Community chat
- **Newsletter**: Release announcements

## 📊 Metrics & Monitoring

### Repository Health
- Test coverage across all repos
- CI/CD pipeline status
- Issue resolution time
- Release frequency

### Community Metrics
- Contributor growth
- Issue creation rate
- PR merge rate
- User adoption

## 🛠️ Development Tools

### Local Development
```bash
# Start development environment
docker-compose up -d

# Run all tests
./scripts/test-all.sh

# Generate documentation
./scripts/docs-build.sh
```

### CI/CD Integration
- Automated testing across repositories
- Release coordination
- Documentation deployment
- Security scanning

## 📞 Support & Communication

### Getting Help
- **Documentation**: Check repository-specific docs first
- **Issues**: Create in appropriate repository
- **Discussions**: Use for general questions
- **Discord**: Real-time community support

### Reporting Issues
- **Bug Reports**: Use repository-specific issue templates
- **Feature Requests**: Start discussion first
- **Security Issues**: Contact maintainers directly

## 🤝 Contributing to Meta

### Areas for Contribution
- **Documentation**: Improve guides and tutorials
- **Scripts**: Enhance automation tools
- **Processes**: Improve development workflows
- **Community**: Help with community management

### Contribution Process
1. Check existing issues and discussions
2. Follow contribution guidelines
3. Submit PR with clear description
4. Participate in review process

## 📄 License

MIT License - see [LICENSE](LICENSE) for details.

---

**Engine Framework Coordination** | [engine-agi](https://github.com/engine-agi)