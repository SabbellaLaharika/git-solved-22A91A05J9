# DevOps Simulator

A comprehensive CI/CD configuration management tool for enterprise deployments.

## Project Status
- **Version**: 1.0.0 (Production), 2.0.0-beta (Development)
- **Environments**: Production & Development
- **Student**: SabbellaLaharika
- **Student ID**: 22A91A05J9

## Features

### Core Features
- Automated deployment scripts
- Real-time monitoring
- Configuration management
- Backup and recovery system

### Production Features
- SSL/TLS encryption
- Auto-scaling
- Load balancer integration
- Scheduled backups

### Development Features (Beta)
- Docker Compose integration
- Hot reload enabled
- Debug mode active
- Enhanced logging
- Mock external APIs

## Quick Start

### Production Mode
```bash
export DEPLOY_ENV=production
./scripts/deploy.sh
```

### Development Mode
```bash
export NODE_ENV=development
npm install
npm run dev
```

## Documentation
See `/docs` folder for detailed documentation.

## Contributing
Please read CONTRIBUTING.md before submitting pull requests.

## License
MIT License

---

## ⚠️ Experimental Features (NOT PRODUCTION-READY)

> Use in testing environments ONLY. Not validated for production use.

- 🤖 AI-powered deployment optimization (experimental)
- 🌐 Multi-cloud orchestration — AWS, Azure, GCP (experimental)
- 📈 Predictive scaling with machine learning (experimental)
- 🔒 Zero-trust security architecture (experimental)
- 🎯 Chaos engineering tools (experimental)

To enable experimental features:
```bash
export EXPERIMENTAL_AI=true
./scripts/deploy.sh
```
