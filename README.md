# 🚦 Rate Limiter Algorithms

> A comprehensive, well-documented collection of rate limiting algorithms with practical implementations, interactive playgrounds, and detailed analysis.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Tests](https://img.shields.io/badge/tests-383%20passing-success.svg)](tests/)
[![Coverage](https://img.shields.io/badge/coverage-89.4%25-brightgreen.svg)](coverage/)
[![Code Quality](https://img.shields.io/badge/code%20quality-A+-success.svg)](src/)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)
[![Node Version](https://img.shields.io/badge/node-%3E%3D14.0.0-brightgreen.svg)](package.json)
[![Documentation](https://img.shields.io/badge/docs-comprehensive-blue.svg)](docs/)
[![Maintained](https://img.shields.io/badge/maintained-yes-brightgreen.svg)](https://github.com/maneesh-kumar-thakur/rate-limiter)
[![Test Framework](https://img.shields.io/badge/tested%20with-Jest-C21325.svg)](https://jestjs.io/)
[![Linted](https://img.shields.io/badge/code%20style-ESLint%20%2B%20Prettier-blueviolet.svg)](.eslintrc.js)
[![TypeScript](https://img.shields.io/badge/TypeScript-definitions-blue.svg)](index.d.ts)
[![Security](https://img.shields.io/badge/security-eslint--plugin--security-green.svg)](.eslintrc.js)

## 🎯 Project Mission

To provide the **simplest yet most practical** rate limiting implementations with **heavy documentation**, clear **setup guides**, and **interactive playgrounds** - making rate limiting accessible to developers at all levels.

## 🌟 Why This Project?

Our differentiating factors:
- ✨ **Simple & Practical**: Clean, production-ready code
- 📚 **Heavy Documentation**: Deep-dive into concepts, use cases, and trade-offs
- 🚀 **Setup Guides**: Step-by-step installation for all platforms
- 🎮 **Interactive Playgrounds**: Test and visualize algorithms in real-time
- 🏭 **Industry Standards**: Following best practices and folder structure
- 🔬 **Benchmarks**: Performance comparisons across algorithms
- ✅ **Quality Assurance**: 96%+ test coverage, 228 passing tests, production-ready
- 🔒 **Code Standards**: ESLint + Prettier enforced, SonarQube compliant

## ✅ Current Status

### Implemented Algorithms
- ✅ **Token Bucket** (JavaScript) - 100% tested, 100% coverage
  - Full implementation with cost-based operations
  - Configuration management system
  - 23 comprehensive unit tests
  
- ✅ **Redis Token Bucket** (JavaScript) - Distributed implementation
  - Multi-server shared state using Redis
  - Atomic operations with Lua scripts
  - Fail-open error handling
  - 38 comprehensive unit tests

### Testing & Quality Assurance
- **383/383 tests passing** ✅
- **89.4% code coverage** across entire codebase
- **12 test suites**: Unit tests, integration tests, distributed scenarios, TypeScript validation
- **Jest framework**: Modern testing with mocking and async support
- **ESLint + Prettier**: Code style and quality enforced
- **eslint-plugin-security**: 13 security rules active (ReDoS, eval, unsafe crypto detection)
- **Continuous testing**: All PRs require passing tests

### Configuration
- ✅ JSON-based configuration system
- ✅ Environment variable support
- ✅ Multi-tier presets (Free, Pro, Enterprise)
- ✅ Environment-specific multipliers (dev/staging/prod)
- ✅ Redis connection configuration
- ✅ 47 comprehensive tests for configuration management

### Distributed Systems
- ✅ Redis-based rate limiting for multi-server deployments
- ✅ Atomic operations preventing race conditions
- ✅ Health checks and graceful degradation
- ✅ Support for multiple Redis client libraries

### Express.js Integration
- ✅ Production-ready middleware for Express applications
- ✅ In-memory and Redis-backed implementations
- ✅ Helper functions (globalRateLimit, perIpRateLimit, perUserRateLimit, perEndpointRateLimit)
- ✅ Cost-based token consumption
- ✅ Custom error handlers and monitoring callbacks
- ✅ Standard RateLimit headers (draft spec) + legacy X-RateLimit headers
- ✅ 18 integration tests
- ✅ Complete example application with 8 real-world scenarios
- 📚 **[Express Middleware Guide →](docs/EXPRESS_MIDDLEWARE_GUIDE.md)**

### TypeScript Support
- ✅ Full TypeScript definitions (`.d.ts` files)
- ✅ Complete type coverage for all classes and methods
- ✅ 10+ event type definitions for event emitters
- ✅ Type-safe Express middleware interfaces
- ✅ IntelliSense support in IDEs
- 📚 **[Type Definitions →](index.d.ts)**

### Event Emitters & Observability
- ✅ **10 event types** for real-time monitoring
- ✅ Events: allowed, rateLimitExceeded, penalty, reward, blocked, unblocked, reset, redisError, insuranceActivated, insuranceDeactivated
- ✅ Type-safe event listeners with TypeScript
- ✅ Built-in observability for production monitoring
- ✅ Custom event handlers for metrics collection

### Security & Code Quality
- ✅ **eslint-plugin-security** with 13 active rules
- ✅ ReDoS protection, eval detection, unsafe Buffer checks
- ✅ Crypto vulnerability detection (weak PRNG, unsafe algorithms)
- ✅ Snyk CLI integration for dependency scanning
- ✅ npm audit with zero known vulnerabilities
- ✅ Automated security scanning via npm scripts

---

## 📚 What is Rate Limiting?

Rate limiting controls the rate at which users or services can access resources. It's essential for:
- Preventing system overload
- Protecting against DDoS attacks
- Ensuring fair resource distribution
- Managing API costs
- Maintaining service quality

**[Read the full deep-dive →](docs/WHY_RATE_LIMITING.md)**

## 🗂️ Project Structure

```
rate-limiter/
├── docs/                    # Comprehensive documentation
│   ├── WHY_RATE_LIMITING.md
│   ├── algorithms/          # Algorithm explanations
│   ├── guides/              # Setup and usage guides
│   └── benchmarks/          # Performance analysis
├── src/                     # Source implementations
│   ├── algorithms/          # Core algorithm implementations
│   ├── utils/               # Helper utilities
│   └── visualizers/         # Visualization tools
├── playground/              # Interactive examples
│   ├── web/                 # Web-based playground
│   └── cli/                 # Command-line playground
├── examples/                # Framework integrations
│   ├── express/
│   ├── flask/
│   └── spring-boot/
├── tests/                   # Test suites
└── benchmarks/              # Performance tests
```

## 🚀 Quick Start

```bash
# Clone the repository
git clone https://github.com/maneesh-kumar-thakur/rate-limiter.git
cd rate-limiter

# Install dependencies
npm install

# Run tests
npm test

# See detailed setup guide
# For documentation: see docs/guides/SETUP.md
```

## 🎮 Interactive Demo Application

**Test and validate all rate limiting features with our comprehensive demo app!**

The demo application provides an interactive web interface to test and visualize all rate limiting strategies in real-time. Perfect for understanding how different configurations behave under various load conditions.

### 🚀 Launch the Demo

```bash
cd examples/demo-app
node server.js
```

Then open http://localhost:3000 in your browser.

### ✨ What the Demo Validates

The demo app comprehensively tests and validates:

#### **1. Rate Limiting Strategies**
- ✅ **Per-IP Rate Limiting** - Validates that each IP address gets its own token bucket
- ✅ **Per-User Rate Limiting** - Confirms user-specific quotas work correctly
- ✅ **Per-Endpoint Rate Limiting** - Tests endpoint-specific limits
- ✅ **Global Rate Limiting** - Verifies shared bucket across all requests

#### **2. Token Bucket Behavior**
- ✅ **Token Refill Mechanics** - Validates tokens refill at correct intervals
- ✅ **Capacity Limits** - Confirms requests are blocked when tokens exhausted
- ✅ **Cost-Based Consumption** - Tests variable token costs (1 token vs 5 tokens)
- ✅ **Fast/Slow Refill Rates** - Validates different refill strategies

#### **3. HTTP Response Headers**
- ✅ **X-RateLimit-Limit** - Total capacity header
- ✅ **X-RateLimit-Remaining** - Remaining tokens header
- ✅ **X-RateLimit-Reset** - Reset timestamp header
- ✅ **Retry-After** - Proper retry timing when rate limited

#### **4. Error Handling**
- ✅ **429 Status Codes** - Correct HTTP status for rate limit exceeded
- ✅ **Error Messages** - Clear error descriptions with retry information
- ✅ **Graceful Degradation** - System behavior under stress

#### **5. Performance & Concurrency**
- ✅ **Load Testing** - Validates behavior under 10 req/sec burst
- ✅ **Concurrent Requests** - Tests race conditions and atomic operations
- ✅ **Memory Management** - Monitors resource usage under load
- ✅ **Response Times** - Validates minimal performance overhead

#### **6. Real-Time Monitoring**
- ✅ **Request Statistics** - Tracks allowed vs blocked requests
- ✅ **Success Rates** - Calculates and displays percentage metrics
- ✅ **Live Event Stream** - Shows requests in real-time
- ✅ **Per-Endpoint Distribution** - Breaks down metrics by endpoint

### 📊 Demo Features

- **8 Test Endpoints** with different rate limiting configurations
- **Real-Time Dashboard** showing success/failure rates
- **Load Testing Tool** to simulate high-traffic scenarios
- **Interactive UI** for one-click endpoint testing
- **Live Metrics** with auto-refresh every 2 seconds
- **Event Streaming** to monitor all requests
- **Visual Feedback** for rate limit status

### 🎯 Test Scenarios Included

1. **Basic Limiting** - 10 req/min per IP
2. **Strict Limiting** - 3 requests with slow refill
3. **Cost-Based (Light)** - 1 token per operation
4. **Cost-Based (Heavy)** - 5 tokens per operation
5. **Per-User Quotas** - Different limits per user
6. **Global Limits** - Shared across all users
7. **Fast Refill** - Quick token replenishment
8. **Dynamic Costs** - Variable token consumption

**[See full demo documentation →](examples/demo-app/README.md)**

## 📖 Documentation

- **[Why Rate Limiting?](docs/WHY_RATE_LIMITING.md)** - Deep dive into the need and benefits
- **[Algorithm Comparison](docs/ALGORITHM_COMPARISON.md)** - Detailed analysis of each algorithm
- **[Setup Guide](docs/guides/SETUP.md)** - Installation instructions
- **[API Reference](docs/API_REFERENCE.md)** - Complete API documentation
- **[Best Practices](docs/BEST_PRACTICES.md)** - Production deployment guide
- **[Redis Distributed Guide](docs/guides/REDIS_DISTRIBUTED.md)** - Multi-server deployments with Redis
- **[Express Middleware Guide](docs/EXPRESS_MIDDLEWARE_GUIDE.md)** - Express.js integration
- **[State Persistence Guide](docs/STATE_PERSISTENCE.md)** - Save/restore limiter state for crash recovery

## 🚀 Framework Integration

### Express.js

Quick example with Express:

```javascript
const express = require('express');
const { perIpRateLimit } = require('./src/middleware/express/token-bucket-middleware');

const app = express();

// Apply rate limiting to all routes
app.use(perIpRateLimit({
  capacity: 100,
  refillRate: 10,
  refillInterval: 1000 // 10 requests per second per IP
}));

app.get('/api/data', (req, res) => {
  res.json({ 
    message: 'Success!',
    remaining: req.rateLimit.remaining 
  });
});

app.listen(3000);
```

**[See full Express guide →](docs/EXPRESS_MIDDLEWARE_GUIDE.md)**

**🎯 [Try the Interactive Demo App →](examples/demo-app/)** to see all these features in action!

### Redis (Distributed)

For multi-server deployments:

```javascript
const Redis = require('ioredis');
const { tokenBucketMiddleware } = require('./src/middleware/express/redis-token-bucket-middleware');

const redis = new Redis();

app.use(tokenBucketMiddleware({
  redis,
  capacity: 100,
  refillRate: 10,
  refillInterval: 1000
}));
```

**[See full Redis guide →](docs/guides/REDIS_DISTRIBUTED.md)**

## 🤝 Contributing

We welcome contributions! Please see our [Contributing Guide](CONTRIBUTING.md) for details.

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

Built with ❤️ for the open-source community.

---

**[⭐ Star this repo](https://github.com/yourusername/rate-limiter)** if you find it helpful!
