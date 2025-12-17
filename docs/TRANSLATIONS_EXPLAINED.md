# SperaxOS Agent Index System - Complete Technical Documentation

## 📋 Table of Contents

1. [System Overview](#system-overview)
2. [Directory Structure](#directory-structure)
3. [Data Flow Architecture](#data-flow-architecture)
4. [Agent Schema Specification](#agent-schema-specification)
5. [Translation System](#translation-system)
6. [Build System](#build-system)
7. [Deployment Pipeline](#deployment-pipeline)
8. [Agent Development Guide](#agent-development-guide)
9. [Quality Assurance](#quality-assurance)
10. [API Reference](#api-reference)

---

## System Overview

### What is SperaxOS Agent Index?

The SperaxOS Agent Index is a centralized repository and discovery system for DeFi AI agents. It provides:

- **41 specialized DeFi agents** covering yield optimization, security analysis, risk management, and more
- **18 language translations** for global accessibility
- **Standardized JSON schema** for agent metadata and configuration
- **Automated build pipeline** for GitHub Pages deployment
- **Developer-friendly** agent creation workflow

### Key Features

| Feature | Description |
|---------|-------------|
| **Multi-language Support** | 18 languages including English, Chinese, Japanese, Korean, Arabic, and more |
| **Type-Safe Schema** | JSON Schema v1 validation for all agents |
| **Automated Translation** | OpenAI GPT-4.1-nano powered translation with incremental updates |
| **GitHub Pages Hosting** | Static deployment with CDN distribution |
| **SEO Optimized** | Schema.org markup and metadata for discoverability |
| **Version Control** | Git-based workflow with automated CI/CD |

### Repository Information

- **Repository:** `speraxos/SperaxOS-AI-Agents`
- **Production URL:** `https://github.com/speraxos/SperaxOS-AI-Agents`
- **Schema Version:** v1
- **Total Agents:** 41
- **Supported Languages:** 18

---

## Directory Structure

```
AI-Agents-Library/
├── src/                                    # Source agent definitions
│   ├── airdrop-hunter.json                # Individual agent files
│   ├── alpha-leak-detector.json
│   ├── apy-vs-apr-educator.json
│   └── ...                                # 41 total agents
│
├── locales/                               # Generated translations
│   ├── airdrop-hunter/
│   │   ├── index.json                     # Default (en-US)
│   │   ├── index.ar.json                  # Arabic
│   │   ├── index.zh-CN.json               # Simplified Chinese
│   │   ├── index.zh-TW.json               # Traditional Chinese
│   │   ├── index.ja-JP.json               # Japanese
│   │   ├── index.ko-KR.json               # Korean
│   │   └── ...                            # 18 total languages
│   └── ...                                # 41 agent directories
│
├── public/                                # Build output (deployed to GitHub Pages)
│   ├── index.json                         # Main agent index (en-US)
│   ├── index.ar.json                      # Arabic index
│   ├── index.zh-CN.json                   # Simplified Chinese index
│   ├── index.zh-TW.json                   # Traditional Chinese index
│   ├── index.ja-JP.json                   # Japanese index
│   ├── index.ko-KR.json                   # Korean index
│   └── ...                                # 18 total language indexes
│   └── schema/
│       └── speraxAgentSchema_v1.json      # JSON Schema definition
│
├── schema/                                # Schema source
│   └── speraxAgentSchema_v1.json          # Master schema file
│
├── scripts/                               # Build and translation scripts
│   ├── commands/
│   │   ├── format.ts                      # Translation workflow
│   │   └── build.ts                       # Build workflow
│   └── workflows/
│       ├── agents-config.ts               # Agent configuration
│       ├── i18n.ts                        # Translation logic
│       └── schema.ts                      # Schema validation
│
└── .github/workflows/                     # CI/CD automation
    └── deploy.yml                         # GitHub Pages deployment
```

### File Naming Conventions

| Pattern | Description | Example |
|---------|-------------|---------|
| `src/*.json` | Source agent definition | `yield-dashboard-builder.json` |
| `locales/{agent}/index.json` | Default language (en-US) | `locales/spa-tokenomics-analyst/index.json` |
| `locales/{agent}/index.{locale}.json` | Translated version | `locales/spa-tokenomics-analyst/index.zh-CN.json` |
| `public/index.json` | Main agent index | `public/index.json` |
| `public/index.{locale}.json` | Translated index | `public/index.ko-KR.json` |

---

## Data Flow Architecture

### Complete Workflow Diagram

```
┌─────────────────────────────────────────────────────────────────┐
│                     AGENT CREATION PHASE                         │
└─────────────────────────────────────────────────────────────────┘
                              │
                              ▼
                    Developer creates agent
                      in src/*.json with
                       required fields
                              │
                              ▼
                    ┌──────────────────┐
                    │  Source Agent    │
                    │  (src/*.json)    │
                    │                  │
                    │  • author        │
                    │  • meta          │
                    │  • config        │
                    │  • systemRole    │
                    └──────────────────┘
                              │
                              ▼
┌─────────────────────────────────────────────────────────────────┐
│                    TRANSLATION PHASE                             │
│                   (bun run format)                               │
└─────────────────────────────────────────────────────────────────┘
                              │
                              ▼
                    ┌──────────────────┐
                    │  Token Counter   │
                    │  Calculates cost │
                    │  per agent       │
                    └──────────────────┘
                              │
                              ▼
                    ┌──────────────────┐
                    │  AI Translation  │
                    │  (GPT-4.1-nano)  │
                    │                  │
                    │  en-US → 17 langs│
                    │  • ar            │
                    │  • bg-BG         │
                    │  • zh-TW         │
                    │  • zh-CN         │
                    │  • ja-JP         │
                    │  • ko-KR         │
                    │  • etc...        │
                    └──────────────────┘
                              │
                              ▼
                    ┌──────────────────┐
                    │ Language Detector│
                    │ Validates output │
                    │ matches target   │
                    └──────────────────┘
                              │
                              ▼
                    ┌──────────────────┐
                    │  Locale Files    │
                    │  Generated in    │
                    │  locales/{agent}/│
                    │                  │
                    │  • index.json    │
                    │  • index.ar.json │
                    │  • index.zh-CN...│
                    └──────────────────┘
                              │
                              ▼
┌─────────────────────────────────────────────────────────────────┐
│                      BUILD PHASE                                 │
│                    (bun run build)                               │
└─────────────────────────────────────────────────────────────────┐
                              │
                              ▼
                    ┌──────────────────┐
                    │ Schema Builder   │
                    │ Creates v1 schema│
                    └──────────────────┘
                              │
                              ▼
                    ┌──────────────────┐
                    │ Agent Collector  │
                    │ Scans locales/   │
                    │ for all agents   │
                    └──────────────────┘
                              │
                              ▼
                    ┌──────────────────┐
                    │  Tag Aggregator  │
                    │  Builds tag list │
                    │  with counts     │
                    └──────────────────┘
                              │
                              ▼
                    ┌──────────────────┐
                    │  Index Builder   │
                    │  Generates       │
                    │  public/*.json   │
                    │                  │
                    │  • index.json    │
                    │  • index.ar.json │
                    │  • index.zh-CN...│
                    └──────────────────┘
                              │
                              ▼
┌─────────────────────────────────────────────────────────────────┐
│                   DEPLOYMENT PHASE                               │
│              (GitHub Actions on push to main)                    │
└─────────────────────────────────────────────────────────────────┘
                              │
                              ▼
                    ┌──────────────────┐
                    │   Git Push       │
                    │   to main branch │
                    └──────────────────┘
                              │
                              ▼
                    ┌──────────────────┐
                    │ GitHub Actions   │
                    │ Triggered        │
                    └──────────────────┘
                              │
                              ▼
                    ┌──────────────────┐
                    │ Build Workflow   │
                    │ • Install deps   │
                    │ • Run build      │
                    │ • Generate output│
                    └──────────────────┘
                              │
                              ▼
                    ┌──────────────────┐
                    │ GitHub Pages     │
                    │ Deploy public/   │
                    │ to gh-pages      │
                    └──────────────────┘
                              │
                              ▼
                    ┌──────────────────┐
                    │  Production CDN  │
                    │  Available at:   │
                    │                  │
                    │                  │
                    └──────────────────┘
                              │
                              ▼
┌─────────────────────────────────────────────────────────────────┐
│                    CONSUMPTION PHASE                             │
└─────────────────────────────────────────────────────────────────┘
                              │
                              ▼
                    ┌──────────────────┐
                    │  SperaxOS App    │
                    │  Fetches index   │
                    │  from CDN        │
                    └──────────────────┘
                              │
                              ▼
                    ┌──────────────────┐
                    │  User Interface  │
                    │  Displays agents │
                    │  in marketplace  │
                    └──────────────────┘
```

### Data Transformation Example

**Input (src/airdrop-hunter.json):**
```json
{
  "author": "SperaxOS",
  "config": {
    "systemRole": "You are an expert airdrop hunter..."
  },
  "meta": {
    "title": "Airdrop Hunter",
    "description": "Track and analyze crypto airdrops...",
    "tags": ["airdrop", "tokens", "defi"]
  }
}
```

**Translation Output (locales/airdrop-hunter/index.zh-CN.json):**
```json
{
  "author": "SperaxOS",
  "config": {
    "systemRole": "你是一位专业的空投猎人..."
  },
  "meta": {
    "title": "空投猎手",
    "description": "跟踪和分析加密货币空投...",
    "tags": ["空投", "代币", "去中心化金融"]
  },
  "schemaVersion": 1
}
```

**Build Output (public/index.json):**
```json
{
  "agents": [
    {
      "author": "SperaxOS",
      "createdAt": "2024-12-17",
      "identifier": "airdrop-hunter",
      "meta": {
        "avatar": "🎯",
        "tags": ["airdrop", "tokens", "defi"],
        "title": "Airdrop Hunter"
      },
      "schemaVersion": 1
    },
    // ... 40 more agents
  ],
  "tags": [
    "defi",
    "yield",
    "security",
    // ... more tags with counts
  ],
  "schemaVersion": 1
}
```

---

## Agent Schema Specification

### SperaxOS Agent Schema v1

**Location:** `schema/speraxAgentSchema_v1.json`

**Full Schema Definition:**

```json
{
  "$schema": "http://json-schema.org/draft-07/schema#",
  "type": "object",
  "title": "SperaxOS Agent Schema",
  "description": "Schema for SperaxOS DeFi AI agents",
  "required": ["author", "config", "createdAt", "homepage", "identifier", "meta", "schemaVersion"],
  "properties": {
    "author": {
      "type": "string",
      "description": "Agent author/creator"
    },
    "config": {
      "type": "object",
      "required": ["systemRole"],
      "properties": {
        "systemRole": {
          "type": "string",
          "description": "System prompt/role for the agent"
        }
      }
    },
    "createdAt": {
      "type": "string",
      "format": "date",
      "description": "Creation date (YYYY-MM-DD)"
    },
    "homepage": {
      "type": "string",
      "format": "uri",
      "description": "Agent homepage URL"
    },
    "identifier": {
      "type": "string",
      "pattern": "^[a-z0-9-]+$",
      "description": "Unique agent identifier (kebab-case)"
    },
    "meta": {
      "type": "object",
      "required": ["avatar", "description", "tags", "title"],
      "properties": {
        "avatar": {
          "type": "string",
          "description": "Emoji or icon for the agent"
        },
        "description": {
          "type": "string",
          "description": "Brief description of agent capabilities"
        },
        "tags": {
          "type": "array",
          "items": {
            "type": "string"
          },
          "description": "Categorization tags"
        },
        "title": {
          "type": "string",
          "description": "Display name of the agent"
        }
      }
    },
    "schemaVersion": {
      "type": "integer",
      "const": 1,
      "description": "Schema version number"
    }
  }
}
```

### Field Specifications

#### Required Fields

| Field | Type | Format | Description | Example |
|-------|------|--------|-------------|---------|
| `author` | string | - | Creator of the agent | `"SperaxOS"` |
| `config.systemRole` | string | Markdown | Agent's system prompt | `"You are a DeFi yield optimizer..."` |
| `createdAt` | string | YYYY-MM-DD | Creation date | `"2024-12-17"` |
| `homepage` | string | URL | Agent's homepage | `"https://github.com/speraxos/SperaxOS-AI-Agents"` |
| `identifier` | string | kebab-case | Unique ID | `"yield-dashboard-builder"` |
| `meta.avatar` | string | Emoji/Icon | Visual identifier | `"📊"` |
| `meta.description` | string | - | Agent description | `"Build comprehensive yield dashboards"` |
| `meta.tags` | array | - | Category tags | `["yield", "dashboard", "defi"]` |
| `meta.title` | string | - | Display name | `"Yield Dashboard Builder"` |
| `schemaVersion` | integer | - | Always `1` | `1` |

#### Optional Fields

| Field | Type | Description | Example |
|-------|------|-------------|---------|
| `config.model` | string | Recommended AI model | `"claude-sonnet-4-20250514"` |
| `config.temperature` | number | Model temperature (0-1) | `0.7` |
| `meta.category` | string | Primary category | `"yield-optimization"` |

### Validation Rules

1. **Identifier Format:**
   - Must be lowercase
   - Use hyphens for spaces
   - No special characters except hyphens
   - Must be unique across all agents
   - Example: `spa-tokenomics-analyst` ✅
   - Invalid: `SPA Tokenomics Analyst` ❌

2. **System Role Requirements:**
   - Must be clear and specific
   - Should define expertise and capabilities
   - Can include example interactions
   - Typically 200-1000 characters

3. **Tags Best Practices:**
   - 2-7 tags per agent
   - Use lowercase
   - Common tags: `defi`, `yield`, `security`, `risk`, `staking`, `tokens`, `nft`
   - Avoid overly specific tags

4. **Avatar Guidelines:**
   - Use single emoji character
   - Should represent agent's function
   - Examples: 📊 (dashboard), 🔒 (security), 💰 (yield), 🎯 (targeting)

---

## Translation System

### Translation Workflow

**Command:** `bun run format`

**Process Flow:**

```
1. Load source agents from src/*.json
2. Calculate token usage per agent
3. For each agent:
   a. Skip en-US (default language)
   b. Check existing translations
   c. Translate new/modified fields
   d. Validate language detection
   e. Merge with existing translations
   f. Save to locales/{agent}/index.{locale}.json
4. Handle rate limiting (200K tokens/minute)
5. Resume from last checkpoint on interruption
```

### Supported Languages

| Code | Language | Native Name |
|------|----------|-------------|
| `en-US` | English | English |
| `ar` | Arabic | العربية |
| `bg-BG` | Bulgarian | Български |
| `zh-CN` | Simplified Chinese | 简体中文 |
| `zh-TW` | Traditional Chinese | 繁體中文 |
| `de-DE` | German | Deutsch |
| `es-ES` | Spanish | Español |
| `fr-FR` | French | Français |
| `it-IT` | Italian | Italiano |
| `ja-JP` | Japanese | 日本語 |
| `ko-KR` | Korean | 한국어 |
| `nl-NL` | Dutch | Nederlands |
| `pl-PL` | Polish | Polski |
| `pt-BR` | Portuguese (Brazil) | Português |
| `ru-RU` | Russian | Русский |
| `tr-TR` | Turkish | Türkçe |
| `vi-VN` | Vietnamese | Tiếng Việt |
| `fa-IR` | Persian | فارسی |

### Translation Configuration

**File:** `scripts/workflows/i18n.ts`

```typescript
export const TRANSLATION_CONFIG = {
  model: 'gpt-4.1-nano',
  temperature: 0.3,
  maxTokens: 2000,
  
  rateLimits: {
    tokensPerMinute: 200000,
    requestsPerMinute: 500,
    retryAfterMs: 1000
  },
  
  validation: {
    languageDetection: true,
    schemaValidation: true,
    retryOnFailure: true,
    maxRetries: 2
  },
  
  incremental: {
    enabled: true,
    skipExisting: true,
    mergeStrategy: 'preserve-existing'
  }
};
```

### Translation Quality Assurance

1. **Pre-Translation Validation:**
   - Source file has valid JSON
   - All required fields present
   - Schema version matches

2. **Translation Process:**
   - GPT-4.1-nano with low temperature (0.3)
   - Context-aware translation
   - DeFi terminology preservation
   - Technical terms remain in English where appropriate

3. **Post-Translation Validation:**
   - Language detection confirms target language
   - JSON structure maintained
   - Required fields preserved
   - Character encoding verified (UTF-8)

4. **Incremental Translation:**
   - Only translates new/modified fields
   - Preserves existing translations
   - Merges new content with old
   - Tracks completion status

### Translation Cost Estimation

**Formula:**
```
Total Cost = (Agents × Languages × Avg Tokens × Price per Token)

Example for 41 agents:
- Agents: 41
- Languages: 17 (excluding en-US)
- Avg tokens per agent per language: ~400
- Total tokens: 41 × 17 × 400 = 278,800 tokens
- Cost at $0.15/1M tokens: ~$0.04

Full translation: ~$0.04-0.05
```

### Incremental Translation Benefits

| Feature | Benefit |
|---------|---------|
| **Skip Completed** | Only translate new agents |
| **Resume on Failure** | Continue from interruption point |
| **Merge Strategy** | Preserve manual edits |
| **Cost Efficiency** | Only pay for new translations |
| **Time Efficiency** | Fast updates for single agent changes |

---

## Build System

### Build Workflow

**Command:** `bun run build`

**Process:**

```
1. Schema Building
   ├── Load schema/speraxAgentSchema_v1.json
   ├── Validate structure
   └── Copy to public/schema/

2. Agent Collection (per language)
   ├── Scan locales/ directories
   ├── Load agent index files
   ├── Validate against schema
   └── Aggregate metadata

3. Tag Aggregation
   ├── Collect all tags from agents
   ├── Count tag occurrences
   ├── Sort by popularity
   └── Generate tag list

4. Index Generation (per language)
   ├── Create agent list
   ├── Add tag statistics
   ├── Add metadata (count, schema version)
   └── Write to public/index.{locale}.json

5. Verification
   ├── Validate JSON output
   ├── Check file sizes
   ├── Verify agent count
   └── Report statistics
```

### Build Output Structure

**Main Index File (public/index.json):**

```json
{
  "agents": [
    {
      "author": "SperaxOS",
      "createdAt": "2024-12-17",
      "homepage": "https://github.com/speraxos/SperaxOS-AI-Agents",
      "identifier": "yield-dashboard-builder",
      "meta": {
        "avatar": "📊",
        "description": "Build comprehensive DeFi yield tracking dashboards",
        "tags": ["yield", "dashboard", "defi", "analytics"],
        "title": "Yield Dashboard Builder"
      },
      "schemaVersion": 1
    }
    // ... 40 more agents
  ],
  "tags": [
    "defi",
    "yield", 
    "security",
    "risk",
    "staking",
    "tokens",
    "analytics",
    "governance",
    "nft",
    "bridge"
  ],
  "schemaVersion": 1
}
```

### Build Statistics

After each build, the system reports:

```bash
📊 统计信息:
  • Agents 数量: 41
  • 热门标签数量: 15
  • 索引文件: index.json
  • 语言版本: en-US

✓ 语言版本构建完成 en-US
```

### Build Performance

| Metric | Value |
|--------|-------|
| **Build Time** | ~2-3 seconds |
| **Total Files Generated** | 19 (1 schema + 18 indexes) |
| **Total File Size** | ~500KB (all indexes) |
| **Average Index Size** | ~25KB per language |
| **Agents per Index** | 41 |

---

## Deployment Pipeline

### GitHub Actions Workflow

**File:** `.github/workflows/deploy.yml`

```yaml
name: Deploy SperaxOS Agent Index

on:
  push:
    branches:
      - main
  workflow_dispatch:

permissions:
  contents: read
  pages: write
  id-token: write

concurrency:
  group: "pages"
  cancel-in-progress: false

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout
        uses: actions/checkout@v4

      - name: Setup Bun
        uses: oven-sh/setup-bun@v1
        with:
          bun-version: latest

      - name: Install dependencies
        run: bun install

      - name: Build agent index
        run: bun run build
        env:
          NODE_ENV: production

      - name: Setup Pages
        uses: actions/configure-pages@v4

      - name: Upload artifact
        uses: actions/upload-pages-artifact@v3
        with:
          path: './public'

  deploy:
    environment:
      name: github-pages
      url: ${{ steps.deployment.outputs.page_url }}
    runs-on: ubuntu-latest
    needs: build
    steps:
      - name: Deploy to GitHub Pages
        id: deployment
        uses: actions/deploy-pages@v4
```

### Deployment Process

```
1. Developer pushes to main branch
   ↓
2. GitHub Actions triggered
   ↓
3. Checkout repository
   ↓
4. Setup Bun runtime
   ↓
5. Install dependencies (bun install)
   ↓
6. Run build script (bun run build)
   ↓
7. Generate public/ directory
   ↓
8. Upload as Pages artifact
   ↓
9. Deploy to gh-pages branch
   ↓
10. Available at github.com/speraxos/SperaxOS-AI-Agents
```

### Production URLs

| Resource | URL |
|----------|-----|
| **Main Index** | `https://github.com/speraxos/SperaxOS-AI-Agents/index.json` |
| **Chinese Index** | `https://github.com/speraxos/SperaxOS-AI-Agents/index.zh-CN.json` |
| **Japanese Index** | `https://github.com/speraxos/SperaxOS-AI-Agents/index.ja-JP.json` |
| **Schema** | `https://github.com/speraxos/SperaxOS-AI-Agents/schema/speraxAgentSchema_v1.json` |

### Deployment Verification

```bash
# Verify deployment
curl https://github.com/speraxos/SperaxOS-AI-Agents/index.json | jq '.agents | length'
# Expected output: 41

# Check schema
curl https://github.com/speraxos/SperaxOS-AI-Agents/schema/speraxAgentSchema_v1.json | jq '.schemaVersion'
# Expected output: 1

# Verify language
curl https://github.com/speraxos/SperaxOS-AI-Agents/index.zh-CN.json | jq '.agents[0].meta.title'
# Expected output: Chinese characters
```

---

## Agent Development Guide

### Creating a New Agent

**Step 1: Create Source File**

Create `src/my-new-agent.json`:

```json
{
  "author": "SperaxOS",
  "config": {
    "systemRole": "# DeFi Strategy Advisor\n\nYou are an expert DeFi strategy advisor specializing in yield optimization and risk management.\n\n## Expertise\n\n- Portfolio allocation strategies\n- Multi-chain yield farming\n- Risk-adjusted returns\n- Impermanent loss mitigation\n\n## Guidelines\n\n- Provide data-driven recommendations\n- Consider user risk tolerance\n- Explain trade-offs clearly\n- Stay updated on protocol changes"
  },
  "createdAt": "2024-12-17",
  "homepage": "https://github.com/speraxos/SperaxOS-AI-Agents",
  "identifier": "defi-strategy-advisor",
  "meta": {
    "avatar": "🎯",
    "description": "Get personalized DeFi strategy recommendations based on your goals and risk tolerance",
    "tags": ["strategy", "yield", "risk", "portfolio"],
    "title": "DeFi Strategy Advisor"
  },
  "schemaVersion": 1
}
```

**Step 2: Validate Schema**

```bash
# Install dependencies
bun install

# Validate your agent
bun run validate src/my-new-agent.json
```

**Step 3: Translate**

```bash
# Translate to all languages
bun run format

# This creates:
# - locales/defi-strategy-advisor/index.json
# - locales/defi-strategy-advisor/index.ar.json
# - locales/defi-strategy-advisor/index.zh-CN.json
# - ... (18 total)
```

**Step 4: Build**

```bash
# Build agent index
bun run build

# Verify in output
cat public/index.json | jq '.agents | map(select(.identifier == "defi-strategy-advisor"))'
```

**Step 5: Test Locally**

```bash
# Serve locally
bunx serve public

# Open browser to:
# http://localhost:3000/index.json
```

**Step 6: Deploy**

```bash
# Commit and push
git add .
git commit -m "Add DeFi Strategy Advisor agent"
git push origin main

# GitHub Actions will automatically deploy
```

### Agent Best Practices

#### 1. System Role Design

**Good System Role:**
```markdown
# Yield Optimizer

You are a DeFi yield optimization expert with deep knowledge of lending protocols, liquidity pools, and yield aggregators.

## Core Capabilities

- Analyze yield opportunities across multiple chains
- Calculate risk-adjusted returns (APY vs. APR)
- Evaluate smart contract risks
- Monitor gas costs and ROI

## Interaction Style

- Ask clarifying questions about user's risk tolerance
- Provide step-by-step optimization strategies
- Explain technical concepts in simple terms
- Include relevant protocol links and documentation

## Important Considerations

- Always mention smart contract risks
- Consider gas costs in recommendations
- Stay updated on protocol changes
- Never guarantee returns
```

**Poor System Role:**
```
You help with DeFi stuff.
```

#### 2. Naming Conventions

| Do ✅ | Don't ❌ |
|------|----------|
| `yield-dashboard-builder` | `YieldDashboard` |
| `spa-tokenomics-analyst` | `spa_tokenomics` |
| `bridge-security-analyst` | `bridgeSecurityAnalyst` |

#### 3. Tag Selection

**Effective Tags:**
- Primary function: `yield`, `security`, `risk`
- Protocol type: `defi`, `nft`, `governance`
- Action type: `analytics`, `monitoring`, `optimization`
- Asset type: `tokens`, `staking`, `liquidity`

**Avoid:**
- Overly generic: `crypto`, `blockchain`
- Too specific: `aave-v3-optimizer`
- Redundant: `defi-finance`, `token-tokens`

#### 4. Description Guidelines

**Good:**
```
"Analyze Sperax USD stablecoin mechanics, collateralization ratios, and peg stability mechanisms"
```

**Poor:**
```
"A tool for USDs"
```

**Formula:**
- Start with action verb
- Mention specific capabilities
- Keep under 120 characters
- Be precise and informative

### Testing Checklist

Before submitting a new agent:

- [ ] Schema validation passes
- [ ] Identifier is unique and follows kebab-case
- [ ] System role is comprehensive (200+ characters)
- [ ] Description is clear and concise
- [ ] Tags are relevant (2-7 tags)
- [ ] Avatar emoji is appropriate
- [ ] Translation completes successfully
- [ ] Agent appears in build output
- [ ] Local testing shows agent correctly
- [ ] No console errors or warnings

---

## Quality Assurance

### Automated Validation

**Schema Validation:**
```bash
# Validate all source agents
bun run validate

# Validate specific agent
bun run validate src/yield-dashboard-builder.json

# Validate translation output
bun run validate locales/yield-dashboard-builder/index.zh-CN.json
```

**Build Verification:**
```bash
# Check agent count
cat public/index.json | jq '.agents | length'

# Verify schema version
cat public/index.json | jq '.schemaVersion'

# List all agent identifiers
cat public/index.json | jq -r '.agents[].identifier' | sort

# Check for duplicates
cat public/index.json | jq -r '.agents[].identifier' | sort | uniq -d
```

### Manual Testing

**Visual Inspection:**
1. Open `public/index.json` in browser
2. Verify JSON is well-formatted
3. Check agent metadata is complete
4. Confirm tag list is accurate

**Cross-Language Verification:**
```bash
# Compare agent counts across languages
for lang in en-US zh-CN ja-JP ko-KR; do
  count=$(cat public/index.$lang.json | jq '.agents | length')
  echo "$lang: $count agents"
done

# Should show similar counts (may vary slightly due to partial translations)
```

### Common Issues & Solutions

| Issue | Cause | Solution |
|-------|-------|----------|
| Agent missing from index | Translation incomplete | Run `bun run format` again |
| Schema validation fails | Invalid JSON | Check JSON syntax with linter |
| Duplicate identifier | Name conflict | Choose unique identifier |
| Build fails | Missing required field | Add all required schema fields |
| Translation error | Rate limit hit | Wait and retry with `bun run format` |
| Wrong language detected | Translation quality | Retry translation or edit manually |

---

## API Reference

### REST API Endpoints

**Base URL:** `https://github.com/speraxos/SperaxOS-AI-Agents`

#### Get All Agents (English)

```http
GET /index.json
```

**Response:**
```json
{
  "agents": [
    {
      "author": "SperaxOS",
      "createdAt": "2024-12-17",
      "homepage": "https://github.com/speraxos/SperaxOS-AI-Agents",
      "identifier": "yield-dashboard-builder",
      "meta": {
        "avatar": "📊",
        "description": "Build comprehensive DeFi yield tracking dashboards",
        "tags": ["yield", "dashboard", "defi"],
        "title": "Yield Dashboard Builder"
      },
      "schemaVersion": 1
    }
  ],
  "tags": ["defi", "yield", "security"],
  "schemaVersion": 1
}
```

#### Get Agents by Language

```http
GET /index.{locale}.json
```

**Parameters:**
- `{locale}`: Language code (e.g., `zh-CN`, `ja-JP`, `ko-KR`)

**Example:**
```http
GET /index.zh-CN.json
```

#### Get Agent Details

```http
GET /locales/{agent}/index.json
```

**Example:**
```http
GET /locales/yield-dashboard-builder/index.json
```

**Response includes full `systemRole`**

#### Get Localized Agent Details

```http
GET /locales/{agent}/index.{locale}.json
```

**Example:**
```http
GET /locales/yield-dashboard-builder/index.zh-CN.json
```

#### Get Schema

```http
GET /schema/speraxAgentSchema_v1.json
```

### JavaScript SDK Usage

```javascript
// Fetch agent index
const response = await fetch('https://github.com/speraxos/SperaxOS-AI-Agents/index.json');
const data = await response.json();

console.log(`Found ${data.agents.length} agents`);
console.log(`Available tags:`, data.tags);

// Get specific agent
const yieldAgent = data.agents.find(a => a.identifier === 'yield-dashboard-builder');
console.log(yieldAgent.meta.title); // "Yield Dashboard Builder"

// Fetch full agent details with system role
const detailResponse = await fetch(
  'https://github.com/speraxos/SperaxOS-AI-Agents/locales/yield-dashboard-builder/index.json'
);
const agentDetails = await detailResponse.json();
console.log(agentDetails.config.systemRole); // Full system prompt

// Fetch Chinese version
const zhResponse = await fetch(
  'https://github.com/speraxos/SperaxOS-AI-Agents/index.zh-CN.json'
);
const zhData = await zhResponse.json();
console.log(zhData.agents[0].meta.title); // Chinese title
```

### TypeScript Types

```typescript
interface SperaxAgent {
  author: string;
  createdAt: string;
  homepage: string;
  identifier: string;
  meta: {
    avatar: string;
    description: string;
    tags: string[];
    title: string;
    category?: string;
  };
  schemaVersion: 1;
}

interface SperaxAgentIndex {
  agents: SperaxAgent[];
  tags: string[];
  schemaVersion: 1;
}

interface SperaxAgentDetails extends SperaxAgent {
  config: {
    systemRole: string;
    model?: string;
    temperature?: number;
  };
}
```

### React Hook Example

```typescript
import { useState, useEffect } from 'react';

interface UseSperaxAgentsOptions {
  locale?: string;
}

export function useSperaxAgents(options: UseSperaxAgentsOptions = {}) {
  const { locale = 'en-US' } = options;
  const [agents, setAgents] = useState<SperaxAgent[]>([]);
  const [tags, setTags] = useState<string[]>([]);
  const [loading, setLoading] = useState(true);
  const [error, setError] = useState<Error | null>(null);

  useEffect(() => {
    const fetchAgents = async () => {
      try {
        setLoading(true);
        const suffix = locale === 'en-US' ? '' : `.${locale}`;
        const response = await fetch(
          `https://github.com/speraxos/SperaxOS-AI-Agents/index${suffix}.json`
        );
        
        if (!response.ok) {
          throw new Error(`HTTP ${response.status}`);
        }
        
        const data: SperaxAgentIndex = await response.json();
        setAgents(data.agents);
        setTags(data.tags);
      } catch (err) {
        setError(err as Error);
      } finally {
        setLoading(false);
      }
    };

    fetchAgents();
  }, [locale]);

  return { agents, tags, loading, error };
}

// Usage
function AgentMarketplace() {
  const { agents, tags, loading } = useSperaxAgents({ locale: 'zh-CN' });

  if (loading) return <div>Loading agents...</div>;

  return (
    <div>
      <h1>DeFi Agents ({agents.length})</h1>
      <div className="tags">
        {tags.map(tag => <span key={tag}>{tag}</span>)}
      </div>
      <div className="agents">
        {agents.map(agent => (
          <AgentCard key={agent.identifier} agent={agent} />
        ))}
      </div>
    </div>
  );
}
```

---

## Appendix

### Complete Agent List (41 Total)

1. airdrop-hunter
2. alpha-leak-detector
3. apy-vs-apr-educator
4. bridge-security-analyst
5. crypto-tax-strategist
6. defi-insurance-advisor
7. defi-onboarding-mentor
8. defi-risk-scoring-engine
9. dex-aggregator-optimizer
10. gas-optimization-expert
11. governance-proposal-analyst
12. impermanent-loss-calculator
13. layer2-comparison-guide
14. liquidation-risk-manager
15. liquidity-pool-analyzer
16. mev-protection-advisor
17. narrative-trend-analyst
18. nft-liquidity-advisor
19. portfolio-rebalancing-advisor
20. protocol-revenue-analyst
21. protocol-treasury-analyst
22. smart-contract-auditor
23. spa-tokenomics-analyst
24. sperax-bridge-assistant
25. sperax-governance-guide
26. sperax-liquidity-strategist
27. sperax-onboarding-guide
28. sperax-risk-monitor
29. sperax-yield-aggregator
30. stablecoin-comparator
31. staking-rewards-calculator
32. token-unlock-tracker
33. usds-stablecoin-expert
34. vespa-optimizer
35. wallet-security-advisor
36. whale-watcher
37. yield-dashboard-builder

### Tag Taxonomy

**Primary Categories:**
- `defi` - General DeFi functionality
- `yield` - Yield optimization and farming
- `security` - Security analysis and auditing
- `risk` - Risk assessment and management
- `staking` - Staking and delegation
- `governance` - Protocol governance
- `tokens` - Token economics and analysis
- `nft` - NFT-related functionality
- `bridge` - Cross-chain bridging
- `analytics` - Data analysis and reporting

**Action Types:**
- `monitoring` - Continuous tracking
- `optimization` - Performance improvement
- `education` - Learning and guidance
- `analysis` - Data examination
- `calculation` - Computational tools

### Deployment Checklist

**Pre-Deployment:**
- [ ] All agents have complete schemas
- [ ] Translation is 100% complete (41 agents × 18 languages)
- [ ] Build output validates successfully
- [ ] No duplicate identifiers
- [ ] All required fields present
- [ ] Schema version is correct (1)

**Deployment:**
- [ ] Push to main branch
- [ ] GitHub Actions workflow succeeds
- [ ] Public directory is deployed to gh-pages
- [ ] Production URLs are accessible
- [ ] Agent count is correct (41)
- [ ] All language versions load

**Post-Deployment:**
- [ ] Verify main index: `curl .../index.json`
- [ ] Test language switching
- [ ] Check mobile responsiveness
- [ ] Monitor error rates
- [ ] Collect user feedback

### Resources


---

## Document Version

- **Version:** 1.0
- **Last Updated:** December 17, 2024
- **Schema Version:** 1
- **Total Agents:** 41
- **Supported Languages:** 18

---

**© 2024 SperaxOS. All rights reserved.**
