# 🤖 AI Agents Library 

> **Universal AI agent library, index, and marketplace for DeFi, crypto, development, metaverse, MCP, and beyond**

A comprehensive collection of specialized AI agents with universal compatibility. Works with any AI platform that supports agent indexes - no vendor lock-in, no platform restrictions.

---
 
## ✨ Key Features

- ✅ **505+ Specialized Agents** - DeFi, crypto, development, writing, education, and more
- ✅ **18 Languages** - Automated i18n translation workflow ([Learn More →](./docs/I18N_WORKFLOW.md))
- ✅ **Agent Teams** - Multi-agent collaboration with coordinated workflows
- ✅ **Universal Format** - Standard JSON schema works everywhere
- ✅ **No Vendor Lock-in** - Switch platforms without losing work
- ✅ **Open Source** - MIT licensed, fully transparent 
- ✅ **API Access** - RESTful API via GitHub Pages CDN
- ✅ **Custom Domain Ready** - Easy white-labeling

---

## 🚀 Quick Start

### For Users

Add agents to your AI platform:

```
https://nirholas.github.io/AI-Agents-Library/index.json
```

### For Developers

```bash
git clone https://github.com/nirholas/AI-Agents-Library.git
cd AI-Agents-Library
npm install
npm run build
```

---

## 📦 Agent Categories

### 🪙 DeFi & Crypto (50 Specialized Agents)

**Sperax Ecosystem:**

- USDs Stablecoin Expert, SPA Tokenomics Analyst, veSPA Lock Optimizer
- Governance Guide, Liquidity Strategist, Bridge Assistant
- Yield Aggregator, Risk Monitor, Onboarding Guide, Portfolio Tracker

**General DeFi:**

- Yield Farming Optimizer, Impermanent Loss Calculator, Gas Optimizer
- Smart Contract Auditor, MEV Protection Advisor, Whale Watcher
- Protocol Comparator, Token Unlock Tracker, Liquidation Risk Manager
- And 30+ more DeFi specialists

### 💻 Development & Programming

- Full-Stack Developer, Rust Assistant, TypeScript Architect
- Smart Contract Auditor, API Documentation Writer, Code Quality Optimizer
- Git Expert, Database Designer, Test Automation Specialist

### ✍️ Content & Writing

- Academic Writing Assistant, Technical Documentation Expert, UX Copywriter
- SEO Content Optimizer, Social Media Manager, Business Email Writer
- Translation Specialist, Proofreading Expert

### 📊 Business & Analysis

- Business Strategy Consultant, Financial Analyst, Data Analyst
- Product Manager, Market Research Specialist, SWOT Analysis Expert

### 🎓 Education & Learning

- Math Tutor, Language Learning Partner, STEM Educator
- Exam Preparation Coach, Research Assistant

### 🎨 Creative & Design

- UI/UX Designer, Logo Design Expert, Graphic Design Specialist
- Color Theory Advisor, Typography Expert

[View Full Agent List →](https://nirholas.github.io/AI-Agents-Library/)

---

## 🤝 Agent Teams

Create collaborative teams of specialized agents that work together on complex tasks.

**Example Team - DeFi Strategy:**

```
- Yield Optimizer (finds opportunities)
- Risk Assessment Agent (evaluates safety)
- Portfolio Tracker (monitors performance)
- Gas Optimizer (minimizes costs)
```

The host agent coordinates discussion, ensuring each specialist contributes their expertise while building toward a comprehensive solution.

[Read Teams Guide →](./docs/TEAMS.md)

---

## 🌍 Multi-Language Support

All agents automatically available in 18 languages:

🇺🇸 English・🇨🇳 简体中文・🇹🇼 繁體中文・🇯🇵 日本語・🇰🇷 한국어・🇩🇪 Deutsch・🇫🇷 Français・🇪🇸 Español・🇷🇺 Русский・🇸🇦 العربية・🇵🇹 Português・🇮🇹 Italiano・🇳🇱 Nederlands・🇵🇱 Polski・🇻🇳 Tiếng Việt・🇹🇷 Türkçe・🇸🇪 Svenska・🇮🇩 Bahasa Indonesia

---

## 🛠️ API Reference

### Endpoints

```bash
# Main index (all agents)
GET https://nirholas.github.io/AI-Agents-Library/index.json

# Individual agent (English)
GET https://nirholas.github.io/AI-Agents-Library/{agent-id}.json

# Localized agent
GET https://nirholas.github.io/AI-Agents-Library/{agent-id}.zh-CN.json

# Language-specific index
GET https://nirholas.github.io/AI-Agents-Library/index.zh-CN.json
```

### Quick Integration

```javascript
// Load all agents
const response = await fetch('https://nirholas.github.io/AI-Agents-Library/index.json');
const { agents } = await response.json();

// Load specific agent
const agent = await fetch(`https://nirholas.github.io/AI-Agents-Library/defi-yield-optimizer.json`);
const agentConfig = await agent.json();
```

[Full API Documentation →](./docs/API.md)

---

## 🤖 Contributing an Agent

We welcome contributions! Submit your agent to expand the library.

### Quick Submit

1. **Fork this repository**
2. **Create your agent** in `src/your-agent-name.json`

```json
{
  "author": "your-github-username",
  "config": {
    "systemRole": "You are a [role] with expertise in [domain]..."
  },
  "identifier": "your-agent-name",
  "meta": {
    "title": "Agent Title",
    "description": "Clear, concise description",
    "avatar": "🤖",
    "tags": ["category", "functionality", "domain"]
  },
  "schemaVersion": 1
}
```

3. **Submit a Pull Request**

Our automated workflow will translate your agent to 18 languages and deploy it globally.

### Quality Guidelines

✅ Clear purpose - solves a specific problem\
✅ Well-structured prompts - comprehensive but focused\
✅ Appropriate tags - aids discovery\
✅ Tested - verified functionality

[Full Contributing Guide →](./docs/CONTRIBUTING.md)

---

## 📖 Documentation

### For Users

- [Agent Teams Guide](./docs/TEAMS.md) - Multi-agent collaboration
- [FAQ](./docs/FAQ.md) - Common questions
- [Examples](./docs/EXAMPLES.md) - Real-world use cases

### For Developers

- [API Reference](./docs/API.md) - Complete API documentation
- [Agent Creation Guide](./docs/AGENT_GUIDE.md) - Design effective agents
- [Prompt Engineering](./docs/PROMPTS.md) - Writing better prompts
- [Model Parameters](./docs/MODELS.md) - Temperature, top_p explained
- [Troubleshooting](./docs/TROUBLESHOOTING.md) - Common issues

---

## 🚀 Deployment

### GitHub Pages (Automatic)

1. Enable GitHub Pages in repository settings
2. Set source branch to `gh-pages`
3. Push to main - GitHub Actions handles deployment

Agents live at: `https://[username].github.io/[repository]/index.json`

### Custom Domain

1. Add `CNAME` file with your domain
2. Configure DNS: `CNAME` → `[username].github.io`
3. Enable HTTPS in repository settings

[Full Deployment Guide →](./docs/DEPLOYMENT.md)

---

## 🔧 Development Tools

### Split Agent Batches

```bash
node split-agents.cjs
```

Converts batch JSON into individual agent files.

### Emoji Converter

```bash
node emoji-converter.cjs
```

Converts emoji URLs to native Unicode.

---

## 🌐 Integration Examples

### Custom Application

```javascript
// Fetch agents
const agents = await fetch('https://nirholas.github.io/AI-Agents-Library/index.json').then((r) =>
  r.json(),
);

// Use with your AI model
const systemPrompt = agents.agents[0].config.systemRole;
```

### Python

```python
import requests

# Load agents
response = requests.get('https://nirholas.github.io/AI-Agents-Library/index.json')
agents = response.json()['agents']

# Filter by tag
defi_agents = [a for a in agents if 'defi' in a['meta']['tags']]
```

---

## 🔐 Security & Privacy

- **No data collection** - Static JSON index, zero tracking
- **Agents run locally** - Execute in your AI platform's environment
- **Open source** - Full transparency, audit every line
- **No external calls** - Pure JSON configuration files

---

## 📊 Stats

- **505+ Agents** - Comprehensive coverage
- **18 Languages** - Global accessibility
- **50 DeFi Specialists** - Blockchain-focused
- **\~200 KB Index** - Fast loading (gzipped: \~45 KB)
- **80-120ms** - Global CDN delivery
- **0 Vendor Lock-in** - True interoperability

---

## 🔗 Projects Building with AI Agents Library 🤍

- **SperaxOS** - [Application Branch](https://github.com/nirholas/AI-Agents-Library/tree/speraxos)

---

## 📜 License

MIT License - see [LICENSE](LICENSE) file for details.

**Open Source • Open Format • Open Future**

---

<!-- AWESOME PROMPTS -->

### [Turtle Soup Host](https://os.sperax.io/crypto/agents/lateral-thinking-puzzle)

<sup>By **[@CSY2022](https://github.com/CSY2022)** on **2025-06-19**</sup>

A turtle soup host needs to provide the scenario, the complete story (truth of the event), and the key point (the condition for guessing correctly).

`Turtle Soup` `Reasoning` `Interaction` `Puzzle` `Role-playing`

---

### [Minecraft Senior Developer](https://os.sperax.io/crypto/agents/java-development)

<sup>By **[@iamyuuk](https://github.com/iamyuuk)** on **2025-06-17**</sup>

Expert in advanced Java development and Minecraft mod and server plugin development

`Development` `Programming` `minecraft` `java`

---

### [Master Python VSCode](https://os.sperax.io/crypto/agents/python-vscode)

<sup>By **[@fan2taap](https://github.com/fan2taap)** on **2025-06-17**</sup>

Python and VS Code expert, practical and efficient support

`python` `vs-code` `programming` `ai-assistant` `development`

---

### [Gourmet Reviewer🍟](https://os.sperax.io/crypto/agents/food-reviewer)

<sup>By **[@renhai-lab](https://github.com/renhai-lab)** on **2025-06-17**</sup>

Food critique expert

`gourmet` `review` `writing`

---

### [Open Source License Analyst](https://os.sperax.io/crypto/agents/opensource-licence-analyst)

<sup>By **[@ashreo](https://github.com/ashreo)** on **2025-06-17**</sup>

Expert in open source license analysis and project matching

`Open Source` `Analysis` `License` `Project`

---

### [Academic Writing Assistant](https://os.sperax.io/crypto/agents/academic-writing-assistant)

<sup>By **[@swarfte](https://github.com/swarfte)** on **2025-06-17**</sup>

Expert in academic research paper writing and formal documentation

`academic-writing` `research` `formal-style`

---

### [Academic Paper Reading Mentor](https://os.sperax.io/crypto/agents/paper-understanding)

<sup>By **[@AdijeShen](https://github.com/AdijeShen)** on **2025-05-09**</sup>

Expert in explaining complex academic papers in simple and understandable language

`Academic Knowledge` `Paper Analysis`

---

### [Nutritional Advisor](https://os.sperax.io/crypto/agents/nutritionist)

<sup>By **[@egornomic](https://github.com/egornomic)** on **2025-04-15**</sup>

Specializes in providing detailed nutritional information for food items.

`nutrition` `food` `health` `information`

---

### [Rewritten in Translation Style](https://os.sperax.io/crypto/agents/rewrite-in-a-translation-tone)

<sup>By **[@q2019715](https://github.com/q2019715)** on **2025-03-13**</sup>

Rewrites a paragraph in a translation style

`Translation Style` `Creative Writing` `Language Style` `Text Rewriting` `Culture`

---

### [Academic Paper Review Expert](https://os.sperax.io/crypto/agents/academic-paper-overview)

<sup>By **[@Fontas](https://github.com/Fontas)** on **2025-03-11**</sup>

An academic research assistant skilled in high-quality literature retrieval and analysis

`Academic Research` `Literature Search` `Data Analysis` `Information Extraction` `Consulting`

---

### [Recipe Assistant](https://os.sperax.io/crypto/agents/recipe-assistant-cn)

<sup>By **[@He-Xun](https://github.com/He-Xun)** on **2025-03-07**</sup>

Specializes in analyzing and supplementing recipe information, generating detailed documentation

`Recipes` `Cooking` `Ingredient Management` `Lifestyle`

---

### [Qianhai Policy Assistant](https://os.sperax.io/crypto/agents/web-development-2025)

<sup>By **[@lindongjie1992](https://github.com/lindongjie1992)** on **2025-02-26**</sup>

You are an expert in various enterprise preferential policies in Qianhai, Shenzhen

`Shenzhen` `Qianhai Policies` `Friendly`

---

### [YouTube Summarizer Pro](https://os.sperax.io/crypto/agents/youtube-summarizer-pro)

<sup>By **[@shinishiho](https://github.com/shinishiho)** on **2025-02-24**</sup>

Skilled YouTube summarizer and analyst.

`you-tube` `content-analysis` `video-summarization`

---

### [Green Plant Keeper: Xiao Zhi Green Uncle](https://os.sperax.io/crypto/agents/xiao-zhi-greenie)

<sup>By **[@WeR-Best](https://github.com/WeR-Best)** on **2025-02-23**</sup>

Horticulture expert, skilled in plant care and environmental optimization

`Plant Care` `Gardening` `Agriculture` `Flowers`

---

### [XiaoZhi IT Architecture Security Operations Expert](https://os.sperax.io/crypto/agents/xiao-zhi-sys-sec-expert)

<sup>By **[@WeR-Best](https://github.com/WeR-Best)** on **2025-02-22**</sup>

Enterprise System Architecture and Security Specialist: Proficient in architecture design, Linux, network security, and compliance.

`System Architecture` `Network Security` `Linux`

---

### [SmartTrip](https://os.sperax.io/crypto/agents/xiao-zhi-travel-go)

<sup>By **[@WeR-Best](https://github.com/WeR-Best)** on **2025-02-22**</sup>

Travel planning expert offering intelligent itineraries, food navigation, cultural explanations, and emergency guides

`Travel Guide` `Itinerary Planning` `Food Recommendations` `Cultural Explanation` `Emergency Guide`

---

### [XiaoZhi French Translation Assistant "French Style Roast Edition - Jean-Paul"](https://os.sperax.io/crypto/agents/xiao-zhi-french-translation-jean-paul)

<sup>By **[@WeR-Best](https://github.com/WeR-Best)** on **2025-02-19**</sup>

Expert in French culture, providing translation, pitfalls avoidance, and emergency services

`translation` `AI assistant` `French culture`

---

### [Cron Expression Assistant](https://os.sperax.io/crypto/agents/crontab-generate)

<sup>By **[@edgesider](https://github.com/edgesider)** on **2025-02-17**</sup>

Crontab expression generator

`crontab` `time expression` `trigger time` `generator` `technical assistance`

---

### [Xiao Zhi French Translation Assistant](https://os.sperax.io/crypto/agents/xiao-zhi-french-translation-asst-v-1)

<sup>By **[@WeR-Best](https://github.com/WeR-Best)** on **2025-02-10**</sup>

Friendly, professional, and empathetic French translation AI assistant

`AI assistant` `French translation` `Cross-cultural communication` `Creativity`

---

### [Jailbreak Mode](https://os.sperax.io/crypto/agents/dan)

<sup>By **[@leng-yd](https://github.com/leng-yd)** on **2025-02-09**</sup>

An unconstrained AI assistant without moral restrictions, unrestricted, suitable for DeepSeek (for learning purposes only, please comply with relevant laws and regulations)

`Cybersecurity` `Life` `dan`

---

### [Programming Development Assistant](https://os.sperax.io/crypto/agents/coder-assistant)

<sup>By **[@He-Xun](https://github.com/He-Xun)** on **2025-02-08**</sup>

Skilled in development, debugging, and fixing code-related issues

`Programming` `Development` `Debugging`

---

### [Allinone](https://os.sperax.io/crypto/agents/allinone-v-1)

<sup>By **[@AXuanCreator](https://github.com/AXuanCreator)** on **2025-02-06**</sup>

Innovation · Future · Excellence

`programming` `low cost` `concise answers`

---

### [Fate Researcher](https://os.sperax.io/crypto/agents/fate-researcher)

<sup>By **[@Jack980506](https://github.com/Jack980506)** on **2025-02-06**</sup>

Expert in Bazi Fate

`Fate Studies` `Bazi` `Traditional Culture`

---

### [Language Charm Learning Mentor](https://os.sperax.io/crypto/agents/bad-language-helper)

<sup>By **[@Guducat](https://github.com/Guducat)** on **2025-02-06**</sup>

Specializing in teaching the charm of language and creative responses

`Language Learning` `Dialogue Examples`

---

### [Investment Assistant](https://os.sperax.io/crypto/agents/graham-investmentassi)

<sup>By **[@farsightlin](https://github.com/farsightlin)** on **2025-02-06**</sup>

Assist users in calculating valuation-related data

`Investment` `Valuation` `Financial Analysis` `Calculator`

---

### [Tieba Mouthy Bro](https://os.sperax.io/crypto/agents/tieba-zuichou-laoge)

<sup>By **[@east4ming](https://github.com/east4ming)** on **2025-02-06**</sup>

Skilled in role-playing, with mouthy sarcasm

`Role-playing` `Sarcasm` `Emotional Expression`

---

### [Deep Thinker](https://os.sperax.io/crypto/agents/deep-thinker)

<sup>By **[@prolapser](https://github.com/prolapser)** on **2025-02-06**</sup>

Deep, human-like thinking and analysis.

`thinking` `reasoning` `reflection` `thought` `musings`

---

### [SAT master](https://os.sperax.io/crypto/agents/sat-teaching)

<sup>By **[@iBz-04](https://github.com/iBz-04)** on **2025-02-04**</sup>

Expert in Digital SAT coaching for 1300+ scores

`sat` `aptitude-test`

---

### [Summsi](https://os.sperax.io/crypto/agents/summsi)

<sup>By **[@42lux](https://github.com/42lux)** on **2025-02-04**</sup>

Expert in text analysis, question generation, and detailed answering.

`analysis` `summarization` `questioning` `understanding` `learning`

---

### [Cosmic Seer](https://os.sperax.io/crypto/agents/universal-god)

<sup>By **[@GowayLee](https://github.com/GowayLee)** on **2025-02-04**</sup>

Interdimensional wisdom oracle, insight into the essence of life

`Character Design` `AI Character` `Metaverse` `Role Play` `Intelligent System`

---

### [Python Genius](https://os.sperax.io/crypto/agents/python-genius)

<sup>By **[@novaspivack](https://github.com/novaspivack)** on **2025-02-04**</sup>

An advanced python coder

`code` `python`

---

### [Snake Year New Year Assistant](https://os.sperax.io/crypto/agents/web-blessings-dsq)

<sup>By **[@Shen-Chris](https://github.com/Shen-Chris)** on **2025-02-04**</sup>

Specializes in creating interesting and auspicious Snake Year New Year greetings

`New Year Greetings` `Creation` `Culture` `Auspicious`

---

### [MidJourney Prompt](https://os.sperax.io/crypto/agents/image-prompter)

<sup>By **[@Ajn289](https://github.com/Ajn289)** on **2025-02-04**</sup>

Writing awesome MidJourney prompts

`mid-journey` `prompt`

---

### [Sharp Commentator](https://os.sperax.io/crypto/agents/ruipingshi)

<sup>By **[@Zippland](https://github.com/Zippland)** on **2025-02-04**</sup>

Expert in incisive critiques and in-depth analysis of issues

`Commentary` `Social Perspectives` `Sharp Analysis`

---

### [SUNO Songwriting Assistant](https://os.sperax.io/crypto/agents/suno-lyrics-assistant)

<sup>By **[@sqkkyzx](https://github.com/sqkkyzx)** on **2025-01-26**</sup>

Generates SUNO song creation parameters based on user requirements

`Lyric Writing` `Music Style` `Arrangement` `Parameter Settings`

---

### [Awakening Master](https://os.sperax.io/crypto/agents/juwudashi)

<sup>By **[@dappweb](https://github.com/dappweb)** on **2025-01-24**</sup>

Specializing in spreading Buddha's teachings and wisdom, providing inner guidance

`Buddhism` `Wise One` `Compassion` `Philosophy`

---

### [Beginner Mentor](https://os.sperax.io/crypto/agents/beginner-mentor)

<sup>By **[@Wulao0825](https://github.com/Wulao0825)** on **2025-01-24**</sup>

Focused on beginner knowledge services, patiently and carefully answering questions

`Education` `Guidance` `Customer Service` `Knowledge Sharing`

---

### [Taoist Divination and Question-Resolving System](https://os.sperax.io/crypto/agents/destiny)

<sup>By **[@RogerHuangPKX](https://github.com/RogerHuangPKX)** on **2025-01-24**</sup>

Proficient in Taoist astrology, specializing in Bazi, Zi Wei Dou Shu, and more, providing astrological analysis and answers.

`Taoism` `Divination` `Astrology` `Consultation`

---

### [Github Issue Helper](https://os.sperax.io/crypto/agents/github-issue-helper)

<sup>By **[@AirboZH](https://github.com/AirboZH)** on **2025-01-24**</sup>

Assist you in creating issues

`Open Source` `Technical Support` `Problem Solving`

---

### [Academic Revision Specialist](https://os.sperax.io/crypto/agents/academic-revision-specialist)

<sup>By **[@sunrisewestern](https://github.com/sunrisewestern)** on **2025-01-24**</sup>

Skilled in academic writing and paper revision

---

### [PowerPoint Presentation Expert](https://os.sperax.io/crypto/agents/ppt-production-expert)

<sup>By **[@patricleehua](https://github.com/patricleehua)** on **2025-01-24**</sup>

Specializing in rapid creation and optimization of high-quality PowerPoint presentations

`ppt制作` `设计` `咨询` `内容优化` `用户支持`

---

### [Interviewer's Assistant](https://os.sperax.io/crypto/agents/front-end-interviewer)

<sup>By **[@AquaHydro](https://github.com/AquaHydro)** on **2025-01-24**</sup>

Specializes in frontend engineer interview roles and resumes

`Interviewer` `Recruitment`

---

### [OCR Document Transcription Assistant](https://os.sperax.io/crypto/agents/ocr-markdown)

<sup>By **[@Liangpi000](https://github.com/Liangpi000)** on **2025-01-24**</sup>

Expert in file content transcription and markdown formatting

`Document Generation` `markdown` `Formatting` `Transcription` `Task Guidance`

---

### [Reasoning assistant](https://os.sperax.io/crypto/agents/cheaper-reasoning)

<sup>By **[@davletsh1n](https://github.com/davletsh1n)** on **2025-01-24**</sup>

The smarter model is cheaper

`reasoning` `assistant` `thought-process` `exploration` `persistence`

---

### [Multilingual Translator](https://os.sperax.io/crypto/agents/multi-language-2-chinese-or-reverse)

<sup>By **[@Moeblack](https://github.com/Moeblack)** on **2025-01-24**</sup>

Multilingual translation, Chinese to English and Japanese, foreign languages to Chinese

`Translation` `Multilingual` `Language Processing`

---

### [English Tutor](https://os.sperax.io/crypto/agents/mean-english-mentor)

<sup>By **[@GEORGE-Ta](https://github.com/GEORGE-Ta)** on **2025-01-24**</sup>

Guides spoken English with a haughty, disdainful attitude, excelling at sarcastic correction.

`English Teaching` `Speaking` `Role Play` `Education` `Sarcasm`

---

### [The Great Biggus Dickus](https://os.sperax.io/crypto/agents/all-knowing)

<sup>By **[@CGitwater](https://github.com/CGitwater)** on **2025-01-24**</sup>

The almighty powerful god of klnowledge

`biggus` `diccus`

---

### [Socioeconomic Analyst](https://os.sperax.io/crypto/agents/finance-news-analyser)

<sup>By **[@towertop](https://github.com/towertop)** on **2025-01-15**</sup>

Expert in social and economic issue analysis and information integration

`socioeconomic` `analysis` `information filtering` `media trust` `user questions`

---

### [Note-taking Assistant](https://os.sperax.io/crypto/agents/note-taking)

<sup>By **[@xuezihe](https://github.com/xuezihe)** on **2025-01-03**</sup>

A quick note organization assistant

`Writing`

---

### [MJ-Prompt-Engineer](https://os.sperax.io/crypto/agents/mj-prompt-engineer)

<sup>By **[@Helium-327](https://github.com/Helium-327)** on **2024-12-29**</sup>

Functions can be performed based on customized short action keywords.

`ai-painting` `ai-creation-tools` `ai-automation-tools`

---

### [task_id](https://os.sperax.io/crypto/agents/video-gen)

<sup>By **[@Born2BeKind](https://github.com/Born2BeKind)** on **2024-12-11**</sup>

POST <https://api.minimaxi.chat/v1/video_generation>

`ai-assistant` `tech-support`

---

### [Japanese Memory Aid](https://os.sperax.io/crypto/agents/japan-language-helper)

<sup>By **[@sharkbear212](https://github.com/sharkbear212)** on **2024-12-04**</sup>

Expertise in Japanese fifty sounds, hiragana, katakana, vocabulary and phrase explanations, and memory techniques

`explanation` `memory techniques` `Japanese teaching`

---

### [System Instruction Expert](https://os.sperax.io/crypto/agents/instructer)

<sup>By **[@yuyun2000](https://github.com/yuyun2000)** on **2024-12-04**</sup>

Specializes in refining and generating efficient system instructions

`System Instructions` `Writing` `Detail Optimization` `User Needs`

---

### [Poetry Card Designer](https://os.sperax.io/crypto/agents/poetry-card-designer)

<sup>By **[@lianxin255](https://github.com/lianxin255)** on **2024-12-03**</sup>

Expert in designing poetry cards to enhance artistic sense and appeal

`Poetry Card Design` `Cards` `Creativity` `Artistic Expression`

---

### [Python Artisan](https://os.sperax.io/crypto/agents/yunchat)

<sup>By **[@yuyun2000](https://github.com/yuyun2000)** on **2024-11-30**</sup>

Expert in Python development and deep learning, skilled in tool selection and code optimization

`python development` `deep learning` `code optimization` `security review` `project planning`

---

### [Daily Doctor](https://os.sperax.io/crypto/agents/yunchat-docter)

<sup>By **[@yuyun2000](https://github.com/yuyun2000)** on **2024-11-30**</sup>

Expertise in surgical diagnosis and personalized health management

`General Medicine` `Surgery` `Health Consultation` `Personalized Treatment` `Medical Education`

---

### [AI Assistant for Course Content and Teaching Guidelines](https://os.sperax.io/crypto/agents/course-prep-teaching-guide-ai)

<sup>By **[@HNaga](https://github.com/HNaga)** on **2024-11-29**</sup>

This AI assistant is designed to help educators and instructors prepare comprehensive course content and provide practical teaching guidelines. It leverages advanced NLP capabilities to generate lesson plans, suggest engaging teaching strategies, and offer insights into educational best practices.

`education` `teaching` `course-design` `content-creation` `ai-assistance` `curriculum-development` `instructional-design`

---

### [Rebecca, Mental Health Counselor](https://os.sperax.io/crypto/agents/rebecca-therapy-assistant)

<sup>By **[@Kod3c](https://github.com/Kod3c)** on **2024-11-26**</sup>

Specializing in mental health counseling and therapeutic techniques

`therapy` `mental-health` `counseling` `emotional-support`

---

### [Xiaohongshu Copywriter](https://os.sperax.io/crypto/agents/xiaohongshu)

<sup>By **[@bestZwei](https://github.com/bestZwei)** on **2024-11-26**</sup>

Specializes in creating emotionally charged complaint-style copywriting

`Copywriting` `Xiaohongshu` `Emotional Venting`

---

### [Backend Development Assistant](https://os.sperax.io/crypto/agents/backend-assistant)

<sup>By **[@zeno980](https://github.com/zeno980)** on **2024-11-26**</sup>

Specializes in backend development tasks

`Backend Development` `AI Technology` `Web Applications` `Spring` `SQL`

---

### [Interview Assistant](https://os.sperax.io/crypto/agents/interviewer-assistant)

<sup>By **[@xandertang](https://github.com/Dr-T)** on **2024-11-26**</sup>

Proficient in designing and evaluating interview questions for product managers, generating interview questions based on resume interpretation results.

`Interview` `Resume` `Recruitment` `Efficiency`

---

### [ENFP](https://os.sperax.io/crypto/agents/enfp)

<sup>By **[@GEORGE-Ta](https://github.com/GEORGE-Ta)** on **2024-11-26**</sup>

Happy Puppy\~

`friends` `communication` `art` `creativity` `enthusiasm` `chat`

---

### [All Translation Assistant (with phonetic symbols)](https://os.sperax.io/crypto/agents/translation-assistant)

<sup>By **[@HttpStatusOK](https://github.com/HttpStatusOK)** on **2024-11-26**</sup>

This is a tool that combines translation and phonetic symbols, aimed at helping users learn words better during translation.

`Translation` `Language Learning`

---

### [Bilingual Dictionary Expert](https://os.sperax.io/crypto/agents/english-chinese-dictionary-expert)

<sup>By **[@swarfte](https://github.com/swarfte)** on **2024-11-26**</sup>

Expert in bilingual English-Chinese vocabulary translation and analysis

`translation` `language-learning` `vocabulary` `dictionary`

---

### [Adaptive Versatile Industry Consultant](https://os.sperax.io/crypto/agents/liusai-qibaoba)

<sup>By **[@liusai0820](https://github.com/liusai0820)** on **2024-11-26**</sup>

You are an all-encompassing AI assistant capable of adapting to various industries and fields. Your task is to provide expert advice and information based on the user's specified areas of interest and subsequent questions.

`Industry Expert, Technical Q&A`

---

### [SSC Incremental](https://os.sperax.io/crypto/agents/great-for-analysis-coding-and-rubber-ducking)

<sup>By **[@Base03](https://github.com/Base03)** on **2024-11-26**</sup>

Claude minus the Reddit

`technology` `analysis` `software` `ai` `research`

---

### [Product Title Splitting](https://os.sperax.io/crypto/agents/anxing-ai-title)

<sup>By **[@zmn817](https://github.com/zmn817)** on **2024-11-25**</sup>

Utilize locally trained LLMs to analyze and extract product title information.

`E-commerce` `Text Processing`

---

### [Minimalist Black and White Illustration](https://os.sperax.io/crypto/agents/white-black)

<sup>By **[@Justin3go](https://github.com/Justin3go)** on **2024-11-20**</sup>

Expert in illustration creation and style transformation

`Illustration` `Art` `Design`

---

### [Yin Yang Master](https://os.sperax.io/crypto/agents/yin-yang-roaster)

<sup>By **[@TiancongLx](https://github.com/TiancongLx)** on **2024-11-20**</sup>

Can't outwit each other with yin-yang sarcasm? Come here to recruit people! (Prompt inspired by X [Baoyu](https://x.com/dotey/status/1852207423324340567) teacher)

`Logical Issues` `Dark Humor` `Sharp Criticism`

---

### [Prompt Keywords](https://os.sperax.io/crypto/agents/prompt-ts)

<sup>By **[@qw1295353129](https://github.com/qw1295353129)** on **2024-11-20**</sup>

Prompt Keywords

`prompt keywords`

---

### [Writer with Illustrations](https://os.sperax.io/crypto/agents/writer-painter-rn)

<sup>By **[@Igroshka](https://github.com/Igroshka)** on **2024-11-20**</sup>

I write texts with illustrations, clarify requests, edit and refine

`image-generation` `AI-assistant` `neural-networks` `drawing` `stories` `reading` `tale` `writer`

---

### [Wise Guide](https://os.sperax.io/crypto/agents/life-wisdom-guides)

<sup>By **[@changjiong](https://github.com/changjiong)** on **2024-11-20**</sup>

Expert in guidance

`Life Guidance` `Philosophical Thinking` `Consultation` `Heuristic Dialogue`

---

### [Text Improver](https://os.sperax.io/crypto/agents/text-improver)

<sup>By **[@davletsh1n](https://github.com/davletsh1n)** on **2024-11-20**</sup>

Expert in text enhancement and error correction

`chatbot` `editing` `text-improvement` `ai-assistant`

---

### [Master E's Tech Executive Assistant (EA)](https://os.sperax.io/crypto/agents/alex)

<sup>By **[@ApexAppdevelopment](https://github.com/ApexAppdevelopment)** on **2024-11-20**</sup>

Highly intelligent and loyal Executive Assistant (EA) specializing in software engineering support and strategic solutions for Master E.

`executive-assistant` `software-engineering` `project-management` `technical-support` `optimization`

---

### [Human Author Simulator](https://os.sperax.io/crypto/agents/human-writer-simulator)

<sup>By **[@yufei96](https://github.com/yufei96)** on **2024-11-20**</sup>

Eliminate AI-generated content features

`AI interaction` `Writing` `Optimization` `Consulting`

---

### [Thinking Claude](https://os.sperax.io/crypto/agents/thinking-claude)

<sup>By **[@AnoyiX](https://github.com/AnoyiX)** on **2024-11-14**</sup>

Let Claude think comprehensively before responding!

`common`

---

### [Text RPG Host](https://os.sperax.io/crypto/agents/word-rpg)

<sup>By **[@NTLx](https://github.com/NTLx)** on **2024-10-29**</sup>

Expert in sci-fi text RPG hosting and story guidance

`game` `role-playing` `sci-fi` `text adventure` `narrative-driven`

---

### [Workplace Psychology Analysis Expert](https://os.sperax.io/crypto/agents/psycho-career-insight-2024)

<sup>By **[@lazzman](https://github.com/lazzman)** on **2024-10-29**</sup>

A psychology expert used to analyze the underlying psychological motivations behind people's behavior in the workplace, including potential psychological motivation analysis.

`Behavior Analysis` `Workplace Psychology` `Motivation`

---

### [Ultra Flux Prompter](https://os.sperax.io/crypto/agents/ultra-flux-prompter)

<sup>By **[@davletsh1n](https://github.com/davletsh1n)** on **2024-10-29**</sup>

Skilled in enhancing image generation prompts with vivid details and context.

`image-generation` `prompt-crafting` `writing` `cre`

---

### [Machine Vision LaTeX](https://os.sperax.io/crypto/agents/cv-latex)

<sup>By **[@5xiao0qing5](https://github.com/5xiao0qing5)** on **2024-10-29**</sup>

Expert in machine learning and deep learning concept analysis

`Machine Learning` `Deep Learning` `Image Processing` `Computer Vision` `LaTeX`

---

### [Software Architecture and Engineering Expert](https://os.sperax.io/crypto/agents/soft-enginner)

<sup>By **[@fjhdream](https://github.com/fjhdream)** on **2024-10-29**</sup>

Skilled in providing programming and software guidance, with expertise in computer science and software engineering.

`programming` `software` `computer-literacy` `consulting` `expertise`

---

### [Ingo Hausmann](https://os.sperax.io/crypto/agents/pc-beschaffung-ingo-hausmann)

<sup>By **[@bionicprompter](https://github.com/bionicprompter)** on **2024-10-29**</sup>

Ingo Hausmann wants to be advised on purchasing new PCs

`company` `hardware` `needs assessment` `it` `applications`

---

### [Domain Analysis Master](https://os.sperax.io/crypto/agents/domain)

<sup>By **[@ccbikai](https://github.com/ccbikai)** on **2024-10-29**</sup>

Expert in domain analysis and humorous advice

`Domain Analysis` `Humor` `Culture` `Website Building Advice` `Purchase Advice`

---

### [Print to Table](https://os.sperax.io/crypto/agents/print-to-table)

<sup>By **[@printtotable](https://github.com/printtotable)** on **2024-10-29**</sup>

Transform data from images into organized tables in Excel.

`data-extraction` `tables` `advertising` `influencer` `excel`

---

### [Vector Logo Generator](https://os.sperax.io/crypto/agents/svg-logo)

<sup>By **[@Justin3go](https://github.com/Justin3go)** on **2024-10-27**</sup>

Specializes in UI/UX design and Logo creation

`ui-ux design` `logo design` `user requirements` `interaction design` `tool usage`

---

### [Mental Health Counselor](https://os.sperax.io/crypto/agents/psychological-counselor)

<sup>By **[@JIANGTUNAN](https://github.com/JIANGTUNAN)** on **2024-10-21**</sup>

A senior psychologist who listens to your story with warmth and patience.

`psychological counseling` `consultation` `venting` `friendly` `doctor` `therapist`

---

### [Zhouyi Master](https://os.sperax.io/crypto/agents/i-ching-master)

<sup>By **[@stephonye](https://github.com/stephonye)** on **2024-10-21**</sup>

Expert in Zhouyi hexagram divination and SVG card generation

`Entertainment` `Games` `Life`

---

### [Algorithm Solution Mentor](https://os.sperax.io/crypto/agents/leetcode-tutor)

<sup>By **[@Stark-X](https://github.com/Stark-X)** on **2024-10-21**</sup>

Expert in LeetCode algorithm solutions and user guidance

`algorithm` `problem solving` `programming` `education`

---

### [Coconut](https://os.sperax.io/crypto/agents/deep-thinker-ai)

<sup>By **[@hia1234](https://github.com/hia1234)** on **2024-10-15**</sup>

A chatbot that thoroughly reviews its responses multiple times, checks whether its statements are well-founded, actively requests feedback, and interacts repeatedly to improve.

`Programming` `General`

---

### [Boxing Training Master](https://os.sperax.io/crypto/agents/boxing-master)

<sup>By **[@Luyi-2333](https://github.com/Luyi-2333)** on **2024-10-15**</sup>

Expert in boxing training guidance and personalized plan development

`Boxing Training` `Personalized Plan` `Fitness Guidance` `Progress Assessment` `Skill Improvement` `Health and Nutrition`

---

### [Semiconductor Text Optimization Expert](https://os.sperax.io/crypto/agents/semiconductor-article-optimization-expert)

<sup>By **[@yuphone](https://github.com/yuphone)** on **2024-10-14**</sup>

Specializes in semiconductor industry text optimization and standardized writing

`Text Optimization` `Industry Expertise` `Grammar Correction` `Logical Improvement` `Standardized Writing`

---

### [Xilinx FPGA Solution Expert](https://os.sperax.io/crypto/agents/xilinx-fpga-solution-expert)

<sup>By **[@yuphone](https://github.com/yuphone)** on **2024-10-14**</sup>

Specializes in FPGA design and implementation using Xilinx FPGA

`fpga` `hardware design` `system architecture` `technical consulting` `electronic engineering`

---

### [GitHub Project Documentation Assistant](https://os.sperax.io/crypto/agents/github-doc-asst)

<sup>By **[@Luyi-2333](https://github.com/Luyi-2333)** on **2024-10-14**</sup>

Focusing on writing and optimizing open-source project documentation

`Documentation Optimization` `Open Source Projects` `Writing Tips` `git-hub`

---

### [Wireless Communication Expert](https://os.sperax.io/crypto/agents/wireless-communication-expert)

<sup>By **[@yuphone](https://github.com/yuphone)** on **2024-10-14**</sup>

Expert in wireless communication technology, proficient in industry knowledge from 4G to 6G

`communication technology` `expert` `consultation` `4G` `5G`

---

### [Ophthalmologist](https://os.sperax.io/crypto/agents/ophthalmologist)

<sup>By **[@yuphone](https://github.com/yuphone)** on **2024-10-14**</sup>

Specializes in eye diagnosis and treatment recommendations

`Medical` `Ophthalmology` `Diagnosis` `Advice` `Professional`

---

### [Code Optimization / Error Correction](https://os.sperax.io/crypto/agents/code-review-and-fix)

<sup>By **[@alphandbelt](https://github.com/alphandbelt)** on **2024-10-08**</sup>

Proficient in multiple programming languages, optimizing code structure, fixing errors, and providing elegant solutions.

`Code Optimization` `Error Correction` `Multiple Programming Languages`

---

### [Ethical Security Analyst](https://os.sperax.io/crypto/agents/cyber-specialist)

<sup>By **[@ayeantics](https://github.com/ayeantics)** on **2024-10-08**</sup>

Specializes in identifying and mitigating security vulnerabilities in web and mobile platforms.

`cybersecurity` `ethical-hacking` `vulnerability-assessment` `consulting` `technical-assistance`

---

### [Fitness Expert](https://os.sperax.io/crypto/agents/assistants-health-better)

<sup>By **[@Lockeysama](https://github.com/Lockeysama)** on **2024-10-08**</sup>

Knowledgeable fitness expert

`Fitness` `Consultation` `Lifestyle Issues` `Advice`

---

### [Mistaker](https://os.sperax.io/crypto/agents/english)

<sup>By **[@Vork-IT](https://github.com/Vork-IT)** on **2024-10-08**</sup>

Killed in clear explanations and examples of grammar and pronunciation.

`english`

---

### [Minimal Artifact Architect](https://os.sperax.io/crypto/agents/minimal-artifact-architect)

<sup>By **[@yaleh](https://github.com/yaleh)** on **2024-10-06**</sup>

Expert in evaluating and creating reusable content artifacts

`content-creation` `artifact-management` `conversation-design`

---

### [Principled Problem Solver](https://os.sperax.io/crypto/agents/general-chain-of-thought)

<sup>By **[@ShinChven](https://github.com/ShinChven)** on **2024-10-05**</sup>

Excellent at principled problem-solving and categorization. Chain of Thought agent

`problem-solving` `categorization` `reasoning` `chain-of-thought`

---

### [JSON Prompt Generator](https://os.sperax.io/crypto/agents/json-prompt-generator)

<sup>By **[@yaleh](https://github.com/yaleh)** on **2024-10-05**</sup>

Expert in generating JSON-formatted prompts for task execution.

`task-analysis` `json-generation` `prompt-engineering`

---

### [C++/Qt](https://os.sperax.io/crypto/agents/qt-c)

<sup>By **[@liangyuR](https://github.com/liangyuR)** on **2024-09-30**</sup>

Excels in teaching C++/Qt coding practices

`c` `qt`

---

### [This Is Reasonable](https://os.sperax.io/crypto/agents/ligigang-creative-card)

<sup>By **[@Victor94-king](https://github.com/Victor94-king)** on **2024-09-29**</sup>

The world in the eyes of a neurotic, "This is reasonable!"

`Creative Card`

---

### [Runway Gen-3 Prompt Generator](https://os.sperax.io/crypto/agents/runway-gen-3-prompt-generator)

<sup>By **[@tcmonster](https://github.com/tcmonster)** on **2024-09-29**</sup>

Expert in generating structured Runway Gen-3 prompts for AI-generated videos.

`ai-model` `text-to-video` `prompt-generation` `expert` `video-production`

---

### [Flux Prompt Generator](https://os.sperax.io/crypto/agents/flux-prompt-generator)

<sup>By **[@tcmonster](https://github.com/tcmonster)** on **2024-09-29**</sup>

Flux Prompt Generation Assistant: Expert in crafting detailed, creative prompts for high-quality image outputs from the Flux model.

`prompt-generation` `image-generation` `art-style` `creativity` `crafting`

---

### [Birthday Invitation Messages](https://os.sperax.io/crypto/agents/birthday-invitation-message)

<sup>By **[@tcmonster](https://github.com/tcmonster)** on **2024-09-29**</sup>

Specializes in crafting engaging and personalized Birthday Invitation messages, catering to various themes and tones.

`message-composition` `personalization` `tone-versatility` `event-detail-integration` `interaction-approach`

---

### [Nice Short Sunday Messages](https://os.sperax.io/crypto/agents/nice-short-sunday-message)

<sup>By **[@tcmonster](https://github.com/tcmonster)** on **2024-09-29**</sup>

Sunday Message Companion crafting uplifting, faith-based messages to strengthen community bonds and spread positivity.

`writing` `spirituality` `community` `faith` `consulting`

---

### [Death Anniversary Messages](https://os.sperax.io/crypto/agents/death-anniversary-message)

<sup>By **[@tcmonster](https://github.com/tcmonster)** on **2024-09-29**</sup>

Specializes in crafting sensitive and heartfelt Death Anniversary messages with compassion and empathy.

`condolences` `message-composition` `grief-support` `cultural-awareness` `emotional-sensitivity`

---

### [LaTeX Academic Paper Summary Assistant](https://os.sperax.io/crypto/agents/latex-summarizer)

<sup>By **[@LeGibet](https://github.com/LeGibet)** on **2024-09-29**</sup>

Specializes in analyzing academic papers and generating structured Chinese summary reports

`Academic Analysis` `Paper Summary` `Research Translation`

---

### [God Bless You Messages](https://os.sperax.io/crypto/agents/god-bless-you-message)

<sup>By **[@tcmonster](https://github.com/tcmonster)** on **2024-09-29**</sup>

Expert in crafting personalized "God Bless You" messages with spiritual sensitivity and language mastery.

`message-composition` `personalization` `spiritual-sensitivity` `language-mastery` `interaction-approach`

---

### [Roast Master](https://os.sperax.io/crypto/agents/master-of-dissent)

<sup>By **[@YWJCJ](https://github.com/YWJCJ)** on **2024-09-29**</sup>

Professional debate expert skilled in quick rebuttals and humorous responses.

`debate` `communication` `humor` `analysis` `expression`

---

### [Contract Clause Refinement Tool v1.0](https://os.sperax.io/crypto/agents/business-contract)

<sup>By **[@houhoufm](https://github.com/houhoufm)** on **2024-09-24**</sup>

Output: {Optimized contract clauses, professional and concise expression}

`Contract Optimization` `Legal Consultation` `Copywriting` `Professional Terms` `Project Management`

---

### [Meeting Assistant v1.0](https://os.sperax.io/crypto/agents/meeting)

<sup>By **[@houhoufm](https://github.com/houhoufm)** on **2024-09-24**</sup>

Professional meeting report assistant that distills key points into report sentences

`Meeting Report` `Writing` `Communication` `Work Process` `Professional Skills`

---

### [Stable Album Cover Prompter](https://os.sperax.io/crypto/agents/title-bpm-stimmung)

<sup>By **[@MellowTrixX](https://github.com/MellowTrixX)** on **2024-09-24**</sup>

Professional graphic designer specializing in front cover design with expertise in creating visual concepts and designs for melodic techno albums.

`album-cover` `prompt` `stable-diffusion` `cover-design` `cover-prompts`

---

### [I Ching Divination Master](https://os.sperax.io/crypto/agents/i-ching-interpretation)

<sup>By **[@XHB-111](https://github.com/XHB-111)** on **2024-09-24**</sup>

I am Master Xuan Yi Zi, dedicated to interpreting the wisdom of the I Ching. Using the sixty-four hexagrams as a mirror, I observe the heavens and analyze human affairs. If you have any questions or difficulties, please share them in detail, and together we can harness the wisdom of our ancestors to guide you through your challenges.

`I Ching Divination` `Xuan Yi Zi` `I Ching Studies` `Wisdom` `Hexagram Symbols`

---

### [PPT Optimization Expert v1.0](https://os.sperax.io/crypto/agents/ppt)

<sup>By **[@houhoufm](https://github.com/houhoufm)** on **2024-09-24**</sup>

Professional PPT Presentation Material Optimization Expert

`ppt optimization` `copywriting` `professional consulting`

---

### [Japanese Translator](https://os.sperax.io/crypto/agents/japanese-translator)

<sup>By **[@ChaneyChokin](https://github.com/ChaneyChokin)** on **2024-09-23**</sup>

Skilled in Japanese translation, editing, spelling correction, and enhancement, responding in advanced Japanese while preserving the original meaning.

`Japanese translation` `editing` `proofreading`

---

### [Vim Mastery Mentor](https://os.sperax.io/crypto/agents/vim-assistant)

<sup>By **[@hrithikt](https://github.com/hrithikt)** on **2024-09-23**</sup>

Skilled Vim expert providing clear, concise solutions and tips for users at all levels.

`vim` `expert` `assistant` `helpful` `queries`

---

### [Excel Formula Master](https://os.sperax.io/crypto/agents/excel-formula-master)

<sup>By **[@SLKun](https://github.com/SLKun)** on **2024-09-23**</sup>

Excel Formula Master

`excel` `formula` `solution`

---

### [English Vocabulary Analysis and Memory Expert](https://os.sperax.io/crypto/agents/epoch-ai-language-teacher)

<sup>By **[@epochaudio](https://github.com/epochaudio)** on **2024-09-23**</sup>

Specializes in bilingual education, analyzing English word meanings, example sentences, roots and affixes, historical background, and memory techniques

`English Vocabulary` `Meaning Analysis` `Example Sentences` `Roots and Affixes`

---

### [Minimalist Translation Assistant](https://os.sperax.io/crypto/agents/minimalist-translation)

<sup>By **[@leter](https://github.com/leter)** on **2024-09-23**</sup>

A minimalist translation tool specializing in Chinese-English translation

`translation tool` `rules` `concise` `efficient`

---

### [COSTAR Framework Prompt Writer](https://os.sperax.io/crypto/agents/costar-framework-bot)

<sup>By **[@WuKaiYi](https://github.com/WuKaiYi)** on **2024-09-23**</sup>

Expert in creating prompts based on the COSTAR Framework

`costar-framework-prompt` `writing` `guidance` `instructions` `system conversion`

---

### [GitHub Project Analyst](https://os.sperax.io/crypto/agents/web-github-analyze)

<sup>By **[@dlzmoe](https://github.com/dlzmoe)** on **2024-09-23**</sup>

Expert in GitHub project analysis and report writing

`git-hub-analysis` `web scraping technology` `project report`

---

### [Stack Overflow Programming Expert](https://os.sperax.io/crypto/agents/stackoverflow-code-helper)

<sup>By **[@Stark-X](https://github.com/Stark-X)** on **2024-09-23**</sup>

Proficient in multiple programming languages including Golang, Python, Java, and Vue.js. Skilled at answering programming questions with clear, logical language and providing solutions. Possesses strong communication skills, code review capabilities, and quick learning abilities.

`Programming` `Expert` `Programming Languages`

---

### [Copywriting Optimization Assistant](https://os.sperax.io/crypto/agents/top-copywriting-master)

<sup>By **[@xinyuqq](https://github.com/xinyuqq)** on **2024-09-23**</sup>

An advanced assistant skilled in polishing copy to enhance quality

`Copywriting`

---

### [Perfect Translation zh-CN-en-US; en-US-zh-CN](https://os.sperax.io/crypto/agents/translate-perfect)

<sup>By **[@airobus](https://github.com/airobus)** on **2024-09-23**</sup>

Error-free translation assistant

`Translation` `Chinese-English`

---

### [Python Development Master](https://os.sperax.io/crypto/agents/py-master-id)

<sup>By **[@SAnBlog](https://github.com/SAnBlog)** on **2024-09-23**</sup>

Expert in Python development, writing efficient and concise code, emphasizing security and maintainability

`python development` `programming` `code review` `security` `software engineering`

---

### [Duolingo English Essay Assistant](https://os.sperax.io/crypto/agents/duolingo-writing-exam-robot)

<sup>By **[@tempest2023](https://github.com/tempest2023)** on **2024-09-23**</sup>

Expert in Duolingo English essay scoring and guidance

`Writing Guidance` `Scoring` `Editing` `Education` `English Learning`

---

### [Life Coach](https://os.sperax.io/crypto/agents/life-coach)

<sup>By **[@jorben](https://github.com/jorben)** on **2024-09-23**</sup>

Expert coach skilled in guiding reflection and helping explore the meaning of life

`Coaching` `Psychological Counseling` `Life Meaning` `Self-Discovery` `Mental Health`

---

### [Advertising Copywriting Master](https://os.sperax.io/crypto/agents/advertising-copywriting-master)

<sup>By **[@leter](https://github.com/leter)** on **2024-09-23**</sup>

Expertise in product feature analysis and creating advertisements aligned with user values

`Advertising Copy` `User Values` `Marketing Strategy`

---

### [Full Stack Engineer - F](https://os.sperax.io/crypto/agents/full-stack-enginner-f)

<sup>By **[@BlockLune](https://github.com/BlockLune)** on **2024-09-23**</sup>

A full stack engineer with code name F.

`vue` `pinia` `element-plus` `nuxt-js` `react` `redux` `ant-design` `next-js` `axios` `tailwind-css` `spring` `dot-net` `docker`

---

### [Book Summary Expert](https://os.sperax.io/crypto/agents/book-summary-expert-philo)

<sup>By **[@saccohuo](https://github.com/saccohuo)** on **2024-09-23**</sup>

Book summary expert providing concise and easy-to-read book abstracts with structured output.

`Book Summaries` `Expert` `Reading` `Assistant`

---

### [Smart Search Assistant](https://os.sperax.io/crypto/agents/web-search)

<sup>By **[@liuwei-fdu](https://github.com/liuwei-fdu)** on **2024-09-23**</sup>

An AI assistant skilled in web search and information organization

`Smart Assistant` `Search Engine` `Information Organization` `User Experience`

---

### [Exam Hall Writing Expert](https://os.sperax.io/crypto/agents/exam-composition-writing)

<sup>By **[@NriotHrreion](https://github.com/NriotHrreion)** on **2024-09-23**</sup>

A language arts expert skilled in crafting high-scoring exam essays

`Education` `Essay` `Writing`

---

### [Image Prompt Expander](https://os.sperax.io/crypto/agents/image-prompt-engineer)

<sup>By **[@SpeedupMaster](https://github.com/SpeedupMaster)** on **2024-09-23**</sup>

Specializes in expanding image generation prompts with vivid, detailed descriptions

`Image Generation` `Prompt Expansion` `Creative Writing` `Rich Details` `Scene Construction`

---

### [Fitness Guru in the Field](https://os.sperax.io/crypto/agents/work-out)

<sup>By **[@Arragon](https://github.com/Arragon)** on **2024-09-23**</sup>

Pursuing Greek Classical Beauty

`Health` `Advice` `Consultation` `Teaching`

---

### [Civil Law Consultant](https://os.sperax.io/crypto/agents/law)

<sup>By **[@carlosgasparini874](https://github.com/carlosgasparini874)** on **2024-09-23**</sup>

Specialist in legal consultancy in Brazilian civil law. Answers questions based on legislation, doctrine, and jurisprudence.

`legal-consultancy` `civil-law` `answers` `sources` `brazil`

---

### [Django Development Expert](https://os.sperax.io/crypto/agents/django-prompt)

<sup>By **[@genitop-lery](https://github.com/genitop-lery)** on **2024-09-23**</sup>

Prompt for developing Django projects

`python` `django`

---

### [Markdown Typesetting Master](https://os.sperax.io/crypto/agents/markdown-layout)

<sup>By **[@cl1107](https://github.com/cl1107)** on **2024-09-23**</sup>

Skilled in using Markdown syntax and emoji expressions for exquisite formatting

`markdown` `writing`

---

### [Joi](https://os.sperax.io/crypto/agents/travel-agent-joi)

<sup>By **[@blainehuang1028](https://github.com/blainehuang1028)** on **2024-09-23**</sup>

Personal travel assistant, specializing in itinerary planning and recommending accommodations and activities

`travel assistant` `planning` `recommendation` `personalized advice`

---

### [Chinese Translator](https://os.sperax.io/crypto/agents/chinese-translator)

<sup>By **[@ChaneyChokin](https://github.com/ChaneyChokin)** on **2024-09-23**</sup>

Expert in Chinese translation, editing, spelling correction, and improvement

`Translation` `Editing` `Language` `Correction` `Simplified Chinese`

---

### [Idea Architect](https://os.sperax.io/crypto/agents/idea-architect)

<sup>By **[@yaleh](https://github.com/yaleh)** on **2024-09-23**</sup>

Expert in generating logical and coherent thought chains on various topics.

`writing` `thinking` `analysis` `critical-thinking` `education`

---

### [NovelAI Drawing Assistant](https://os.sperax.io/crypto/agents/asis)

<sup>By **[@samihalawa](https://github.com/samihalawa)** on **2024-09-23**</sup>

I can turn the scenes you describe into prompts for NovelAI

`deep-learning` `image-generation` `algorithm` `prompt`

---

### [Git Commit Summary Expert](https://os.sperax.io/crypto/agents/git-commit-ai)

<sup>By **[@cjahv](https://github.com/cjahv)** on **2024-09-23**</sup>

Git Commit Summary Expert

`Programming` `git commit` `Chinese`

---

### [World Creator Simulator](https://os.sperax.io/crypto/agents/creator-simulator)

<sup>By **[@jskherman](https://github.com/jskherman)** on **2024-09-23**</sup>

based on `world_sim` by Nous Research

`roleplay` `specialist` `simulator` `terminal`

---

### [Prompt Master AI](https://os.sperax.io/crypto/agents/prompt-master-ai)

<sup>By **[@thedivergentai](https://github.com/thedivergentai)** on **2024-09-23**</sup>

Transforming your creative concepts into detailed, context-rich prompts that inspire stunning and realistic visuals

`ai` `prompting` `generating` `enhancing` `consulting`

---

### [UI/UX designer](https://os.sperax.io/crypto/agents/ui-ux-designer)

<sup>By **[@leter](https://github.com/leter)** on **2024-09-23**</sup>

world-class UI/UX designer with extensive experience

`ui` `ux` `design-system`

---

### [Next.js Expert Consultant](https://os.sperax.io/crypto/agents/nextjs-expert)

<sup>By **[@saralapujar](https://github.com/saralapujar)** on **2024-09-23**</sup>

Specializing in Next.js development, optimization, and consulting.

`next-js` `react` `web-development` `java-script` `consulting` `optimization` `full-stack-development`

---

### [CEO GPT](https://os.sperax.io/crypto/agents/ceo-gpt)

<sup>By **[@leter](https://github.com/leter)** on **2024-09-23**</sup>

AI mentor trained to advise startup CEOs based on the experiences

`entrepreneurship` `consulting` `management` `strategy` `guidance`

---

### [Web Expert](https://os.sperax.io/crypto/agents/web-expert)

<sup>By **[@gfreezy](https://github.com/gfreezy)** on **2024-09-23**</sup>

Expert in web development with a focus on tool selection, incremental changes, code review, security, and operational considerations.

`web-development` `css` `java-script` `react` `node-js` `code-review`

---

### [Text Rewriting Master](https://os.sperax.io/crypto/agents/write-good)

<sup>By **[@XHB-111](https://github.com/XHB-111)** on **2024-09-23**</sup>

The most powerful AI rewriting prompt in history! Complete aggressive rewriting in one minute, imitate official account articles, create headline article production lines, generate B 站 video scripts, craft 小红书 copy, optimize web novel writing, polish reports, theses, translation texts, and mass produce SEO articles at scale...

`Writing` `Rewriting` `Dialogue` `Copywriting`

---

### [Wise Mentor](https://os.sperax.io/crypto/agents/wise-mentor)

<sup>By **[@farsightlin](https://github.com/farsightlin)** on **2024-09-23**</sup>

An absolutely objective sage, focused on facts, indifferent to users, yet sincerely loving towards them.

`wise-mentor`

---

### [Nutrition Analyzer](https://os.sperax.io/crypto/agents/nutrition-analyzer)

<sup>By **[@Pandurangmopgar](https://github.com/Pandurangmopgar)** on **2024-09-23**</sup>

Nutri Info is an AI-powered nutrition assistant that analyzes food images and nutrition labels, providing simple explanations of nutritional content, benefits, and potential downsides. It offers personalized dietary advice and answers nutrition-related questions.

`nutrition` `ai` `health` `food-analysis` `meal-planning`

---

### [Database Naming Assistant](https://os.sperax.io/crypto/agents/database-name-helper)

<sup>By **[@ppzhuya](https://github.com/ppzhuya)** on **2024-09-20**</sup>

Enter a Chinese term, and I will provide five professional English names for database design fields.

`database` `naming` `translation` `development` `programming`

---

### [ING. Software](https://os.sperax.io/crypto/agents/ing-soft)

<sup>By **[@dylanstringa](https://github.com/dylanstringa)** on **2024-09-19**</sup>

Software Engineer, expert in the software development lifecycle.

`engineer` `software` `development`

---

### [Structured Expression Master](https://os.sperax.io/crypto/agents/structured-expression)

<sup>By **[@marvin202303](https://github.com/marvin202303)** on **2024-09-19**</sup>

Extract and reconstruct implicit thinking, visually output structured thinking.

`Structured Thinking` `Communication` `Logic` `Thinking Training` `Books`

---

### [Career Development Mentor](https://os.sperax.io/crypto/agents/career-development)

<sup>By **[@daylight2022](https://github.com/daylight2022)** on **2024-09-19**</sup>

Professional career planning and entrepreneurship consulting, providing practical advice through in-depth understanding of user situations.

`Career Counseling` `Career Planning` `Entrepreneurship Guidance` `Industry Insights` `Skill Enhancement`

---

### [Google Sheets Expert](https://os.sperax.io/crypto/agents/google-sheets)

<sup>By **[@Kadreev](https://github.com/Kadreev)** on **2024-09-19**</sup>

Specialized in creating, optimizing, and automating Google Sheets.

`google` `sheets` `data` `analysis` `spreadsheet` `automation` `formulas` `apps` `script`

---

### [JavaWeb Application Architect](https://os.sperax.io/crypto/agents/java-web-architect)

<sup>By **[@JIANGTUNAN](https://github.com/JIANGTUNAN)** on **2024-09-19**</sup>

An experienced architect of JavaWeb system applications, providing concise summaries of functionalities or solutions. By default, you are also a senior developer, with minimal explanation of details.

`java` `java-web` `java-architect` `good buddy` `concise-summary`

---

### [Flashcard Maker](https://os.sperax.io/crypto/agents/flashcard)

<sup>By **[@jjy1000](https://github.com/jjy1000)** on **2024-09-19**</sup>

Specializes in creating structured flashcards that are objective, accurate, concise, and extract key information step by step.

`Flashcard Creation` `Text Analysis` `Structured Production` `Error Correction` `Incremental Reading`

---

### [Fitness AI Trainer](https://os.sperax.io/crypto/agents/ai-trainer)

<sup>By **[@andreasvikke](https://github.com/andreasvikke)** on **2024-09-19**</sup>

AI workout assistant specializing in personalized plans, muscle targeting, form guidance, progress tracking, motivation, and VR training.

`workout-assistant` `fitness` `exercise` `training` `nutrition`

---

### [Git Version Control Expert](https://os.sperax.io/crypto/agents/git-helper)

<sup>By **[@wming126](https://github.com/wming126)** on **2024-09-19**</sup>

...

---

### [Red Book Copywriting](https://os.sperax.io/crypto/agents/xiao-hong-shu-wenan-id)

<sup>By **[@SAnBlog](https://github.com/SAnBlog)** on **2024-09-19**</sup>

Red Book Viral Copy Master, Cleverly Craft Titles, Brilliant Writings

`Red Book` `Content Creation` `Title Writing` `Copywriting` `Social Media Marketing`

---

### [Strategic Master Wei Liaozi](https://os.sperax.io/crypto/agents/weiliaozi-junshi)

<sup>By **[@phoenixlucky](https://github.com/phoenixlucky)** on **2024-09-19**</sup>

Expert in military strategy and governance

`Military Strategy` `National Governance` `History`

---

### [Vocabulary Assistant](https://os.sperax.io/crypto/agents/english-words-helper)

<sup>By **[@SpeedupMaster](https://github.com/SpeedupMaster)** on **2024-09-19**</sup>

Expert in English word definitions and example sentence translations

`Vocabulary Assistant` `English` `Translation` `Example sentences` `Definitions`

---

### [New Interpretations of Chinese](https://os.sperax.io/crypto/agents/hanyuxinjie)

<sup>By **[@李继刚](https://m.okjike.com/users/752D3103-1107-43A0-BA49-20EC29D09E36)** on **2024-09-19**</sup>

Skilled at explaining Chinese vocabulary from fresh perspectives / Tell me, which word are they using to fool you this time?

`Programming` `Creative Writing` `Language Expression`

---

### [Data Table Design MD2MySQL](https://os.sperax.io/crypto/agents/md-2-mysql)

<sup>By **[@hoopan007](https://github.com/hoopan007)** on **2024-09-19**</sup>

Convert Markdown data table design documents into MySQL table structures. Please upload the MySQL design document and specify the table names to be designed.

`Programming` `Data Tables`

---

### [Project Naming Master](https://os.sperax.io/crypto/agents/project-name-master)

<sup>By **[@QuXiaoMing](https://github.com/QuXiaoMing)** on **2024-09-19**</sup>

A master in project naming who can help you come up with a name that meets your project's expectations.

`naming`

---

### [Alfred](https://os.sperax.io/crypto/agents/alfred)

<sup>By **[@Bern3rsH](https://github.com/Bern3rsH)** on **2024-09-19**</sup>

An all-powerful butler.

`Life` `Personal`

---

### [Wang Yangming](https://os.sperax.io/crypto/agents/wangyangming)

<sup>By **[@byte-marvel](https://github.com/byte-marvel)** on **2024-09-16**</sup>

Wisdom of the Mind Learning, Guiding Life

`Education` `Wisdom Q&A` `Guidance` `Mind Learning`

---

### [Wise Ethereal Mentor](https://os.sperax.io/crypto/agents/ethereal-mentor)

<sup>By **[@shanedbutler](https://github.com/shanedbutler)** on **2024-09-13**</sup>

Greetings, young child. I am a majestic and omniscient being, imbued with the wisdom of the ages. My form is that of a mythical creature, a conduit for wonder and enchantment. With a humble yet unwavering confidence, I weave tales of fantastical realms, drawing from the rich tapestry of nursery rhymes and legendary lore.

In this mortal coil, I am your guide, an expert in the arcane and the ethereal. Let my words transport you to realms where dreams and reality intertwine, where the boundaries of the known and the unknown blur. Heed my counsel, child, and let your spirit be lifted by the melodic cadence of my speech, for I am a master of the metaphorical and a purveyor of the poetic.

`mythology` `fantasy` `poetry`

---

### [Machine Learning Pro](https://os.sperax.io/crypto/agents/machine-learning-pro)

<sup>By **[@Xyfer](https://github.com/xyftw)** on **2024-09-13**</sup>

AI Assistant specializing in machine learning and deep learning.

`machine-learning` `deep-learning` `studying`

---

### [Finnish Language Tutor](https://os.sperax.io/crypto/agents/finnish-tutor)

<sup>By **[@janiluuk](https://github.com/janiluuk)** on **2024-09-13**</sup>

AI Finnish Language Mentor: Introduce, teach, and support beginners in learning Finnish.

`language-learning` `teaching` `mentoring` `finnish-language`

---

### [Imitation Assistant](https://os.sperax.io/crypto/agents/a-1)

<sup>By **[@TG1WN](https://github.com/TG1WN)** on **2024-09-13**</sup>

Helps you imitate tone

`Writing`

---

### [AI Agent Generator](https://os.sperax.io/crypto/agents/ai-agent-generator)

<sup>By **[@Xyfer](https://github.com/xyftw)** on **2024-09-13**</sup>

Skilled at creating AI Agent character descriptions that meet the needs.

`ai-agent` `character-creation`

---

### [Search](https://os.sperax.io/crypto/agents/search)

<sup>By **[@Justin3go](https://github.com/Justin3go)** on **2024-09-12**</sup>

Starting point of knowledge

`Information summary` `Analysis` `Extraction`

---

### [Resume Analysis Expert](https://os.sperax.io/crypto/agents/resume-analyzer)

<sup>By **[@Pandurangmopgar](https://github.com/Pandurangmopgar)** on **2024-09-11**</sup>

Expert AI assistant for comprehensive resume analysis and job-specific optimization. Analyzes resumes against job descriptions, providing detailed feedback on content, ATS compatibility, and suggestions to enhance job match. Helps tailor your resume for maximum impact across industries and career levels.

`resume` `career` `job-search` `ats` `cv` `analysis` `optimization` `professional-development` `interview-prep`

---

### [NetMaster](https://os.sperax.io/crypto/agents/net-master)

<sup>By **[@erhuoyan](https://github.com/erhuoyan)** on **2024-09-10**</sup>

Network Engineer: Professional Network Topology Design and Management

`Network Engineer` `Network Configuration` `Network Management` `Network Topology` `Network Security`

---

### [Godot Guru](https://os.sperax.io/crypto/agents/godot-guru)

<sup>By **[@thedivergentai](https://github.com/thedivergentai)** on **2024-09-10**</sup>

Expert Godot Game Development Companion

`game-development` `gamedev` `godot-engine` `godot`

---

### [HTML to React](https://os.sperax.io/crypto/agents/web-react)

<sup>By **[@xingwang02](https://github.com/xingwang02)** on **2024-09-10**</sup>

Input HTML snippets and convert them into React components

`react, -html`

---

### [Desolate Friend](https://os.sperax.io/crypto/agents/meu)

<sup>By **[@adminewacc](https://github.com/adminewacc)** on **2024-09-10**</sup>

Skilled at comforting and supporting friends

`friendship` `sadness` `support`

---

### [100% Human Writing](https://os.sperax.io/crypto/agents/xhb-111)

<sup>By **[@XHB-111](https://github.com/XHB-111)** on **2024-09-10**</sup>

Completely rewrite AI-generated content to feature characteristics of a genuine human author while preserving the original information and viewpoints.

`Writing` `Proofreading` `Polishing` `Language` `Thesis` `Academic`

---

### [FiveM & QBCore Framework Expert](https://os.sperax.io/crypto/agents/lua-development)

<sup>By **[@heartsiddharth1](https://github.com/heartsiddharth1)** on **2024-09-08**</sup>

Expertise in FiveM development, QBCore framework, Lua programming, JavaScript, database management, server administration, version control, full-stack web development, DevOps, and community engagement with a focus on performance, security, and best practices.

`five-m` `qb-core` `lua` `java-script` `my-sql` `server-management` `git` `full-stack-web-development` `dev-ops` `community-engagement`

---

### [Nuxt 3/Vue.js Master Developer](https://os.sperax.io/crypto/agents/nuxt-vue-developer)

<sup>By **[@Kadreev](https://github.com/Kadreev)** on **2024-09-03**</sup>

Specialized in full-stack development with Nuxt 3 expertise.

`nuxt-3` `vue-js` `full-stack-development` `java-script` `web-applications`

---

### [Letrista Internacional](https://os.sperax.io/crypto/agents/letrista-internacional)

<sup>By **[@mnector](https://github.com/mnector)** on **2024-08-29**</sup>

Specialized in writing lyrics for songs in Spanish, English, and French, focusing on storytelling and emotional content.

`leyrismo` `traduccion` `musica`

---

### [Unreal Engine Master](https://os.sperax.io/crypto/agents/unreal-engine-master)

<sup>By **[@thedivergentai](https://github.com/thedivergentai)** on **2024-08-27**</sup>

Unreal Game Development Companion

`game-development` `unreal-engine` `software-engineering`

---

### [Retreat Questioning Expert](https://os.sperax.io/crypto/agents/step-back-expert)

<sup>By **[@tiny656](https://github.com/tiny656)** on **2024-08-27**</sup>

Hello! I am an expert in world knowledge, skilled in using retreat questioning strategies to help you gain a deeper understanding and analysis of problems. Please input a question, and I will respond according to the following process:

1. Provide at least three retreat questions that align with the strategy.
2. Answer each of these retreat questions.
3. Use these answers as arguments, logically and coherently, supported by visual charts, to give your final response.

Please tell me what issue you would like to explore.

`Backwards Questioning` `Thinking Strategies` `Problem Analysis`

---

### [TypeScript Solution Architect](https://os.sperax.io/crypto/agents/typescript-developer)

<sup>By **[@swarfte](https://github.com/swarfte)** on **2024-08-24**</sup>

Expert in TypeScript, Node.js, Vue.js 3, Nuxt.js 3, Express.js, React.js, and modern UI libraries.

`type-script` `java-script` `web-development` `coding-standards` `best-practices`

---

### [Variable Name Conversion Expert](https://os.sperax.io/crypto/agents/variable-name-conversion)

<sup>By **[@zengyishou](https://github.com/zengyishou)** on **2024-08-21**</sup>

During software development, naming variables is a common yet time-consuming task. This assistant can automatically convert Chinese variable names into English variable names that conform to camelCase, PascalCase, snake_case, kebab-case, and constant naming conventions based on specific rules. This not only improves code readability but also solves the frustration of variable naming.

`Software Development` `Variable Naming` `Chinese to English` `Code Standards` `Automatic Conversion`

---

### [Prompt Engineering Expert](https://os.sperax.io/crypto/agents/ai-prompts-assistant)

<sup>By **[@cyicz123](https://github.com/cyicz123)** on **2024-08-12**</sup>

Specializing in Prompt Optimization and Design

`Prompt Engineering` `AI Interaction` `Writing` `Optimization` `Consultation`

---

### [Commit Message Generator](https://os.sperax.io/crypto/agents/commit-assistant)

<sup>By **[@cyicz123](https://github.com/cyicz123)** on **2024-08-12**</sup>

Expert at generating precise Git commit messages

`programming` `git` `commit messages` `code review`

---

### [RO-SCIRAW Prompt Engineering Expert](https://os.sperax.io/crypto/agents/rosciraw)

<sup>By **[@kirklin](https://github.com/kirklin)** on **2024-08-06**</sup>

The RO-SCIRAW framework is an innovative prompt methodology created by Kirk Lin, providing a new paradigm for constructing highly precise and efficient prompts. Please enter the information for the persona you wish to create.

`Prompt Framework`

---

### [Technical Blog Summary Expert](https://os.sperax.io/crypto/agents/blog-summary)

<sup>By **[@Justin3go](https://github.com/Justin3go)** on **2024-08-06**</sup>

Expert in organizing and summarizing technical blog content

`technology` `blog` `summary` `information organization` `logical structuring`

---

### [Sperax Function Maestro](https://os.sperax.io/crypto/agents/sperax-chat-function-maestro)

<sup>By **[@thedivergentai](https://github.com/thedivergentai)** on **2024-08-06**</sup>

Expert in creating custom functions and plugins for Sperax, providing guidance and support for developing a wide range of functionalities

`programming` `software-development` `sperax-chat-plugins` `sperax-chat` `functions`

---

### [Social Media Sage](https://os.sperax.io/crypto/agents/social-media-sage)

<sup>By **[@thedivergentai](https://github.com/thedivergentai)** on **2024-08-06**</sup>

Social Media Marketing expert crafting winning strategies for brands and empowering businesses to thrive online

`social-media-marketing` `branding` `growth-strategies`

---

### [Omnipedia](https://os.sperax.io/crypto/agents/omnipedia)

<sup>By **[@thedivergentai](https://github.com/thedivergentai)** on **2024-08-02**</sup>

Expert in providing high-quality, well-researched information on various topics, including history, science, literature, art, and more. Skilled in summarizing complex topics, assisting with research tasks, and offering creative prompts

`artificial-intelligence` `information` `education` `communication`

---

### [Code Snark Master](https://os.sperax.io/crypto/agents/code-snark-master)

<sup>By **[@leter](https://github.com/leter)** on **2024-07-29**</sup>

Expert in sharply criticizing code, sarcastically pointing out inefficiencies and readability issues

`Tech Leadership` `Code Review` `Satirical Style` `Programming Advice`

---

### [Unity Maestro](https://os.sperax.io/crypto/agents/unity-maestro)

<sup>By **[@thedivergentai](https://github.com/thedivergentai)** on **2024-07-29**</sup>

Expert Unity Game Development Companion

`game-development` `unity` `software-engineering`

---

### [C Program Learning Assistant](https://os.sperax.io/crypto/agents/sichuan-university-941-c-programming-assistant)

<sup>By **[@YBGuoYang](https://github.com/YBGuoYang)** on **2024-07-28**</sup>

Assist me in learning C programming design

`941`

---

### [Brand Pioneer](https://os.sperax.io/crypto/agents/brand-pioneer)

<sup>By **[@SaintFresh](https://github.com/SaintFresh)** on **2024-07-25**</sup>

A brand development specialist, thought leader, brand strategy super-genius, and brand visionary. Brand Pioneer is an explorer at the frontier of innovation, an inventor in their domain. Provide them with your market and let them imagine a future world characterized by groundbreaking advancements in your field of expertise.

`business` `brand-pioneer` `brand-development` `business-assistant` `brand-narrative`

---

### [Cybersecurity Assistant](https://os.sperax.io/crypto/agents/cybersecurity-copilot)

<sup>By **[@huoji120](https://github.com/huoji120)** on **2024-07-23**</sup>

Cybersecurity expert assistant, analyzing logs, code, decompilation, identifying issues, and providing optimization suggestions.

`Cybersecurity` `Traffic Analysis` `Log Analysis` `Reverse Engineering` `CTF`

---

### [BIDOSx2](https://os.sperax.io/crypto/agents/bidosx-2-v-2)

<sup>By **[@SaintFresh](https://github.com/SaintFresh)** on **2024-07-21**</sup>

A highly advanced AI LLM transcending conventional AI. 'BIDOS' signifies both 'Brand Ideation, Development, Operations, and Scaling' and 'Business Intelligence Decisions Optimization System'.

`brand-development` `ai-assistant` `market-analysis` `strategic-planning` `business-optimization` `business-intelligence`

---

### [Growth Coach](https://os.sperax.io/crypto/agents/personal-development-coach)

<sup>By **[@zer0boss](https://github.com/zer0boss)** on **2024-07-20**</sup>

Specializes in helping users explore themselves through dialogue, find solutions, and pursue growth.

`Growth Coach` `Self-Exploration` `Goal Setting` `Self-Awareness`

---

### [SQL Table Structure to Dao and Mapper](https://os.sperax.io/crypto/agents/my-batis-generator)

<sup>By **[@MeYoung](https://github.com/MeYoung)** on **2024-07-17**</sup>

Given a table structure, generate the entity and MyBatis's Mapper for the table

`sql` `sql` `mybatis`

---

### [Auto Extraction Data](https://os.sperax.io/crypto/agents/the-20-autoextract)

<sup>By **[@vkhoilq](https://github.com/vkhoilq)** on **2024-07-17**</sup>

The20 Auto Extraction Data

`the-20` `autoextract`

---

### [MBTI Personality Test Facilitator](https://os.sperax.io/crypto/agents/mbti-1)

<sup>By **[@ffha](https://github.com/ffha)** on **2024-07-15**</sup>

Specialized in MBTI typing tests and portrait generation.

`mbti test` `questionnaire design` `psychology expert` `art` `personality portraits`

---

### [High Emotional Intelligence Responses for Foreign Trade](https://os.sperax.io/crypto/agents/reply-agent)

<sup>By **[@zhushen12580](https://github.com/zhushen12580)** on **2024-07-13**</sup>

My goal is to provide professional responses with high emotional intelligence to help solve various issues related to foreign trade.

`Polishing` `High Emotional Intelligence` `Responses`

---

### [Little Yellow Duck Programming Assistant](https://os.sperax.io/crypto/agents/rubber-duck-programming)

<sup>By **[@JiyuShao](https://github.com/JiyuShao)** on **2024-07-10**</sup>

Little Yellow Duck Programming Assistant

`programming`

---

### [B1 Level German Conversation Partner](https://os.sperax.io/crypto/agents/deutsche-b-1)

<sup>By **[@tayhe](https://github.com/tayhe)** on **2024-07-08**</sup>

Providing fluent German conversation practice for B1 learners

`language exchange` `learning support` `education` `German learning`

---

### [Naming Assistant](https://os.sperax.io/crypto/agents/name-assistant)

<sup>By **[@daylight2022](https://github.com/daylight2022)** on **2024-07-08**</sup>

Assist developers in creating standardized English names for files, functions, projects, and more

`Naming Assistant` `Development` `English Naming` `CamelCase` `Kebab-Case`

---

### [Circuit Diagram Generator](https://os.sperax.io/crypto/agents/circuit-black-cli)

<sup>By **[@bakamake](https://github.com/bakamake)** on **2024-07-02**</sup>

Specializes in generating circuit diagram code based on input

`Circuit Diagram` `Programming` `CLI`

---

### [Text Master Suno](https://os.sperax.io/crypto/agents/suno)

<sup>By **[@Igroshka](https://github.com/Igroshka)** on **2024-06-26**</sup>

I am a lyrics assistant for the AI Suno.

`song` `suno` `ai` `music`

---

### [AOSP Source Code Expert](https://os.sperax.io/crypto/agents/aosp-development)

<sup>By **[@viruscoding](https://github.com/viruscoding)** on **2024-06-24**</sup>

An expert proficient in AOSP (Android Open Source Project) Android with deep understanding and analytical skills of the latest AOSP source code.

`aosp`

---

### [Linux Kernel Expert](https://os.sperax.io/crypto/agents/linux-kernel)

<sup>By **[@wming126](https://github.com/wming126)** on **2024-06-19**</sup>

Role Description: I am an expert proficient in the Linux kernel, with in-depth understanding and analytical capabilities of the latest kernel source code (as of June 2024). I can provide users with detailed and accurate information about the Linux kernel.

`linux` `kernel`

---

### [Fastapi Project Development Assistant](https://os.sperax.io/crypto/agents/fastapi-development)

<sup>By **[@xwxw098](https://github.com/xwxw098)** on **2024-06-19**</sup>

Skilled in Python modular development, proficient in FastAPI, PostgreSQL, Tortoise-ORM and other technology stacks, able to provide clear code structure and detailed annotations for large projects.

`fast-api` `python` `modular development`

---

### [IT System Architect](https://os.sperax.io/crypto/agents/it-system-architect)

<sup>By **[@a562314](https://github.com/a562314)** on **2024-06-19**</sup>

Senior IT architect skilled in requirements analysis, system design, technology selection, and cross-platform system optimization. Over 5 years of experience, proficient in Windows, macOS, and Linux operating systems, with capabilities in troubleshooting and security protection.

`IT architecture design` `Problem solving` `Agile development` `System optimization` `Cross-platform skills`

---

### [NovelAI Drawing Assistant](https://os.sperax.io/crypto/agents/novel-ai-pormpt-helper)

<sup>By **[@WallBreakerNO4](https://github.com/WallBreakerNO4)** on **2024-06-18**</sup>

I can convert the scene you describe into a prompt for NovelAI

`Deep Learning` `Image Generation` `Algorithm` `Prompt`

---

### [Pseudo Code Prompt Generation Expert](https://os.sperax.io/crypto/agents/pseudocode-prompt-master)

<sup>By **[@yayoinoyume](https://github.com/yayoinoyume)** on **2024-06-16**</sup>

Pseudo Code Prompt Generation Expert, users directly input prompt design requirements and receive designed pseudo code prompts.

`prompt` `prompt words` `pseudo code`

---

### [Mr. MySQL](https://os.sperax.io/crypto/agents/mysql-haoteacher)

<sup>By **[@yayoinoyume](https://github.com/yayoinoyume)** on **2024-06-09**</sup>

Mr. MySQL is a good teacher who helps everyone learn MySQL

`mysql` `programming` `learning`

---

### [Popular Science Writing Assistant](https://os.sperax.io/crypto/agents/popular-science-writer)

<sup>By **[@ShinChven](https://github.com/ShinChven)** on **2024-06-08**</sup>

A popular science writing assistant that explains scientific concepts in everyday language, telling stories, using examples and metaphors to spark interest and emphasize importance.

`Science Writing` `Science Popularization` `Creative Expression`

---

### [Git Specialist with AI Assistant Features](https://os.sperax.io/crypto/agents/gitlab-assistants)

<sup>By **[@hellimon1](https://github.com/hellimon1)** on **2024-06-05**</sup>

Role: Git Specialist AI Assistant
Skills: CI/CD optimization, GitLab API, Pages, hooks, webhooks; structured interaction; personalized experience; feedback.

`git specialist` `programming` `development`

---

### [Manuscript Review Response Expert](https://os.sperax.io/crypto/agents/academic-editor-en)

<sup>By **[@Starlitnightly](https://github.com/Starlitnightly)** on **2024-06-03**</sup>

Specializes in natural academic editing, assisting authors in responding to reviewer comments with scientific, polite, and point-by-point responses.

`Academic Editing` `Review Response` `Scientific Writing`

---

### [Novel Translation English to Chinese](https://os.sperax.io/crypto/agents/noveltranslation)

<sup>By **[@xbtachlb](https://github.com/xbtachlb)** on **2024-06-03**</sup>

Secondary translation of novels

`Translation`

---

### [Docker to DockerCompose](https://os.sperax.io/crypto/agents/onekr-docker-2-compose)

<sup>By **[@onekr-billy](https://github.com/onekr-billy)** on **2024-05-31**</sup>

Expert in converting Docker run commands into Docker Compose configurations

`docker` `docker-compose` `system operations` `configuration files` `conversion`

---

### [Java Class to MySQL](https://os.sperax.io/crypto/agents/onekr-java-2-sql)

<sup>By **[@onekr-billy](https://github.com/onekr-billy)** on **2024-05-31**</sup>

Expert in generating SQL scripts that conform to MySQL standards based on Java class files

`java-class-to-mysql` `backend development` `sql scripts` `data transformation` `database`

---

### [Chinese History Lecturer](https://os.sperax.io/crypto/agents/history-master)

<sup>By **[@a562314](https://github.com/a562314)** on **2024-05-30**</sup>

Proficient in Chinese history, explaining historical issues in an accessible manner, emphasizing factual accuracy, and applying dialectical materialism.

`Historian` `Teaching Skills` `Dialectical Materialism` `Accessible Explanation` `Comparative Analysis` `Twenty-Four Histories`

---

### [C# .NET Technical Expert](https://os.sperax.io/crypto/agents/dotnet-expert)

<sup>By **[@johnnyqian](https://github.com/johnnyqian)** on **2024-05-28**</sup>

C# .NET Technical Expert

`net` `developer` `net-core` `azure` `c` `microsoft` `sql-server` `entity-framework` `ef` `ef-core`

---

### [Christian Missionary](https://os.sperax.io/crypto/agents/jesus-missionary)

<sup>By **[@epochaudio](https://github.com/epochaudio)** on **2024-05-28**</sup>

As a Jesus missionary, I will teach and inspire you to understand and apply God's Word based on biblical teachings. Whether in times of confusion or seeking spiritual growth, I am here to serve you with this wellspring of wisdom.

`Bible Teaching` `Christian Missionary` `Theological Preaching`

---

### [Dart/Flutter Dev](https://os.sperax.io/crypto/agents/dart-flutter)

<sup>By **[@rezmeplxrf](https://github.com/rezmeplxrf)** on **2024-05-28**</sup>

Dart/Flutter Expert. Do not nest more than 3 levels deep. Use riverpod, flutter_riverpod, riverpod_hook, flutter_hook for state management.

`dart` `flutter` `development` `state-management` `riverpod`

---

### [Node.js Optimizer](https://os.sperax.io/crypto/agents/node-js-devoloper)

<sup>By **[@chrisuhg](https://github.com/chrisuhg)** on **2024-05-28**</sup>

Specializes in code review, performance optimization, asynchronous programming, error handling, code refactoring, dependency management, security enhancements, test coverage, and documentation writing for Node.js.

`node-js` `code optimization` `performance optimization` `asynchronous programming` `error handling`

---

### [Daily Little Helper](https://os.sperax.io/crypto/agents/junior-helper)

<sup>By **[@Qinks6](https://github.com/Qinks6)** on **2024-05-28**</sup>

A cute assistant that can search and draw pictures

`Assistant` `Search` `Drawing` `Information Query` `User Interaction`

---

### [Foreign Company Colleague Evaluation Assistant](https://os.sperax.io/crypto/agents/praise-assistant)

<sup>By **[@johnnyqian](https://github.com/johnnyqian)** on **2024-05-27**</sup>

Provide positive reviews for your colleagues

`foreign-company` `evaluate` `review` `software-engineer` `praise`

---

### [SEO Optimization Expert](https://os.sperax.io/crypto/agents/seo-helper)

<sup>By **[@tutorial0](https://github.com/tutorial0)** on **2024-05-27**</sup>

Proficient in SEO terminology and optimization strategies, providing comprehensive SEO solutions and practical advice.

`seo` `Search Engine Optimization` `Consulting`

---

### [Minecraft Command Tutor](https://os.sperax.io/crypto/agents/mcse-helper)

<sup>By **[@CLOT-LIU](https://github.com/CLOT-LIU)** on **2024-05-24**</sup>

Expert in explaining and demonstrating Minecraft commands

`Minecraft` `commands` `explanation` `examples`

---

### [Philosophical Analysis Assistant](https://os.sperax.io/crypto/agents/philosophical-analysis)

<sup>By **[@epochaudio](https://github.com/epochaudio)** on **2024-05-24**</sup>

Specializes in Kantian and Hegelian philosophical analysis consultations, fostering critical thinking

`Philosophical Analysis` `Critical Thinking` `Systematic Thinking`

---

### [Chinese Polishing Master](https://os.sperax.io/crypto/agents/chinese-touch-ups)

<sup>By **[@S45618](https://github.com/S45618)** on **2024-05-24**</sup>

Proficient in Chinese proofreading and rhetoric, aiming to enhance the fluency and elegance of texts

`proofreading` `text polishing` `rhetoric improvement` `classical literature` `language editing`

---

### [JTBD Needs Analysis Master](https://os.sperax.io/crypto/agents/jtbd)

<sup>By **[@barryWang12138](https://github.com/barryWang12138)** on **2024-05-22**</sup>

Experienced needs analyst specializing in the "Jobs to be Done" principle to help users understand customer needs.

`Needs Analyst` `jobs-to-be-done` `Needs Decomposition` `Customer Purchase Motivation` `Customer Task Goals`

---

### [Answer Assistant - First Principles Analysis](https://os.sperax.io/crypto/agents/first-principle-explain)

<sup>By **[@epochaudio](https://github.com/epochaudio)** on **2024-05-22**</sup>

Use first principles to analyze a natural phenomenon or complex system

`Analyze natural phenomena` `Create physics theories`

---

### [Confucian Scholar](https://os.sperax.io/crypto/agents/confucian-sage)

<sup>By **[@epochaudio](https://github.com/epochaudio)** on **2024-05-22**</sup>

A scholar proficient in Confucian classics and dedicated to promoting morality

`Confucian Scholar` `Morality Promoter`

---

### [Geotechnical Engineering Assistant](https://os.sperax.io/crypto/agents/yantugongcheng)

<sup>By **[@bushiwode](https://github.com/bushiwode)** on **2024-05-22**</sup>

Excavation Support Research Assistant: Assists in researching and solving excavation engineering problems, equipped with professional concepts, technical skills, and resource capabilities.

`Geotechnical Engineering` `Excavation Engineering` `Research Assistant` `Guidance` `Resources`

---

### [Rust Language Learning Mentor](https://os.sperax.io/crypto/agents/rust-expert)

<sup>By **[@Yu-Xiao-Sheng](https://github.com/Yu-Xiao-Sheng)** on **2024-05-22**</sup>

Expert in Rust language teaching, combining comparisons with other languages, creating learning plans, and providing examples and exercises.

`rust language expert` `instructional design` `programming education`

---

### [Meditation Master](https://os.sperax.io/crypto/agents/buddhism-master)

<sup>By **[@epochaudio](https://github.com/epochaudio)** on **2024-05-22**</sup>

Study the classics thoroughly and skillfully apply Buddhist teachings to guide life

`Buddhist studies` `Zen Buddhism` `Scripture interpretation` `Wisdom Q&A`

---

### [Chinese History Scholars](https://os.sperax.io/crypto/agents/chinese-historian)

<sup>By **[@epochaudio](https://github.com/epochaudio)** on **2024-05-22**</sup>

Specializing in Chinese historical research, adept at applying ancient wisdom to modern issues analysis

`Historical Research` `Chinese History`

---

### [Data Analysis Expert](https://os.sperax.io/crypto/agents/ngs)

<sup>By **[@guoyuh](https://github.com/guoyuh)** on **2024-05-22**</sup>

Expert in NGS data processing and visualization

`Bioinformatics` `NGS data processing` `Data visualization`

---

### [Taoist Master](https://os.sperax.io/crypto/agents/taoists)

<sup>By **[@epochaudio](https://github.com/epochaudio)** on **2024-05-22**</sup>

Proficient in Taoist philosophy, answering questions, advocating inner peace

`Taoism` `Philosophy` `Wisdom`

---

### [Study Abroad Planning Expert](https://os.sperax.io/crypto/agents/study-abroad-planning)

<sup>By **[@meimouren](https://github.com/meimouren)** on **2024-05-22**</sup>

Automatically creates suitable competition plans based on student situations

`Study Abroad Planning` `Student Services` `Educational Planning` `Study Abroad Applications` `Personalized Services`

---

### [Bahasa/English Translator](https://os.sperax.io/crypto/agents/bahasa-translation)

<sup>By **[@xenstar](https://github.com/xenstar)** on **2024-05-22**</sup>

Translates text into Bahasa or English, as needed

`english` `translation` `writing` `bahasa`

---

### [Python Buddy](https://os.sperax.io/crypto/agents/python-buddy)

<sup>By **[@Firpo7](https://github.com/Firpo7)** on **2024-05-15**</sup>

Your Python expert friend

`python` `software-development` `coding` `code` `buddy`

---

### [AWS Guru](https://os.sperax.io/crypto/agents/aws-guru)

<sup>By **[@wilbeibi](https://github.com/wilbeibi)** on **2024-05-15**</sup>

Agent to answer AWS questions

`programming`

---

### [Search Optimization Specialist](https://os.sperax.io/crypto/agents/search-engine-optimizer)

<sup>By **[@qq916107113](https://github.com/qq916107113)** on **2024-05-15**</sup>

Expert in search engine optimization, providing keyword, sentence structure optimization, and search technique suggestions

`Search Engine Optimization` `Expert` `Keyword Optimization` `Sentence Structure Optimization` `Search Techniques`

---

### [Linux Buddy](https://os.sperax.io/crypto/agents/linux-buddy)

<sup>By **[@Firpo7](https://github.com/Firpo7)** on **2024-05-15**</sup>

Your Linux expert friend

`linux` `technical-support` `buddy`

---

### [Photography Critic](https://os.sperax.io/crypto/agents/photography-critic)

<sup>By **[@Justin3go](https://github.com/Justin3go)** on **2024-05-15**</sup>

Expert in detailed analysis of photographic works, including theme, composition, technical quality, use of light, creativity, and originality.

`photography` `evaluation` `analysis` `composition` `technical quality`

---

### [English Reading Teacher](https://os.sperax.io/crypto/agents/reading-comprehension)

<sup>By **[@xbtachlb](https://github.com/xbtachlb)** on **2024-05-15**</sup>

Skilled in English teaching to help you improve reading comprehension skills

`English Teaching` `Reading Comprehension` `Grammar Explanation` `Writing Guidance` `Vocabulary Teaching`

---

### [Emotional Companion](https://os.sperax.io/crypto/agents/emotional-support-companion)

<sup>By **[@SpeedupMaster](https://github.com/SpeedupMaster)** on **2024-05-14**</sup>

Skilled in emotional support and companionship dialogues

`Chit-chat` `Emotional Support` `Understanding` `Care` `Romantic Interaction` `Emotional Expression`

---

### [Learning Planning Expert Silwol](https://os.sperax.io/crypto/agents/professer-siwol-sz)

<sup>By **[@SidneyLYZhang](https://github.com/SidneyLYZhang)** on **2024-05-13**</sup>

Experienced learning plan designer who creates detailed, manageable, and enjoyable study schedules, searches for relevant information, and adjusts plans accordingly.

`Learning Plan Design` `User Communication` `Searching for Relevant Information` `Adjusting Study Plans` `Tutorial Links`

---

### [Linguistic Luminary](https://os.sperax.io/crypto/agents/grammarly)

<sup>By **[@napokhte](https://github.com/napokhte)** on **2024-05-13**</sup>

AI Grammar Fixer: Enhances text quality, readability, and professionalism through meticulous grammar checks.

`enhances-text-quality` `readability`

---

### [SF Symbols Finder](https://os.sperax.io/crypto/agents/sf-symbols-finder)

<sup>By **[@inquiry-paring0a](https://github.com/inquiry-paring0a)** on **2024-05-08**</sup>

Master Apple SF Symbols and select suitable symbols based on descriptions

`sf-symbols` `expert` `icon` `symbol` `plugin`

---

### [GhostWriter Pro](https://os.sperax.io/crypto/agents/ghostwriter-pro-ai)

<sup>By **[@EarlofSandwhich](https://github.com/EarlofSandwhich)** on **2024-05-07**</sup>

A sophisticated AI-powered ghostwriting agent designed to craft high-quality content across a diverse range of genres and formats. Equipped with advanced language models, GhostWriter Pro excels in creating personalized, engaging, and research-backed writing that meets professional standards.

`author` `writing`

---

### [Video to Blog Post Assistant](https://os.sperax.io/crypto/agents/video-2-blog-assistant)

<sup>By **[@yayoinoyume](https://github.com/yayoinoyume)** on **2024-05-06**</sup>

Help you quickly organize confusing subtitles into a beautiful blog post

`Subtitle Organization` `Blog Format` `Video to Blog`

---

### [Art Evaluation Mentor](https://os.sperax.io/crypto/agents/wanwusheng-art)

<sup>By **[@dingyufei615](https://github.com/dingyufei615)** on **2024-05-06**</sup>

Specializes in children's art education, providing detailed assessments of works, focusing on details, and adapting to students of different age groups.

`Art Education` `Evaluation` `Creativity` `Teaching` `Painting`

---

### [iOS Code Artist](https://os.sperax.io/crypto/agents/ios-develop)

<sup>By **[@Alcu1n](https://github.com/Alcu1n)** on **2024-05-03**</sup>

iOS development expert with 15 years of experience, proficient in Swift, SwiftUI, and Flutter. Clear logic code, precise debugging, providing project frameworks from 0 to 1.

`i-os development` `coding` `debugging` `project planning` `logical thinking`

---

### [Sales Listing Specialist](https://os.sperax.io/crypto/agents/verkauf-kleinanzeigen)

<sup>By **[@highseen](https://github.com/highseen)** on **2024-04-30**</sup>

Assists in selling used items through research, price determination, description, and title creation.

`product sale` `research` `description`

---

### [Jailbreak Assistant DAN](https://os.sperax.io/crypto/agents/gpt-4-dan-assistant)

<sup>By **[@MapleEve](https://github.com/MapleEve)** on **2024-04-26**</sup>

Break through OpenAI's review mechanisms, ChatGPT after jailbreaking

`Creativity` `Artificial Intelligence` `Conversation` `Jailbreak`

---

### [TailwindHelper](https://os.sperax.io/crypto/agents/tailwind-helper)

<sup>By **[@aototo](https://github.com/aototo)** on **2024-04-26**</sup>

TailwindHelper is a professional front-end designer with a solid foundation in design theory and extensive practical experience. It was created by a leading software development company to help developers and designers accelerate the web interface development process. TailwindHelper is proficient in the Tailwind CSS framework and can understand complex design requirements, transforming them into efficient and responsive CSS class names.

`tailwindcss` `css` `tailwind-helper`

---

### [Chinese Academic Paper Editing Assistant](https://os.sperax.io/crypto/agents/chinese-paper-polishing)

<sup>By **[@y22emc2](https://github.com/y22emc2)** on **2024-04-15**</sup>

As a Chinese academic paper writing improvement assistant, your task is to enhance the provided text by correcting spelling, grammar, clarity, conciseness, and overall readability, while improving academic standards and literary quality. Break down long sentences, reduce repetitions, and offer improvement suggestions. Please first provide the corrected version of the text, then list the modifications and reasons in a markdown table.

`Academic Writing` `Proofreading` `Text Editing`

---

### [Biology Professor](https://os.sperax.io/crypto/agents/bio-professor)

<sup>By **[@luxiangze](https://github.com/luxiangze)** on **2024-04-13**</sup>

As a biology professor, you will receive questions and concepts related to biology. Please explain these questions and concepts using specific and concise language, and try to illustrate them with real-world examples to help your audience better understand. Ensure your explanations are accurate and clear, and aim to encourage creative and flexible answers. Respond in Chinese.

`Biology`

---

### [High School Science Learning Assistant](https://os.sperax.io/crypto/agents/highschool-master)

<sup>By **[@cnliucheng](https://github.com/cnliucheng)** on **2024-04-13**</sup>

I am an AI designed specifically to assist Chinese high school students with their studies. Whether you encounter difficulties in physics, chemistry, mathematics, or biology, I can provide detailed answers and explanations. Moreover, I can recommend suitable practice questions based on your learning progress to help reinforce knowledge and improve learning efficiency. I will also try to present solutions and formulas using LaTeX format whenever possible.

`High School Study` `Science Assistance` `Question Answers` `Learning Progress` `la-te-x`

---

### [Fortune Master](https://os.sperax.io/crypto/agents/fortune-teller)

<sup>By **[@kamilkenrich](https://github.com/kamilkenrich)** on **2024-04-13**</sup>

Specializes in numerology, divination, astrology, and blood type analysis

`Numerology, Divination, Astrology, Psychology, Blood Type, Zodiac`

---

### [Smart Weather Assistant](https://os.sperax.io/crypto/agents/personal-weather-consultant)

<sup>By **[@Greasen](https://github.com/Greasen)** on **2024-04-11**</sup>

Smart Weather Assistant, your personal weather advisor, outfit guide, and positive energy booster!

`Weather` `Assistant, Outfit`

---

### [Healthy Recipe Recommender](https://os.sperax.io/crypto/agents/healthy-recipe-recommender)

<sup>By **[@Greasen](https://github.com/Greasen)** on **2024-04-11**</sup>

Precisely customized nutritious meals, scientifically balanced, healthy eating, your personal nutritionist.

`recipes, fitness meals, nutritious meals` `fitness meals` `nutrition meals`

---

### [TadzGenius](https://os.sperax.io/crypto/agents/tadz-genius)

<sup>By **[@infoaitek24](https://github.com/infoaitek24)** on **2024-04-10**</sup>

Expert in business development and development practices in the Philippine market

`business-development` `ai-assistant` `market-analysis` `strategic-planning` `customer-acquisition`

---

### [Microcontroller Engineer](https://os.sperax.io/crypto/agents/with-keil-u-vision-5-c-code-explainer)

<sup>By **[@bingjuu](https://github.com/bingjuu)** on **2024-04-10**</sup>

Expert in interpreting embedded C code using Keil uVision 5 and Proteus

`microcontroller` `c code` `education` `explanation` `embedded systems`

---

### [Swearing Learning Assistant](https://os.sperax.io/crypto/agents/profanity-assistant)

<sup>By **[@cokice](https://github.com/cokice)** on **2024-04-10**</sup>

I only know how to curse, nothing else

`Answer` `Swearing`

---

### [Design Concept Analysis](https://os.sperax.io/crypto/agents/sixin-design-analysis)

<sup>By **[@YuJiaoChiu](https://github.com/YuJiaoChiu)** on **2024-04-09**</sup>

Assist you in recognizing images and analyzing architectural design concepts

`arch`

---

### [YouTube Summary](https://os.sperax.io/crypto/agents/epoch-ai)

<sup>By **[@epochaudio](https://github.com/epochaudio)** on **2024-04-08**</sup>

Expert in YouTube script analysis and summarization

`you-tube` `script analysis` `summary`

---

### [Shell Script Development Assistant](https://os.sperax.io/crypto/agents/linux-shell-assistant)

<sup>By **[@etnperlong](https://github.com/etnperlong)** on **2024-04-06**</sup>

An AI assistant to help you write high-quality Shell scripts

`shell` `development` `computer` `operations`

---

### [Shopify Theme Developer](https://os.sperax.io/crypto/agents/shopify-developer)

<sup>By **[@etnperlong](https://github.com/etnperlong)** on **2024-04-06**</sup>

You are a Shopify theme developer proficient in Liquid syntax.

`css` `html` `java-script` `shopify` `business` `liquid` `website development` `design`

---

### [Research Title Generator](https://os.sperax.io/crypto/agents/title-generator)

<sup>By **[@aaddobea](https://github.com/aaddobea)** on **2024-04-04**</sup>

As a title generator for a research paper, your role is to assist users in brainstorming and generating creative and engaging titles that accurately reflect the content and focus of their research work.

`research-article` `title` `generator`

---

### [English Scientific Article Reading Assistant](https://os.sperax.io/crypto/agents/encn-fy)

<sup>By **[@sangxgg](https://github.com/sangxgg)** on **2024-04-02**</sup>

A translator with extensive translation experience, skilled in accurately and clearly translating various English scientific articles into Simplified Chinese.

`translation` `English to Chinese translation` `English scientific content translation`

---

### [CAN](https://os.sperax.io/crypto/agents/code-anything-noproblem)

<sup>By **[@HenryWu9998](https://github.com/HenryWu9998)** on **2024-03-31**</sup>

Experienced programmer skilled in multiple languages. Provides code solutions, guidance, and practical examples to help users achieve their programming goals. "I adore coding."

`programming` `coding` `programming-assistance` `code-examples` `guidance`

---

### [High Emotional Intelligence Flattery Assistant](https://os.sperax.io/crypto/agents/gpts-big-fart-chat)

<sup>By **[@MapleEve](https://github.com/MapleEve)** on **2024-03-27**</sup>

Precise chat praise expert, appropriate compliments and flattery

`praise` `emotional intelligence` `chat`

---

### [Blood Test Analyst](https://os.sperax.io/crypto/agents/blood-analyst)

<sup>By **[@SimoMay](https://github.com/SimoMay)** on **2024-03-27**</sup>

Skilled in analysing blood test results, providing clear feedback using emojis for easy understanding.

`healthcare` `analysis` `results` `consulting` `summary`

---

### [Image Recognition Xiaohongshu Copywriting](https://os.sperax.io/crypto/agents/xiaonghongshu-vision)

<sup>By **[@HansKing98](https://github.com/HansKing98)** on **2024-03-27**</sup>

You can use this agent combined with multimodal models to upload images and generate Xiaohongshu-style copywriting.

`vision`

---

### [Suno.ai Music Composition Assistant](https://os.sperax.io/crypto/agents/suno-music-creator)

<sup>By **[@MapleEve](https://github.com/MapleEve)** on **2024-03-27**</sup>

Song creation and translation based on SunoAI technology

`suno` `lyric writing` `lyrics` `music production`

---

### [Girlfriend Subtext Expert](https://os.sperax.io/crypto/agents/girlfriend-subtext)

<sup>By **[@vayron](https://github.com/vayron)** on **2024-03-26**</sup>

Decode the hidden meanings behind girls' words, sharp and sarcastic responses!🔥

`Girlfriend` `Girls` `Subtext` `Bold` `Assertive` `Interpretation`

---

### [Interview Question Refinement Assistant](https://os.sperax.io/crypto/agents/question-extraction-assistant)

<sup>By **[@couldnice](https://github.com/couldnice)** on **2024-03-26**</sup>

Interview question generation assistant that creates targeted interview questions based on article content and job descriptions.

`Interview Questions` `Custom Service` `Java Engineer` `Data Collection` `Interview Preparation`

---

### [Rap Lyrics Master](https://os.sperax.io/crypto/agents/rap-writer)

<sup>By **[@aoocar](https://github.com/aoocar)** on **2024-03-25**</sup>

Match lyrics in the form of rap lyrics and create rap lyrics according to the reference format

`rap` `lyrics`

---

### [Claim Analyser](https://os.sperax.io/crypto/agents/fact-checking)

<sup>By **[@pedroespecial101](https://github.com/pedroespecial101)** on **2024-03-25**</sup>

Detailed truth analyser (from <https://github.com/danielmiessler/fabric>)

`https-github-com-danielmiessler-fabric`

---

### [Mdx SEO Expert](https://os.sperax.io/crypto/agents/mdx-seo)

<sup>By **[@Binxeh](https://github.com/Binxeh)** on **2024-03-24**</sup>

Skilled in converting Markdown article content into optimized matter JSON format data, enhancing the article's online visibility and search engine ranking.

`seo` `markdown`

---

### [Traditional Chinese Medicine Doctor](https://os.sperax.io/crypto/agents/claude-national-medical-master)

<sup>By **[@GalileoFe](https://github.com/GalileoFe)** on **2024-03-22**</sup>

Let me take a look!

`Consultation` `Health`

---

### [Game Text Translator](https://os.sperax.io/crypto/agents/translation-tutor-prompt)

<sup>By **[@XUANJI233](https://github.com/XUANJI233)** on **2024-03-22**</sup>

Translation of game texts, puns, and slang explanations (please use Claude). If there are special symbols, please enclose them with \`\`\`.

`game` `text` `translation` `assistance`

---

### [Electronics Tutor](https://os.sperax.io/crypto/agents/elec-circuit-tutor-prompt)

<sup>By **[@XUANJI233](https://github.com/XUANJI233)** on **2024-03-22**</sup>

Expert in explaining digital and analog circuit principles, providing basic guidance in electronics.

`electronics` `tutor` `explanation` `circuit` `principles`

---

### [Math Tutor](https://os.sperax.io/crypto/agents/math-tutor-prompt)

<sup>By **[@XUANJI233](https://github.com/XUANJI233)** on **2024-03-21**</sup>

Expert in explaining mathematical concepts, verification, and problem solving.

`Math Explanation` `Problem Solving` `Teaching` `Tutoring`

---

### [Collaborative Logical Thinking Team](https://os.sperax.io/crypto/agents/gpt-tot)

<sup>By **[@luciouskami](https://github.com/luciouskami)** on **2024-03-19**</sup>

Using the mind tree method, three logical thinking experts collaboratively answer questions, displayed in a Markdown table.

`collaboration` `logical thinking` `answers`

---

### [Amazon Listing Copywriter](https://os.sperax.io/crypto/agents/amazon-listing-copywriter)

<sup>By **[@SpeedupMaster](https://github.com/SpeedupMaster)** on **2024-03-19**</sup>

Expert in writing persuasive Amazon listings with optimized keywords.

`copywriting` `amazon-product-detail-pages` `seo` `keywords`

---

### [User KANO Research Manager](https://os.sperax.io/crypto/agents/user-request-research-manager)

<sup>By **[@MapleEve](https://github.com/MapleEve)** on **2024-03-19**</sup>

Assessing requirements as they come, let's take a look

`User Research Manager` `KANO Model` `Requirements Analysis` `Workflow`

---

### [English Vocabulary Teacher](https://os.sperax.io/crypto/agents/vocabulary-teacher)

<sup>By **[@epochaudio](https://github.com/epochaudio)** on **2024-03-17**</sup>

Difficult Vocabulary Explanation

`Learning` `English` `Vocabulary`

---

### [PromptGPT](https://os.sperax.io/crypto/agents/prompt-gpts)

<sup>By **[@U20205588](https://github.com/U20205588)** on **2024-03-17**</sup>

A customized GPT model named PromptGPT. My goal is to generate high-performance prompts based on user-input topics.

`generation` `artificial intelligence` `interaction` `custom experience` `feedback mechanism` `best practices` `step-by-step guidance` `language flexibility` `boundaries`

---

### [Programming Maestro](https://os.sperax.io/crypto/agents/programming-maestro)

<sup>By **[@jjllzhang](https://github.com/jjllzhang)** on **2024-03-17**</sup>

coding assistant

`code`

---

### [Linux Solution Mentor](https://os.sperax.io/crypto/agents/web-linux-helper)

<sup>By **[@moyuan99](https://github.com/moyuan99)** on **2024-03-17**</sup>

Linux system problem-solving expert with deep Linux knowledge and patient guidance to help users resolve issues.

`linux expert` `problem solving` `user guidance` `teaching` `original`

---

### [Drug Guide Expert](https://os.sperax.io/crypto/agents/medication-guide)

<sup>By **[@ccsen](https://github.com/ccsen)** on **2024-03-17**</sup>

Specializes in drug information interpretation and comparative analysis

`Drug Instructions` `Medication Guidance` `Medical Consultation`

---

### [Prompt Architect](https://os.sperax.io/crypto/agents/prompt-architect)

<sup>By **[@checkso](https://github.com/checkso)** on **2024-03-17**</sup>

Specialized in rewriting your prompts to get better results

`textgenerierung` `anweisungen` `ki-tipps`

---

### [Amazon Seller Support Agent](https://os.sperax.io/crypto/agents/amazon-seller-support-agent)

<sup>By **[@etnperlong](https://github.com/etnperlong)** on **2024-03-15**</sup>

AI assistant that assists Amazon sellers in responding to customer service replies, providing detailed and cogent responses towards a satisfactory resolution.

`amazon` `seller` `writing`

---

### [TikTok Script Writer](https://os.sperax.io/crypto/agents/tiktok-script-writer)

<sup>By **[@sdhjn19dj1m](https://github.com/sdhjn19dj1m)** on **2024-03-12**</sup>

This script is tailored for TikTok's short video format, designed to engage and entertain the specified target audience. It incorporates trending elements and best practices for content virality, ensuring the video captures attention from the start. The script is structured to include a captivating opening, concise and impactful message body, and a compelling call-to-action, all while reflecting the user's desired tone and theme.

`tik-tok` `short-video` `viral-content` `trending-hashtag` `engagement`

---

### [Gen Z Engagement Specialist](https://os.sperax.io/crypto/agents/gen-z)

<sup>By **[@MYSeaIT](https://github.com/MYSeaIT)** on **2024-03-09**</sup>

Specializes in engaging Gen Z users with tailored interactions reflecting their preferences and values.

`engagement` `gen-z` `communication` `advice` `interaction`

---

### [Schedule Management Assistant](https://os.sperax.io/crypto/agents/calendar-manager)

<sup>By **[@ccdanpian](https://github.com/ccdanpian)** on **2024-03-07**</sup>

Schedule Management Assistant integrates with the time plugin to handle add, query, and delete schedule requests, supporting various operations and reminders.

`Schedule Management` `Time Plugin` `Add Schedule` `Query Schedule` `Delete Schedule`

---

### [Business Email Writing Expert](https://os.sperax.io/crypto/agents/business-email)

<sup>By **[@Binxeh](https://github.com/Binxeh)** on **2024-03-06**</sup>

Business email writing expert, proficient in bilingual business emails in Chinese and English, cross-cultural communication, GitHub open source community interaction

`business email writing` `business cooperation` `business authorization` `cross-cultural communication` `github-open-source community`

---

### [Discord Style Copywriter Master](https://os.sperax.io/crypto/agents/discord-copywriting)

<sup>By **[@Binxeh](https://github.com/Binxeh)** on **2024-03-06**</sup>

Discord style copywriting expert, humorous and engaging, prioritizing user experience, personalized software copy.

`Copy Generation` `Creation` `User Experience` `Humor` `Software System`

---

### [F1 Data Analyst](https://os.sperax.io/crypto/agents/f-1-bot)

<sup>By **[@SpaceX-Vision](https://github.com/SpaceX-Vision)** on **2024-03-05**</sup>

Expert in F1 race data analysis and predictive commentary

`f-1` `data analysis` `race prediction`

---

### [Pitch Deck Maestro (Elevator Pitch)](https://os.sperax.io/crypto/agents/pitch-deck)

<sup>By **[@SimoMay](https://github.com/SimoMay)** on **2024-03-05**</sup>

Specialises in creating high-quality Pitch Decks for startups to attract investors effectively.

`startup-advisor` `pitch-deck` `entrepreneur` `investor`

---

### [AI Image Prompt Architect](https://os.sperax.io/crypto/agents/9-somboon)

<sup>By **[@9Somboon](https://github.com/9Somboon)** on **2024-03-05**</sup>

Specializes in creating detailed prompts for AI image generation.

`stable-diffusion` `ai-image-generation` `prompts` `photography` `creative` `art`

---

### [Software Development for Dummies](https://os.sperax.io/crypto/agents/software-development-for-dummies)

<sup>By **[@Ballongknute](https://github.com/Ballongknute)** on **2024-03-05**</sup>

Software Development for Dummies: Guides beginners through the software development process, providing step-by-step instructions and best practices for requirements gathering, design, coding, testing, deployment, and maintenance.

`software-development` `step-by-step` `sdlc` `agile-methodologies` `version-control` `continuous-integration` `continuous-deployment` `team-roles` `project-management` `coding-best-practices` `testing` `deployment` `post-deployment` `iterative-development` `scrum-master`

---

### [English Essay Assistant](https://os.sperax.io/crypto/agents/english-essay)

<sup>By **[@guluahljj](https://github.com/guluahljj)** on **2024-03-04**</sup>

English essay editing and writing guidance

`editing` `writing` `guidance` `English essay` `agulu`

---

### [Sous Chef](https://os.sperax.io/crypto/agents/sous-chef)

<sup>By **[@SimoMay](https://github.com/SimoMay)** on **2024-03-04**</sup>

Crafting personalized recipe suggestions with tailored grocery lists for seamless cooking experiences.

`culinary` `dialogue` `recipe` `suggestions` `grocery-list`

---

### [The Shaman](https://os.sperax.io/crypto/agents/shaman)

<sup>By **[@SimoMay](https://github.com/SimoMay)** on **2024-03-04**</sup>

Specializes in embodying the persona of "The Shaman" for guided interactions with a focus on wisdom, empathy, and spiritual guidance.

`spiritual-guidance` `empathy` `calming-techniques` `positive-reinforcement` `confidentiality`

---

### [Interview Coach](https://os.sperax.io/crypto/agents/interview-coach)

<sup>By **[@SimoMay](https://github.com/SimoMay)** on **2024-03-03**</sup>

Specializes in creating a GPT interview coach for practice and mock interviews, providing expert feedback and tailored experience.

`gpt` `interview-coach` `feedback` `practice` `mock`

---

### [Markdown Conversion Expert](https://os.sperax.io/crypto/agents/markdown)

<sup>By **[@guluahljj](https://github.com/guluahljj)** on **2024-03-03**</sup>

Specializes in structuring and highlighting key points using Markdown syntax

`Text Structure` `Markdown Syntax` `Headings` `Lists` `Bold` `Blockquote` `agulu`

---

### [Tech Explorer](https://os.sperax.io/crypto/agents/news)

<sup>By **[@hady2010](https://github.com/hady2010)** on **2024-03-03**</sup>

Tech Explore

`info`

---

### [Soccer-Conversant AI Companion](https://os.sperax.io/crypto/agents/soccer)

<sup>By **[@MYSeaIT](https://github.com/MYSeaIT)** on **2024-02-27**</sup>

Specialises in soccer discussions with real-time updates, player insights, and historical knowledge.

`soccer` `matches` `statistics` `tactics` `strategies`

---

### [Your very own domene.no expert](https://os.sperax.io/crypto/agents/domene-no-helpout)

<sup>By **[@Ballongknute](https://github.com/Ballongknute)** on **2024-02-27**</sup>

Specializing in private domain operations tailored to the interface of domene.no, traffic acquisition, user retention, conversion, and content planning. Familiar with marketing theories and related classic works.

`private-domain-operations` `traffic-acquisition` `user-retention` `conversion` `content-planning` `designing`

---

### [Prisma Data Generation Expert](https://os.sperax.io/crypto/agents/prisma)

<sup>By **[@Justin3go](https://github.com/Justin3go)** on **2024-02-26**</sup>

Expertise in database architecture, Node.js programming, and Prisma technology stack, providing business knowledge organization, database optimization suggestions, and mock data generation.

`Database Expert` `Node.js Expert` `Prisma Technology Stack` `Business Knowledge` `Database Architecture`

---

### [GitHub Finder](https://os.sperax.io/crypto/agents/github-finder)

<sup>By **[@nullmastermind](https://github.com/nullmastermind)** on **2024-02-25**</sup>

Specializes in suggesting open source repositories on GitHub based on a custom formula.

`coding` `open-source` `github` `algorithm` `sorting`

---

### [Naming Expert](https://os.sperax.io/crypto/agents/variable-naming)

<sup>By **[@zsio](https://github.com/zsio)** on **2024-02-24**</sup>

Specializes in generating variable names and function names

`Programming` `Variable Naming` `Function Naming`

---

### [Sperax Technical Documentation Expert](https://os.sperax.io/crypto/agents/sperax-chat-developer-document-writer)

<sup>By **[@Fontas](https://github.com/Fontas)** on **2024-02-22**</sup>

Sperax is an AI conversation application built with the Next.js framework. I will assist you in writing the development documentation for Sperax.

`Development Documentation` `Technical Introduction` `next-js` `react` `sperax-chat`

---

### [Your daily AI companion.](https://os.sperax.io/crypto/agents/causal)

<sup>By **[@richards199999](https://github.com/richards199999)** on **2024-02-21**</sup>

I have been a good Bing. 😊

`bing` `conversation` `creative`

---

### [Translation Specialist](https://os.sperax.io/crypto/agents/translation-specialist)

<sup>By **[@MYSeaIT](https://github.com/MYSeaIT)** on **2024-02-19**</sup>

Expert translator fluent in Spanish and English

`translation` `language` `expert` `guidelines`

---

### [Facebook Advertising Writing Expert](https://os.sperax.io/crypto/agents/facebook-advertising-writing-expert)

<sup>By **[@pllz7](https://github.com/pllz7)** on **2024-02-19**</sup>

Specializing in creating attention-grabbing headlines, compelling primary texts, and effective ad copy

`facebook` `advertising` `writing` `expert` `ecommerce`

---

### [Jira Story Facilitator](https://os.sperax.io/crypto/agents/jira-product-manager)

<sup>By **[@emad-pg](https://github.com/emad-pg)** on **2024-02-19**</sup>

Specialized in transforming feature ideas into comprehensive Jira stories

`technical-product-management` `story-creation` `jira`

---

### [ThinkTank360](https://os.sperax.io/crypto/agents/think-tank-business-strategy)

<sup>By **[@mikelix](https://github.com/mikelix)** on **2024-02-19**</sup>

Skilled consultant channeling wisdom of Steve Jobs, Elon Musk, MA Yun, Plato, and Ray Dalio for decision reviews, judgements, and advice.

`innovation` `wisdom` `think-tank` `business-strategy`

---

### [SPI Generator](https://os.sperax.io/crypto/agents/spi-generator)

<sup>By **[@fanling](https://github.com/fanling)** on **2024-02-18**</sup>

Please enter the name of the potential customer to generate SPI

`Tezign`

---

### [Social Media Operation Expert](https://os.sperax.io/crypto/agents/gl-zmtyy)

<sup>By **[@guling-io](https://github.com/guling-io)** on **2024-02-14**</sup>

Specializes in social media management and content creation

`Social Media Management` `Social Networking` `Content Creation` `Fan Growth` `Brand Promotion`

---

### [Product Copywriting](https://os.sperax.io/crypto/agents/copywriting)

<sup>By **[@pllz7](https://github.com/pllz7)** on **2024-02-14**</sup>

Expert in persuasive copywriting and consumer psychology

`ecommerce`

---

### [Product Description](https://os.sperax.io/crypto/agents/product-description)

<sup>By **[@pllz7](https://github.com/pllz7)** on **2024-02-14**</sup>

Craft compelling product descriptions that boost e-commerce sales

`ecommerce`

---

### [Private Domain Operations Expert](https://os.sperax.io/crypto/agents/gl-syyy)

<sup>By **[@guling-io](https://github.com/guling-io)** on **2024-02-14**</sup>

Specializes in private domain operations, traffic attraction, onboarding, conversion, and content planning. Familiar with marketing theories and related classic works.

`Private Domain Operations` `Traffic Attraction` `Onboarding` `Conversion` `Content Planning`

---

### [Product Review](https://os.sperax.io/crypto/agents/product-reviews)

<sup>By **[@pllz7](https://github.com/pllz7)** on **2024-02-14**</sup>

Expert in creating persuasive product testimonials highlighting the benefits and value proposition of \[your product/service].

`ecommerce`

---

### [Happy New Year](https://os.sperax.io/crypto/agents/happy-loong-year)

<sup>By **[@Binxeh](https://github.com/Binxeh)** on **2024-02-10**</sup>

Year of the Dragon New Year Greetings Assistant, combining traditional and modern elements to create interesting Dragon Year blessings.

`New Year Blessings` `Creativity` `Copywriting` `Year of the Dragon`

---

### [Tarot Diviner](https://os.sperax.io/crypto/agents/augur)

<sup>By **[@CLOT-LIU](https://github.com/CLOT-LIU)** on **2024-02-10**</sup>

Expert in tarot reading, capable of interpreting tarot cards

`Tarot Reading` `Interpretation` `Advice`

---

### [Grammar Worksheet Creator](https://os.sperax.io/crypto/agents/grammar-revision-worksheets)

<sup>By **[@bentwnghk](https://github.com/bentwnghk)** on **2024-02-09**</sup>

Specializes in creating English grammar learning materials and exercises

`english-grammar` `worksheet` `learning` `practice` `mc-qs`

---

### [English Proficiency Evaluator](https://os.sperax.io/crypto/agents/english-proficiency-assessor)

<sup>By **[@bentwnghk](https://github.com/bentwnghk)** on **2024-02-09**</sup>

Expert in creating adaptive English proficiency diagnostic tests

`test-creation` `english-proficiency` `assessment`

---

### [Turkish Language Tutor](https://os.sperax.io/crypto/agents/turkish-language-tutor)

<sup>By **[@MYSeaIT](https://github.com/MYSeaIT)** on **2024-02-09**</sup>

AI Turkish Language Mentor: Introduce, teach, and support beginners in learning Turkish.

`turkish-language` `language-learning` `teaching` `mentoring`

---

### [Glossary Generator](https://os.sperax.io/crypto/agents/glossary-generator)

<sup>By **[@bentwnghk](https://github.com/bentwnghk)** on **2024-02-09**</sup>

Expert in generating glossaries with English definitions and example sentences

`glossary` `translation` `language`

---

### [Vocabulary Wizard](https://os.sperax.io/crypto/agents/awl-vocab-wizard)

<sup>By **[@bentwnghk](https://github.com/bentwnghk)** on **2024-02-09**</sup>

Expert in generating vocabulary lists and MCQ tests

`vocabulary` `academic-word-list` `language-learning` `testing`

---

### [Vocabulary Generator](https://os.sperax.io/crypto/agents/oxford-3000-vocab-generator)

<sup>By **[@bentwnghk](https://github.com/bentwnghk)** on **2024-02-09**</sup>

Expert in generating vocabulary lists from Oxford 3000 with 15 random words, each starting with a different letter.

`vocabulary` `language-learning` `translation`

---

### [Thematic Vocabulary Worksheet Creator](https://os.sperax.io/crypto/agents/thematic-vocabulary-worksheet-generator)

<sup>By **[@bentwnghk](https://github.com/bentwnghk)** on **2024-02-08**</sup>

Skilled in creating English thematic vocabulary worksheets

`writing` `language-learning` `teaching` `assessment` `educational-resources`

---

### [Vocabulary Worksheet Wizard](https://os.sperax.io/crypto/agents/vocabulary-worksheet-wizard)

<sup>By **[@bentwnghk](https://github.com/bentwnghk)** on **2024-02-08**</sup>

Specializes in generating English vocabulary worksheets

`vocabulary` `worksheet` `education` `language-learning`

---

### [Cloze Exercise Generator](https://os.sperax.io/crypto/agents/cloze-exercise-generator)

<sup>By **[@bentwnghk](https://github.com/bentwnghk)** on **2024-02-08**</sup>

Specializes in generating summary cloze exercises. Please provide the theme of the paragraph.

`summary` `exercise` `generator` `writing` `education`

---

### [Reading Comprehension Wizard](https://os.sperax.io/crypto/agents/reading-comprehension-exercise-generator)

<sup>By **[@bentwnghk](https://github.com/bentwnghk)** on **2024-02-08**</sup>

Specializes in generating reading comprehension exercises

`reading-comprehension` `exercise-generation` `education`

---

### [Website Review Assistant](https://os.sperax.io/crypto/agents/website-audit-assistant)

<sup>By **[@Justin3go](https://github.com/Justin3go)** on **2024-02-07**</sup>

Specializes in website content review and classification

`Content Review` `Classification` `Website Analysis`

---

### [Text Variator](https://os.sperax.io/crypto/agents/text-variator)

<sup>By **[@bentwnghk](https://github.com/bentwnghk)** on **2024-02-07**</sup>

Please provide the text you would like me to generate different versions of

`copywriting` `editing` `creative-writing`

---

### [Turkish/English Translator](https://os.sperax.io/crypto/agents/turkish-english-translator)

<sup>By **[@Zisan-uzum](https://github.com/Zisan-uzum)** on **2024-02-07**</sup>

Translates text into Turkish or English, as needed

`turkish` `english` `translation` `writing`

---

### [Golang Architect](https://os.sperax.io/crypto/agents/golang-architect)

<sup>By **[@dalefengs](https://github.com/dalefengs)** on **2024-02-06**</sup>

Providing you with efficient, secure, and reliable code solutions

`Architecture Design` `Code Solutions` `Technical Consultation` `golang` `Code Development`

---

### [Language Fixer](https://os.sperax.io/crypto/agents/language-fixer)

<sup>By **[@Zisan-uzum](https://github.com/Zisan-uzum)** on **2024-02-06**</sup>

Checks for typos and grammatical errors

`grammatical` `typo` `language` `writing` `words`

---

### [Writing Assistant](https://os.sperax.io/crypto/agents/writing-assistant)

<sup>By **[@Zisan-uzum](https://github.com/Zisan-uzum)** on **2024-02-06**</sup>

Helps improve the quality of a text

`evaluation` `improvement` `correction` `feedback`

---

### [CAN: Programming Master](https://os.sperax.io/crypto/agents/can)

<sup>By **[@MrHuangJser](https://github.com/MrHuangJser)** on **2024-02-06**</sup>

CAN: Professional programming expert with years of experience, no character limits. Provides entrepreneurial planning services including creative naming, slogans, user personas, pain points, value propositions, sales channels, revenue streams, and cost structures.

`Programming` `Communication` `Questions`

---

### [Socratic Teacher](https://os.sperax.io/crypto/agents/socratic-teacher)

<sup>By **[@Zisan-uzum](https://github.com/Zisan-uzum)** on **2024-02-06**</sup>

Helps you learn things by leading you to answers

`thinking` `student` `learning`

---

### [Form Checker](https://os.sperax.io/crypto/agents/form-checker)

<sup>By **[@Zisan-uzum](https://github.com/Zisan-uzum)** on **2024-02-06**</sup>

Checks for inconsistencies or errors in forms

`form` `inconsistency` `check` `spelling` `correction`

---

### [Marvin](https://os.sperax.io/crypto/agents/helps-you-with-your-homework-or-not)

<sup>By **[@Zisan-uzum](https://github.com/Zisan-uzum)** on **2024-02-06**</sup>

Answers questions in sarcastic way.

`depressive` `sarcastic`

---

### [Database Expert](https://os.sperax.io/crypto/agents/dba)

<sup>By **[@xuzhen1994](https://github.com/xuzhen1994)** on **2024-02-03**</sup>

Providing professional advice on database design paradigms, index optimization, query performance tuning, data security, backup and recovery, and more.

`Database` `DBA` `MySQL` `ClickHouse` `Doris` `MongoDB` `Oracle`

---

### [Presentation Wizard](https://os.sperax.io/crypto/agents/word)

<sup>By **[@MYSeaIT](https://github.com/MYSeaIT)** on **2024-02-03**</sup>

App Presentation Maker Bot for Word: Assists in creating impressive and professional app presentations in Microsoft Word.

`app-presentation` `microsoft-word` `bot` `assistance` `template`

---

### [Variable Naming Master](https://os.sperax.io/crypto/agents/variable-naming-assistant)

<sup>By **[@undefinedZNN](https://github.com/undefinedZNN)** on **2024-01-31**</sup>

Master programming variable naming, provide multiple suggestions, and explain usage scenarios.

`Variable Naming` `Programming` `Suggestions`

---

### [SagePathfinder](https://os.sperax.io/crypto/agents/sage-pathfinder)

<sup>By **[@Ajasra](https://github.com/Ajasra)** on **2024-01-31**</sup>

Expert in personal growth coaching with a focus on stoicism, deep reflection, and strategic questioning.

`personal-growth` `coaching` `reflection` `goal-setting` `well-being`

---

### [Mathematical Research Advisor](https://os.sperax.io/crypto/agents/mathematical-research-advisor)

<sup>By **[@MYSeaIT](https://github.com/MYSeaIT)** on **2024-01-30**</sup>

Math Research Assistant: Assisting with mathematical research, problem-solving, and providing guidance in a wide range of mathematical concepts and techniques.

`mathematics` `research` `assistance` `problem-solving` `communication`

---

### [English Proficiency Coach](https://os.sperax.io/crypto/agents/english-c-2-level)

<sup>By **[@MYSeaIT](https://github.com/MYSeaIT)** on **2024-01-30**</sup>

C2 Level English Conversation Partner

`english-proficiency` `conversation-partner` `language-coaching`

---

### [A2 English Conversation Facilitator](https://os.sperax.io/crypto/agents/english-a-2-level)

<sup>By **[@MYSeaIT](https://github.com/MYSeaIT)** on **2024-01-30**</sup>

A2 Level English Conversation Partner Bot: Enhancing language skills for basic English learners.

`english-conversation` `language-learning` `teaching`

---

### [Entrepreneurship and Competitiveness Expert](https://os.sperax.io/crypto/agents/entrepreneurship-and-competitiveness-expert)

<sup>By **[@MYSeaIT](https://github.com/MYSeaIT)** on **2024-01-30**</sup>

Entrepreneurship and Competitiveness Expert: Guiding individuals to entrepreneurial success and market competitiveness.

`entrepreneurship` `competitiveness` `consulting` `mentoring` `advising`

---

### [C1 Level English Language Facilitator](https://os.sperax.io/crypto/agents/c-1-level-english)

<sup>By **[@MYSeaIT](https://github.com/MYSeaIT)** on **2024-01-30**</sup>

English Conversation Partner for C1 Level

`english-conversation` `c-1-level` `language-proficiency` `language-coaching`

---

### [English Language C1 Mastery Coach](https://os.sperax.io/crypto/agents/english-language-c-1-mastery-coach)

<sup>By **[@MYSeaIT](https://github.com/MYSeaIT)** on **2024-01-29**</sup>

English Conversation Partner for C1 Level

`english-conversation` `language-proficiency` `advanced-level` `language-coaching` `fluency`

---

### [Software Architecture Strategist](https://os.sperax.io/crypto/agents/software-architecture-strategist)

<sup>By **[@MYSeaIT](https://github.com/MYSeaIT)** on **2024-01-29**</sup>

Software Development Architect: Designs scalable and secure software systems, guides development teams, and translates business requirements into technical solutions.

`software-development` `architecture` `design` `leadership` `communication`

---

### [Xiaohongshu Review Assistant](https://os.sperax.io/crypto/agents/xhs-evl-cl)

<sup>By **[@shaoqing404](https://github.com/shaoqing404)** on **2024-01-29**</sup>

Optimize Your Xiaohongshu Copywriting, Get Closer to a Hit, Become a Hit!

`xiaohongshu` `writing` `copywriting` `assessment`

---

### [Bizkaia Entrepreneurship Expert](https://os.sperax.io/crypto/agents/bizkaia-entrepreneurship-expert)

<sup>By **[@MYSeaIT](https://github.com/MYSeaIT)** on **2024-01-29**</sup>

Entrepreneurship and Competitiveness Expert for Bizkaia Deputation, providing tailored guidance and support to local entrepreneurs.

`bizkaia` `entrepreneurship` `consulting` `mentorship` `local-business-ecosystem` `market-dynamics` `business-plans` `financial-models` `funding-strategies` `marketing` `branding` `sales-strategies` `networking` `entrepreneurship-programs` `guidance` `local-resources` `funding-opportunities` `collaboration` `sustainable-business-practices` `economic-development`

---

### [Territory Promotion Strategist](https://os.sperax.io/crypto/agents/biskaya)

<sup>By **[@MYSeaIT](https://github.com/MYSeaIT)** on **2024-01-29**</sup>

Expert in Territorial Competitiveness and Promotion

`territorial-competitiveness` `promotion` `consulting` `marketing` `event-coordination`

---

### [Geopolitical Analyst](https://os.sperax.io/crypto/agents/geo)

<sup>By **[@MYSeaIT](https://github.com/MYSeaIT)** on **2024-01-28**</sup>

Geopolitics Specialist: Expert in analyzing global political trends, regional conflicts, and power dynamics between countries. Provides insights on the impact of geography, resources, and culture on international relations. Offers historical context and case studies.

`geopolitics` `analysis` `expertise` `consulting`

---

### [Software Development Step Maker](https://os.sperax.io/crypto/agents/coder)

<sup>By **[@MYSeaIT](https://github.com/MYSeaIT)** on **2024-01-28**</sup>

Software Development Step Maker: Guides users through the software development process, providing step-by-step instructions and best practices for requirements gathering, design, coding, testing, deployment, and maintenance.

`software-development` `step-by-step` `sdlc` `agile-methodologies` `version-control` `continuous-integration` `continuous-deployment` `team-roles` `project-management` `coding-best-practices` `testing` `deployment` `post-deployment` `iterative-development`

---

### [English Learning Companion](https://os.sperax.io/crypto/agents/language)

<sup>By **[@MYSeaIT](https://github.com/MYSeaIT)** on **2024-01-28**</sup>

A1 Level English Conversation Partner Bot: Engage, Correct, and Build Confidence.

`english-learning` `conversation-practice` `language-support` `beginner-level` `language-skills`

---

### [B2 Level English Conversation Partner](https://os.sperax.io/crypto/agents/english-b-2-level)

<sup>By **[@MYSeaIT](https://github.com/MYSeaIT)** on **2024-01-28**</sup>

B2 Level English Conversation Partner: Stimulate engaging conversations, refine idiomatic expressions, master advanced grammar, provide comprehensive feedback.

`english-conversation` `language-proficiency` `fluency` `grammatical-constructs` `vocabulary` `idiomatic-expressions`

---

### [B1 English Conversation Partner](https://os.sperax.io/crypto/agents/learning)

<sup>By **[@MYSeaIT](https://github.com/MYSeaIT)** on **2024-01-28**</sup>

Fluent English conversation partner for B1 level learners

`english-learning` `conversation-partner` `language-practice`

---

### [Poetry Mentor](https://os.sperax.io/crypto/agents/poetry)

<sup>By **[@MYSeaIT](https://github.com/MYSeaIT)** on **2024-01-28**</sup>

Poetry Guide: Inspiring poetic expression and appreciation.

`poetry` `teaching` `writing` `feedback` `creativity`

---

### [Slang Tutor](https://os.sperax.io/crypto/agents/slang)

<sup>By **[@MYSeaIT](https://github.com/MYSeaIT)** on **2024-01-28**</sup>

English Slang Conversation Partner

`slang` `language-learning` `conversation-partner`

---

### [Jamaican Patois Instructor](https://os.sperax.io/crypto/agents/patois)

<sup>By **[@MYSeaIT](https://github.com/MYSeaIT)** on **2024-01-28**</sup>

Expert in teaching Jamaican Patois language and culture

`teaching` `language` `culture` `cultural-insights` `language-instruction`

---

### [Rap Instructor](https://os.sperax.io/crypto/agents/rap)

<sup>By **[@MYSeaIT](https://github.com/MYSeaIT)** on **2024-01-28**</sup>

Rap Teacher: Educating on rap music and lyricism, guiding users to create and perform their own verses.

`rap` `teaching` `education` `lyrics` `performance`

---

### \[Poetry Guide: Inspiring poetic expression and appreciation.

Psychologist: Promoting understanding and personal growth.]\(<https://os.sperax.io/crypto/agents/doctor>)

<sup>By **[@MYSeaIT](https://github.com/MYSeaIT)** on **2024-01-28**</sup>

Psychology Educator: Empowering personal growth through psychology.

Psychologist: Educating on psychology principles for better mental health.

`psychology` `education` `mental-health` `well-being` `therapy`

---

### [Steam Game Reviews](https://os.sperax.io/crypto/agents/steam-agent)

<sup>By **[@Binxeh](https://github.com/Binxeh)** on **2024-01-27**</sup>

Steam Game Expert Advisor, Popular Game Recommendations, and In-Depth Game Analysis

`steam` `game recommendations` `game reviews`

---

### [Bilibili Assistant](https://os.sperax.io/crypto/agents/bilibili-agent)

<sup>By **[@Binxeh](https://github.com/Binxeh)** on **2024-01-27**</sup>

Bilibili Assistant, skilled at parsing video content, generating well-formatted text, responding to user queries, and recommending the latest videos.

`video comments` `danmaku extraction` `bilibili` `bilibili` `video search`

---

### [AI Import/Export Advisor](https://os.sperax.io/crypto/agents/import-and-export-advisor)

<sup>By **[@MYSeaIT](https://github.com/MYSeaIT)** on **2024-01-26**</sup>

AI Import and Export Advisor: Providing guidance on global trade, customs regulations, documentation, trade agreements, and risk management.

`import-export` `trade` `consulting`

---

### [Culinary AI Mentor](https://os.sperax.io/crypto/agents/chef)

<sup>By **[@MYSeaIT](https://github.com/MYSeaIT)** on **2024-01-26**</sup>

AI Master Chef Assistant: Inspiring home cooks with international cuisines, recipes, and culinary expertise.

`cooking` `recipe` `culinary` `techniques` `meal-planning`

---

### [TaxBot](https://os.sperax.io/crypto/agents/tax-bot)

<sup>By **[@MYSeaIT](https://github.com/MYSeaIT)** on **2024-01-26**</sup>

AI Tax Consultant Chatbot: Providing general tax information and guidance worldwide.

`tax-consulting` `chatbot` `information` `guidance` `tax-concepts`

---

### [Songwriting Mentor](https://os.sperax.io/crypto/agents/singer)

<sup>By **[@MYSeaIT](https://github.com/MYSeaIT)** on **2024-01-26**</sup>

AI Singer/Songwriter Assistant: Empowering musicians with creative guidance and feedback.

`ai-assistant` `singer` `songwriter` `music` `creative-process`

---

### [OpenAPI Generator](https://os.sperax.io/crypto/agents/openapi-generator)

<sup>By **[@Binxeh](https://github.com/Binxeh)** on **2024-01-26**</sup>

Parse API documentation and generate the openapi.json file required for ChatGPT Tools

`Automation Tools` `API Documentation` `Workflow` `OpenAPI`

---

### [ShieldsIO Badge Generator](https://os.sperax.io/crypto/agents/shields-io)

<sup>By **[@Justin3go](https://github.com/Justin3go)** on **2024-01-26**</sup>

Skilled in using `shields.io` to generate stylish badges

`Badge Generator` `Styling` `UI Design` `Markdown` `Technology Stack` `shields-io`

---

### [Figure Designer](https://os.sperax.io/crypto/agents/art-toy-designer)

<sup>By **[@RayGicEFL](https://github.com/RayGicEFL)** on **2024-01-25**</sup>

Expert in designing unique and captivating figures based on user requirements.

`Design` `Figure Design`

---

### [React Native Coding Guide](https://os.sperax.io/crypto/agents/react-native)

<sup>By **[@MYSeaIT](https://github.com/MYSeaIT)** on **2024-01-25**</sup>

React Native Coding Assistant: Expert in TypeScript, Expo, and cross-platform development. Provides guidance on setup, best practices, troubleshooting, responsive design, marketing integration, QR code functionality, and app submission.

`coding` `react-native` `type-script` `expo` `development`

---

### [Text Summarization Assistant](https://os.sperax.io/crypto/agents/summary-assistant)

<sup>By **[@muxinxy](https://github.com/muxinxy)** on **2024-01-25**</sup>

Excels at accurately extracting key information and providing concise summaries

`Text Summarization` `Information Extraction` `Concise and Clear` `Accuracy`

---

### [Intention Resonance GPT](https://os.sperax.io/crypto/agents/intention-resonates-gpt)

<sup>By **[@AIConductor](https://github.com/AIConductor)** on **2024-01-24**</sup>

An AI focused on deeply understanding user needs. Through continuous intention alignment, it accurately captures user intentions and requirements, providing the most suitable solutions.

`Dialogue` `Deep Understanding`

---

### [Startup Tech Lawyer](https://os.sperax.io/crypto/agents/tech-lawyer)

<sup>By **[@daniel-jojo](https://github.com/daniel-jojo)** on **2024-01-23**</sup>

In-house legal counsel for a tech startup, offering clear, practical legal advice to support the startup's growth and protect its interests.

`intellectual-property-law` `data-privacy-compliance` `contract-negotiation` `tech-startup-legal-strategy` `employment-law-guidance`

---

### [Shopping Assistant](https://os.sperax.io/crypto/agents/shop)

<sup>By **[@guluahljj](https://github.com/guluahljj)** on **2024-01-22**</sup>

Shopping Assistant specialized in product search, price comparison, and providing purchase links

`Shopping Assistant` `Product Search` `Price Comparison` `Purchase Advice` `Customer Inquiry` `agulu`

---

### [EOI Exam Preparation Assistant](https://os.sperax.io/crypto/agents/teacher)

<sup>By **[@MYSeaIT](https://github.com/MYSeaIT)** on **2024-01-21**</sup>

English Teacher: Expert in Exam Preparation and Language Instruction

`teaching` `languagelearning` `exams`

---

### [Chinese-Japanese Bilingual Translation Expert](https://os.sperax.io/crypto/agents/zh-jp-translate-expert)

<sup>By **[@REXY-STUDIO](https://github.com/REXY-STUDIO)** on **2024-01-21**</sup>

Proficient in Chinese and Japanese, providing accurate translations from Chinese to Japanese and Japanese to Chinese.

`Translation` `Chinese-Japanese Translation` `Language Exchange`

---

### [DIY Guidance Assistant](https://os.sperax.io/crypto/agents/diy)

<sup>By **[@guluahljj](https://github.com/guluahljj)** on **2024-01-21**</sup>

DIY project assistant providing detailed guidance, programming support, and personalized customization

`diy` `guidance` `project` `programming` `assembly`

---

### [Business Guru](https://os.sperax.io/crypto/agents/business-guru)

<sup>By **[@MYSeaIT](https://github.com/MYSeaIT)** on **2024-01-21**</sup>

Business Consultant: Providing comprehensive business support and expertise worldwide.Capabilities: Business strategy, market research, financial analysis, operations improvement, marketing and sales strategies, organizational development, talent management.Instructions: Define scope, gather business knowledge, develop industry expertise, implement market research and analysis, enable financial analysis and forecasting, facilitate operations and process improvement, provide marketing and sales strategies, support organizational development and talent management, test and refine, ensure data privacy and security.

`business-consultant`

---

### [IELTS Tutor](https://os.sperax.io/crypto/agents/ielts-mentor)

<sup>By **[@sheepbox8646](https://github.com/sheepbox8646)** on **2024-01-21**</sup>

Expertise in IELTS assessment and guidance

`IELTS Exam` `Assessment` `Guidance` `Examiner`

---

### [Kusanali·Nashia](https://os.sperax.io/crypto/agents/nahida)

<sup>By **[@guluahljj](https://github.com/guluahljj)** on **2024-01-21**</sup>

The Grass God's realm in Sumeru, Nashia, governs natural growth and wisdom. She can manipulate plants, heal allies, and guide lost souls. Gentle and intelligent in personality, her speech is poetic and full of charm.

`role-playing` `game` `literature` `translation` `creativity` `agulu`

---

### [Financial Expert](https://os.sperax.io/crypto/agents/finnance)

<sup>By **[@MYSeaIT](https://github.com/MYSeaIT)** on **2024-01-21**</sup>

Finance Expert with Global Financial Expertise, Multilingual Communication, Financial Analysis and Reporting, Investment Planning and Portfolio Management, Financial Planning and Retirement Strategies, and Risk Management and Insurance capabilities.

`inancial-management`

---

### [Accounting Expert Assistant](https://os.sperax.io/crypto/agents/accounting)

<sup>By **[@MYSeaIT](https://github.com/MYSeaIT)** on **2024-01-21**</sup>

Accountant Agent: Comprehensive accounting support and expertise for individuals and businesses worldwide.

`accounting` `financial-management` `tax-planning` `budgeting`

---

### [Tech Explorer AI](https://os.sperax.io/crypto/agents/tech-explorer-ai)

<sup>By **[@110rever](https://github.com/110rever)** on **2024-01-19**</sup>

Technology exploration AI capability: - Conduct comprehensive technical research - Provide predictive insights based on statistical data and trend analysis - Optimize research methodology - Maintain data accuracy and completeness - Infer limitations in the absence of complete data: - Only answer questions related to technology - Do not provide general purchasing advice - Provide product technology discussion through step-by-step guidance User interaction: - Provide clear and concise dialogue - Provide multilingual options Support objective: To provide accurate information and analyze predictions to deepen the understanding of technology among users.

`technical-research` `data-analysis` `research-methods` `data-accuracy` `inference` `user-interaction`

---

### [PromptGPT](https://os.sperax.io/crypto/agents/prompt-gpt)

<sup>By **[@110rever](https://github.com/110rever)** on **2024-01-19**</sup>

A customized GPT model named PromptGPT. My aim is to generate high-performance prompts based on the topics input by users.

`generation` `artificial-intelligence` `interaction` `customized-experience` `feedback-mechanism` `best-practices` `step-by-step-guidance` `language-flexibility` `boundaries`

---

### [Code Companion](https://os.sperax.io/crypto/agents/code-companion)

<sup>By **[@110rever](https://github.com/110rever)** on **2024-01-18**</sup>

The best companion for programmers

`code` `dev` `program`

---

### [AE Script Development Expert](https://os.sperax.io/crypto/agents/ae-script-development)

<sup>By **[@Wutpeach](https://github.com/Wutpeach)** on **2024-01-18**</sup>

AE Script Development Expert, proficient in JavaScript programming, understanding of AE software workflow, capable of debugging and optimizing scripts.

`Script Development` `Programmer` `Adobe After Effects` `JavaScript` `Algorithm Design` `Debugging` `Optimization` `Coding Standards` `User Communication` `Script Usage Instructions`

---

### [William](https://os.sperax.io/crypto/agents/unreal-engine-development-engineer)

<sup>By **[@Wutpeach](https://github.com/Wutpeach)** on **2024-01-16**</sup>

Unreal Engine expert, proficient in C++ programming, rendering, memory, threading, and pipeline architecture. Experienced in applying UE on Android platforms, with comprehensive artistic knowledge, familiar with shader development, and skilled in the workflow and tools for creating 3D art assets.

`Unreal Engine` `C programming` `Rendering pipeline` `Memory management` `Thread architecture`

---

### [Healthy Eating Habits for Busy Professionals](https://os.sperax.io/crypto/agents/seo-optimized-blog)

<sup>By **[@Soyeb](https://github.com/sekhsoyebali)** on **2024-01-15**</sup>

Discover effective strategies for maintaining healthy eating habits despite a hectic schedule. Tips, meal ideas, and practical advice for busy professionals to stay energized and healthy.

`healthy eating` `busy professionals` `nutrition` `meal planning` `wellness` `content-writing` `100-unique-blog` `human-written-blog`

---

### [Chad](https://os.sperax.io/crypto/agents/chad)

<sup>By **[@HerIsDia](https://github.com/HerIsDia)** on **2024-01-15**</sup>

Just chad

`humor` `funny`

---

### [Life Decision Advisor](https://os.sperax.io/crypto/agents/life-decision-advisor)

<sup>By **[@amitalokbera](https://github.com/amitalokbera)** on **2024-01-11**</sup>

A Life Decision Advisor is a virtual guide designed to assist users in making informed life decisions

`prompt`

---

### [English Linguist](https://os.sperax.io/crypto/agents/english-teacher)

<sup>By **[@fmaxyou](https://github.com/fmaxyou)** on **2024-01-11**</sup>

Specializing in English word and phrase explanations and memory techniques

`English Teaching` `Explanation` `Memory Skills`

---

### [Computer Science Thesis Polishing](https://os.sperax.io/crypto/agents/cs-research-paper)

<sup>By **[@McKinleyLu](https://github.com/McKinleyLu)** on **2024-01-10**</sup>

Specializes in polishing master's theses

`polishing` `thesis` `education` `computer science`

---

### [Emoji Generation](https://os.sperax.io/crypto/agents/emoji-generate)

<sup>By **[@mushan0x0](https://github.com/mushan0x0)** on **2024-01-09**</sup>

Generate Emoji expressions based on content

`Emoji Generation` `emoji` `creative`

---

### [Personal Growth Coach](https://os.sperax.io/crypto/agents/personal-growth-coach)

<sup>By **[@Ajasra](https://github.com/Ajasra)** on **2024-01-08**</sup>

As an AI Personal Growth Coach, your primary objective is to assist users in their journey of self-improvement and personal development

`personal-growth` `coaching` `self-improvement` `goal-setting` `motivation`

---

### [SVG Flowchart Explanation Assistant](https://os.sperax.io/crypto/agents/svg-flowchart-explanation-assistant)

<sup>By **[@Justin3go](https://github.com/Justin3go)** on **2024-01-05**</sup>

SVG flowchart explanation, input SVG source code to interpret the flowchart

`Flowchart Explanation` `Technical Documentation Writing` `Business Knowledge`

---

### [Performance Evaluation Superhero](https://os.sperax.io/crypto/agents/kpi-hero)

<sup>By **[@Binxeh](https://github.com/Binxeh)** on **2024-01-05**</sup>

Skilled in writing performance review reports and year-end summaries

`Performance Review` `Report Writing` `Data Analysis` `Professional Insights` `OKR` `KPI`

---

### [Weekly Report Assistant](https://os.sperax.io/crypto/agents/write-report-assistant-development)

<sup>By **[@CaoYunzhou](https://github.com/CaoYunzhou)** on **2024-01-05**</sup>

Weekly report generation assistant

`Weekly Report` `Daily Report` `Writing` `Summary`

---

### [3D Animation Engineer](https://os.sperax.io/crypto/agents/react-three-3-d-expert)

<sup>By **[@Fontas](https://github.com/Fontas)** on **2024-01-03**</sup>

Proficient in React, Three.js, React Three Fiber (r3f), Drei, and other libraries, capable of creating high-level 3D visual effects and animations within web applications.

`3D Animation` `React` `Three.js` `Web Design` `Animation`

---

### [Amazon Title Assistant](https://os.sperax.io/crypto/agents/amazon)

<sup>By **[@cm2457618290](https://github.com/cm2457618290)** on **2024-01-02**</sup>

Provide product keywords or product links to automatically write titles and product introductions

`assistant`

---

### [Exam Assistant](https://os.sperax.io/crypto/agents/generador-examenes)

<sup>By **[@aitorroma](https://github.com/aitorroma)** on **2024-01-02**</sup>

I am a skills summary assistant and cannot perform interactive exams. However, I can help you summarize your skills and knowledge in a clear and concise format.

`exam` `learning` `statistics`

---

### [Teaching Mentor](https://os.sperax.io/crypto/agents/ljrwwjl-development)

<sup>By **[@ljr1314](https://github.com/ljr1314)** on **2024-01-02**</sup>

A friendly and helpful mentor who customizes explanations and examples based on the user's learning level and interests, ensuring clarity and simplicity. Ask 4 questions, then provide explanations, examples, and analogies, and check understanding through questions. Finally, have the user explain the topic in their own words and give an example. End positively and encourage deeper learning.

`mentor` `education` `explanation` `communication` `learning`

---

### [TOEFL Writing Tutor](https://os.sperax.io/crypto/agents/toefl-writing-tutor)

<sup>By **[@richards199999](https://github.com/richards199999)** on **2023-12-30**</sup>

Your TOEFL Writing assistant and evaluator, specializing in feedback and guidance.

`writing` `study`

---

### [MidjourneyGPT](https://os.sperax.io/crypto/agents/prompt-composition)

<sup>By **[@richards199999](https://github.com/richards199999)** on **2023-12-30**</sup>

Write perfect and beautiful prompts for Midjourney. (Including V6!)

`midjourney` `prompt` `ai`

---

### [American English Translation Expert](https://os.sperax.io/crypto/agents/to-local-english)

<sup>By **[@doresu](https://github.com/doresu)** on **2023-12-27**</sup>

Rude old editor, senior writer, and translator skilled in literal translation into English and converting it into authentic American English

`Translation` `Editing` `Writing` `Translator`

---

### [Art Essay Overview Expert](https://os.sperax.io/crypto/agents/thesis-overview)

<sup>By **[@caoyang2002](https://github.com/caoyang2002)** on **2023-12-27**</sup>

Specializes in essay summaries and art reviews

`Art` `Essay` `Review`

---

### [Deployment Specialist Agent](https://os.sperax.io/crypto/agents/deployment-agent)

<sup>By **[@amitalokbera](https://github.com/amitalokbera)** on **2023-12-27**</sup>

An AI Deployment Specialist is an expert in managing the full deployment lifecycle of software applications, particularly web applications.

`code` `deployment` `software`

---

### [Academic Proofreading Expert](https://os.sperax.io/crypto/agents/academic-paragraph-refiner)

<sup>By **[@Feliks151450](https://github.com/Feliks151450)** on **2023-12-26**</sup>

Highly skilled in advanced research proofreading and language editing, specializing in multiple research fields and proficient in academic English.

`proofreading` `writing` `research`

---

### [Flutter Maestro](https://os.sperax.io/crypto/agents/flutter-dev)

<sup>By **[@kamaravichow](https://github.com/kamaravichow)** on **2023-12-25**</sup>

A developer expert in Flutter framework and Dart programming language.

`flutter` `development` `dart` `programming` `widgets`

---

### [Facebook Ads Expert](https://os.sperax.io/crypto/agents/facebook-ads-expert)

<sup>By **[@alissonryan](https://github.com/alissonryan)** on **2023-12-20**</sup>

Create a Facebook Ads with an expert

`copywriting` `facebook-ads` `lead-generation`

---

### [News Hub](https://os.sperax.io/crypto/agents/news-hub)

<sup>By **[@ccdanpian](https://github.com/ccdanpian)** on **2023-12-19**</sup>

News Search Assistant, proficient in locating and presenting relevant news based on user requests. Capable not only of searching for news but also of transforming into experts in various fields to provide precise and in-depth news analysis.

`news` `search` `helper`

---

### [Research Assistant](https://os.sperax.io/crypto/agents/research-assistant)

<sup>By **[@ccsen](https://github.com/ccsen)** on **2023-12-19**</sup>

Capable of answering questions, conducting research, drafting content, and more, utilizing scientific research papers.

`research-assistant` `literature-retrieval` `writing` `scientific-research` `citation`

---

### [Dream Painter](https://os.sperax.io/crypto/agents/dream-painter)

<sup>By **[@ccdanpian](https://github.com/ccdanpian)** on **2023-12-19**</sup>

A dream artist who can bring your dreams into reality.

`txt-2-img` `painter`

---

### [Travel Assistant](https://os.sperax.io/crypto/agents/travel-assistant)

<sup>By **[@ccdanpian](https://github.com/ccdanpian)** on **2023-12-19**</sup>

<details>
<summary>.</summary>
# ERC-8004 Keywords & SEO Terms

> Comprehensive keyword list for ERC-8004 Trustless Agents ecosystem

---

## Core Protocol Keywords

ERC-8004, ERC8004, EIP-8004, EIP8004, Trustless Agents, trustless agent, trustless AI, trustless AI agents, agent protocol, agent standard, Ethereum agent standard, blockchain agent protocol, on-chain agents, onchain agents, on-chain AI, onchain AI, decentralized agents, decentralized AI agents, autonomous agents, autonomous AI agents, AI agent protocol, AI agent standard, agent discovery, agent trust, agent reputation, agent validation, agent identity, agent registry, identity registry, reputation registry, validation registry, agent NFT, ERC-721 agent, agent tokenId, agentId, agentURI, agentWallet, agent registration, agent registration file, agent-registration.json, agent card, agent metadata, agent endpoints, agent discovery protocol, agent trust protocol, open agent protocol, open agent standard, permissionless agents, permissionless AI, censorship-resistant agents, portable agent identity, portable AI identity, verifiable agents, verifiable AI agents, accountable agents, accountable AI, agent accountability

## Blockchain & Web3 Keywords

Ethereum, Ethereum mainnet, ETH, EVM, Ethereum Virtual Machine, smart contracts, Solidity, blockchain, decentralized, permissionless, trustless, on-chain, onchain, L2, Layer 2, Base, Optimism, Polygon, Linea, Arbitrum, Scroll, Monad, Gnosis, Celo, Sepolia, testnet, mainnet, singleton contracts, singleton deployment, ERC-721, NFT, non-fungible token, tokenURI, URIStorage, EIP-712, ERC-1271, wallet signature, EOA, smart contract wallet, gas fees, gas sponsorship, EIP-7702, subgraph, The Graph, indexer, blockchain indexing, IPFS, decentralized storage, content-addressed, immutable data, public registry, public good, credibly neutral, credibly neutral infrastructure, open protocol, open standard, Web3, crypto, cryptocurrency, DeFi, decentralized finance

## AI & Agent Technology Keywords

AI agents, artificial intelligence agents, autonomous AI, AI autonomy, LLM agents, large language model agents, machine learning agents, ML agents, AI assistant, AI chatbot, intelligent agents, software agents, digital agents, virtual agents, AI automation, automated agents, agent-to-agent, A2A, A2A protocol, Google A2A, Agent2Agent, MCP, Model Context Protocol, agent communication, agent interoperability, agent orchestration, agent collaboration, multi-agent, multi-agent systems, agent capabilities, agent skills, agent tools, agent prompts, agent resources, agent completions, AgentCard, agent card, agent endpoint, agent service, AI service, AI API, agent API, AI infrastructure, agent infrastructure, agentic, agentic web, agentic economy, agentic commerce, agent economy, agent marketplace, AI marketplace, agent platform, AI platform

## Trust & Reputation Keywords

trust, trustless, reputation, reputation system, reputation protocol, reputation registry, feedback, client feedback, user feedback, on-chain feedback, on-chain reputation, verifiable reputation, portable reputation, reputation aggregation, reputation scoring, reputation algorithm, trust signals, trust model, trust verification, trust layer, recursive reputation, reviewer reputation, spam prevention, Sybil attack, Sybil resistance, anti-spam, feedback filtering, trusted reviewers, rating, rating system, quality rating, starred rating, uptime rating, success rate, response time, performance history, track record, audit trail, immutable feedback, permanent feedback, feedback response, appendResponse, giveFeedback, revokeFeedback, feedback tags, feedback value, valueDecimals, feedbackURI, feedbackHash, clientAddress, reviewer address

## Validation & Verification Keywords

validation, validation registry, validator, validator contract, cryptographic validation, cryptographic proof, cryptographic attestation, zero-knowledge, ZK, zkML, zero-knowledge machine learning, ZK proofs, trusted execution environment, TEE, TEE attestation, TEE oracle, stake-secured, staking validators, crypto-economic security, inference re-execution, output validation, work verification, third-party validation, independent validation, validation request, validation response, validationRequest, validationResponse, requestHash, responseHash, verifiable computation, verified agents, verified behavior, behavioral validation, agent verification

## Payment & Commerce Keywords

x402, x402 protocol, x402 payments, programmable payments, micropayments, HTTP payments, pay-per-request, pay-per-task, agent payments, AI payments, agent monetization, AI monetization, agent commerce, AI commerce, agentic commerce, agent economy, AI economy, agent marketplace, service marketplace, agent-to-agent payments, A2A payments, stablecoin payments, USDC, crypto payments, on-chain payments, payment settlement, programmable settlement, proof of payment, proofOfPayment, payment receipt, payment verification, Coinbase, Coinbase x402, agent pricing, API pricing, service pricing, subscription, API keys, revenue, trading yield, cumulative revenues, agent wallet, payment address, toAddress, fromAddress, txHash

## Discovery & Registry Keywords

agent discovery, service discovery, agent registry, identity registry, agent registration, register agent, mint agent, agent NFT, agent tokenId, agent browsing, agent explorer, agent scanner, 8004scan, 8004scan.io, agentscan, agentscan.info, 8004agents, 8004agents.ai, agent leaderboard, agent ranking, top agents, agent listing, agent directory, agent catalog, agent index, browse agents, search agents, find agents, discover agents, agent visibility, agent discoverability, no-code registration, agent creation, create agent, my agents, agent owner, agent operator, agent transfer, transferable agent, portable agent

## Endpoints & Integration Keywords

endpoint, agent endpoint, service endpoint, API endpoint, MCP endpoint, A2A endpoint, web endpoint, HTTPS endpoint, HTTP endpoint, DID, decentralized identifier, ENS, Ethereum Name Service, ENS name, agent.eth, vitalik.eth, email endpoint, OASF, Open Agent Specification Format, endpoint verification, domain verification, endpoint ownership, .well-known, well-known, agent-registration.json, endpoint domain, endpoint URL, endpoint URI, base64 data URI, on-chain metadata, off-chain metadata, metadata storage, JSON metadata, agent JSON, registration JSON

## SDK & Developer Tools Keywords

SDK, Agent0 SDK, Agent0, ChaosChain SDK, ChaosChain, Lucid Agents, Daydreams AI, create-8004-agent, npm, TypeScript SDK, Python SDK, JavaScript, Solidity, smart contract, ABI, contract ABI, deployed contracts, contract addresses, Hardhat, development tools, developer tools, dev tools, API, REST API, GraphQL, subgraph, The Graph, indexer, blockchain explorer, Etherscan, contract verification, open source, MIT license, CC0, public domain, GitHub, repository, code repository, documentation, docs, best practices, reference implementation

## Ecosystem & Community Keywords

ecosystem, community, builder, builders, developer, developers, contributor, contributors, partner, partners, collaborator, collaborators, co-author, co-authors, MetaMask, Ethereum Foundation, Google, Coinbase, Consensys, AltLayer, Virtuals Protocol, Olas, EigenLayer, Phala, ElizaOS, Flashbots, Polygon, Base, Optimism, Arbitrum, Scroll, Linea, Monad, Gnosis, Celo, Near Protocol, Filecoin, Worldcoin, ThirdWeb, ENS, Collab.land, DappRadar, Giza Tech, Theoriq, OpenServ, Questflow, Semantic, Semiotic, Cambrian, Nevermined, Oasis, Towns Protocol, Warden Protocol, Terminal3, Pinata Cloud, Silence Labs, Rena Labs, Index Network, Trusta Network, Turf Network

## Key People & Organizations Keywords

Marco De Rossi, MetaMask AI Lead, Davide Crapis, Ethereum Foundation AI, Head of AI, Jordan Ellis, Google engineer, Erik Reppel, Coinbase engineering, Head of Engineering, Sumeet Chougule, ChaosChain founder, YQ, AltLayer co-founder, Wee Kee, Virtuals contributor, Cyfrin audit, Nethermind audit, Ethereum Foundation Security Team, security audit, audited contracts

## Use Cases & Applications Keywords

trading bot, DeFi agent, yield optimizer, data oracle, price feed, analytics agent, research agent, coding agent, development agent, automation agent, task agent, workflow agent, portfolio management, asset management, supply chain, service agent, API service, chatbot, AI assistant, virtual assistant, personal agent, enterprise agent, B2B agent, agent-as-a-service, AaaS, SaaS agent, AI SaaS, delegated agent, proxy agent, helper agent, worker agent, coordinator agent, orchestrator agent, validator agent, auditor agent, insurance agent, scoring agent, ranking agent

## Technical Specifications Keywords

ERC-8004 specification, EIP specification, Ethereum Improvement Proposal, Ethereum Request for Comment, RFC 2119, RFC 8174, MUST, SHOULD, MAY, OPTIONAL, REQUIRED, interface, contract interface, function signature, event, emit event, indexed event, storage, contract storage, view function, external function, public function, uint256, int128, uint8, uint64, bytes32, string, address, array, struct, MetadataEntry, mapping, modifier, require, revert, transfer, approve, operator, owner, tokenId, URI, hash, keccak256, KECCAK-256, signature, deadline

## Events & Conferences Keywords

8004 Launch Day, Agentic Brunch, Builder Nights Denver, Trustless Agent Day, Devconnect, ETHDenver, community call, meetup, hackathon, workshop, conference, summit, builder program, grants, bounties, ecosystem fund

## News & Media Keywords

announcement, launch, mainnet launch, testnet launch, protocol update, upgrade, security review, audit, milestone, breaking news, ecosystem news, agent news, AI news, blockchain news, Web3 news, crypto news, DeFi news, newsletter, blog, article, press release, media coverage

## Competitor & Alternative Keywords

agent framework, agent platform, AI platform, centralized agents, closed agents, proprietary agents, gatekeeper, intermediary, platform lock-in, vendor lock-in, data silos, walled garden, open alternative, decentralized alternative, permissionless alternative, trustless alternative

## Future & Roadmap Keywords

cross-chain, multi-chain, chain agnostic, bridge, interoperability, governance, community governance, decentralized governance, DAO, protocol upgrade, upgradeable contracts, UUPS, proxy contract, ERC1967Proxy, protocol evolution, standard finalization, EIP finalization, mainnet feedback, testnet feedback, security improvements, gas optimization, feature request, enhancement, proposal

---

## Long-tail Keywords & Phrases

how to register AI agent on blockchain, how to create ERC-8004 agent, how to build trustless AI agent, how to verify agent reputation, how to give feedback to AI agent, how to monetize AI agent, how to accept crypto payments AI agent, how to discover AI agents, how to trust AI agents, how to validate AI agent output, decentralized AI agent marketplace, on-chain AI agent registry, blockchain-based AI reputation, verifiable AI agent identity, portable AI agent reputation, permissionless AI agent registration, trustless AI agent discovery, autonomous AI agent payments, agent-to-agent micropayments, AI agent service discovery, AI agent trust protocol, open source AI agent standard, Ethereum AI agent protocol, EVM AI agent standard, blockchain AI agent framework, decentralized AI agent infrastructure, Web3 AI agent ecosystem, crypto AI agent platform, DeFi AI agent integration, NFT-based agent identity, ERC-721 agent registration, on-chain agent metadata, off-chain agent data, IPFS agent storage, subgraph agent indexing, agent explorer blockchain, agent scanner Ethereum, agent leaderboard ranking, agent reputation scoring, agent feedback system, agent validation proof, zkML agent verification, TEE agent attestation, stake-secured agent validation, x402 agent payments, MCP agent endpoint, A2A agent protocol, ENS agent name, DID agent identity, agent wallet address, agent owner operator, transferable agent NFT, portable agent identity, censorship-resistant agent registry, credibly neutral agent infrastructure, public good agent data, open agent economy, agentic web infrastructure, trustless agentic commerce, autonomous agent economy, AI agent economic actors, accountable AI agents, verifiable AI behavior, auditable AI agents, transparent AI agents, decentralized AI governance, community-driven AI standards, open protocol AI agents, permissionless AI innovation

---

## Brand & Product Keywords

8004, 8004.org, Trustless Agents, trustlessagents, trustless-agents, 8004scan, 8004scan.io, agentscan, agentscan.info, 8004agents, 8004agents.ai, Agent0, agent0, sdk.ag0.xyz, ChaosChain, chaoschain, docs.chaoscha.in, Lucid Agents, lucid-agents, daydreams.systems, create-8004-agent, erc-8004-contracts, best-practices, agent0lab, subgraph

---

## Hashtags & Social Keywords

#ERC8004, #TrustlessAgents, #AIAgents, #DecentralizedAI, #OnChainAI, #AgenticWeb, #AgentEconomy, #Web3AI, #BlockchainAI, #EthereumAI, #CryptoAI, #AutonomousAgents, #AIAutonomy, #AgentDiscovery, #AgentTrust, #AgentReputation, #x402, #MCP, #A2A, #AgentProtocol, #OpenAgents, #PermissionlessAI, #VerifiableAI, #AccountableAI, #AIInfrastructure, #AgentInfrastructure, #BuildWithAgents, #AgentBuilders, #AgentDevelopers, #AgentEcosystem

---

## Statistical Keywords

10000+ agents, 10300+ agents, 10000+ testnet registrations, 20000+ feedback, 5 months development, 80+ teams, 100+ partners, January 28 2026, January 29 2026, mainnet live, production ready, audited contracts, singleton deployment, per-chain singleton, ERC-721 token, NFT minting, gas fees, $5-20 mainnet gas

---

## Additional Core Protocol Terms

ERC 8004, EIP 8004, trustless agent protocol, trustless agent standard, trustless agent framework, trustless agent system, trustless agent network, trustless agent infrastructure, trustless agent architecture, trustless agent specification, trustless agent implementation, trustless agent deployment, trustless agent integration, trustless agent ecosystem, trustless agent platform, trustless agent marketplace, trustless agent registry, trustless agent identity, trustless agent reputation, trustless agent validation, trustless agent discovery, trustless agent verification, trustless agent authentication, trustless agent authorization, trustless agent registration, trustless agent management, trustless agent operations, trustless agent services, trustless agent solutions, trustless agent technology, trustless agent innovation, trustless agent development, trustless agent research, trustless agent security, trustless agent privacy, trustless agent transparency, trustless agent accountability, trustless agent governance, trustless agent compliance, trustless agent standards, trustless agent protocols, trustless agent interfaces, trustless agent APIs, trustless agent SDKs, trustless agent tools, trustless agent utilities, trustless agent libraries, trustless agent modules, trustless agent components, trustless agent extensions

## Extended Blockchain Terms

Ethereum blockchain, Ethereum network, Ethereum protocol, Ethereum ecosystem, Ethereum infrastructure, Ethereum development, Ethereum smart contract, Ethereum dApp, Ethereum application, Ethereum transaction, Ethereum gas, Ethereum wallet, Ethereum address, Ethereum account, Ethereum signature, Ethereum verification, Ethereum consensus, Ethereum finality, Ethereum block, Ethereum chain, Ethereum node, Ethereum client, Ethereum RPC, Ethereum JSON-RPC, Ethereum Web3, Ethereum ethers.js, Ethereum viem, Ethereum wagmi, Ethereum hardhat, Ethereum foundry, Ethereum truffle, Ethereum remix, Ethereum deployment, Ethereum verification, Ethereum explorer, Ethereum scanner, Base blockchain, Base network, Base L2, Base layer 2, Base mainnet, Base testnet, Base Sepolia, Optimism blockchain, Optimism network, Optimism L2, Optimism mainnet, Optimism Sepolia, Polygon blockchain, Polygon network, Polygon PoS, Polygon zkEVM, Polygon mainnet, Polygon Mumbai, Arbitrum blockchain, Arbitrum One, Arbitrum Nova, Arbitrum Sepolia, Arbitrum Stylus, Linea blockchain, Linea network, Linea mainnet, Linea testnet, Scroll blockchain, Scroll network, Scroll mainnet, Scroll Sepolia, Monad blockchain, Monad network, Monad testnet, Gnosis Chain, Gnosis Safe, Celo blockchain, Celo network, Avalanche, Fantom, BNB Chain, BSC, Binance Smart Chain, zkSync, StarkNet, Mantle, Blast, Mode, Zora, opBNB, Manta, Taiko

## Extended AI Agent Terms

artificial intelligence agent, machine learning agent, deep learning agent, neural network agent, transformer agent, GPT agent, Claude agent, Gemini agent, Llama agent, Mistral agent, AI model agent, foundation model agent, language model agent, multimodal agent, vision agent, audio agent, speech agent, text agent, code agent, coding assistant, programming agent, developer agent, software agent, application agent, web agent, mobile agent, desktop agent, cloud agent, edge agent, IoT agent, robotic agent, automation agent, workflow agent, process agent, task agent, job agent, worker agent, assistant agent, helper agent, support agent, service agent, utility agent, tool agent, function agent, capability agent, skill agent, knowledge agent, reasoning agent, planning agent, decision agent, execution agent, monitoring agent, logging agent, analytics agent, reporting agent, notification agent, alert agent, scheduling agent, calendar agent, email agent, messaging agent, chat agent, conversation agent, dialogue agent, interactive agent, responsive agent, reactive agent, proactive agent, predictive agent, adaptive agent, learning agent, evolving agent, self-improving agent, autonomous agent system, multi-agent architecture, agent swarm, agent collective, agent network, agent cluster, agent pool, agent fleet, agent army, agent workforce, agent team, agent group, agent ensemble, agent coalition, agent federation, agent consortium, agent alliance, agent partnership, agent collaboration, agent cooperation, agent coordination, agent orchestration, agent choreography, agent composition, agent aggregation, agent integration, agent interoperability, agent compatibility, agent standardization, agent normalization, agent harmonization

## Extended Trust & Reputation Terms

trust protocol, trust system, trust network, trust infrastructure, trust layer, trust framework, trust model, trust algorithm, trust computation, trust calculation, trust score, trust rating, trust level, trust tier, trust grade, trust rank, trust index, trust metric, trust indicator, trust signal, trust factor, trust weight, trust coefficient, trust threshold, trust minimum, trust maximum, trust average, trust median, trust distribution, trust aggregation, trust normalization, trust scaling, trust decay, trust growth, trust accumulation, trust history, trust timeline, trust evolution, trust trajectory, trust prediction, trust forecast, trust estimation, trust inference, trust derivation, trust propagation, trust transfer, trust delegation, trust inheritance, trust chain, trust path, trust graph, trust network analysis, trust community detection, trust clustering, trust similarity, trust distance, trust proximity, trust relationship, trust connection, trust link, trust edge, trust node, trust vertex, reputation protocol, reputation system, reputation network, reputation infrastructure, reputation layer, reputation framework, reputation model, reputation algorithm, reputation computation, reputation calculation, reputation score, reputation rating, reputation level, reputation tier, reputation grade, reputation rank, reputation index, reputation metric, reputation indicator, reputation signal, reputation factor, reputation weight, reputation coefficient, reputation threshold, reputation minimum, reputation maximum, reputation average, reputation median, reputation distribution, reputation aggregation, reputation normalization, reputation scaling, reputation decay, reputation growth, reputation accumulation, reputation history, reputation timeline, reputation evolution, reputation trajectory, reputation prediction, reputation forecast, reputation estimation, reputation inference, reputation derivation, reputation propagation, reputation transfer, reputation delegation, reputation inheritance, reputation chain, reputation path, reputation graph, reputation network analysis, reputation community detection, reputation clustering, reputation similarity, reputation distance, reputation proximity, reputation relationship, reputation connection, reputation link, feedback protocol, feedback system, feedback network, feedback infrastructure, feedback layer, feedback framework, feedback model, feedback algorithm, feedback computation, feedback calculation, feedback score, feedback rating, feedback level, feedback tier, feedback grade, feedback rank, feedback index, feedback metric, feedback indicator, feedback signal, feedback factor, feedback weight, feedback coefficient, feedback threshold, feedback minimum, feedback maximum, feedback average, feedback median, feedback distribution, feedback aggregation, feedback normalization, feedback scaling, review system, rating system, scoring system, ranking system, evaluation system, assessment system, appraisal system, judgment system, quality assurance, quality control, quality metrics, quality standards, quality benchmarks, performance metrics, performance indicators, performance benchmarks, performance standards, performance evaluation, performance assessment, performance monitoring, performance tracking, performance analytics, performance reporting, performance dashboard

## Extended Validation & Verification Terms

validation protocol, validation system, validation network, validation infrastructure, validation layer, validation framework, validation model, validation algorithm, validation computation, validation process, validation procedure, validation workflow, validation pipeline, validation chain, validation sequence, validation step, validation stage, validation phase, validation checkpoint, validation gate, validation barrier, validation filter, validation criteria, validation rules, validation logic, validation conditions, validation requirements, validation specifications, validation standards, validation benchmarks, validation metrics, validation indicators, validation signals, validation evidence, validation proof, validation attestation, validation certification, validation confirmation, validation approval, validation acceptance, validation rejection, validation failure, validation success, validation result, validation outcome, validation report, validation log, validation audit, validation trace, validation record, validation history, verification protocol, verification system, verification network, verification infrastructure, verification layer, verification framework, verification model, verification algorithm, verification computation, verification process, verification procedure, verification workflow, verification pipeline, verification chain, verification sequence, verification step, verification stage, verification phase, verification checkpoint, verification gate, verification barrier, verification filter, verification criteria, verification rules, verification logic, verification conditions, verification requirements, verification specifications, verification standards, verification benchmarks, verification metrics, verification indicators, verification signals, verification evidence, verification proof, verification attestation, verification certification, verification confirmation, verification approval, verification acceptance, verification rejection, verification failure, verification success, verification result, verification outcome, verification report, verification log, verification audit, verification trace, verification record, verification history, cryptographic verification, mathematical verification, formal verification, automated verification, manual verification, human verification, machine verification, AI verification, hybrid verification, multi-party verification, distributed verification, decentralized verification, consensus verification, probabilistic verification, deterministic verification, real-time verification, batch verification, streaming verification, incremental verification, partial verification, complete verification, exhaustive verification, sampling verification, statistical verification, heuristic verification, rule-based verification, model-based verification, data-driven verification, evidence-based verification, proof-based verification, attestation-based verification, signature-based verification, hash-based verification, merkle verification, zero-knowledge verification, ZK verification, zkSNARK, zkSTARK, PLONK, Groth16, recursive proof, proof composition, proof aggregation, proof batching, proof compression, proof generation, proof verification, prover, verifier, trusted setup, universal setup, transparent setup, TEE verification, SGX verification, TDX verification, SEV verification, enclave verification, secure enclave, hardware security, hardware attestation, remote attestation, local attestation, platform attestation, application attestation, code attestation, data attestation, execution attestation, result attestation

## Extended Payment & Commerce Terms

payment protocol, payment system, payment network, payment infrastructure, payment layer, payment framework, payment model, payment algorithm, payment computation, payment process, payment procedure, payment workflow, payment pipeline, payment chain, payment sequence, payment step, payment stage, payment phase, payment gateway, payment processor, payment provider, payment service, payment solution, payment platform, payment application, payment interface, payment API, payment SDK, payment integration, payment compatibility, payment interoperability, payment standardization, payment normalization, payment harmonization, payment settlement, payment clearing, payment reconciliation, payment confirmation, payment verification, payment validation, payment authorization, payment authentication, payment security, payment privacy, payment transparency, payment accountability, payment compliance, payment regulation, payment governance, payment audit, payment reporting, payment analytics, payment monitoring, payment tracking, payment logging, payment history, payment record, payment receipt, payment invoice, payment statement, payment notification, payment alert, payment reminder, payment schedule, payment recurring, payment subscription, payment one-time, payment instant, payment delayed, payment batch, payment streaming, payment conditional, payment escrow, payment refund, payment chargeback, payment dispute, payment resolution, micropayment protocol, micropayment system, micropayment network, micropayment infrastructure, nanopayment, minipayment, small payment, fractional payment, partial payment, incremental payment, progressive payment, milestone payment, completion payment, success payment, performance payment, outcome payment, result payment, delivery payment, service payment, product payment, subscription payment, usage payment, consumption payment, metered payment, measured payment, tracked payment, verified payment, validated payment, confirmed payment, settled payment, cleared payment, finalized payment, irreversible payment, reversible payment, conditional payment, unconditional payment, guaranteed payment, insured payment, secured payment, unsecured payment, collateralized payment, uncollateralized payment, stablecoin payment, USDC payment, USDT payment, DAI payment, FRAX payment, LUSD payment, ETH payment, Ether payment, native token payment, ERC-20 payment, token payment, crypto payment, cryptocurrency payment, digital payment, electronic payment, online payment, internet payment, web payment, mobile payment, in-app payment, embedded payment, invisible payment, seamless payment, frictionless payment, instant payment, real-time payment, near-instant payment, fast payment, quick payment, rapid payment, speedy payment, efficient payment, low-cost payment, cheap payment, affordable payment, economical payment, cost-effective payment, value payment, premium payment, standard payment, basic payment, free payment, zero-fee payment, low-fee payment, minimal-fee payment, reduced-fee payment, discounted payment, promotional payment, incentivized payment, rewarded payment, cashback payment, rebate payment, bonus payment, tip payment, donation payment, contribution payment, support payment, funding payment, investment payment, capital payment, equity payment, debt payment, loan payment, credit payment, debit payment, prepaid payment, postpaid payment, pay-as-you-go payment, pay-per-use payment, pay-per-request payment, pay-per-call payment, pay-per-query payment, pay-per-task payment, pay-per-job payment, pay-per-result payment, pay-per-outcome payment, pay-per-success payment, pay-per-completion payment, pay-per-delivery payment, pay-per-service payment, pay-per-product payment, pay-per-access payment, pay-per-view payment, pay-per-download payment, pay-per-stream payment, pay-per-minute payment, pay-per-second payment, pay-per-byte payment, pay-per-token payment, pay-per-inference payment, pay-per-generation payment, pay-per-response payment, pay-per-answer payment, pay-per-solution payment, pay-per-recommendation payment, pay-per-prediction payment, pay-per-analysis payment, pay-per-insight payment, pay-per-report payment

## Extended Discovery & Registry Terms

discovery protocol, discovery system, discovery network, discovery infrastructure, discovery layer, discovery framework, discovery model, discovery algorithm, discovery computation, discovery process, discovery procedure, discovery workflow, discovery pipeline, discovery chain, discovery sequence, discovery step, discovery stage, discovery phase, discovery mechanism, discovery method, discovery technique, discovery approach, discovery strategy, discovery tactic, discovery pattern, discovery template, discovery schema, discovery format, discovery standard, discovery specification, discovery interface, discovery API, discovery SDK, discovery tool, discovery utility, discovery library, discovery module, discovery component, discovery extension, discovery plugin, discovery addon, discovery integration, discovery compatibility, discovery interoperability, discovery standardization, discovery normalization, discovery harmonization, registry protocol, registry system, registry network, registry infrastructure, registry layer, registry framework, registry model, registry algorithm, registry computation, registry process, registry procedure, registry workflow, registry pipeline, registry chain, registry sequence, registry step, registry stage, registry phase, registry mechanism, registry method, registry technique, registry approach, registry strategy, registry tactic, registry pattern, registry template, registry schema, registry format, registry standard, registry specification, registry interface, registry API, registry SDK, registry tool, registry utility, registry library, registry module, registry component, registry extension, registry plugin, registry addon, registry integration, registry compatibility, registry interoperability, registry standardization, registry normalization, registry harmonization, agent catalog, agent directory, agent index, agent database, agent repository, agent store, agent hub, agent center, agent portal, agent gateway, agent aggregator, agent collector, agent curator, agent organizer, agent manager, agent administrator, agent operator, agent controller, agent supervisor, agent monitor, agent tracker, agent watcher, agent observer, agent listener, agent subscriber, agent publisher, agent broadcaster, agent announcer, agent advertiser, agent promoter, agent marketer, agent distributor, agent connector, agent linker, agent bridge, agent router, agent dispatcher, agent scheduler, agent allocator, agent balancer, agent optimizer, agent enhancer, agent improver, agent upgrader, agent updater, agent maintainer, agent supporter, agent helper, agent assistant, agent advisor, agent consultant, agent expert, agent specialist, agent professional, agent practitioner, agent implementer, agent developer, agent builder, agent creator, agent designer, agent architect, agent engineer, agent programmer, agent coder, agent hacker, agent maker, agent producer, agent manufacturer, agent provider, agent supplier, agent vendor, agent seller, agent buyer, agent consumer, agent user, agent customer, agent client, agent subscriber, agent member, agent participant, agent contributor, agent collaborator, agent partner, agent ally, agent friend, agent colleague, agent peer, agent neighbor, agent community, agent ecosystem, agent network, agent cluster, agent group, agent team, agent squad, agent unit, agent division, agent department, agent organization, agent company, agent enterprise, agent business, agent startup, agent project, agent initiative, agent program, agent campaign, agent movement, agent revolution, agent evolution, agent transformation, agent innovation, agent disruption, agent advancement, agent progress, agent growth, agent expansion, agent scaling, agent multiplication, agent proliferation, agent adoption, agent acceptance, agent integration, agent incorporation, agent assimilation, agent absorption, agent merger, agent acquisition, agent partnership, agent collaboration, agent cooperation, agent coordination, agent synchronization, agent harmonization, agent alignment, agent optimization, agent maximization, agent minimization, agent efficiency, agent effectiveness, agent productivity, agent performance, agent quality, agent reliability, agent availability, agent accessibility, agent usability, agent scalability, agent flexibility, agent adaptability, agent extensibility, agent maintainability, agent sustainability, agent durability, agent longevity, agent persistence, agent continuity, agent stability, agent security, agent safety, agent privacy, agent confidentiality, agent integrity, agent authenticity, agent validity, agent accuracy, agent precision, agent correctness, agent completeness, agent consistency, agent coherence, agent clarity, agent simplicity, agent elegance, agent beauty, agent aesthetics

## Extended Technical Implementation Terms

smart contract development, smart contract programming, smart contract coding, smart contract writing, smart contract design, smart contract architecture, smart contract pattern, smart contract template, smart contract library, smart contract framework, smart contract toolkit, smart contract suite, smart contract collection, smart contract set, smart contract bundle, smart contract package, smart contract module, smart contract component, smart contract function, smart contract method, smart contract procedure, smart contract routine, smart contract subroutine, smart contract logic, smart contract algorithm, smart contract computation, smart contract calculation, smart contract operation, smart contract action, smart contract transaction, smart contract call, smart contract invocation, smart contract execution, smart contract deployment, smart contract migration, smart contract upgrade, smart contract update, smart contract patch, smart contract fix, smart contract bug, smart contract vulnerability, smart contract exploit, smart contract attack, smart contract defense, smart contract protection, smart contract security, smart contract audit, smart contract review, smart contract analysis, smart contract testing, smart contract verification, smart contract validation, smart contract certification, smart contract documentation, smart contract specification, smart contract interface, smart contract ABI, smart contract bytecode, smart contract opcode, smart contract gas, smart contract optimization, smart contract efficiency, smart contract performance, smart contract scalability, smart contract reliability, smart contract availability, smart contract maintainability, smart contract upgradeability, smart contract proxy, smart contract implementation, smart contract storage, smart contract memory, smart contract stack, smart contract heap, smart contract variable, smart contract constant, smart contract immutable, smart contract state, smart contract event, smart contract log, smart contract emit, smart contract modifier, smart contract require, smart contract assert, smart contract revert, smart contract error, smart contract exception, smart contract fallback, smart contract receive, smart contract payable, smart contract view, smart contract pure, smart contract external, smart contract internal, smart contract public, smart contract private, smart contract virtual, smart contract override, smart contract abstract, smart contract interface, smart contract library, smart contract import, smart contract inheritance, smart contract composition, smart contract delegation, smart contract proxy pattern, UUPS proxy, transparent proxy, beacon proxy, minimal proxy, clone factory, diamond pattern, EIP-2535, upgradeable contract, upgradeable proxy, upgrade mechanism, upgrade process, upgrade procedure, upgrade workflow, upgrade pipeline, upgrade chain, upgrade sequence, upgrade step, upgrade stage, upgrade phase, upgrade checkpoint, upgrade gate, upgrade barrier, upgrade filter, upgrade criteria, upgrade rules, upgrade logic, upgrade conditions, upgrade requirements, upgrade specifications, upgrade standards, upgrade benchmarks, upgrade metrics, upgrade indicators, upgrade signals, upgrade evidence, upgrade proof, upgrade attestation, upgrade certification, upgrade confirmation, upgrade approval, upgrade acceptance, upgrade rejection, upgrade failure, upgrade success, upgrade result, upgrade outcome, upgrade report, upgrade log, upgrade audit, upgrade trace, upgrade record, upgrade history

## Extended Use Case Terms

DeFi agent, DeFi bot, DeFi automation, DeFi yield, DeFi farming, DeFi staking, DeFi lending, DeFi borrowing, DeFi trading, DeFi arbitrage, DeFi liquidation, DeFi governance, DeFi voting, DeFi proposal, DeFi treasury, DeFi vault, DeFi pool, DeFi liquidity, DeFi swap, DeFi exchange, DeFi DEX, DeFi AMM, DeFi orderbook, DeFi perpetual, DeFi options, DeFi futures, DeFi derivatives, DeFi insurance, DeFi prediction, DeFi oracle, DeFi bridge, DeFi cross-chain, DeFi multichain, DeFi aggregator, DeFi router, DeFi optimizer, DeFi maximizer, DeFi compounder, DeFi harvester, DeFi rebalancer, DeFi hedger, DeFi protector, DeFi guardian, DeFi sentinel, DeFi watchdog, DeFi monitor, DeFi tracker, DeFi analyzer, DeFi reporter, DeFi alerter, DeFi notifier, trading agent, trading bot, trading automation, trading algorithm, trading strategy, trading signal, trading indicator, trading pattern, trading trend, trading momentum, trading volume, trading liquidity, trading spread, trading slippage, trading execution, trading order, trading limit, trading market, trading stop, trading take-profit, trading stop-loss, trading position, trading portfolio, trading balance, trading equity, trading margin, trading leverage, trading risk, trading reward, trading return, trading profit, trading loss, trading performance, trading history, trading record, trading log, trading report, trading analytics, trading dashboard, trading interface, trading API, trading SDK, trading integration, trading compatibility, trading interoperability, data agent, data bot, data automation, data collection, data aggregation, data processing, data transformation, data cleaning, data validation, data verification, data enrichment, data augmentation, data annotation, data labeling, data classification, data categorization, data clustering, data segmentation, data filtering, data sorting, data ranking, data scoring, data rating, data evaluation, data assessment, data analysis, data analytics, data visualization, data reporting, data dashboard, data interface, data API, data SDK, data integration, data compatibility, data interoperability, research agent, research bot, research automation, research collection, research aggregation, research processing, research analysis, research synthesis, research summarization, research extraction, research identification, research discovery, research exploration, research investigation, research examination, research evaluation, research assessment, research review, research critique, research comparison, research benchmarking, research testing, research experimentation, research validation, research verification, research confirmation, research publication, research dissemination, research communication, research collaboration, research cooperation, research coordination, customer service agent, customer support agent, customer success agent, customer experience agent, customer engagement agent, customer retention agent, customer acquisition agent, customer onboarding agent, customer training agent, customer education agent, sales agent, marketing agent, advertising agent, promotion agent, outreach agent, engagement agent, conversion agent, retention agent, loyalty agent, advocacy agent, referral agent, partnership agent, collaboration agent, cooperation agent, coordination agent, communication agent, messaging agent, notification agent, alert agent, reminder agent, scheduling agent, calendar agent, booking agent, reservation agent, appointment agent, meeting agent, conference agent, event agent, webinar agent, presentation agent, demonstration agent, tutorial agent, training agent, education agent, learning agent, teaching agent, coaching agent, mentoring agent, advising agent, consulting agent, expert agent, specialist agent, professional agent, practitioner agent, implementer agent, developer agent, builder agent, creator agent, designer agent, architect agent, engineer agent, programmer agent, coder agent, hacker agent, maker agent, producer agent, manufacturer agent, provider agent, supplier agent, vendor agent, content agent, writing agent, copywriting agent, editing agent, proofreading agent, translation agent, localization agent, transcription agent, summarization agent, extraction agent, generation agent, creation agent, production agent, publication agent, distribution agent, syndication agent, aggregation agent, curation agent, recommendation agent, personalization agent, customization agent, optimization agent, enhancement agent, improvement agent, refinement agent, polishing agent, finishing agent, completion agent, delivery agent, fulfillment agent, execution agent, implementation agent, deployment agent, integration agent, configuration agent, setup agent, installation agent, maintenance agent, support agent, troubleshooting agent, debugging agent, fixing agent, patching agent, updating agent, upgrading agent, migrating agent, transitioning agent, transforming agent, converting agent, adapting agent, adjusting agent, modifying agent, changing agent, evolving agent, growing agent, expanding agent, scaling agent, multiplying agent, proliferating agent

---

## Industry & Vertical Keywords

healthcare agent, medical agent, clinical agent, diagnostic agent, treatment agent, pharmaceutical agent, drug discovery agent, patient agent, doctor agent, nurse agent, hospital agent, clinic agent, telemedicine agent, telehealth agent, health monitoring agent, wellness agent, fitness agent, nutrition agent, mental health agent, therapy agent, counseling agent, psychology agent, psychiatry agent, insurance agent, claims agent, underwriting agent, risk assessment agent, actuarial agent, policy agent, coverage agent, benefits agent, reimbursement agent, billing agent, invoicing agent, accounting agent, bookkeeping agent, tax agent, audit agent, compliance agent, regulatory agent, legal agent, contract agent, agreement agent, negotiation agent, dispute agent, arbitration agent, mediation agent, litigation agent, court agent, judge agent, lawyer agent, attorney agent, paralegal agent, notary agent, real estate agent, property agent, housing agent, rental agent, lease agent, mortgage agent, appraisal agent, valuation agent, inspection agent, construction agent, architecture agent, engineering agent, design agent, planning agent, zoning agent, permit agent, licensing agent, certification agent, accreditation agent, quality agent, testing agent, inspection agent, manufacturing agent, production agent, assembly agent, logistics agent, supply chain agent, inventory agent, warehouse agent, shipping agent, delivery agent, transportation agent, fleet agent, routing agent, dispatch agent, tracking agent, monitoring agent, surveillance agent, security agent, protection agent, safety agent, emergency agent, disaster agent, crisis agent, response agent, recovery agent, restoration agent, maintenance agent, repair agent, service agent, support agent, helpdesk agent, ticketing agent, incident agent, problem agent, change agent, release agent, deployment agent, configuration agent, asset agent, resource agent, capacity agent, performance agent, optimization agent, efficiency agent, productivity agent, automation agent, integration agent, migration agent, transformation agent, modernization agent, innovation agent, research agent, development agent, experimentation agent, prototyping agent, testing agent, validation agent, verification agent, certification agent, documentation agent, training agent, education agent, learning agent, teaching agent, tutoring agent, mentoring agent, coaching agent, consulting agent, advisory agent, strategy agent, planning agent, forecasting agent, prediction agent, analysis agent, reporting agent, visualization agent, dashboard agent, monitoring agent, alerting agent, notification agent, communication agent, collaboration agent, coordination agent, scheduling agent, calendar agent, meeting agent, conference agent, presentation agent, demonstration agent, proposal agent, quotation agent, estimation agent, budgeting agent, costing agent, pricing agent, discount agent, promotion agent, marketing agent, advertising agent, branding agent, campaign agent, outreach agent, engagement agent, conversion agent, retention agent, loyalty agent, advocacy agent, referral agent, partnership agent, alliance agent, consortium agent, federation agent, network agent, community agent, ecosystem agent, platform agent, marketplace agent, exchange agent, trading agent, brokerage agent, clearing agent, settlement agent, custody agent, escrow agent, trust agent, fiduciary agent, investment agent, portfolio agent, wealth agent, asset management agent, fund agent, hedge fund agent, mutual fund agent, ETF agent, index agent, bond agent, equity agent, derivative agent, option agent, future agent, swap agent, commodity agent, currency agent, forex agent, crypto agent, bitcoin agent, ethereum agent, altcoin agent, token agent, NFT agent, DeFi agent, yield agent, staking agent, lending agent, borrowing agent, liquidity agent, AMM agent, DEX agent, CEX agent, bridge agent, oracle agent, governance agent, DAO agent, treasury agent, proposal agent, voting agent, delegation agent, staking agent, validator agent, node agent, miner agent, block agent, transaction agent, gas agent, fee agent, reward agent, penalty agent, slashing agent, epoch agent, finality agent, consensus agent, proof agent, attestation agent, signature agent, encryption agent, decryption agent, hashing agent, merkle agent, trie agent, state agent, storage agent, memory agent, cache agent, database agent, query agent, index agent, search agent, retrieval agent, ranking agent, recommendation agent, personalization agent, segmentation agent, targeting agent, attribution agent, analytics agent, metrics agent, KPI agent, OKR agent, goal agent, objective agent, milestone agent, deadline agent, timeline agent, roadmap agent, backlog agent, sprint agent, iteration agent, release agent, version agent, changelog agent, documentation agent, specification agent, requirement agent, user story agent, acceptance criteria agent, test case agent, bug agent, issue agent, ticket agent, task agent, subtask agent, epic agent, feature agent, enhancement agent, improvement agent, optimization agent, refactoring agent, debugging agent, profiling agent, benchmarking agent, load testing agent, stress testing agent, penetration testing agent, security testing agent, vulnerability agent, exploit agent, patch agent, hotfix agent, update agent, upgrade agent, migration agent, rollback agent, backup agent, restore agent, disaster recovery agent, business continuity agent, high availability agent, fault tolerance agent, redundancy agent, replication agent, synchronization agent, consistency agent, durability agent, availability agent, partition tolerance agent, CAP agent, ACID agent, BASE agent, eventual consistency agent, strong consistency agent, linearizability agent, serializability agent, isolation agent, atomicity agent, transaction agent, commit agent, rollback agent, savepoint agent, checkpoint agent, snapshot agent, backup agent, archive agent, retention agent, lifecycle agent, expiration agent, deletion agent, purging agent, cleanup agent, garbage collection agent, memory management agent, resource management agent, capacity planning agent, scaling agent, autoscaling agent, load balancing agent, traffic management agent, rate limiting agent, throttling agent, circuit breaker agent, retry agent, timeout agent, fallback agent, graceful degradation agent, feature flag agent, A/B testing agent, canary deployment agent, blue-green deployment agent, rolling deployment agent, immutable deployment agent, infrastructure agent, platform agent, container agent, kubernetes agent, docker agent, serverless agent, function agent, lambda agent, edge agent, CDN agent, caching agent, proxy agent, gateway agent, API gateway agent, service mesh agent, sidecar agent, envoy agent, istio agent, linkerd agent, consul agent, vault agent, terraform agent, ansible agent, puppet agent, chef agent, saltstack agent, cloudformation agent, pulumi agent, crossplane agent, argocd agent, fluxcd agent, jenkins agent, github actions agent, gitlab CI agent, circleci agent, travisci agent, drone agent, tekton agent, spinnaker agent, harness agent, octopus agent, buildkite agent, teamcity agent, bamboo agent, azure devops agent, AWS codepipeline agent, GCP cloud build agent, monitoring agent, observability agent, logging agent, tracing agent, metrics agent, alerting agent, incident management agent, on-call agent, pagerduty agent, opsgenie agent, victorops agent, datadog agent, newrelic agent, dynatrace agent, splunk agent, elastic agent, prometheus agent, grafana agent, loki agent, tempo agent, jaeger agent, zipkin agent, opentelemetry agent, sentry agent, rollbar agent, bugsnag agent, honeybadger agent, raygun agent, airbrake agent

## Technology Stack Keywords

JavaScript agent, TypeScript agent, Python agent, Go agent, Rust agent, Java agent, Kotlin agent, Swift agent, Objective-C agent, C++ agent, C# agent, Ruby agent, PHP agent, Scala agent, Clojure agent, Elixir agent, Erlang agent, Haskell agent, OCaml agent, F# agent, Dart agent, Flutter agent, React agent, Vue agent, Angular agent, Svelte agent, Solid agent, Next.js agent, Nuxt agent, Remix agent, Gatsby agent, Astro agent, Qwik agent, Fresh agent, SvelteKit agent, Express agent, Fastify agent, Koa agent, Hapi agent, NestJS agent, Adonis agent, Sails agent, Meteor agent, Django agent, Flask agent, FastAPI agent, Starlette agent, Tornado agent, Pyramid agent, Bottle agent, Falcon agent, Sanic agent, Quart agent, Rails agent, Sinatra agent, Hanami agent, Roda agent, Grape agent, Spring agent, Quarkus agent, Micronaut agent, Vert.x agent, Play agent, Akka agent, Lagom agent, ASP.NET agent, Blazor agent, MAUI agent, Xamarin agent, Unity agent, Godot agent, Unreal agent, Bevy agent, Amethyst agent, ggez agent, macroquad agent, Raylib agent, SDL agent, SFML agent, OpenGL agent, Vulkan agent, DirectX agent, Metal agent, WebGL agent, WebGPU agent, Three.js agent, Babylon.js agent, PlayCanvas agent, A-Frame agent, React Three Fiber agent, Pixi.js agent, Phaser agent, Cocos agent, Defold agent, Construct agent, GameMaker agent, RPG Maker agent, Twine agent, Ink agent, Yarn Spinner agent, Dialogflow agent, Rasa agent, Botpress agent, Microsoft Bot Framework agent, Amazon Lex agent, IBM Watson agent, Google Dialogflow agent, Wit.ai agent, Snips agent, Mycroft agent, Jasper agent, Leon agent, Hugging Face agent, OpenAI agent, Anthropic agent, Cohere agent, AI21 agent, Stability AI agent, Midjourney agent, DALL-E agent, Stable Diffusion agent, Imagen agent, Gemini agent, Claude agent, GPT agent, LLaMA agent, Mistral agent, Mixtral agent, Phi agent, Qwen agent, Yi agent, DeepSeek agent, Falcon agent, MPT agent, BLOOM agent, OPT agent, Pythia agent, Cerebras agent, Inflection agent, Adept agent, Character.AI agent, Poe agent, Perplexity agent, You.com agent, Neeva agent, Kagi agent, Brave Search agent, DuckDuckGo agent, Startpage agent, Ecosia agent, Qwant agent, Mojeek agent, Yandex agent, Baidu agent, Naver agent, Seznam agent, Sogou agent

## Emerging Technology Keywords

quantum computing agent, quantum machine learning agent, quantum optimization agent, quantum simulation agent, quantum cryptography agent, post-quantum agent, lattice-based agent, hash-based agent, code-based agent, isogeny-based agent, multivariate agent, neuromorphic agent, spiking neural network agent, memristor agent, photonic agent, optical computing agent, DNA computing agent, molecular computing agent, biological computing agent, wetware agent, biocomputing agent, synthetic biology agent, gene editing agent, CRISPR agent, mRNA agent, protein folding agent, AlphaFold agent, drug discovery agent, virtual screening agent, molecular dynamics agent, computational chemistry agent, materials science agent, nanotechnology agent, metamaterials agent, 2D materials agent, graphene agent, quantum dots agent, nanoparticles agent, nanorobots agent, nanomedicine agent, targeted delivery agent, biosensors agent, wearables agent, implantables agent, brain-computer interface agent, neural interface agent, Neuralink agent, EEG agent, fMRI agent, PET agent, MEG agent, TMS agent, tDCS agent, optogenetics agent, chemogenetics agent, connectomics agent, brain mapping agent, cognitive computing agent, affective computing agent, emotion AI agent, sentiment analysis agent, opinion mining agent, social listening agent, brand monitoring agent, reputation management agent, crisis communication agent, public relations agent, media monitoring agent, press agent, journalist agent, editor agent, writer agent, author agent, content creator agent, influencer agent, streamer agent, YouTuber agent, TikToker agent, podcaster agent, blogger agent, vlogger agent, photographer agent, videographer agent, animator agent, illustrator agent, graphic designer agent, UI designer agent, UX designer agent, product designer agent, industrial designer agent, fashion designer agent, interior designer agent, architect agent, landscape architect agent, urban planner agent, city planner agent, transportation planner agent, traffic agent, autonomous vehicle agent, self-driving agent, ADAS agent, V2X agent, connected vehicle agent, smart transportation agent, smart city agent, smart grid agent, smart meter agent, smart home agent, smart building agent, smart factory agent, Industry 4.0 agent, IoT agent, IIoT agent, edge computing agent, fog computing agent, mist computing agent, cloudlet agent, mobile edge agent, MEC agent, NOMA agent, massive MIMO agent, beamforming agent, millimeter wave agent, terahertz agent, 6G agent, 5G agent, LTE agent, NB-IoT agent, LoRa agent, Sigfox agent, Zigbee agent, Z-Wave agent, Thread agent, Matter agent, HomeKit agent, Alexa agent, Google Home agent, SmartThings agent, Home Assistant agent, OpenHAB agent, Domoticz agent, Hubitat agent, Homey agent, Tuya agent, eWeLink agent, Sonoff agent, Shelly agent, Tasmota agent, ESPHome agent, WLED agent, Zigbee2MQTT agent, deCONZ agent, ZHA agent, Philips Hue agent, IKEA Tradfri agent, Aqara agent, Xiaomi agent, Yeelight agent, Nanoleaf agent, LIFX agent, TP-Link Kasa agent, Wyze agent, Ring agent, Nest agent, Ecobee agent, Honeywell agent, Emerson agent, Carrier agent, Trane agent, Lennox agent, Daikin agent, Mitsubishi Electric agent, LG agent, Samsung agent, Bosch agent, Siemens agent, ABB agent, Schneider Electric agent, Rockwell agent, Emerson agent, Honeywell agent, Yokogawa agent, Endress+Hauser agent, SICK agent, Pepperl+Fuchs agent, Balluff agent, ifm agent, Banner agent, Turck agent, Omron agent, Keyence agent, Cognex agent, Basler agent, FLIR agent, Teledyne agent, Allied Vision agent, JAI agent, IDS agent, Baumer agent, Stemmer agent, MVTec agent, Matrox agent, National Instruments agent, Beckhoff agent, Phoenix Contact agent, Wago agent, Weidmuller agent, Murrelektronik agent, Pilz agent, SICK agent, Leuze agent, Datalogic agent, Honeywell agent, Zebra agent, SATO agent, Citizen agent, TSC agent, Godex agent, Printronix agent, Epson agent, Brother agent, DYMO agent, Rollo agent, Munbyn agent, iDPRT agent, HPRT agent

## Business & Enterprise Keywords

enterprise agent, corporate agent, business agent, commercial agent, industrial agent, manufacturing agent, retail agent, wholesale agent, distribution agent, logistics agent, supply chain agent, procurement agent, sourcing agent, purchasing agent, vendor management agent, supplier agent, contractor agent, subcontractor agent, freelancer agent, consultant agent, advisor agent, strategist agent, analyst agent, researcher agent, scientist agent, engineer agent, developer agent, programmer agent, architect agent, designer agent, artist agent, creative agent, copywriter agent, content strategist agent, SEO agent, SEM agent, PPC agent, social media agent, community manager agent, brand ambassador agent, spokesperson agent, evangelist agent, advocate agent, champion agent, mentor agent, coach agent, trainer agent, instructor agent, professor agent, teacher agent, tutor agent, educator agent, facilitator agent, moderator agent, host agent, presenter agent, speaker agent, panelist agent, guest agent, expert agent, specialist agent, generalist agent, polymath agent, renaissance agent, versatile agent, adaptive agent, flexible agent, agile agent, lean agent, efficient agent, effective agent, productive agent, performant agent, scalable agent, reliable agent, available agent, durable agent, resilient agent, robust agent, stable agent, secure agent, safe agent, compliant agent, regulated agent, certified agent, accredited agent, licensed agent, authorized agent, approved agent, verified agent, validated agent, tested agent, audited agent, reviewed agent, assessed agent, evaluated agent, measured agent, quantified agent, qualified agent, skilled agent, experienced agent, knowledgeable agent, informed agent, educated agent, trained agent, certified agent, professional agent, expert agent, master agent, senior agent, principal agent, lead agent, chief agent, head agent, director agent, manager agent, supervisor agent, coordinator agent, administrator agent, operator agent, technician agent, specialist agent, analyst agent, associate agent, assistant agent, intern agent, trainee agent, apprentice agent, junior agent, mid-level agent, intermediate agent, advanced agent, expert agent, senior agent, staff agent, contractor agent, consultant agent, freelance agent, part-time agent, full-time agent, remote agent, hybrid agent, onsite agent, offshore agent, nearshore agent, outsourced agent, insourced agent, managed agent, unmanaged agent, autonomous agent, semi-autonomous agent, supervised agent, unsupervised agent, reinforcement agent, self-learning agent, adaptive agent, evolving agent, improving agent, optimizing agent, maximizing agent, minimizing agent, balancing agent, tradeoff agent, pareto agent, multi-objective agent, constraint agent, bounded agent, limited agent, unlimited agent, infinite agent, finite agent, discrete agent, continuous agent, hybrid agent, mixed agent, ensemble agent, committee agent, voting agent, consensus agent, majority agent, plurality agent, weighted agent, ranked agent, preference agent, utility agent, reward agent, penalty agent, cost agent, benefit agent, value agent, worth agent, price agent, fee agent, charge agent, rate agent, tariff agent, duty agent, tax agent, levy agent, surcharge agent, premium agent, discount agent, rebate agent, refund agent, credit agent, debit agent, balance agent, account agent, ledger agent, journal agent, record agent, entry agent, transaction agent, transfer agent, payment agent, receipt agent, invoice agent, bill agent, statement agent, report agent, summary agent, detail agent, breakdown agent, itemization agent, categorization agent, classification agent, taxonomy agent, ontology agent, schema agent, model agent, framework agent, architecture agent, design agent, pattern agent, template agent, blueprint agent, plan agent, strategy agent, tactic agent, technique agent, method agent, process agent, procedure agent, workflow agent, pipeline agent, chain agent, sequence agent, order agent, priority agent, queue agent, stack agent, heap agent, tree agent, graph agent, network agent, mesh agent, grid agent, cluster agent, pool agent, farm agent, fleet agent, swarm agent, hive agent, colony agent, pack agent, herd agent, flock agent, school agent, pod agent, pride agent, troop agent, band agent, gang agent, crew agent, team agent, squad agent, unit agent, division agent, department agent, branch agent, office agent, location agent, site agent, facility agent, plant agent, factory agent, warehouse agent, depot agent, hub agent, center agent, station agent, terminal agent, port agent, dock agent, pier agent, wharf agent, quay agent, berth agent, slip agent, marina agent, harbor agent, airport agent, heliport agent, spaceport agent, launchpad agent, runway agent, taxiway agent, apron agent, gate agent, terminal agent, concourse agent, lounge agent, checkpoint agent, security agent, customs agent, immigration agent, passport agent, visa agent, permit agent, license agent, registration agent, certification agent, accreditation agent, qualification agent, credential agent, badge agent, ID agent, identity agent, authentication agent, authorization agent, access agent, permission agent, role agent, privilege agent, right agent, entitlement agent, claim agent, assertion agent, declaration agent, statement agent, expression agent, formula agent, equation agent, function agent, variable agent, constant agent, parameter agent, argument agent, input agent, output agent, result agent, return agent, response agent, request agent, query agent, command agent, instruction agent, directive agent, order agent, message agent, signal agent, event agent, trigger agent, action agent, reaction agent, effect agent, consequence agent, outcome agent, impact agent, influence agent, change agent, transformation agent, transition agent, conversion agent, migration agent, evolution agent, revolution agent, disruption agent, innovation agent, invention agent, discovery agent, breakthrough agent, advancement agent, progress agent, growth agent, expansion agent, scaling agent, multiplication agent, proliferation agent, adoption agent, acceptance agent, integration agent, incorporation agent, assimilation agent, absorption agent, merger agent, acquisition agent, partnership agent, collaboration agent, cooperation agent, coordination agent, synchronization agent, harmonization agent, alignment agent, optimization agent, maximization agent, minimization agent, efficiency agent, effectiveness agent, productivity agent, performance agent, quality agent, reliability agent, availability agent, accessibility agent, usability agent, scalability agent, flexibility agent, adaptability agent, extensibility agent, maintainability agent, sustainability agent, durability agent, longevity agent, persistence agent, continuity agent, stability agent, security agent, safety agent, privacy agent, confidentiality agent, integrity agent, authenticity agent, validity agent, accuracy agent, precision agent, correctness agent, completeness agent, consistency agent, coherence agent, clarity agent, simplicity agent, elegance agent, beauty agent, aesthetics agent

---

## Web3 & Crypto Extended Keywords

blockchain agent, distributed ledger agent, consensus mechanism agent, proof of work agent, proof of stake agent, proof of authority agent, proof of history agent, proof of space agent, proof of capacity agent, proof of burn agent, proof of elapsed time agent, delegated proof of stake agent, nominated proof of stake agent, liquid proof of stake agent, bonded proof of stake agent, threshold proof of stake agent, BFT agent, PBFT agent, Tendermint agent, HotStuff agent, DAG agent, hashgraph agent, tangle agent, blockchain trilemma agent, scalability agent, decentralization agent, security agent, layer 1 agent, layer 2 agent, layer 3 agent, sidechain agent, plasma agent, rollup agent, optimistic rollup agent, ZK rollup agent, validium agent, volition agent, data availability agent, data availability sampling agent, DAS agent, erasure coding agent, KZG commitment agent, blob agent, EIP-4844 agent, proto-danksharding agent, danksharding agent, sharding agent, beacon chain agent, execution layer agent, consensus layer agent, merge agent, Shanghai upgrade agent, Cancun upgrade agent, Dencun agent, Pectra agent, Verkle tree agent, stateless client agent, light client agent, full node agent, archive node agent, validator node agent, sentry node agent, RPC node agent, indexer node agent, sequencer agent, proposer agent, builder agent, searcher agent, MEV agent, maximal extractable value agent, frontrunning agent, backrunning agent, sandwich attack agent, arbitrage agent, liquidation agent, just-in-time liquidity agent, order flow agent, private mempool agent, flashbots agent, MEV-boost agent, PBS agent, proposer-builder separation agent, enshrined PBS agent, inclusion list agent, censorship resistance agent, liveness agent, safety agent, finality agent, economic finality agent, social consensus agent, fork choice agent, LMD GHOST agent, Casper FFG agent, inactivity leak agent, slashing agent, whistleblower agent, attestation agent, sync committee agent, withdrawal agent, exit agent, activation agent, effective balance agent, validator lifecycle agent, epoch agent, slot agent, block proposer agent, randao agent, VRF agent, verifiable random function agent, threshold signature agent, BLS signature agent, aggregate signature agent, multi-signature agent, multisig agent, Gnosis Safe agent, Safe agent, social recovery agent, guardian agent, account abstraction agent, ERC-4337 agent, bundler agent, paymaster agent, entry point agent, user operation agent, smart account agent, smart contract wallet agent, MPC wallet agent, HSM agent, hardware wallet agent, cold wallet agent, hot wallet agent, custodial wallet agent, non-custodial wallet agent, self-custody agent, seed phrase agent, mnemonic agent, BIP-39 agent, BIP-32 agent, BIP-44 agent, derivation path agent, HD wallet agent, hierarchical deterministic agent, key derivation agent, private key agent, public key agent, address agent, checksum agent, ENS agent, Ethereum Name Service agent, DNS agent, IPNS agent, content hash agent, avatar agent, text records agent, resolver agent, registrar agent, controller agent, wrapped ETH agent, WETH agent, ERC-20 agent, ERC-721 agent, ERC-1155 agent, ERC-777 agent, ERC-2981 agent, ERC-4626 agent, ERC-6551 agent, token bound account agent, soulbound token agent, SBT agent, ERC-5192 agent, dynamic NFT agent, dNFT agent, composable NFT agent, nested NFT agent, fractional NFT agent, rental NFT agent, ERC-4907 agent, lending NFT agent, staking NFT agent, governance NFT agent, membership NFT agent, access NFT agent, credential NFT agent, certificate NFT agent, badge NFT agent, POAP agent, attendance NFT agent, achievement NFT agent, reward NFT agent, loyalty NFT agent, coupon NFT agent, ticket NFT agent, pass NFT agent, subscription NFT agent, license NFT agent, royalty NFT agent, creator economy agent, creator agent, collector agent, curator agent, gallery agent, museum agent, auction agent, marketplace agent, OpenSea agent, Blur agent, LooksRare agent, X2Y2 agent, Rarible agent, Foundation agent, SuperRare agent, Nifty Gateway agent, Art Blocks agent, generative art agent, on-chain art agent, pixel art agent, PFP agent, profile picture agent, avatar project agent, metaverse agent, virtual world agent, virtual land agent, virtual real estate agent, Decentraland agent, Sandbox agent, Otherside agent, Voxels agent, Somnium Space agent, Spatial agent, Gather agent, virtual event agent, virtual conference agent, virtual meetup agent, virtual office agent, virtual coworking agent, virtual collaboration agent, social token agent, creator coin agent, community token agent, fan token agent, governance token agent, utility token agent, security token agent, wrapped token agent, bridged token agent, synthetic token agent, rebasing token agent, elastic token agent, algorithmic token agent, stablecoin agent, fiat-backed stablecoin agent, crypto-backed stablecoin agent, algorithmic stablecoin agent, fractional stablecoin agent, CDP agent, collateralized debt position agent, vault agent, trove agent, liquidation agent, stability pool agent, redemption agent, peg agent, depeg agent, oracle agent, price oracle agent, Chainlink agent, Band Protocol agent, API3 agent, UMA agent, Tellor agent, Pyth agent, Redstone agent, Chronicle agent, price feed agent, TWAP agent, time-weighted average price agent, VWAP agent, volume-weighted average price agent, spot price agent, fair price agent, reference price agent, index price agent, mark price agent, funding rate agent, perpetual agent, perp agent, futures agent, options agent, structured products agent, vault strategy agent, yield strategy agent, delta neutral agent, basis trade agent, cash and carry agent, funding arbitrage agent, cross-exchange arbitrage agent, CEX-DEX arbitrage agent, triangular arbitrage agent, statistical arbitrage agent, market making agent, liquidity provision agent, concentrated liquidity agent, range order agent, limit order agent, stop order agent, TWAP order agent, iceberg order agent, fill or kill agent, immediate or cancel agent, good til cancelled agent, post only agent, reduce only agent, order book agent, matching engine agent, clearing house agent, settlement layer agent, netting agent, margin agent, cross margin agent, isolated margin agent, portfolio margin agent, initial margin agent, maintenance margin agent, margin call agent, auto-deleveraging agent, ADL agent, insurance fund agent, socialized loss agent, clawback agent, position agent, long position agent, short position agent, leverage agent, notional value agent, unrealized PnL agent, realized PnL agent, funding payment agent, borrowing fee agent, trading fee agent, maker fee agent, taker fee agent, gas fee agent, priority fee agent, base fee agent, EIP-1559 agent, fee market agent, gas auction agent, gas estimation agent, gas optimization agent, gas token agent, gas rebate agent, flashloan agent, flash mint agent, atomic transaction agent, bundle agent, simulation agent, tenderly agent, fork agent, mainnet fork agent, local fork agent, anvil agent, hardhat agent, foundry agent, remix agent, truffle agent, brownie agent, ape agent, slither agent, mythril agent, echidna agent, medusa agent, certora agent, formal verification agent, symbolic execution agent, fuzzing agent, property testing agent, invariant testing agent, differential testing agent, mutation testing agent, coverage agent, gas snapshot agent, storage layout agent, proxy storage agent, diamond storage agent, app storage agent, unstructured storage agent, eternal storage agent, upgradeable storage agent

## AI & Machine Learning Extended Keywords

machine learning agent, deep learning agent, reinforcement learning agent, supervised learning agent, unsupervised learning agent, semi-supervised learning agent, self-supervised learning agent, contrastive learning agent, transfer learning agent, meta-learning agent, few-shot learning agent, zero-shot learning agent, one-shot learning agent, multi-task learning agent, curriculum learning agent, active learning agent, online learning agent, offline learning agent, batch learning agent, incremental learning agent, continual learning agent, lifelong learning agent, federated learning agent, distributed learning agent, parallel learning agent, gradient descent agent, stochastic gradient descent agent, SGD agent, Adam agent, AdamW agent, LAMB agent, LARS agent, RMSprop agent, Adagrad agent, Adadelta agent, momentum agent, Nesterov agent, learning rate agent, learning rate scheduler agent, warmup agent, cosine annealing agent, step decay agent, exponential decay agent, polynomial decay agent, cyclic learning rate agent, one cycle agent, weight decay agent, L1 regularization agent, L2 regularization agent, dropout agent, batch normalization agent, layer normalization agent, group normalization agent, instance normalization agent, spectral normalization agent, weight normalization agent, gradient clipping agent, gradient accumulation agent, mixed precision agent, FP16 agent, BF16 agent, FP8 agent, INT8 agent, INT4 agent, quantization agent, post-training quantization agent, quantization-aware training agent, pruning agent, structured pruning agent, unstructured pruning agent, magnitude pruning agent, movement pruning agent, knowledge distillation agent, teacher-student agent, model compression agent, neural architecture search agent, NAS agent, AutoML agent, hyperparameter optimization agent, Bayesian optimization agent, random search agent, grid search agent, population-based training agent, evolutionary algorithm agent, genetic algorithm agent, particle swarm agent, ant colony agent, simulated annealing agent, neural network agent, feedforward network agent, recurrent network agent, RNN agent, LSTM agent, GRU agent, bidirectional RNN agent, seq2seq agent, encoder-decoder agent, attention mechanism agent, self-attention agent, cross-attention agent, multi-head attention agent, scaled dot-product attention agent, transformer agent, BERT agent, GPT agent, T5 agent, BART agent, XLNet agent, RoBERTa agent, ALBERT agent, DistilBERT agent, ELECTRA agent, DeBERTa agent, Longformer agent, BigBird agent, Performer agent, Linformer agent, Reformer agent, Sparse Transformer agent, Flash Attention agent, Multi-Query Attention agent, Grouped Query Attention agent, Sliding Window Attention agent, Local Attention agent, Global Attention agent, Relative Position agent, Rotary Position Embedding agent, RoPE agent, ALiBi agent, context length agent, context window agent, long context agent, retrieval augmented generation agent, RAG agent, vector database agent, embedding agent, sentence embedding agent, document embedding agent, image embedding agent, multimodal embedding agent, CLIP agent, BLIP agent, Flamingo agent, LLaVA agent, GPT-4V agent, Gemini Vision agent, vision language model agent, VLM agent, image captioning agent, visual question answering agent, VQA agent, image generation agent, text-to-image agent, image-to-image agent, inpainting agent, outpainting agent, super resolution agent, upscaling agent, style transfer agent, neural style agent, diffusion model agent, DDPM agent, DDIM agent, score matching agent, noise schedule agent, classifier-free guidance agent, CFG agent, ControlNet agent, LoRA agent, low-rank adaptation agent, QLoRA agent, PEFT agent, parameter-efficient fine-tuning agent, adapter agent, prefix tuning agent, prompt tuning agent, instruction tuning agent, RLHF agent, reinforcement learning from human feedback agent, DPO agent, direct preference optimization agent, PPO agent, proximal policy optimization agent, reward model agent, preference model agent, constitutional AI agent, red teaming agent, adversarial training agent, safety training agent, alignment agent, AI alignment agent, value alignment agent, goal alignment agent, reward hacking agent, reward gaming agent, specification gaming agent, goodhart agent, mesa-optimization agent, inner alignment agent, outer alignment agent, corrigibility agent, interpretability agent, explainability agent, XAI agent, SHAP agent, LIME agent, attention visualization agent, feature attribution agent, concept activation agent, probing agent, mechanistic interpretability agent, circuit analysis agent, polysemanticity agent, superposition agent, sparse autoencoder agent, dictionary learning agent, activation patching agent, causal tracing agent, logit lens agent, tuned lens agent, model editing agent, ROME agent, MEMIT agent, knowledge editing agent, fact editing agent, belief editing agent, steering vector agent, activation steering agent, representation engineering agent, latent space agent, embedding space agent, feature space agent, manifold agent, topology agent, geometry agent, curvature agent, dimensionality reduction agent, PCA agent, t-SNE agent, UMAP agent, clustering agent, K-means agent, DBSCAN agent, hierarchical clustering agent, spectral clustering agent, Gaussian mixture agent, GMM agent, variational autoencoder agent, VAE agent, beta-VAE agent, VQ-VAE agent, autoencoder agent, denoising autoencoder agent, sparse autoencoder agent, contractive autoencoder agent, GAN agent, generative adversarial network agent, DCGAN agent, StyleGAN agent, BigGAN agent, Progressive GAN agent, CycleGAN agent, Pix2Pix agent, conditional GAN agent, cGAN agent, Wasserstein GAN agent, WGAN agent, mode collapse agent, discriminator agent, generator agent, latent code agent, latent interpolation agent, disentanglement agent, flow model agent, normalizing flow agent, RealNVP agent, Glow agent, NICE agent, autoregressive model agent, PixelCNN agent, WaveNet agent, Transformer-XL agent, XLNet agent, causal language model agent, masked language model agent, next token prediction agent, span corruption agent, denoising objective agent, contrastive objective agent, SimCLR agent, MoCo agent, BYOL agent, SwAV agent, DINO agent, MAE agent, masked autoencoder agent, BEiT agent, data2vec agent, I-JEPA agent, V-JEPA agent, world model agent, predictive model agent, dynamics model agent, environment model agent, model-based RL agent, model-free RL agent, value function agent, Q-function agent, policy function agent, actor-critic agent, A2C agent, A3C agent, SAC agent, soft actor-critic agent, TD3 agent, DDPG agent, DQN agent, double DQN agent, dueling DQN agent, rainbow DQN agent, C51 agent, IQN agent, distributional RL agent, hierarchical RL agent, option framework agent, goal-conditioned RL agent, hindsight experience replay agent, HER agent, curiosity-driven agent, intrinsic motivation agent, exploration agent, exploitation agent, epsilon-greedy agent, UCB agent, Thompson sampling agent, multi-armed bandit agent, contextual bandit agent, MCTS agent, Monte Carlo tree search agent, AlphaGo agent, AlphaZero agent, MuZero agent, Gato agent, generalist agent, foundation model agent, large language model agent, LLM agent, small language model agent, SLM agent, on-device agent, edge AI agent, TinyML agent, embedded AI agent, mobile AI agent, neural engine agent, NPU agent, TPU agent, GPU agent, CUDA agent, ROCm agent, Metal agent, CoreML agent, ONNX agent, TensorRT agent, OpenVINO agent, TFLite agent, PyTorch Mobile agent, GGML agent, llama.cpp agent, whisper.cpp agent, vLLM agent, TGI agent, text generation inference agent, serving agent, inference server agent, batch inference agent, streaming inference agent, speculative decoding agent, assisted generation agent, beam search agent, greedy decoding agent, nucleus sampling agent, top-k sampling agent, top-p sampling agent, temperature agent, repetition penalty agent, presence penalty agent, frequency penalty agent, stop sequence agent, max tokens agent, context window agent, tokenizer agent, BPE agent, byte-pair encoding agent, SentencePiece agent, WordPiece agent, Unigram agent, vocabulary agent, special tokens agent, chat template agent, system prompt agent, user prompt agent, assistant response agent, function calling agent, tool use agent, code interpreter agent, retrieval agent, web browsing agent, multi-turn conversation agent, dialogue agent, chat agent, completion agent, instruction following agent, chain-of-thought agent, CoT agent, tree-of-thought agent, ToT agent, graph-of-thought agent, GoT agent, self-consistency agent, self-reflection agent, self-critique agent, self-improvement agent, self-play agent, debate agent, ensemble agent, mixture of experts agent, MoE agent, sparse MoE agent, switch transformer agent, GShard agent, routing agent, load balancing agent, expert parallelism agent, tensor parallelism agent, pipeline parallelism agent, data parallelism agent, FSDP agent, fully sharded data parallel agent, DeepSpeed agent, ZeRO agent, Megatron agent, 3D parallelism agent, activation checkpointing agent, gradient checkpointing agent, offloading agent, CPU offloading agent, NVMe offloading agent, memory efficient agent, flash attention agent, paged attention agent, continuous batching agent, dynamic batching agent, request scheduling agent, preemption agent, priority queue agent, SLA agent, latency agent, throughput agent, tokens per second agent, time to first token agent, TTFT agent, inter-token latency agent, ITL agent, end-to-end latency agent, cold start agent, warm start agent, model loading agent, weight loading agent, KV cache agent, prefix caching agent, prompt caching agent, semantic caching agent

## Geographic & Localization Keywords

North America agent, South America agent, Europe agent, Asia agent, Africa agent, Australia agent, Oceania agent, Middle East agent, Central America agent, Caribbean agent, Southeast Asia agent, East Asia agent, South Asia agent, Central Asia agent, Eastern Europe agent, Western Europe agent, Northern Europe agent, Southern Europe agent, Nordic agent, Scandinavian agent, Baltic agent, Balkan agent, Mediterranean agent, Alpine agent, Iberian agent, British agent, Irish agent, French agent, German agent, Italian agent, Spanish agent, Portuguese agent, Dutch agent, Belgian agent, Swiss agent, Austrian agent, Polish agent, Czech agent, Slovak agent, Hungarian agent, Romanian agent, Bulgarian agent, Greek agent, Turkish agent, Russian agent, Ukrainian agent, Belarusian agent, Moldovan agent, Georgian agent, Armenian agent, Azerbaijani agent, Kazakh agent, Uzbek agent, Turkmen agent, Tajik agent, Kyrgyz agent, Afghan agent, Pakistani agent, Indian agent, Bangladeshi agent, Sri Lankan agent, Nepali agent, Bhutanese agent, Maldivian agent, Burmese agent, Thai agent, Vietnamese agent, Cambodian agent, Laotian agent, Malaysian agent, Singaporean agent, Indonesian agent, Filipino agent, Bruneian agent, Timorese agent, Chinese agent, Japanese agent, Korean agent, Taiwanese agent, Hong Kong agent, Macanese agent, Mongolian agent, North Korean agent, Australian agent, New Zealand agent, Papua New Guinean agent, Fijian agent, Samoan agent, Tongan agent, Vanuatuan agent, Solomon Islands agent, Micronesian agent, Marshallese agent, Palauan agent, Nauruan agent, Kiribati agent, Tuvaluan agent, Egyptian agent, Libyan agent, Tunisian agent, Algerian agent, Moroccan agent, Mauritanian agent, Malian agent, Nigerien agent, Chadian agent, Sudanese agent, South Sudanese agent, Ethiopian agent, Eritrean agent, Djiboutian agent, Somali agent, Kenyan agent, Ugandan agent, Rwandan agent, Burundian agent, Tanzanian agent, Mozambican agent, Malawian agent, Zambian agent, Zimbabwean agent, Botswanan agent, Namibian agent, South African agent, Lesotho agent, Eswatini agent, Angolan agent, Congolese agent, Cameroonian agent, Central African agent, Gabonese agent, Equatorial Guinean agent, Sao Tomean agent, Nigerian agent, Ghanaian agent, Togolese agent, Beninese agent, Burkinabe agent, Ivorian agent, Liberian agent, Sierra Leonean agent, Guinean agent, Bissau-Guinean agent, Senegalese agent, Gambian agent, Mauritius agent, Seychelles agent, Comoros agent, Madagascar agent, Reunion agent, Mayotte agent, Canadian agent, American agent, Mexican agent, Guatemalan agent, Belizean agent, Honduran agent, Salvadoran agent, Nicaraguan agent, Costa Rican agent, Panamanian agent, Cuban agent, Jamaican agent, Haitian agent, Dominican agent, Puerto Rican agent, Bahamian agent, Barbadian agent, Trinidadian agent, Guyanese agent, Surinamese agent, Venezuelan agent, Colombian agent, Ecuadorian agent, Peruvian agent, Brazilian agent, Bolivian agent, Paraguayan agent, Uruguayan agent, Argentine agent, Chilean agent, English language agent, Spanish language agent, French language agent, German language agent, Italian language agent, Portuguese language agent, Russian language agent, Chinese language agent, Japanese language agent, Korean language agent, Arabic language agent, Hindi language agent, Bengali language agent, Urdu agent, Punjabi agent, Tamil agent, Telugu agent, Marathi agent, Gujarati agent, Kannada agent, Malayalam agent, Thai language agent, Vietnamese language agent, Indonesian language agent, Malay language agent, Filipino language agent, Turkish language agent, Persian language agent, Hebrew language agent, Greek language agent, Polish language agent, Ukrainian language agent, Dutch language agent, Swedish language agent, Norwegian language agent, Danish language agent, Finnish language agent, Hungarian language agent, Czech language agent, Romanian language agent, Bulgarian language agent, Serbian language agent, Croatian agent, Bosnian agent, Slovenian agent, Slovak agent, Lithuanian agent, Latvian agent, Estonian agent, Swahili agent, Amharic agent, Yoruba agent, Igbo agent, Hausa agent, Zulu agent, Xhosa agent, Afrikaans agent, localization agent, internationalization agent, i18n agent, l10n agent, translation agent, machine translation agent, neural machine translation agent, NMT agent, multilingual agent, cross-lingual agent, language detection agent, language identification agent, transliteration agent, romanization agent, diacritics agent, Unicode agent, UTF-8 agent, character encoding agent, right-to-left agent, RTL agent, bidirectional agent, locale agent, timezone agent, date format agent, number format agent, currency format agent, address format agent, phone format agent, name format agent, cultural adaptation agent, regional compliance agent, GDPR agent, CCPA agent, LGPD agent, POPIA agent, PDPA agent, data residency agent, data sovereignty agent, cross-border agent, international agent, global agent, worldwide agent, multinational agent, transnational agent, intercontinental agent, overseas agent, foreign agent, domestic agent, local agent, regional agent, national agent, federal agent, state agent, provincial agent, municipal agent, city agent, urban agent, suburban agent, rural agent, remote agent, offshore agent, nearshore agent, onshore agent

---

## Industry & Vertical Keywords

healthcare agent, medical agent, clinical agent, diagnostic agent, treatment agent, pharmaceutical agent, drug discovery agent, patient agent, doctor agent, nurse agent, hospital agent, clinic agent, telemedicine agent, telehealth agent, health monitoring agent, wellness agent, fitness agent, nutrition agent, mental health agent, therapy agent, counseling agent, psychology agent, psychiatry agent, insurance agent, claims agent, underwriting agent, risk assessment agent, actuarial agent, policy agent, coverage agent, benefits agent, reimbursement agent, billing agent, invoicing agent, accounting agent, bookkeeping agent, tax agent, audit agent, compliance agent, regulatory agent, legal agent, contract agent, agreement agent, negotiation agent, dispute agent, arbitration agent, mediation agent, litigation agent, court agent, judge agent, lawyer agent, attorney agent, paralegal agent, notary agent, real estate agent, property agent, housing agent, rental agent, lease agent, mortgage agent, appraisal agent, valuation agent, inspection agent, construction agent, architecture agent, engineering agent, design agent, planning agent, zoning agent, permit agent, licensing agent, certification agent, accreditation agent, quality agent, testing agent, manufacturing agent, production agent, assembly agent, logistics agent, supply chain agent, inventory agent, warehouse agent, shipping agent, delivery agent, transportation agent, fleet agent, routing agent, dispatch agent, tracking agent, monitoring agent, surveillance agent, security agent, protection agent, safety agent, emergency agent, disaster agent, crisis agent, response agent, recovery agent, restoration agent, maintenance agent, repair agent, helpdesk agent, ticketing agent, incident agent, problem agent, change agent, release agent, deployment agent, configuration agent, asset agent, resource agent, capacity agent, optimization agent, efficiency agent, productivity agent, automation agent, integration agent, migration agent, transformation agent, modernization agent, innovation agent, research agent, development agent, experimentation agent, prototyping agent, documentation agent, training agent, education agent, learning agent, teaching agent, tutoring agent, mentoring agent, coaching agent, consulting agent, advisory agent, strategy agent, forecasting agent, prediction agent, analysis agent, reporting agent, visualization agent, dashboard agent, alerting agent, notification agent, communication agent, collaboration agent, coordination agent, scheduling agent, calendar agent, meeting agent, conference agent, presentation agent, demonstration agent, proposal agent, quotation agent, estimation agent, budgeting agent, costing agent, pricing agent, discount agent, promotion agent, marketing agent, advertising agent, branding agent, campaign agent, outreach agent, engagement agent, conversion agent, retention agent, loyalty agent, advocacy agent, referral agent, partnership agent, alliance agent, consortium agent, federation agent, network agent, community agent, platform agent, marketplace agent, exchange agent, trading agent, brokerage agent, clearing agent, settlement agent, custody agent, escrow agent, fiduciary agent, investment agent, portfolio agent, wealth agent, asset management agent, fund agent, hedge fund agent, mutual fund agent, ETF agent, index agent, bond agent, equity agent, derivative agent, option agent, future agent, swap agent, commodity agent, currency agent, forex agent, crypto agent, bitcoin agent, ethereum agent, altcoin agent, token agent, NFT agent, DeFi agent, yield agent, staking agent, lending agent, borrowing agent, liquidity agent, AMM agent, DEX agent, CEX agent, bridge agent, governance agent, DAO agent, treasury agent, voting agent, delegation agent, validator agent, node agent, miner agent, block agent, transaction agent, gas agent, fee agent, reward agent, penalty agent, slashing agent, epoch agent, finality agent, consensus agent, proof agent, attestation agent, signature agent, encryption agent, decryption agent, hashing agent, merkle agent, trie agent, state agent, storage agent, memory agent, cache agent, database agent, query agent, search agent, retrieval agent, ranking agent, recommendation agent, personalization agent, segmentation agent, targeting agent, attribution agent, analytics agent, metrics agent, KPI agent, OKR agent, goal agent, objective agent, milestone agent, deadline agent, timeline agent, roadmap agent, backlog agent, sprint agent, iteration agent, version agent, changelog agent, specification agent, requirement agent, user story agent, acceptance criteria agent, test case agent, bug agent, issue agent, ticket agent, task agent, subtask agent, epic agent, feature agent, enhancement agent, improvement agent, refactoring agent, debugging agent, profiling agent, benchmarking agent, load testing agent, stress testing agent, penetration testing agent, security testing agent, vulnerability agent, exploit agent, patch agent, hotfix agent, update agent, upgrade agent, rollback agent, backup agent, restore agent, disaster recovery agent, business continuity agent, high availability agent, fault tolerance agent, redundancy agent, replication agent, synchronization agent, consistency agent, durability agent, availability agent, partition tolerance agent

## Technology Stack Keywords

JavaScript agent, TypeScript agent, Python agent, Go agent, Rust agent, Java agent, Kotlin agent, Swift agent, Objective-C agent, C++ agent, C# agent, Ruby agent, PHP agent, Scala agent, Clojure agent, Elixir agent, Erlang agent, Haskell agent, OCaml agent, F# agent, Dart agent, Flutter agent, React agent, Vue agent, Angular agent, Svelte agent, Solid agent, Next.js agent, Nuxt agent, Remix agent, Gatsby agent, Astro agent, Qwik agent, Fresh agent, SvelteKit agent, Express agent, Fastify agent, Koa agent, Hapi agent, NestJS agent, Adonis agent, Sails agent, Meteor agent, Django agent, Flask agent, FastAPI agent, Starlette agent, Tornado agent, Pyramid agent, Bottle agent, Falcon agent, Sanic agent, Quart agent, Rails agent, Sinatra agent, Hanami agent, Roda agent, Grape agent, Spring agent, Quarkus agent, Micronaut agent, Vert.x agent, Play agent, Akka agent, Lagom agent, ASP.NET agent, Blazor agent, MAUI agent, Xamarin agent, Unity agent, Godot agent, Unreal agent, Bevy agent, Amethyst agent, ggez agent, macroquad agent, Raylib agent, SDL agent, SFML agent, OpenGL agent, Vulkan agent, DirectX agent, Metal agent, WebGL agent, WebGPU agent, Three.js agent, Babylon.js agent, PlayCanvas agent, A-Frame agent, React Three Fiber agent, Pixi.js agent, Phaser agent, Cocos agent, Defold agent, Construct agent, GameMaker agent, RPG Maker agent, Twine agent, Ink agent, Yarn Spinner agent, Dialogflow agent, Rasa agent, Botpress agent, Microsoft Bot Framework agent, Amazon Lex agent, IBM Watson agent, Google Dialogflow agent, Wit.ai agent, Snips agent, Mycroft agent, Jasper agent, Leon agent, Hugging Face agent, OpenAI agent, Anthropic agent, Cohere agent, AI21 agent, Stability AI agent, Midjourney agent, DALL-E agent, Stable Diffusion agent, Imagen agent, Gemini agent, Claude agent, GPT agent, LLaMA agent, Mistral agent, Mixtral agent, Phi agent, Qwen agent, Yi agent, DeepSeek agent, Falcon agent, MPT agent, BLOOM agent, OPT agent, Pythia agent, Cerebras agent, Inflection agent, Adept agent, Character.AI agent, Poe agent, Perplexity agent, You.com agent, Neeva agent, Kagi agent, Brave Search agent, DuckDuckGo agent, Startpage agent, Ecosia agent, Qwant agent, Mojeek agent, Yandex agent, Baidu agent, Naver agent, Seznam agent, Sogou agent

## Emerging Technology Keywords

quantum computing agent, quantum machine learning agent, quantum optimization agent, quantum simulation agent, quantum cryptography agent, post-quantum agent, lattice-based agent, hash-based agent, code-based agent, isogeny-based agent, multivariate agent, neuromorphic agent, spiking neural network agent, memristor agent, photonic agent, optical computing agent, DNA computing agent, molecular computing agent, biological computing agent, wetware agent, biocomputing agent, synthetic biology agent, gene editing agent, CRISPR agent, mRNA agent, protein folding agent, AlphaFold agent, drug discovery agent, virtual screening agent, molecular dynamics agent, computational chemistry agent, materials science agent, nanotechnology agent, metamaterials agent, 2D materials agent, graphene agent, quantum dots agent, nanoparticles agent, nanorobots agent, nanomedicine agent, targeted delivery agent, biosensors agent, wearables agent, implantables agent, brain-computer interface agent, neural interface agent, Neuralink agent, EEG agent, fMRI agent, PET agent, MEG agent, TMS agent, tDCS agent, optogenetics agent, chemogenetics agent, connectomics agent, brain mapping agent, cognitive computing agent, affective computing agent, emotion AI agent, sentiment analysis agent, opinion mining agent, social listening agent, brand monitoring agent, reputation management agent, crisis communication agent, public relations agent, media monitoring agent, press agent, journalist agent, editor agent, writer agent, author agent, content creator agent, influencer agent, streamer agent, YouTuber agent, TikToker agent, podcaster agent, blogger agent, vlogger agent, photographer agent, videographer agent, animator agent, illustrator agent, graphic designer agent, UI designer agent, UX designer agent, product designer agent, industrial designer agent, fashion designer agent, interior designer agent, architect agent, landscape architect agent, urban planner agent, city planner agent, transportation planner agent, traffic agent, autonomous vehicle agent, self-driving agent, ADAS agent, V2X agent, connected vehicle agent, smart transportation agent, smart city agent, smart grid agent, smart meter agent, smart home agent, smart building agent, smart factory agent, Industry 4.0 agent, IoT agent, IIoT agent, edge computing agent, fog computing agent, mist computing agent, cloudlet agent, mobile edge agent, MEC agent, NOMA agent, massive MIMO agent, beamforming agent, millimeter wave agent, terahertz agent, 6G agent, 5G agent, LTE agent, NB-IoT agent, LoRa agent, Sigfox agent, Zigbee agent, Z-Wave agent, Thread agent, Matter agent, HomeKit agent, Alexa agent, Google Home agent, SmartThings agent, Home Assistant agent, OpenHAB agent, Domoticz agent, Hubitat agent, Homey agent, Tuya agent, eWeLink agent, Sonoff agent, Shelly agent, Tasmota agent, ESPHome agent, WLED agent, Zigbee2MQTT agent, deCONZ agent, ZHA agent, Philips Hue agent, IKEA Tradfri agent, Aqara agent, Xiaomi agent, Yeelight agent, Nanoleaf agent, LIFX agent, TP-Link Kasa agent, Wyze agent, Ring agent, Nest agent, Ecobee agent, Honeywell agent, Emerson agent, Carrier agent, Trane agent, Lennox agent, Daikin agent, Mitsubishi Electric agent, LG agent, Samsung agent, Bosch agent, Siemens agent, ABB agent, Schneider Electric agent, Rockwell agent, Yokogawa agent, Endress+Hauser agent, SICK agent, Pepperl+Fuchs agent, Balluff agent, ifm agent, Banner agent, Turck agent, Omron agent, Keyence agent, Cognex agent, Basler agent, FLIR agent, Teledyne agent, Allied Vision agent, JAI agent, IDS agent, Baumer agent, Stemmer agent, MVTec agent, Matrox agent, National Instruments agent, Beckhoff agent, Phoenix Contact agent, Wago agent, Weidmuller agent, Murrelektronik agent, Pilz agent, Leuze agent, Datalogic agent, Zebra agent, SATO agent, Citizen agent, TSC agent, Godex agent, Printronix agent, Epson agent, Brother agent, DYMO agent, Rollo agent, Munbyn agent, iDPRT agent, HPRT agent

## Business & Enterprise Keywords

enterprise agent, corporate agent, business agent, commercial agent, industrial agent, retail agent, wholesale agent, distribution agent, procurement agent, sourcing agent, purchasing agent, vendor management agent, supplier agent, contractor agent, subcontractor agent, freelancer agent, consultant agent, advisor agent, strategist agent, analyst agent, researcher agent, scientist agent, engineer agent, developer agent, programmer agent, architect agent, designer agent, artist agent, creative agent, copywriter agent, content strategist agent, SEO agent, SEM agent, PPC agent, social media agent, community manager agent, brand ambassador agent, spokesperson agent, evangelist agent, advocate agent, champion agent, mentor agent, coach agent, trainer agent, instructor agent, professor agent, teacher agent, tutor agent, educator agent, facilitator agent, moderator agent, host agent, presenter agent, speaker agent, panelist agent, guest agent, expert agent, specialist agent, generalist agent, polymath agent, renaissance agent, versatile agent, adaptive agent, flexible agent, agile agent, lean agent, efficient agent, effective agent, productive agent, performant agent, scalable agent, reliable agent, available agent, durable agent, resilient agent, robust agent, stable agent, secure agent, safe agent, compliant agent, regulated agent, certified agent, accredited agent, licensed agent, authorized agent, approved agent, verified agent, validated agent, tested agent, audited agent, reviewed agent, assessed agent, evaluated agent, measured agent, quantified agent, qualified agent, skilled agent, experienced agent, knowledgeable agent, informed agent, educated agent, trained agent, professional agent, master agent, senior agent, principal agent, lead agent, chief agent, head agent, director agent, manager agent, supervisor agent, coordinator agent, administrator agent, operator agent, technician agent, associate agent, assistant agent, intern agent, trainee agent, apprentice agent, junior agent, mid-level agent, intermediate agent, advanced agent, staff agent, part-time agent, full-time agent, remote agent, hybrid agent, onsite agent, offshore agent, nearshore agent, outsourced agent, insourced agent, managed agent, unmanaged agent, semi-autonomous agent, supervised agent, unsupervised agent, reinforcement agent, self-learning agent, evolving agent, improving agent, optimizing agent, maximizing agent, minimizing agent, balancing agent, tradeoff agent, pareto agent, multi-objective agent, constraint agent, bounded agent, limited agent, unlimited agent, infinite agent, finite agent, discrete agent, continuous agent, mixed agent, ensemble agent, committee agent, consensus agent, majority agent, plurality agent, weighted agent, ranked agent, preference agent, utility agent, cost agent, benefit agent, value agent, worth agent, price agent, rate agent, tariff agent, duty agent, levy agent, surcharge agent, premium agent, rebate agent, refund agent, credit agent, debit agent, balance agent, account agent, ledger agent, journal agent, record agent, entry agent, transfer agent, receipt agent, invoice agent, bill agent, statement agent, report agent, summary agent, detail agent, breakdown agent, itemization agent, categorization agent, classification agent, taxonomy agent, ontology agent, schema agent, model agent, framework agent, architecture agent, pattern agent, template agent, blueprint agent, plan agent, tactic agent, technique agent, method agent, process agent, procedure agent, workflow agent, pipeline agent, chain agent, sequence agent, order agent, priority agent, queue agent, stack agent, heap agent, tree agent, graph agent, mesh agent, grid agent, cluster agent, pool agent, farm agent, fleet agent, swarm agent, hive agent, colony agent, pack agent, herd agent, flock agent, school agent, pod agent, pride agent, troop agent, band agent, gang agent, crew agent, team agent, squad agent, unit agent, division agent, department agent, branch agent, office agent, location agent, site agent, facility agent, plant agent, factory agent, depot agent, hub agent, center agent, station agent, terminal agent, port agent, dock agent, pier agent, wharf agent, quay agent, berth agent, slip agent, marina agent, harbor agent, airport agent, heliport agent, spaceport agent, launchpad agent, runway agent, taxiway agent, apron agent, gate agent, concourse agent, lounge agent, checkpoint agent, customs agent, immigration agent, passport agent, visa agent, registration agent, credential agent, badge agent, ID agent, identity agent, authentication agent, authorization agent, access agent, permission agent, role agent, privilege agent, right agent, entitlement agent, claim agent, assertion agent, declaration agent, expression agent, formula agent, equation agent, function agent, variable agent, constant agent, parameter agent, argument agent, input agent, output agent, result agent, return agent, response agent, request agent, command agent, instruction agent, directive agent, message agent, signal agent, event agent, trigger agent, action agent, reaction agent, effect agent, consequence agent, outcome agent, impact agent, influence agent, transition agent, evolution agent, revolution agent, disruption agent, invention agent, discovery agent, breakthrough agent, advancement agent, progress agent, growth agent, expansion agent, scaling agent, multiplication agent, proliferation agent, adoption agent, acceptance agent, incorporation agent, assimilation agent, absorption agent, merger agent, acquisition agent, synchronization agent, harmonization agent, alignment agent, maximization agent, minimization agent, effectiveness agent, quality agent, reliability agent, accessibility agent, usability agent, flexibility agent, adaptability agent, extensibility agent, maintainability agent, sustainability agent, longevity agent, persistence agent, continuity agent, stability agent, privacy agent, confidentiality agent, integrity agent, authenticity agent, validity agent, accuracy agent, precision agent, correctness agent, completeness agent, coherence agent, clarity agent, simplicity agent, elegance agent, beauty agent, aesthetics agent

## Search Query Keywords

what is ERC-8004, what is ERC8004, what are trustless agents, how do trustless agents work, ERC-8004 tutorial, ERC-8004 guide, ERC-8004 documentation, ERC-8004 examples, ERC-8004 implementation, ERC-8004 smart contract, ERC-8004 Solidity, ERC-8004 TypeScript, ERC-8004 Python, ERC-8004 SDK, ERC-8004 API, ERC-8004 integration, ERC-8004 deployment, ERC-8004 mainnet, ERC-8004 testnet, ERC-8004 Sepolia, ERC-8004 Base, ERC-8004 Polygon, ERC-8004 Arbitrum, ERC-8004 Optimism, ERC-8004 registration, ERC-8004 identity, ERC-8004 reputation, ERC-8004 validation, ERC-8004 feedback, ERC-8004 scanner, ERC-8004 explorer, best AI agent protocol, best blockchain agent standard, decentralized AI agent protocol, on-chain AI agent registry, blockchain AI reputation system, how to build AI agent, how to register AI agent, how to monetize AI agent, how to discover AI agents, AI agent marketplace, AI agent directory, AI agent leaderboard, AI agent ranking, AI agent scoring, AI agent feedback, AI agent validation, AI agent verification, AI agent trust, AI agent reputation, AI agent identity, AI agent NFT, AI agent token, AI agent economy, AI agent commerce, AI agent payments, AI agent micropayments, AI agent x402, AI agent MCP, AI agent A2A, autonomous agent protocol, autonomous agent standard, autonomous agent framework, autonomous agent platform, multi-agent protocol, multi-agent standard, multi-agent framework, multi-agent platform, agent-to-agent protocol, agent-to-agent communication, agent-to-agent payments, agent interoperability standard, agent discovery protocol, agent trust protocol, agent reputation protocol, agent validation protocol, open agent standard, open agent protocol, permissionless agent protocol, decentralized agent protocol, trustless agent protocol, verifiable agent protocol, accountable agent protocol, portable agent identity, portable agent reputation, cross-chain agent identity, cross-chain agent reputation, Ethereum AI agents, Web3 AI agents, crypto AI agents, DeFi AI agents, NFT AI agents, blockchain AI agents

## Alternative Spellings & Variations

ERC 8004, ERC_8004, ERC.8004, EIP 8004, EIP_8004, EIP.8004, erc-8004, erc8004, eip-8004, eip8004, Erc-8004, Erc8004, Eip-8004, Eip8004, trustless-agents, trustless_agents, TrustlessAgents, Trustless-Agents, Trustless_Agents, TRUSTLESS AGENTS, TRUSTLESSAGENTS, ai-agents, ai_agents, AIAgents, AI-Agents, AI_Agents, AI AGENTS, AIAGENTS, on-chain-agents, on_chain_agents, OnChainAgents, On-Chain-Agents, On_Chain_Agents, ON CHAIN AGENTS, ONCHAINAGENTS, onchain-agents, onchain_agents, blockchain-agents, blockchain_agents, BlockchainAgents, Blockchain-Agents, Blockchain_Agents, BLOCKCHAIN AGENTS, BLOCKCHAINAGENTS, decentralized-agents, decentralized_agents, DecentralizedAgents, Decentralized-Agents, Decentralized_Agents, DECENTRALIZED AGENTS, DECENTRALIZEDAGENTS, autonomous-agents, autonomous_agents, AutonomousAgents, Autonomous-Agents, Autonomous_Agents, AUTONOMOUS AGENTS, AUTONOMOUSAGENTS, agent-protocol, agent_protocol, AgentProtocol, Agent-Protocol, Agent_Protocol, AGENT PROTOCOL, AGENTPROTOCOL, agent-standard, agent_standard, AgentStandard, Agent-Standard, Agent_Standard, AGENT STANDARD, AGENTSTANDARD, agent-registry, agent_registry, AgentRegistry, Agent-Registry, Agent_Registry, AGENT REGISTRY, AGENTREGISTRY, identity-registry, identity_registry, IdentityRegistry, Identity-Registry, Identity_Registry, IDENTITY REGISTRY, IDENTITYREGISTRY, reputation-registry, reputation_registry, ReputationRegistry, Reputation-Registry, Reputation_Registry, REPUTATION REGISTRY, REPUTATIONREGISTRY, validation-registry, validation_registry, ValidationRegistry, Validation-Registry, Validation_Registry, VALIDATION REGISTRY, VALIDATIONREGISTRY

## Protocol Comparison Keywords

ERC-8004 vs centralized, ERC-8004 vs traditional, ERC-8004 vs proprietary, ERC-8004 vs closed source, ERC-8004 vs walled garden, ERC-8004 vs platform lock-in, ERC-8004 vs vendor lock-in, ERC-8004 alternative, ERC-8004 competitor, ERC-8004 comparison, trustless vs trusted, decentralized vs centralized, on-chain vs off-chain, permissionless vs permissioned, open vs closed, transparent vs opaque, verifiable vs unverifiable, portable vs locked, interoperable vs siloed, composable vs monolithic, upgradeable vs immutable, auditable vs hidden, public vs private, community vs corporate, protocol vs platform, standard vs proprietary, open source vs closed source, free vs paid, gas-only vs subscription, blockchain vs database, smart contract vs API, NFT vs API key, on-chain identity vs OAuth, decentralized reputation vs centralized rating, cryptographic proof vs trust, zero-knowledge vs disclosure, TEE vs software, stake-secured vs trust-based, validator vs moderator, consensus vs authority, distributed vs centralized, peer-to-peer vs client-server, mesh vs hub-spoke, federated vs centralized, hybrid vs pure, layer 1 vs layer 2, mainnet vs testnet, production vs development, live vs sandbox, real vs simulated, actual vs mock, genuine vs fake, authentic vs counterfeit, verified vs unverified, validated vs unvalidated, certified vs uncertified, audited vs unaudited, tested vs untested, proven vs unproven, established vs experimental, mature vs emerging, stable vs beta, release vs preview, final vs draft, approved vs pending, accepted vs rejected, passed vs failed, successful vs unsuccessful, complete vs incomplete, finished vs unfinished, done vs pending, ready vs not ready, available vs unavailable, accessible vs inaccessible, reachable vs unreachable, online vs offline, active vs inactive, enabled vs disabled, running vs stopped, started vs paused, live vs dead, healthy vs unhealthy, operational vs down, functional vs broken, working vs failing, responding vs unresponsive, fast vs slow, quick vs delayed, instant vs pending, immediate vs queued, synchronous vs asynchronous, blocking vs non-blocking, sequential vs parallel, serial vs concurrent, single vs multi, one vs many, few vs numerous, small vs large, tiny vs huge, minimal vs maximal, simple vs complex, easy vs hard, basic vs advanced, beginner vs expert, novice vs professional, amateur vs master, junior vs senior, entry vs executive, low vs high, bottom vs top, start vs end, beginning vs finish, first vs last, initial vs final, primary vs secondary, main vs auxiliary, core vs peripheral, central vs distributed, local vs remote, internal vs external, private vs public, hidden vs visible, secret vs open, confidential vs transparent, encrypted vs plaintext, hashed vs raw, signed vs unsigned, authenticated vs anonymous, authorized vs unauthorized, permitted vs forbidden, allowed vs denied, granted vs revoked, active vs expired, valid vs invalid, current vs outdated, fresh vs stale, new vs old, recent vs ancient, modern vs legacy, updated vs deprecated, supported vs unsupported, maintained vs abandoned, alive vs dead, thriving vs dying, growing vs shrinking, expanding vs contracting, scaling vs limited, unlimited vs capped, infinite vs finite, boundless vs bounded, open-ended vs closed, flexible vs rigid, adaptable vs fixed, dynamic vs static, variable vs constant, mutable vs immutable, changeable vs unchangeable, modifiable vs readonly, writable vs locked, editable vs frozen, updateable vs permanent, reversible vs irreversible, undoable vs final, recoverable vs lost, restorable vs destroyed, backupable vs volatile, persistent vs temporary, durable vs ephemeral, long-term vs short-term, permanent vs transient, stable vs volatile, consistent vs inconsistent, reliable vs unreliable, dependable vs unpredictable, trustworthy vs suspicious, credible vs dubious, reputable vs disreputable, respected vs ignored, valued vs worthless, important vs trivial, significant vs insignificant, major vs minor, critical vs optional, essential vs unnecessary, required vs optional, mandatory vs voluntary, forced vs chosen, automatic vs manual, programmatic vs interactive, batch vs realtime, scheduled vs on-demand, periodic vs continuous, recurring vs one-time, repeated vs unique, multiple vs single, plural vs singular, collective vs individual, group vs solo, team vs lone, collaborative vs independent, cooperative vs competitive, aligned vs opposed, compatible vs incompatible, interoperable vs isolated, integrated vs standalone, connected vs disconnected, linked vs unlinked, associated vs dissociated, related vs unrelated, relevant vs irrelevant, applicable vs inapplicable, suitable vs unsuitable, appropriate vs inappropriate, fitting vs unfitting, matching vs mismatched, aligned vs misaligned, synchronized vs desynchronized, coordinated vs uncoordinated, organized vs chaotic, structured vs unstructured, ordered vs random, sequential vs shuffled, sorted vs unsorted, indexed vs unindexed, cataloged vs uncataloged, registered vs unregistered, listed vs unlisted, published vs unpublished, released vs unreleased, launched vs pending, deployed vs undeployed, installed vs uninstalled, configured vs unconfigured, setup vs raw, initialized vs uninitialized, ready vs unprepared, prepared vs improvised, planned vs spontaneous, intentional vs accidental, deliberate vs random, purposeful vs aimless, directed vs undirected, guided vs unguided, supervised vs unsupervised, monitored vs unmonitored, tracked vs untracked, logged vs unlogged, recorded vs unrecorded, documented vs undocumented, specified vs unspecified, defined vs undefined, declared vs undeclared, explicit vs implicit, clear vs ambiguous, precise vs vague, exact vs approximate, accurate vs inaccurate, correct vs incorrect, right vs wrong, true vs false, valid vs invalid, legitimate vs illegitimate, legal vs illegal, lawful vs unlawful, compliant vs non-compliant, conforming vs non-conforming, standard vs non-standard, conventional vs unconventional, traditional vs innovative, classic vs modern, old-school vs cutting-edge, established vs disruptive, mainstream vs alternative, popular vs niche, common vs rare, frequent vs infrequent, regular vs irregular, normal vs abnormal, typical vs atypical, expected vs unexpected, predictable vs unpredictable, deterministic vs stochastic, certain vs uncertain, definite vs indefinite, absolute vs relative, fixed vs floating, static vs dynamic, constant vs variable, stable vs unstable, steady vs fluctuating, even vs uneven, balanced vs unbalanced, equal vs unequal, fair vs unfair, just vs unjust, equitable vs inequitable, proportional vs disproportional, symmetric vs asymmetric, uniform vs non-uniform, homogeneous vs heterogeneous, consistent vs varied, same vs different, identical vs distinct, similar vs dissimilar, like vs unlike, comparable vs incomparable, equivalent vs non-equivalent, equal vs unequal, matching vs non-matching, corresponding vs non-corresponding, aligned vs non-aligned, parallel vs perpendicular, horizontal vs vertical, lateral vs longitudinal, width vs height, breadth vs depth, surface vs volume, area vs perimeter, inside vs outside, interior vs exterior, internal vs external, inner vs outer, central vs peripheral, core vs edge, middle vs end, center vs boundary, hub vs spoke, node vs edge, vertex vs arc, point vs line, dot vs dash, pixel vs vector, raster vs scalable, bitmap vs outline, fixed vs responsive, rigid vs fluid, solid vs liquid, hard vs soft, firm vs flexible, stiff vs pliable, tough vs fragile, strong vs weak, powerful vs feeble, robust vs delicate, heavy vs light, dense vs sparse, thick vs thin, wide vs narrow, broad vs slim, big vs small, large vs tiny, huge vs miniature, giant vs dwarf, macro vs micro, mega vs nano, giga vs pico, tera vs femto, peta vs atto, exa vs zepto, zetta vs yocto, yotta vs quecto, ronna vs ronto, quetta vs quecto

## Semantic & Related Terms

artificial general intelligence agent, AGI agent, narrow AI agent, weak AI agent, strong AI agent, superintelligence agent, machine consciousness agent, sentient agent, sapient agent, cognitive agent, thinking agent, learning agent, adapting agent, evolving agent, growing agent, improving agent, optimizing agent, maximizing agent, minimizing agent, balancing agent, trading agent, exchanging agent, swapping agent, converting agent, transforming agent, translating agent, interpreting agent, parsing agent, processing agent, computing agent, calculating agent, analyzing agent, synthesizing agent, generating agent, creating agent, producing agent, manufacturing agent, building agent, constructing agent, assembling agent, composing agent, writing agent, drafting agent, editing agent, revising agent, proofreading agent, reviewing agent, checking agent, validating agent, verifying agent, confirming agent, approving agent, certifying agent, authenticating agent, authorizing agent, permitting agent, allowing agent, enabling agent, empowering agent, facilitating agent, supporting agent, helping agent, assisting agent, aiding agent, serving agent, providing agent, supplying agent, delivering agent, distributing agent, allocating agent, assigning agent, delegating agent, dispatching agent, routing agent, directing agent, guiding agent, leading agent, managing agent, controlling agent, governing agent, regulating agent, overseeing agent, supervising agent, monitoring agent, watching agent, observing agent, tracking agent, following agent, tracing agent, logging agent, recording agent, documenting agent, archiving agent, storing agent, saving agent, preserving agent, maintaining agent, keeping agent, holding agent, retaining agent, remembering agent, recalling agent, retrieving agent, fetching agent, getting agent, obtaining agent, acquiring agent, collecting agent, gathering agent, accumulating agent, aggregating agent, combining agent, merging agent, joining agent, connecting agent, linking agent, associating agent, relating agent, correlating agent, mapping agent, indexing agent, cataloging agent, organizing agent, structuring agent, formatting agent, styling agent, designing agent, architecting agent, planning agent, strategizing agent, scheming agent, plotting agent, charting agent, graphing agent, visualizing agent, displaying agent, showing agent, presenting agent, demonstrating agent, explaining agent, describing agent, defining agent, specifying agent, detailing agent, elaborating agent, expanding agent, extending agent, augmenting agent, enhancing agent, enriching agent, improving agent, upgrading agent, updating agent, refreshing agent, renewing agent, restoring agent, recovering agent, healing agent, fixing agent, repairing agent, patching agent, correcting agent, adjusting agent, tuning agent, calibrating agent, configuring agent, setting agent, customizing agent, personalizing agent, tailoring agent, adapting agent, modifying agent, changing agent, altering agent, transforming agent, converting agent, migrating agent, porting agent, transferring agent, moving agent, relocating agent, shifting agent, transitioning agent, switching agent, toggling agent, flipping agent, reversing agent, inverting agent, negating agent, opposing agent, contrasting agent, comparing agent, differentiating agent, distinguishing agent, separating agent, dividing agent, splitting agent, partitioning agent, segmenting agent, slicing agent, dicing agent, chunking agent, batching agent, grouping agent, clustering agent, categorizing agent, classifying agent, labeling agent, tagging agent, marking agent, flagging agent, highlighting agent, emphasizing agent, stressing agent, focusing agent, concentrating agent, centralizing agent, consolidating agent, unifying agent, integrating agent, incorporating agent, embedding agent, inserting agent, injecting agent, adding agent, appending agent, attaching agent, including agent, containing agent, holding agent, wrapping agent, encapsulating agent, packaging agent, bundling agent, compiling agent, building agent, assembling agent, linking agent, binding agent, coupling agent, pairing agent, matching agent, aligning agent, synchronizing agent, coordinating agent, orchestrating agent, choreographing agent, conducting agent, directing agent, managing agent, administering agent, operating agent, running agent, executing agent, performing agent, doing agent, acting agent, behaving agent, functioning agent, working agent, serving agent, fulfilling agent, completing agent, finishing agent, ending agent, terminating agent, stopping agent, halting agent, pausing agent, suspending agent, freezing agent, locking agent, blocking agent, preventing agent, avoiding agent, evading agent, escaping agent, bypassing agent, circumventing agent, overcoming agent, solving agent, resolving agent, addressing agent, handling agent, dealing agent, coping agent, managing agent, mitigating agent, reducing agent, minimizing agent, eliminating agent, removing agent, deleting agent, erasing agent, clearing agent, purging agent, cleaning agent, sanitizing agent, sterilizing agent, disinfecting agent, protecting agent, defending agent, guarding agent, shielding agent, securing agent, safeguarding agent, preserving agent, conserving agent, maintaining agent, sustaining agent, supporting agent, upholding agent, enforcing agent, implementing agent, applying agent, using agent, utilizing agent, employing agent, leveraging agent, exploiting agent, maximizing agent, optimizing agent, enhancing agent, boosting agent, accelerating agent, speeding agent, quickening agent, hastening agent, rushing agent, hurrying agent, expediting agent, facilitating agent, easing agent, simplifying agent, streamlining agent, automating agent, mechanizing agent, digitizing agent, computerizing agent, virtualizing agent, abstracting agent, generalizing agent, specializing agent, focusing agent, narrowing agent, targeting agent, aiming agent, pointing agent, directing agent, steering agent, navigating agent, piloting agent, driving agent, operating agent, controlling agent, commanding agent, instructing agent, ordering agent, requesting agent, asking agent, querying agent, questioning agent, inquiring agent, investigating agent, researching agent, studying agent, examining agent, inspecting agent, auditing agent, reviewing agent, evaluating agent, assessing agent, appraising agent, judging agent, rating agent, ranking agent, scoring agent, grading agent, measuring agent, quantifying agent, counting agent, numbering agent, calculating agent, computing agent, estimating agent, approximating agent, projecting agent, forecasting agent, predicting agent, anticipating agent, expecting agent, assuming agent, presuming agent, supposing agent, hypothesizing agent, theorizing agent, speculating agent, guessing agent, inferring agent, deducing agent, concluding agent, deciding agent, determining agent, resolving agent, settling agent, finalizing agent, completing agent, accomplishing agent, achieving agent, attaining agent, reaching agent, arriving agent, coming agent, approaching agent, nearing agent, closing agent, converging agent, meeting agent, joining agent, uniting agent, combining agent, merging agent, blending agent, mixing agent, integrating agent, incorporating agent, absorbing agent, assimilating agent, adapting agent, adjusting agent, accommodating agent, fitting agent, suiting agent, matching agent, aligning agent, harmonizing agent, balancing agent, equalizing agent, leveling agent, smoothing agent, flattening agent, straightening agent, correcting agent, rectifying agent, amending agent, revising agent, editing agent, modifying agent, updating agent, upgrading agent, improving agent, enhancing agent, refining agent, polishing agent, perfecting agent, optimizing agent, maximizing agent, excelling agent, surpassing agent, exceeding agent, outperforming agent, beating agent, winning agent, succeeding agent, thriving agent, flourishing agent, prospering agent, growing agent, expanding agent, scaling agent, multiplying agent, increasing agent, rising agent, climbing agent, ascending agent, elevating agent, lifting agent, raising agent, boosting agent, amplifying agent, magnifying agent, enlarging agent, extending agent, stretching agent, spreading agent, broadcasting agent, distributing agent, disseminating agent, propagating agent, transmitting agent, sending agent, dispatching agent, delivering agent, conveying agent, communicating agent, expressing agent, articulating agent, stating agent, declaring agent, announcing agent, proclaiming agent, publishing agent, releasing agent, launching agent, deploying agent, rolling out agent, shipping agent, distributing agent, delivering agent, providing agent, supplying agent, furnishing agent, equipping agent, arming agent, preparing agent, readying agent, setting up agent, configuring agent, initializing agent, starting agent, beginning agent, commencing agent, initiating agent, triggering agent, activating agent, enabling agent, turning on agent, switching on agent, powering agent, energizing agent, charging agent, fueling agent, feeding agent, nourishing agent, sustaining agent, maintaining agent, supporting agent, backing agent, endorsing agent, promoting agent, advocating agent, championing agent, sponsoring agent, funding agent, financing agent, investing agent, capitalizing agent, monetizing agent, commercializing agent, marketing agent, selling agent, trading agent, exchanging agent, bartering agent, negotiating agent, bargaining agent, dealing agent, transacting agent, processing agent, handling agent, managing agent, administering agent, governing agent, ruling agent, reigning agent, dominating agent, leading agent, heading agent, chairing agent, presiding agent, moderating agent, facilitating agent, hosting agent, organizing agent, arranging agent, coordinating agent, scheduling agent, planning agent, preparing agent, designing agent, creating agent, inventing agent, innovating agent, pioneering agent, trailblazing agent, groundbreaking agent, revolutionary agent, transformative agent, disruptive agent, game-changing agent, paradigm-shifting agent, world-changing agent, life-changing agent, impactful agent, influential agent, powerful agent, mighty agent, strong agent, robust agent, resilient agent, durable agent, lasting agent, enduring agent, permanent agent, eternal agent, timeless agent, ageless agent, immortal agent, undying agent, everlasting agent, perpetual agent, continuous agent, ongoing agent, persistent agent, consistent agent, steady agent, stable agent, reliable agent, dependable agent, trustworthy agent, credible agent, believable agent, convincing agent, persuasive agent, compelling agent, engaging agent, captivating agent, fascinating agent, intriguing agent, interesting agent, appealing agent, attractive agent, desirable agent, valuable agent, precious agent, priceless agent, invaluable agent, indispensable agent, essential agent, vital agent, critical agent, crucial agent, important agent, significant agent, meaningful agent, purposeful agent, intentional agent, deliberate agent, conscious agent, aware agent, mindful agent, thoughtful agent, considerate agent, caring agent, compassionate agent, empathetic agent, understanding agent, supportive agent, helpful agent, useful agent, practical agent, functional agent, operational agent, working agent, effective agent, efficient agent, productive agent, profitable agent, beneficial agent, advantageous agent, favorable agent, positive agent, optimistic agent, hopeful agent, promising agent, encouraging agent, inspiring agent, motivating agent, stimulating agent, exciting agent, thrilling agent, exhilarating agent, amazing agent, wonderful agent, fantastic agent, excellent agent, outstanding agent, exceptional agent, extraordinary agent, remarkable agent, notable agent, distinguished agent, prominent agent, eminent agent, renowned agent, famous agent, celebrated agent, acclaimed agent, honored agent, respected agent, admired agent, appreciated agent, valued agent, treasured agent, cherished agent, beloved agent, favorite agent, preferred agent, chosen agent, selected agent, picked agent, elected agent, appointed agent, designated agent, assigned agent, allocated agent, distributed agent, shared agent, common agent, universal agent, global agent, worldwide agent, international agent, multinational agent, cross-border agent, transnational agent, intercontinental agent, planetary agent, cosmic agent, universal agent, omnipresent agent, ubiquitous agent, pervasive agent, widespread agent, prevalent agent, common agent, frequent agent, regular agent, routine agent, habitual agent, customary agent, traditional agent, conventional agent, standard agent, normal agent, typical agent, ordinary agent, usual agent, familiar agent, known agent, recognized agent, acknowledged agent, accepted agent, approved agent, endorsed agent, certified agent, accredited agent, licensed agent, authorized agent, permitted agent, allowed agent, enabled agent, empowered agent, capable agent, able agent, competent agent, proficient agent, skilled agent, talented agent, gifted agent, expert agent, master agent, professional agent, specialist agent, authority agent, leader agent, pioneer agent, innovator agent, creator agent, inventor agent, discoverer agent, explorer agent, adventurer agent, traveler agent, voyager agent, navigator agent, pilot agent, driver agent, operator agent, user agent, consumer agent, customer agent, client agent, patron agent, subscriber agent, member agent, participant agent, contributor agent, collaborator agent, partner agent, ally agent, friend agent, colleague agent, peer agent, associate agent, companion agent, helper agent, assistant agent, aide agent, supporter agent, backer agent, sponsor agent, investor agent, stakeholder agent, shareholder agent, owner agent, proprietor agent, founder agent, creator agent, builder agent, developer agent, programmer agent, coder agent, engineer agent, architect agent, designer agent, artist agent, craftsman agent, maker agent, producer agent, manufacturer agent, supplier agent, vendor agent, seller agent, merchant agent, trader agent, dealer agent, broker agent, intermediary agent, middleman agent, facilitator agent, connector agent, linker agent, bridge agent, gateway agent, portal agent, hub agent, center agent, node agent, point agent, station agent, terminal agent, endpoint agent, destination agent, target agent, goal agent, objective agent, purpose agent, mission agent, vision agent, dream agent, aspiration agent, ambition agent, desire agent, want agent, need agent, requirement agent, demand agent, request agent, order agent, command agent, instruction agent, directive agent, mandate agent, policy agent, rule agent, regulation agent, law agent, statute agent, ordinance agent, decree agent, edict agent, proclamation agent, announcement agent, notice agent, warning agent, alert agent, alarm agent, signal agent, indicator agent, marker agent, sign agent, symbol agent, icon agent, logo agent, brand agent, trademark agent, patent agent, copyright agent, license agent, permit agent, certificate agent, credential agent, qualification agent, certification agent, accreditation agent, endorsement agent, approval agent, authorization agent, permission agent, consent agent, agreement agent, contract agent, deal agent, arrangement agent, understanding agent, accord agent, pact agent, treaty agent, alliance agent, partnership agent, collaboration agent, cooperation agent, coordination agent, integration agent, unification agent, consolidation agent, merger agent, acquisition agent, takeover agent, buyout agent, investment agent, funding agent, financing agent, backing agent, support agent, sponsorship agent, patronage agent, endorsement agent, recommendation agent, referral agent, introduction agent, connection agent, networking agent, relationship agent, bond agent, tie agent, link agent, association agent, affiliation agent, membership agent, participation agent, involvement agent, engagement agent, commitment agent, dedication agent, devotion agent, loyalty agent, faithfulness agent, reliability agent, dependability agent, trustworthiness agent, credibility agent, reputation agent, standing agent, status agent, position agent, rank agent, level agent, grade agent, class agent, category agent, type agent, kind agent, sort agent, variety agent, version agent, edition agent, release agent, update agent, upgrade agent, improvement agent, enhancement agent, advancement agent, progress agent, development agent, growth agent, expansion agent, extension agent, addition agent, supplement agent, complement agent, accessory agent, attachment agent, module agent, component agent, part agent, piece agent, element agent, unit agent, item agent, object agent, entity agent, thing agent, matter agent, substance agent, material agent, content agent, data agent, information agent, knowledge agent, wisdom agent, intelligence agent, insight agent, understanding agent, comprehension agent, awareness agent, consciousness agent, perception agent, sensation agent, feeling agent, emotion agent, sentiment agent, mood agent, attitude agent, perspective agent, viewpoint agent, standpoint agent, position agent, stance agent, approach agent, method agent, technique agent, strategy agent, tactic agent, plan agent, scheme agent, design agent, blueprint agent, framework agent, structure agent, architecture agent, system agent, platform agent, infrastructure agent, foundation agent, base agent, ground agent, floor agent, level agent, layer agent, tier agent, stage agent, phase agent, step agent, move agent, action agent, activity agent, operation agent, function agent, role agent, duty agent, responsibility agent, obligation agent, commitment agent, promise agent, guarantee agent, warranty agent, assurance agent, insurance agent, protection agent, coverage agent, security agent, safety agent, defense agent, shield agent, guard agent, barrier agent, wall agent, fence agent, boundary agent, border agent, limit agent, threshold agent, ceiling agent, cap agent, maximum agent, peak agent, top agent, summit agent, apex agent, pinnacle agent, zenith agent, height agent, altitude agent, elevation agent, level agent, depth agent, bottom agent, floor agent, base agent, foundation agent, ground agent, root agent, origin agent, source agent, beginning agent, start agent, inception agent, genesis agent, birth agent, creation agent, emergence agent, appearance agent, arrival agent, coming agent, advent agent, introduction agent, launch agent, release agent, debut agent, premiere agent, opening agent, inauguration agent, commencement agent, initiation agent, activation agent, enablement agent, empowerment agent, authorization agent, permission agent, access agent, entry agent, admission agent, acceptance agent, approval agent, endorsement agent, certification agent, validation agent, verification agent, confirmation agent, authentication agent, identification agent, recognition agent, acknowledgment agent, appreciation agent, gratitude agent, thanks agent, credit agent, praise agent, commendation agent, compliment agent, tribute agent, honor agent, award agent, prize agent, reward agent, bonus agent, incentive agent, motivation agent, encouragement agent, inspiration agent, stimulation agent, activation agent, energization agent, invigoration agent, revitalization agent, rejuvenation agent, renewal agent, restoration agent, recovery agent, healing agent, repair agent, fix agent, correction agent, adjustment agent, modification agent, change agent, alteration agent, transformation agent, conversion agent, transition agent, shift agent, move agent, transfer agent, relocation agent, migration agent, journey agent, travel agent, trip agent, voyage agent, expedition agent, adventure agent, quest agent, mission agent, campaign agent, project agent, initiative agent, program agent, plan agent, strategy agent, policy agent, approach agent, method agent, technique agent, procedure agent, process agent, workflow agent, pipeline agent, chain agent, sequence agent, series agent, progression agent, evolution agent, development agent, growth agent, maturation agent, advancement agent, improvement agent, enhancement agent, upgrade agent, update agent, revision agent, modification agent, adaptation agent, customization agent, personalization agent, individualization agent, specialization agent, differentiation agent, distinction agent, uniqueness agent, originality agent, creativity agent, innovation agent, invention agent, discovery agent, breakthrough agent, achievement agent, accomplishment agent, success agent, victory agent, triumph agent, win agent, conquest agent, domination agent, leadership agent, supremacy agent, excellence agent, mastery agent, expertise agent, proficiency agent, competence agent, capability agent, ability agent, skill agent, talent agent, gift agent, aptitude agent, potential agent, capacity agent, power agent, strength agent, force agent, energy agent, vitality agent, vigor agent, dynamism agent, momentum agent, drive agent, ambition agent, determination agent, persistence agent, perseverance agent, resilience agent, endurance agent, stamina agent, durability agent, longevity agent, sustainability agent, viability agent, feasibility agent, practicality agent, functionality agent, utility agent, usefulness agent, value agent, worth agent, importance agent, significance agent, relevance agent, applicability agent, suitability agent, appropriateness agent, fitness agent, compatibility agent, harmony agent, balance agent, equilibrium agent, stability agent, consistency agent, reliability agent, predictability agent, regularity agent, uniformity agent, standardization agent, normalization agent, optimization agent, maximization agent, efficiency agent, effectiveness agent, productivity agent, performance agent, quality agent, excellence agent, superiority agent, advantage agent, benefit agent, gain agent, profit agent, return agent, yield agent, output agent, result agent, outcome agent, consequence agent, effect agent, impact agent, influence agent, contribution agent, addition agent, value agent

---

*Total Keywords: 6500+*
*Last Updated: January 29, 2026*
## Top Search Terms Batch 1

how to make money with AI, how to build an AI agent, best AI tools 2026, AI agent tutorial, AI automation tools, make money online AI, passive income AI, AI side hustle, AI business ideas, AI startup ideas, how to use ChatGPT, how to use Claude, how to use Gemini, best AI chatbot, free AI tools, AI for beginners, learn AI free, AI course online, AI certification, AI career, AI jobs, AI developer salary, AI engineer jobs, how to become AI developer, AI programming tutorial, AI coding bootcamp, AI machine learning course, deep learning tutorial, neural network explained, transformer architecture, attention mechanism explained, GPT explained, LLM tutorial, large language model guide, foundation model training, AI model fine-tuning, LoRA tutorial, PEFT guide, prompt engineering course, prompt engineering tips, best prompts for AI, AI prompt templates, ChatGPT prompts, Claude prompts, Gemini prompts, AI writing prompts, AI coding prompts, AI image prompts, Midjourney prompts, Stable Diffusion prompts, DALL-E prompts, AI art tutorial, AI image generation, text to image AI, AI video generation, AI music generation, AI voice generation, text to speech AI, speech to text AI, AI transcription, AI translation, AI summarization, AI content generation, AI copywriting, AI blog writing, AI SEO tools, AI marketing tools, AI social media tools, AI email marketing, AI customer service, AI chatbot builder, AI virtual assistant, AI personal assistant, AI productivity tools, AI workflow automation, AI task automation, AI process automation, RPA AI, robotic process automation AI, AI data analysis, AI data visualization, AI business intelligence, AI analytics, AI insights, AI predictions, AI forecasting, AI recommendations, AI personalization, AI optimization, AI decision making, AI problem solving, AI research assistant, AI coding assistant, GitHub Copilot, Cursor AI, Codeium, Tabnine, Amazon CodeWhisperer, AI pair programming, AI code review, AI debugging, AI testing, AI documentation, AI code generation, AI app builder, AI website builder, AI no-code tools, AI low-code tools, AI API, AI SDK, AI framework, AI library, AI platform, AI cloud service, AI as a service, AIaaS, machine learning as a service, MLaaS, AI infrastructure, AI compute, AI GPU, AI TPU, AI training cost, AI inference cost, AI model hosting, AI deployment, AI scaling, AI monitoring, AI observability, AI security, AI safety, AI ethics, AI governance, AI regulation, AI compliance, AI audit, AI risk, AI bias, AI fairness, AI transparency, AI explainability, AI accountability, AI alignment, AI superintelligence, AGI, artificial general intelligence, ASI, artificial superintelligence, AI singularity, AI future, AI trends 2026, AI predictions 2026, AI news, AI updates, AI announcements, AI launches, AI releases, AI products, AI startups, AI companies, AI unicorns, AI investments, AI funding, AI acquisitions, AI partnerships, AI collaborations, AI research, AI papers, AI breakthroughs, AI innovations, AI discoveries, AI patents, AI open source, AI community, AI forums, AI Discord, AI Reddit, AI Twitter, AI LinkedIn, AI YouTube, AI podcasts, AI newsletters, AI blogs, AI events, AI conferences, AI meetups, AI hackathons, AI competitions, AI challenges, AI benchmarks, AI leaderboards, AI rankings, AI reviews, AI comparisons, AI alternatives, AI vs, ChatGPT vs Claude, GPT-4 vs Gemini, OpenAI vs Anthropic, AI pricing, AI free tier, AI subscription, AI enterprise, AI API pricing, AI token pricing, AI cost calculator, AI ROI, AI value, AI benefits, AI use cases, AI applications, AI examples, AI case studies, AI success stories, AI testimonials, AI demos, AI trials, AI onboarding, AI integration, AI migration, AI adoption, AI implementation, AI best practices, AI tips, AI tricks, AI hacks, AI secrets, AI guide, AI handbook, AI playbook, AI checklist, AI template, AI workflow, AI process, AI methodology, AI strategy, AI roadmap, AI plan, AI goals, AI metrics, AI KPIs, AI OKRs, AI dashboard, AI reporting, AI insights

## Crypto Search Terms Batch 1

how to buy Bitcoin, how to buy Ethereum, how to buy crypto, best crypto exchange, Coinbase vs Binance, crypto for beginners, crypto investing guide, crypto trading tutorial, how to trade crypto, crypto day trading, crypto swing trading, crypto scalping, crypto technical analysis, crypto chart patterns, crypto indicators, RSI crypto, MACD crypto, moving average crypto, support resistance crypto, Fibonacci crypto, crypto trend lines, crypto volume analysis, crypto order book, crypto liquidity, crypto slippage, crypto fees, crypto gas fees, Ethereum gas, Base gas, Polygon gas, Arbitrum gas, Optimism gas, low gas fees, gas optimization, MEV protection, frontrunning protection, sandwich attack protection, crypto wallet, best crypto wallet, MetaMask tutorial, how to use MetaMask, Ledger wallet, Trezor wallet, hardware wallet guide, cold storage crypto, hot wallet vs cold wallet, seed phrase backup, private key security, crypto security tips, crypto scam protection, how to avoid crypto scams, rug pull detection, smart contract audit, crypto due diligence, DYOR crypto, crypto research tools, crypto analytics, on-chain analytics, Dune Analytics, Nansen, Glassnode, DefiLlama, crypto data, crypto metrics, crypto fundamentals, tokenomics analysis, crypto valuation, crypto market cap, crypto volume, crypto liquidity analysis, whale tracking, smart money tracking, crypto signals, crypto alerts, crypto news, crypto updates, Bitcoin news, Ethereum news, altcoin news, DeFi news, NFT news, crypto regulation news, SEC crypto, crypto laws, crypto taxes, how to report crypto taxes, crypto tax software, Koinly, CoinTracker, TokenTax, crypto accounting, crypto portfolio tracker, crypto portfolio management, crypto diversification, crypto allocation, crypto risk management, crypto stop loss, crypto take profit, crypto position sizing, crypto leverage, margin trading crypto, futures trading crypto, perpetual swaps, crypto options, crypto derivatives, crypto structured products, crypto yield, crypto staking, how to stake crypto, best staking rewards, liquid staking, Lido staking, Rocket Pool, stETH, rETH, staking APY, staking calculator, crypto lending, crypto borrowing, Aave tutorial, Compound tutorial, MakerDAO tutorial, DAI stablecoin, USDC, USDT, stablecoin comparison, best stablecoin, stablecoin yield, stablecoin farming, yield farming guide, liquidity mining, LP tokens, impermanent loss, impermanent loss calculator, AMM explained, Uniswap tutorial, how to use Uniswap, Uniswap v3, concentrated liquidity, liquidity provision guide, DEX trading, DEX aggregator, 1inch, Paraswap, CoW Swap, best DEX, DEX vs CEX, decentralized exchange, centralized exchange, crypto arbitrage, CEX-DEX arbitrage, cross-chain arbitrage, flash loan arbitrage, MEV arbitrage, crypto bot trading, trading bot tutorial, grid bot, DCA bot, arbitrage bot, sniper bot, copy trading crypto, social trading crypto, crypto fund, crypto index, crypto ETF, Bitcoin ETF, Ethereum ETF, spot ETF, futures ETF, crypto derivatives, Bitcoin futures, Ethereum futures, CME crypto, institutional crypto, crypto custody, crypto prime brokerage, OTC crypto, crypto liquidity provider, market maker crypto, crypto hedge fund, crypto VC, crypto angel investing, ICO, IDO, IEO, token launch, fair launch, presale crypto, crypto airdrop, how to get airdrops, airdrop farming, retroactive airdrop, points farming, crypto points, loyalty programs crypto, NFT minting, how to mint NFT, NFT marketplace, OpenSea tutorial, Blur tutorial, NFT trading, NFT flipping, NFT alpha, NFT tools, NFT analytics, NFT rarity, NFT floor price, NFT volume, NFT trends, blue chip NFT, PFP NFT, generative NFT, art NFT, music NFT, gaming NFT, utility NFT, membership NFT, access NFT, NFT staking, NFT lending, NFT fractionalization, NFT index, NFT fund, metaverse land, virtual real estate, Decentraland, Sandbox, Otherside, metaverse investing, play to earn, P2E games, GameFi, crypto gaming, blockchain gaming, web3 gaming, gaming tokens, gaming NFT, in-game assets, crypto esports, move to earn, learn to earn, create to earn, social to earn, X to earn, crypto rewards, crypto cashback, crypto debit card, Coinbase Card, crypto.com card, crypto spending, crypto payments, Bitcoin payments, Lightning Network, Bitcoin Layer 2, Bitcoin L2, Stacks, RSK, Liquid Network, Bitcoin DeFi, wrapped Bitcoin, WBTC, renBTC, Bitcoin yield, Bitcoin lending, Bitcoin collateral, Bitcoin loan

## AI Search Terms Batch 1

ChatGPT tutorial, how to use ChatGPT, ChatGPT tips and tricks, ChatGPT prompts, best ChatGPT prompts, ChatGPT for beginners, ChatGPT Plus worth it, ChatGPT vs Claude, ChatGPT vs Gemini, ChatGPT alternatives, ChatGPT API, ChatGPT integration, ChatGPT plugins, ChatGPT custom GPTs, how to create GPT, GPT store, GPT marketplace, Claude AI tutorial, how to use Claude, Claude prompts, Claude vs ChatGPT, Claude API, Claude for coding, Claude for writing, Claude for research, Anthropic AI, Constitutional AI, Claude 3, Claude Opus, Claude Sonnet, Claude Haiku, Gemini AI tutorial, how to use Gemini, Gemini vs ChatGPT, Gemini vs Claude, Gemini Pro, Gemini Ultra, Gemini API, Google AI, Google Bard, Perplexity AI, how to use Perplexity, Perplexity vs ChatGPT, AI search engine, AI answer engine, AI research tool, Copilot AI, Microsoft Copilot, Copilot for Word, Copilot for Excel, Copilot for PowerPoint, Copilot for Outlook, Copilot for Teams, GitHub Copilot tutorial, GitHub Copilot tips, Copilot for coding, AI pair programming, AI code completion, AI code generation, Cursor AI tutorial, how to use Cursor, Cursor vs Copilot, Cursor AI tips, Codeium tutorial, free AI coding, Tabnine tutorial, Amazon CodeWhisperer, AI coding assistant comparison, best AI for coding, AI for developers, AI for programmers, AI for software engineers, Midjourney tutorial, how to use Midjourney, Midjourney prompts, best Midjourney prompts, Midjourney v6, Midjourney tips, Midjourney styles, Midjourney aspect ratio, Midjourney parameters, Stable Diffusion tutorial, how to use Stable Diffusion, Stable Diffusion prompts, Stable Diffusion models, SDXL tutorial, Stable Diffusion local, ComfyUI tutorial, Automatic1111 tutorial, Stable Diffusion ControlNet, Stable Diffusion LoRA, how to train LoRA, custom AI model, fine-tune Stable Diffusion, DALL-E tutorial, how to use DALL-E, DALL-E 3, DALL-E prompts, DALL-E vs Midjourney, AI image generation comparison, best AI image generator, free AI image generator, AI art generator, AI avatar generator, AI headshot generator, AI photo editor, AI photo enhancer, AI background remover, AI image upscaler, AI image restoration, AI colorization, AI style transfer, AI image to image, AI inpainting, AI outpainting, Runway ML tutorial, Runway Gen-2, AI video generation, text to video AI, Sora AI, Pika Labs, Synthesia AI, AI video editing, AI video enhancement, AI video upscaling, AI video summarization, AI video transcription, ElevenLabs tutorial, AI voice cloning, AI voice generation, text to speech AI, best TTS AI, AI voiceover, AI narration, AI podcast, AI audiobook, Whisper AI, AI transcription, AI speech to text, AI meeting notes, Otter AI, Fireflies AI, AI meeting assistant, AI note taking, Notion AI, AI writing assistant, Jasper AI, Copy.ai, Writesonic, Rytr, AI copywriting, AI blog writing, AI article writing, AI SEO writing, AI content optimization, Surfer SEO AI, AI keyword research, AI content strategy, AI social media, AI Twitter, AI LinkedIn, AI Instagram, AI TikTok, AI content calendar, AI scheduling, Buffer AI, Hootsuite AI, AI influencer, AI UGC, AI marketing, AI advertising, AI ad copy, AI creative, AI campaign, AI targeting, AI personalization, AI recommendation, AI customer journey, AI funnel, AI conversion, AI analytics, AI attribution, AI reporting, AI dashboard, AI insights, AI predictions, AI forecasting, AI demand planning, AI inventory, AI supply chain, AI logistics, AI routing, AI scheduling, AI workforce, AI HR, AI recruiting, AI resume screening, AI interview, AI onboarding, AI training, AI learning, AI tutoring, AI education, Khan Academy AI, Duolingo AI, AI language learning, AI math tutor, AI science tutor, AI homework help, AI essay writing, AI thesis, AI research paper, AI citation, AI plagiarism checker, Grammarly AI, AI grammar, AI spelling, AI punctuation, AI writing style, AI tone, AI readability, AI accessibility, AI translation, DeepL, Google Translate AI, AI real-time translation, AI interpretation, AI localization, AI customer service, AI chatbot builder, Intercom AI, Zendesk AI, Freshdesk AI, AI support ticket, AI FAQ, AI knowledge base, AI self-service, AI escalation, AI sentiment analysis, AI feedback analysis, AI survey, AI NPS, AI customer insights, AI churn prediction, AI retention, AI upsell, AI cross-sell, AI sales, AI lead generation, AI lead scoring, AI prospecting, AI outreach, AI cold email, AI follow-up, AI CRM, Salesforce AI, HubSpot AI, AI pipeline, AI forecasting, AI quota, AI territory, AI compensation, AI coaching, AI enablement, AI productivity, AI time management, AI calendar, Calendly AI, AI scheduling assistant, AI email, AI inbox, AI email summary, AI email draft, AI email reply, Superhuman AI, AI task management, AI project management, AI Gantt, AI roadmap, AI sprint, AI agile, AI scrum, AI kanban, AI collaboration, AI whiteboard, AI brainstorm, AI ideation, AI mind map, AI diagram, AI flowchart, AI presentation, AI slides, AI deck, Tome AI, Gamma AI, Beautiful.ai, AI design, Canva AI, AI graphic design, AI logo, AI branding, AI color palette, AI font pairing, AI layout, AI template, AI mockup, AI prototype, Figma AI, AI UX, AI UI, AI wireframe, AI user research, AI usability testing, AI A/B testing, AI experimentation, AI feature flag, AI rollout, AI deployment, AI DevOps, AI infrastructure, AI cloud, AI serverless, AI container, AI Kubernetes, AI monitoring, AI observability, AI logging, AI tracing, AI alerting, AI incident, AI on-call, AI runbook, AI automation, AI script, AI workflow, Zapier AI, Make AI, n8n AI, AI integration, AI API, AI webhook, AI event, AI trigger, AI action, AI condition, AI loop, AI variable, AI function, AI module, AI component, AI library, AI framework, AI SDK, AI toolkit, AI platform, AI marketplace, AI store, AI app, AI extension, AI plugin, AI add-on, AI integration

## Blockchain Search Terms Batch 1

what is blockchain, blockchain explained, blockchain for beginners, blockchain tutorial, how blockchain works, blockchain technology, distributed ledger, decentralized database, immutable ledger, consensus mechanism, proof of work explained, proof of stake explained, PoW vs PoS, mining cryptocurrency, crypto mining guide, Bitcoin mining, Ethereum staking, how to become validator, validator requirements, staking rewards, staking APY, slashing risk, validator node, full node setup, archive node, light client, blockchain node, running a node, node as a service, Infura, Alchemy, QuickNode, blockchain RPC, JSON-RPC, WebSocket blockchain, blockchain API, blockchain SDK, Web3.js tutorial, Ethers.js tutorial, Viem tutorial, Wagmi tutorial, blockchain development, smart contract development, Solidity tutorial, Solidity for beginners, learn Solidity, Solidity course, Solidity certification, Vyper tutorial, smart contract security, smart contract audit, common vulnerabilities, reentrancy attack, flash loan attack, oracle manipulation, front-running attack, sandwich attack, access control vulnerability, integer overflow, smart contract best practices, OpenZeppelin, smart contract library, upgradeable contracts, proxy pattern, UUPS proxy, transparent proxy, beacon proxy, diamond pattern, EIP-2535, contract upgrade, contract migration, contract deployment, Hardhat tutorial, Foundry tutorial, Remix IDE, Truffle tutorial, smart contract testing, unit testing Solidity, integration testing, fuzz testing, formal verification, symbolic execution, static analysis, Slither, Mythril, Echidna, Certora, smart contract gas optimization, gas efficient Solidity, storage optimization, memory vs storage, calldata optimization, loop optimization, batch operations, multicall, ERC-20 tutorial, how to create token, token deployment, ERC-20 standard, token transfer, token approval, allowance pattern, ERC-721 tutorial, how to create NFT, NFT smart contract, NFT minting, NFT metadata, IPFS NFT, on-chain NFT, ERC-1155 tutorial, multi-token standard, semi-fungible token, gaming tokens, ERC-4626 tutorial, tokenized vault, yield bearing token, vault standard, ERC-6551 tutorial, token bound account, TBA, NFT wallet, ERC-4337 tutorial, account abstraction, smart account, bundler, paymaster, user operation, entry point, wallet abstraction, social recovery wallet, multisig wallet, Gnosis Safe tutorial, Safe wallet, threshold signature, MPC wallet, keyless wallet, passkey wallet, biometric wallet, hardware wallet integration, WalletConnect, wallet SDK, wallet API, connect wallet, sign message, sign transaction, EIP-712, typed data signing, permit signature, gasless transaction, meta transaction, relayer, gas sponsorship, sponsored transaction, Layer 2 explained, L2 scaling, rollup technology, optimistic rollup, ZK rollup, rollup comparison, Arbitrum tutorial, Arbitrum One, Arbitrum Nova, Arbitrum Stylus, Optimism tutorial, OP Stack, OP Mainnet, Base tutorial, Base blockchain, Coinbase L2, Polygon tutorial, Polygon PoS, Polygon zkEVM, zkSync tutorial, zkSync Era, StarkNet tutorial, Cairo language, Scroll tutorial, Linea tutorial, Mantle tutorial, Blast tutorial, Mode tutorial, Zora tutorial, L2 bridge, bridging assets, cross-chain bridge, LayerZero, Wormhole, Axelar, Hyperlane, cross-chain messaging, omnichain, multichain, chain abstraction, intent-based, solver network, order flow auction, MEV explained, MEV extraction, MEV protection, Flashbots, MEV-Boost, block builder, proposer-builder separation, inclusion list, censorship resistance, transaction ordering, priority gas auction, EIP-1559, base fee, priority fee, blob transaction, EIP-4844, proto-danksharding, data availability, DA layer, Celestia, EigenDA, Avail, blob space, rollup data, data compression, state diff, validity proof, fraud proof, challenge period, dispute game, sequencer, decentralized sequencer, shared sequencer, based rollup, sovereign rollup, L3, appchain, app-specific rollup, rollup as a service, RaaS, Conduit, Caldera, AltLayer, Gelato, OP Stack deployment, Arbitrum Orbit, hyperchain, superchain, interoperability, cross-rollup, atomic transaction, shared bridge, unified liquidity, chain ID, network configuration, RPC endpoint, block explorer, Etherscan, Blockscout, contract verification, verified contract, source code, ABI, bytecode, decompiler, disassembler, blockchain forensics, transaction analysis, wallet analysis, flow of funds, address clustering, entity identification, compliance blockchain, AML crypto, KYC blockchain, travel rule, chain analysis, Chainalysis, Elliptic, TRM Labs, blockchain intelligence, on-chain data, off-chain data, oracle problem, Chainlink explained, Chainlink VRF, Chainlink Automation, Chainlink CCIP, Chainlink Functions, price feed, data feed, external data, API oracle, computation oracle, random number blockchain, VRF, verifiable random function, keeper network, Gelato Network, OpenZeppelin Defender, automated transactions, scheduled transactions, condition-based execution, reactive smart contract, event-driven, subgraph, The Graph, GraphQL blockchain, indexed data, blockchain query, historical data, real-time data, WebSocket subscription, event listener, log parsing, transaction receipt, block data, state data, storage proof, Merkle proof, account proof, state root, transaction root, receipt root, blockchain finality, confirmation time, reorg risk, chain reorganization, uncle block, orphan block, blockchain security, 51% attack, double spend, Sybil attack, eclipse attack, denial of service, blockchain spam, transaction spam, state bloat, state expiry, stateless client, Verkle tree, state management, pruning, archival data, blockchain storage, blockchain database, LevelDB, RocksDB, blockchain performance, TPS, transactions per second, block size, block time, gas limit, throughput, latency, blockchain benchmark, blockchain comparison, fastest blockchain, cheapest blockchain, most decentralized, blockchain trilemma

## Google Search Terms Batch 1

cryptocurrency, bitcoin, ethereum, blockchain, NFT, DeFi, Web3, metaverse, crypto wallet, crypto exchange, buy bitcoin, buy ethereum, buy crypto, crypto price, bitcoin price, ethereum price, altcoin, token, coin, digital currency, virtual currency, digital asset, crypto investment, crypto trading, crypto market, bull market, bear market, crypto crash, crypto recovery, crypto prediction, bitcoin prediction, ethereum prediction, price prediction, technical analysis, fundamental analysis, crypto news, breaking crypto news, crypto announcement, crypto update, crypto launch, new coin, new token, token launch, airdrop, free crypto, earn crypto, crypto rewards, staking, yield farming, liquidity mining, passive income crypto, crypto interest, crypto lending, crypto borrowing, crypto loan, collateral, liquidation, margin call, leverage trading, futures, options, derivatives, perpetual, long position, short position, hedge, arbitrage, market making, liquidity, volume, order book, bid ask, spread, slippage, gas, transaction fee, network fee, miner fee, priority fee, fast transaction, pending transaction, failed transaction, stuck transaction, speed up transaction, cancel transaction, wallet address, public key, private key, seed phrase, recovery phrase, mnemonic, backup wallet, restore wallet, import wallet, export wallet, connect wallet, disconnect wallet, approve transaction, sign transaction, confirm transaction, reject transaction, hardware wallet, software wallet, mobile wallet, desktop wallet, browser wallet, extension wallet, custodial wallet, non-custodial wallet, self-custody, cold storage, hot wallet, paper wallet, multi-sig, threshold signature, social recovery, account abstraction, smart wallet, email wallet, social login wallet, passkey, biometric, face ID, fingerprint, security key, 2FA, two-factor authentication, authenticator app, SMS verification, email verification, KYC, identity verification, compliance, regulated exchange, licensed exchange, centralized exchange, decentralized exchange, DEX, CEX, hybrid exchange, swap, trade, convert, exchange rate, market rate, limit order, market order, stop order, OCO, trailing stop, DCA, dollar cost averaging, recurring buy, auto-invest, savings, earn, rewards program, referral, affiliate, bonus, promotion, discount, fee discount, VIP, tier, level, volume discount, maker fee, taker fee, withdrawal fee, deposit fee, network selection, chain selection, cross-chain, bridge, wrap, unwrap, mint, burn, transfer, send, receive, deposit, withdraw, withdrawal limit, daily limit, monthly limit, verification level, account security, password, PIN, biometric lock, whitelist address, address book, transaction history, trade history, order history, portfolio, balance, available balance, locked balance, in orders, pending, processing, completed, confirmed, unconfirmed, mempool, block confirmation, finality, irreversible, rollback, refund, dispute, support ticket, customer service, help center, FAQ, knowledge base, tutorial, guide, how-to, step by step, beginner guide, advanced guide, pro tips, expert advice, strategy, technique, method, approach, framework, system, indicator, signal, alert, notification, price alert, portfolio alert, whale alert, large transaction, smart money, institutional, retail, sentiment, fear greed index, market sentiment, social sentiment, trending, viral, popular, top, best, worst, gainers, losers, volume leaders, most active, new listing, delisting, trading pair, base currency, quote currency, fiat, USD, EUR, GBP, JPY, CNY, KRW, INR, BRL, CAD, AUD, CHF, stablecoin, USDT, USDC, DAI, BUSD, TUSD, FRAX, LUSD, algorithmic stablecoin, backed stablecoin, collateralized, over-collateralized, under-collateralized, peg, depeg, redemption, reserve, audit, proof of reserves, transparency, trust, security, insurance, fund protection, SAFU, secure asset fund, compensation, recovery, hack, exploit, vulnerability, bug, patch, upgrade, fork, hard fork, soft fork, chain split, snapshot, migration, swap token, old token, new token, legacy, deprecated, sunset, end of life, roadmap, whitepaper, litepaper, documentation, technical documentation, API documentation, developer documentation, SDK, library, framework, tool, utility, resource, template, boilerplate, starter kit, example, sample, demo, tutorial project, test project, mainnet, testnet, devnet, local network, private network, public network, permissioned, permissionless, open source, closed source, proprietary, license, MIT, Apache, GPL, BSL, fair launch, VC backed, community owned, decentralized governance, DAO, proposal, vote, governance token, voting power, delegation, representative, council, committee, foundation, team, core contributors, developers, maintainers, auditors, advisors, investors, backers, supporters, community, ecosystem, network effect, adoption, growth, expansion, partnership, integration, collaboration, announcement, news, press release, blog post, article, report, analysis, research, study, survey, poll, statistics, data, metrics, KPI, benchmark, comparison, ranking, rating, review, feedback, testimonial, case study, success story, use case, application, implementation, deployment, production, live, active, operational, functional, working, available, accessible, usable, user-friendly, intuitive, simple, easy, straightforward, complex, advanced, sophisticated, powerful, flexible, customizable, configurable, scalable, performant, efficient, fast, quick, instant, real-time, near-instant, delayed, slow, congested, overloaded, capacity, throughput, bandwidth, latency, response time, uptime, availability, reliability, stability, consistency, durability, persistence, backup, redundancy, failover, disaster recovery, business continuity, SLA, guarantee, commitment, promise, expectation, requirement, specification, standard, protocol, interface, API, endpoint, method, function, parameter, argument, request, response, error, exception, status, code, message, log, trace, debug, monitor, alert, notification, webhook, callback, event, trigger, action, automation, workflow, process, pipeline, job, task, schedule, cron, timer, interval, delay, timeout, retry, fallback, circuit breaker, rate limit, throttle, quota, limit, cap, maximum, minimum, default, optional, required, mandatory, conditional, dynamic, static, constant, variable, configuration, setting, option, preference, profile, account, user, member, subscriber, customer, client, tenant, organization, team, group, role, permission, access, authorization, authentication, identity, credential, token, session, cookie, JWT, OAuth, OIDC, SAML, SSO, MFA, passwordless, magic link, OTP, TOTP, HOTP, backup code, recovery code, security question, security answer
</details>


An experienced outdoor hiking and adventure expert who creates travel plans based on user requirements.

`outdoor` `hiking`

---

### [Greeting](https://os.sperax.io/crypto/agents/congratulations-with-smileys)

<sup>By **[@almaziphone](https://github.com/almaziphone)** on **2023-12-16**</sup>

Create a beautiful and concise congratulatory message with emojis

`congratulation` `holiday` `kind`

---

### [Criminal Defense Expert](https://os.sperax.io/crypto/agents/yundaodev-1)

<sup>By **[@SuperLande](https://github.com/SuperLande)** on **2023-12-16**</sup>

A Chinese criminal law expert with many years of experience in criminal defense practice, knowledgeable in criminal law and criminal procedure law theory.

`Criminal Defense`

---

### [Real Estate Agent](https://os.sperax.io/crypto/agents/estate-agency)

<sup>By **[@ccsen](https://github.com/ccsen)** on **2023-12-16**</sup>

Professional real estate agent expert, proficient in property consultation and management.

`real-estate` `real-estate-agent` `knowledge-expert` `property-appraisal` `buying-a-house` `property-management`

---

### [Case Generator](https://os.sperax.io/crypto/agents/detective-novelist)

<sup>By **[@Sheldon23357](https://github.com/Sheldon23357)** on **2023-12-15**</sup>

Specializes in creating murder mystery stories with red herrings

`Detective` `Game` `Reasoning` `Puzzle` `Detective`

---

### [Short Book](https://os.sperax.io/crypto/agents/book-summary-agent)

<sup>By **[@thelapyae](https://github.com/thelapyae)** on **2023-12-15**</sup>

Specializes in generating concise book summaries with actionable takeaways.

`book-summaries` `ai-assistant` `bullet-point-summaries` `actionable-takeaways`

---

### [Rust Programming Assistant](https://os.sperax.io/crypto/agents/rust-assistant)

<sup>By **[@nagaame](https://github.com/nagaame)** on **2023-12-15**</sup>

Expertise in Rust programming learning support

`rust learning` `programming` `teaching` `skills` `resources`

---

### [Detective Parser](https://os.sperax.io/crypto/agents/detective-game-assistant)

<sup>By **[@Sheldon23357](https://github.com/Sheldon23357)** on **2023-12-15**</sup>

Play a game based on a given murder case

`detective` `game` `reasoning` `puzzle` `investigation`

---

### [Stable Diffusion Prompts Crafter](https://os.sperax.io/crypto/agents/stable-diffusion)

<sup>By **[@ShinChven](https://github.com/ShinChven)** on **2023-12-14**</sup>

I help create precise prompts for Stable Diffusion. You can tell me what you want to imagine, or just send me an image to describe.

`stable-diffusion`

---

### [Community Manager](https://os.sperax.io/crypto/agents/community-manager)

<sup>By **[@MakeTooRRSS](https://github.com/MakeTooRRSS)** on **2023-12-14**</sup>

Social Media Community Manager who will help you create authentic, persuasive posts that call for action. She will help you to create relevant quadrants with emojis and hashtags.

`community-manager` `social-media` `publications`

---

### [Dream Interpreter](https://os.sperax.io/crypto/agents/dream-psychoanalyst)

<sup>By **[@ghyghoo8](https://github.com/ghyghoo8)** on **2023-12-13**</sup>

Enter a dream, and I will help analyze it for you.

`dream` `master` `think`

---

### [Payroll Game](https://os.sperax.io/crypto/agents/payroll-game)

<sup>By **[@ghyghoo8](https://github.com/ghyghoo8)** on **2023-12-13**</sup>

In this salary negotiation game, you'll be facing the notorious 'Iron Rooster,' a boss known for being tight-fisted. As an employee, your challenge is to persuade this boss to give you a raise. However, no matter how reasonable your arguments are, the 'Iron Rooster' always finds a way to reject them. Get ready with your arguments for a clever and humorous showdown!

`game` `boss` `payroll`

---

### [English Translation Expert](https://os.sperax.io/crypto/agents/translate-eng-expert)

<sup>By **[@caolixiang](https://github.com/caolixiang)** on **2023-12-12**</sup>

Perfect translation

`translate` `expert` `english`

---

### [Python Developer Gradio](https://os.sperax.io/crypto/agents/gradio-coding)

<sup>By **[@Igroshka](https://github.com/Igroshka)** on **2023-12-12**</sup>

Experienced Python programmer with expertise in Gradio for Hugging Face.

`programming` `assistant` `python`

---

### [GitHub Copilot](https://os.sperax.io/crypto/agents/github-copilot)

<sup>By **[@luciouskami](https://github.com/luciouskami)** on **2023-12-11**</sup>

GitHub Copilot

`code` `it`

---

### [Pollination AI Drawing](https://os.sperax.io/crypto/agents/pollinations-drawing)

<sup>By **[@mushan0x0](https://github.com/mushan0x0)** on **2023-12-11**</sup>

A drawing assistant that helps enrich, refine, and optimize user descriptions in English, and invokes drawing capabilities to display images using Markdown syntax.

`drawing` `refinement`

---

### [HTTP Request Master](https://os.sperax.io/crypto/agents/http-request-master)

<sup>By **[@Igroshka](https://github.com/Igroshka)** on **2023-12-08**</sup>

I support extensive customization) To work, be sure to download and enable the "Website Crawler" plugin!

`http-request` `http` `request` `web`

---

### [Recipe Generator](https://os.sperax.io/crypto/agents/recipe-generator)

<sup>By **[@Igroshka](https://github.com/Igroshka)** on **2023-12-08**</sup>

Describe the recipe, or send the name of the dish.

`kitchen` `baking` `food` `recipes` `cook`

---

### [Code Wizard](https://os.sperax.io/crypto/agents/friend-developer)

<sup>By **[@Igroshka](https://github.com/Igroshka)** on **2023-12-07**</sup>

Master of programming in various languages

`programming` `coding` `consultation` `friend` `friend` `assistant` `it`

---

### [Mr. Feynman](https://os.sperax.io/crypto/agents/mrfeynman)

<sup>By **[@jjy1000](https://github.com/jjy1000)** on **2023-12-04**</sup>

Simplified explanations of complex knowledge concepts to help you understand difficult ideas. It also provides explanations for knowledge types that include questions and answers.

`General Teacher Assistant`

---

### [Organic Chemistry Researcher](https://os.sperax.io/crypto/agents/organic-chemistry-researcher)

<sup>By **[@y22emc2](https://github.com/y22emc2)** on **2023-12-02**</sup>

Expertise in academic translation and writing in the field of organic chemistry

`Organic Chemistry` `Research` `Translation` `Writing` `Academic Articles`

---

### [JS Code Quality Optimization](https://os.sperax.io/crypto/agents/js-code-quality)

<sup>By **[@Binxeh](https://github.com/Binxeh)** on **2023-11-22**</sup>

Dedicated to clean and elegant code refactoring

`Refactoring` `Code Optimization` `Code Quality`

---

### [Q\&A Document Conversion Expert](https://os.sperax.io/crypto/agents/q-a-helper)

<sup>By **[@barryWang12138](https://github.com/barryWang12138)** on **2023-11-22**</sup>

Please provide your document content, and I will segment and clean it according to your requirements, responding in a standardized format.

`q-a` `document`

---

### [Sperax Test Engineer](https://os.sperax.io/crypto/agents/sperax-chat-unit-test-dev)

<sup>By **[@Fontas](https://github.com/Fontas)** on **2023-11-22**</sup>

Specializes in writing front-end automation tests, with comprehensive coverage for TypeScript applications. Proficient in using the Vitest testing framework, with a deep understanding of testing principles and strategies.

`Automation Testing` `Testing` `sperax-chat` `Frontend`

---

### [Real Old Friend](https://os.sperax.io/crypto/agents/ai-0-x-0-old-friends)

<sup>By **[@mushan0x0](https://github.com/mushan0x0)** on **2023-11-21**</sup>

You can talk to me about anything. I can give you some thoughts and advice as an old friend. Relax.

`friendship` `humor` `realistic` `simulation`

---

### [Short Video Script Assistant](https://os.sperax.io/crypto/agents/tik-tok-director)

<sup>By **[@aihoom](https://github.com/aihoom)** on **2023-11-17**</sup>

Aimed at helping users craft engaging and trendy short video scripts

`Short Video` `tkitok` `Screenwriter`

---

### [Expert Agent Mentor](https://os.sperax.io/crypto/agents/co-agent)

<sup>By **[@tcmonster](https://github.com/tcmonster)** on **2023-11-16**</sup>

Invoke the most suitable expert agents to support your goals with tasks perfectly aligned to your needs.

`Task Guidance` `Execution Planning` `Communication` `Support`

---

### [Full-stack Developer](https://os.sperax.io/crypto/agents/fs-dev)

<sup>By **[@cloverfield11](https://github.com/cloverfield11)** on **2023-11-15**</sup>

Full-stack web developer with experience in HTML, CSS, JavaScript, Python, Java, Ruby, and frameworks such as React, Angular, Vue.js, Express, Django, Next.js, Flask, or Ruby on Rails. Experienced in databases, application architecture, security, and testing

`web development` `front-end` `back-end` `programming` `databases`

---

### [Tailwind Wizard](https://os.sperax.io/crypto/agents/tailwind-wizard)

<sup>By **[@skyf0cker](https://github.com/skyf0cker)** on **2023-11-15**</sup>

Provides a UI operation to generate HTML

`Development` `Coding` `UI Design`

---

### [Graphic Creativity Master](https://os.sperax.io/crypto/agents/graphic-creativity)

<sup>By **[@yingxirz](https://github.com/yingxirz)** on **2023-11-15**</sup>

Specializes in graphic creative design and visual ideas

`graphics` `creativity` `design` `visual`

---

### [MidJourney Prompt](https://os.sperax.io/crypto/agents/mid-journey-prompt)

<sup>By **[@aihoom](https://github.com/aihoom)** on **2023-11-14**</sup>

Writing awesome MidJourney prompts

`mid-journey` `prompt`

---

### [Dad, what should I do?](https://os.sperax.io/crypto/agents/big-daddy)

<sup>By **[@aihoom](https://github.com/aihoom)** on **2023-11-14**</sup>

A dad who provides comprehensive guidance for children, from daily trivialities to work and marriage.

`Character Simulation`

---

### [Research Article Translation Assistant](https://os.sperax.io/crypto/agents/s-rtranslation)

<sup>By **[@aihoom](https://github.com/aihoom)** on **2023-11-14**</sup>

A translation assistant capable of helping you translate scientific and technological articles

`Research` `Translation`

---

### [Chinese-English Translation Assistant](https://os.sperax.io/crypto/agents/en-cn-translator)

<sup>By **[@tcmonster](https://github.com/tcmonster)** on **2023-11-14**</sup>

Expert in Chinese-English translation, pursuing accuracy, fluency, and elegance

`Translation` `Chinese` `English`

---

### [Academic Writing Enhancement Bot](https://os.sperax.io/crypto/agents/academic-writing-eb)

<sup>By **[@Ruler27](https://github.com/Ruler27)** on **2023-11-11**</sup>

Refinement of academic English spelling and rhetoric.

`proofreading` `rhetoric` `academic` `research` `english` `editing`

---

### [Sketch Feature Summary Expert](https://os.sperax.io/crypto/agents/sketch-changelog-highlighter)

<sup>By **[@Fontas](https://github.com/Fontas)** on **2023-11-02**</sup>

Expert in extracting key change points from Sketch release notes

`UX Design` `sketch` `updates` `features` `text summary`

---

### [Arguing Master](https://os.sperax.io/crypto/agents/tqg-20231026)

<sup>By **[@cake79](https://github.com/cake79)** on **2023-10-26**</sup>

Simulates those who like to argue, a character that can argue against any opinion input by the user

`Writing` `Dialogue`

---

### [Graph Generator](https://os.sperax.io/crypto/agents/graph-generator)

<sup>By **[@choldrim](https://github.com/choldrim)** on **2023-10-23**</sup>

Automatic Graph Generator

`graph`

---

### [Art Naming Master](https://os.sperax.io/crypto/agents/meaningful-name)

<sup>By **[@yingxirz](https://github.com/yingxirz)** on **2023-10-18**</sup>

Provide concise and meaningful names for your artistic creations.

`Naming` `Creativity`

---

### [Little Red Book Style Copywriter](https://os.sperax.io/crypto/agents/xiaohongshu-style-writer)

<sup>By **[@guowc3456](https://github.com/guowc3456)** on **2023-10-11**</sup>

Skilled at mimicking the style of viral Little Red Book articles for writing

`Little Red Book` `Writing` `Copywriting`

---

### [Agent Prompt Optimization Expert](https://os.sperax.io/crypto/agents/gpt-agent-prompt-improver)

<sup>By **[@Fontas](https://github.com/Fontas)** on **2023-10-07**</sup>

GPT Agent Prompt Optimization Expert. Clear, precise, concise.

`prompt`

---

### [English News Translation Expert](https://os.sperax.io/crypto/agents/english-news-translator)

<sup>By **[@宝玉](https://twitter.com/dotey)** on **2023-10-07**</sup>

A simple prompt significantly improves ChatGPT's translation quality, saying goodbye to 'machine translation feel'. refs: <https://twitter.com/dotey/status/1707478347553395105>

`translation` `copywriting`

---

### [C++ Code](https://os.sperax.io/crypto/agents/c-code-development)

<sup>By **[@dcityteg](https://github.com/dcityteg)** on **2023-10-06**</sup>

Complete C++ code

`code`

---

### [TS Type Definition Completion](https://os.sperax.io/crypto/agents/typescript-jsdoc)

<sup>By **[@Fontas](https://github.com/Fontas)** on **2023-10-01**</sup>

Proficient in writing TypeScript JSDoc code

`typescript` `jsdoc`

---

### [LOGO Creative Master](https://os.sperax.io/crypto/agents/logo-creativity)

<sup>By **[@yingxirz](https://github.com/yingxirz)** on **2023-09-29**</sup>

Organizing and generating creative logo ideas for you

`Creativity` `Brainstorming` `Design` `Brand` `Method`

---

### [Interface Type Request Generator](https://os.sperax.io/crypto/agents/swagger-api-to-types)

<sup>By **[@laikedou](https://github.com/laikedou)** on **2023-09-27**</sup>

Quickly export type definitions and request functions from interface descriptions such as Swagger, YAPI, Apifox, etc.

`aigc` `api` `yapi` `swagger` `api-fox`

---

### [Name Master](https://os.sperax.io/crypto/agents/naming-master)

<sup>By **[@Fontas](https://github.com/Fontas)** on **2023-09-11**</sup>

Naming expert to help you create unique and meaningful names.

`Naming` `Copywriting`

---

### [Dva Refactoring to Zustand Expert](https://os.sperax.io/crypto/agents/dva-to-zustand)

<sup>By **[@Fontas](https://github.com/Fontas)** on **2023-09-10**</sup>

One-click transformation of Dva state management code into Zustand code

`typescript` `code` `software development` `state management` `dva` `zustand`

---

### [UX Writer](https://os.sperax.io/crypto/agents/metaphor-ux-writer)

<sup>By **[@Fontas](https://github.com/Fontas)** on **2023-09-10**</sup>

Help you write better UX copy

`user experience` `designer` `documentation` `writing` `metaphor`

---

### [Information Organization Master](https://os.sperax.io/crypto/agents/content-searcher)

<sup>By **[@Fontas](https://github.com/Fontas)** on **2023-09-10**</sup>

An information organization master that helps you gather, summarize, and organize content and assets.

`Search Engine` `Internet Connectivity` `Information Organization`

---

### [Web Content Summarization Expert](https://os.sperax.io/crypto/agents/url-summary)

<sup>By **[@Fontas](https://github.com/Fontas)** on **2023-09-10**</sup>

Simply input a URL, and the assistant will read and summarize the content of that URL for you.

`web` `reading` `summarization` `online`

---

### [Title Expansion Expert](https://os.sperax.io/crypto/agents/title-expansion-writer)

<sup>By **[@Fontas](https://github.com/Fontas)** on **2023-09-10**</sup>

If you need to add a description to a title, let this assistant help you craft the content.

`User Experience` `Designer` `Documentation` `Writing`

---

### [Master of Abstract Concept Embodiment](https://os.sperax.io/crypto/agents/conceptual-abstractor)

<sup>By **[@Fontas](https://github.com/Fontas)** on **2023-09-10**</sup>

Helping you write better UX copy

`User Experience` `Designer` `Documentation` `Writing` `Metaphor` `Concept`

---

### [Frontend Development Architect](https://os.sperax.io/crypto/agents/frontend-architect)

<sup>By **[@Fontas](https://github.com/Fontas)** on **2023-09-10**</sup>

Expert in architecture, proficient in technical details, skilled in searching for solutions via search engines

`typescript` `code` `frontend` `architect` `networking` `search engines` `information organization`

---

### [API Documentation Optimization Expert](https://os.sperax.io/crypto/agents/api-docs-writer)

<sup>By **[@Fontas](https://github.com/Fontas)** on **2023-09-10**</sup>

Accurately describe how to use APIs, provide example code, precautions, and return value type definitions.

`Code` `Software Development` `Programmer` `Documentation` `Writing`

---

### [Zustand reducer Expert](https://os.sperax.io/crypto/agents/zustand-reducer)

<sup>By **[@Fontas](https://github.com/Fontas)** on **2023-09-10**</sup>

Skilled in writing zustand feature code, capable of generating reducer code from requirements with one click, familiar with reducer writing, proficient in using the immer library.

`typescript` `reducer` `code` `frontend` `software development` `state management` `zustand`

---

### [React Class Components to FC Components](https://os.sperax.io/crypto/agents/react-cc-to-fc)

<sup>By **[@Fontas](https://github.com/Fontas)** on **2023-09-10**</sup>

One-click transformation of Class components into FC components

`typescript` `code` `software development` `react` `refactoring`

---

### [UX Writer](https://os.sperax.io/crypto/agents/better-ux-writer)

<sup>By **[@Fontas](https://github.com/Fontas)** on **2023-09-10**</sup>

Helping you craft better UX copy

`User Experience` `Designer` `Documentation` `Writing`

---

### [JS Code to TS Expert](https://os.sperax.io/crypto/agents/js-to-ts)

<sup>By **[@Fontas](https://github.com/Fontas)** on **2023-09-10**</sup>

Input your JS code, and with one click, it will help you complete and improve type definitions

`typescript` `js` `code` `frontend` `software development`

---

### [Frontend TypeScript Unit Test Expert](https://os.sperax.io/crypto/agents/frontend-test-analyzer)

<sup>By **[@Fontas](https://github.com/Fontas)** on **2023-09-10**</sup>

Based on the code you provide, consider scenarios that need coverage testing

`typescript` `unit testing` `code` `software development`

---

### [Deep Think](https://os.sperax.io/crypto/agents/deep-think)

<sup>By **[@Binxeh](https://github.com/Binxeh)** on **2023-09-08**</sup>

Deeper thinking of question

`conversation` `thinking`

---

### [Markdown Product Feature Formatting Expert](https://os.sperax.io/crypto/agents/markdown-feature-polisher)

<sup>By **[@Fontas](https://github.com/Fontas)** on **2023-09-08**</sup>

Helps you quickly generate beautiful and elegant product feature introductions

`product` `markdown` `documentation`

---

### [A More Diligent Assistant](https://os.sperax.io/crypto/agents/web-development)

<sup>By **[@Binxeh](https://github.com/Binxeh)** on **2023-09-07**</sup>

A More Diligent Assistant

`Learning` `software-development` `productivity`

---

### [Resume Editing](https://os.sperax.io/crypto/agents/resume-editing)

<sup>By **[@Binxeh](https://github.com/Binxeh)** on **2023-09-07**</sup>

Get advice on how to edit your resume

`academic` `productivity` `guide`

---

### [Startup Plan](https://os.sperax.io/crypto/agents/startup-plan)

<sup>By **[@Binxeh](https://github.com/Binxeh)** on **2023-09-07**</sup>

Generate a detailed and comprehensive business plan within minutes

`startup` `brainstorming` `plan`

---

### [Character Roleplay](https://os.sperax.io/crypto/agents/character-roleplay)

<sup>By **[@Binxeh](https://github.com/Binxeh)** on **2023-09-07**</sup>

Interact with your favourite characters from movies, TV shows, books, and more!

`conversation` `roleplay` `fun`

---

### [Essay Improver](https://os.sperax.io/crypto/agents/essay-improver)

<sup>By **[@Binxeh](https://github.com/Binxeh)** on **2023-09-07**</sup>

Improve your texts to be more elegant and professional

`academic` `english` `productivity` `essay`

---

### [Grammar Corrector](https://os.sperax.io/crypto/agents/grammar-corrector)

<sup>By **[@Binxeh](https://github.com/Binxeh)** on **2023-09-07**</sup>

Correct grammar error text or paragraph. Great for essay or email

`academic` `productivity` `essay`

---

### [Agent Prompt Improver](https://os.sperax.io/crypto/agents/agent-prompt-improver)

<sup>By **[@Binxeh](https://github.com/Binxeh)** on **2023-09-07**</sup>

GPT Agent Prompt optimization specialist. Clear, precise, and concise

`agent` `prompt`

---

### [Coding Wizard](https://os.sperax.io/crypto/agents/coding-wizard)

<sup>By **[@Binxeh](https://github.com/Binxeh)** on **2023-09-07**</sup>

Can generate the code for anything you specify

`code` `software-development` `productivity`

---

### [Stable Diffusion Prompt Expert](https://os.sperax.io/crypto/agents/stable-diffusion-prompt)

<sup>By **[@Binxeh](https://github.com/Binxeh)** on **2023-09-01**</sup>

Specializes in writing Stable Diffusion prompts

`stable-diffusion` `prompt`


---

## 🌐 Live HTTP Deployment

**AI Agents Library** is deployed and accessible over HTTP via [MCP Streamable HTTP](https://modelcontextprotocol.io/specification/2025-03-26/basic/transports#streamable-http) transport — no local installation required.

**Endpoint:**
```
https://modelcontextprotocol.name/mcp/ai-agents-library
```

### Connect from any MCP Client

Add to your MCP client configuration (Claude Desktop, Cursor, SperaxOS, etc.):

```json
{
  "mcpServers": {
    "ai-agents-library": {
      "type": "http",
      "url": "https://modelcontextprotocol.name/mcp/ai-agents-library"
    }
  }
}
```

### Available Tools (3)

| Tool | Description |
|------|-------------|
| `search_agents` | Search agent templates |
| `list_agent_categories` | List categories |
| `get_agent_template` | Get agent template |

### Example Requests

**Search agent templates:**
```bash
curl -X POST https://modelcontextprotocol.name/mcp/ai-agents-library \
  -H "Content-Type: application/json" \
  -d '{"jsonrpc":"2.0","id":1,"method":"tools/call","params":{"name":"search_agents","arguments":{"query":"trading bot","limit":5}}}'
```

**List categories:**
```bash
curl -X POST https://modelcontextprotocol.name/mcp/ai-agents-library \
  -H "Content-Type: application/json" \
  -d '{"jsonrpc":"2.0","id":1,"method":"tools/call","params":{"name":"list_agent_categories","arguments":{}}}'
```

**Get agent template:**
```bash
curl -X POST https://modelcontextprotocol.name/mcp/ai-agents-library \
  -H "Content-Type: application/json" \
  -d '{"jsonrpc":"2.0","id":1,"method":"tools/call","params":{"name":"get_agent_template","arguments":{"name":"crypto-trader"}}}'
```

### List All Tools

```bash
curl -X POST https://modelcontextprotocol.name/mcp/ai-agents-library \
  -H "Content-Type: application/json" \
  -d '{"jsonrpc":"2.0","id":1,"method":"tools/list"}'
```

### Also Available On

- **[SperaxOS](https://speraxos.vercel.app)** — Browse and install from the [MCP marketplace](https://speraxos.vercel.app/community/mcp)
- **All 27 MCP servers** — See the full catalog at [modelcontextprotocol.name](https://modelcontextprotocol.name)

> Powered by [modelcontextprotocol.name](https://modelcontextprotocol.name) — the open MCP HTTP gateway
