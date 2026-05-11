welcome@jaisairams-Laptop workspace % openclaw skills search "calendar"

🦞 OpenClaw 2026.4.29 (a448042) — I can grep it, git blame it, and gently roast it—pick your coping mechanism.

calendar  Calendar  Calendar management and scheduling. Create events, manage meetings, and sync across calendar providers.
macos-calendar  macOS Calendar  Create, list, and manage macOS Calendar events via AppleScript. Use when the user asks to add a reminder, schedule an event, create a calendar entry, set a d...
lark-calendar  Lark Calendar & Tasks  Create, update, and delete calendar events and tasks in Lark (Feishu). Includes employee directory for automatic name-to-user_id resolution.
dingtalk-calendar  Dingtalk Calendar  钉钉日程管理（创建日程、查询闲忙、会议室预订）。使用 mcporter CLI 连接钉钉 MCP server 执行日程管理、日程查询、会议室预订等操作。使用场景：日程创建管理、会议预订、查询他人闲忙、会议室预约等。
gws-calendar-agenda  Gws Calendar Agenda  Google Calendar: Show upcoming events across all calendars.
afrexai-email-to-calendar  Email to Calendar Extraction Engine  Extract calendar events, deadlines, action items, and follow-ups from emails. Works with any calendar provider (Google, Outlook, Apple, Notion, etc.). No external dependencies — pure agent intelligence. Use when the user forwards an email, asks to check inbox for events, or wants to extract structured scheduling data from any text.
apple-calendar-ops  Apple Calendar Ops  Read, create, update, and delete Apple Calendar events via CalDAV. Use when the user wants to inspect calendars or events, add a calendar event, change an ex...
muguozi1-openclaw-feishu-calendar  Muguozi1 Openclaw Feishu Calendar  Manage Feishu calendars by listing, searching, checking schedules, syncing events, and marking tasks with date/time extraction and attendee assignment.
macos-calendar-assistant  macOS Calendar Assistant  Manage macOS Calendar with OpenClaw in IM-first workflows (Telegram/Discord/Feishu/iMessage/Slack), including screenshot-to-schedule extraction, idempotent c...
tianshu-review-calendar  Tianshu Review Calendar  根据考试日期与科目列表，把复习主题均摊到考前每一天，生成 Markdown 日程表（可打印勾选）。 Use when: 期末周、多门课冲刺；用户说「复习排期」「考前两周计划」。 NOT for: 精确到小时的闹钟；代替个人学习习惯诊断。
welcome@jaisairams-Laptop workspace % openclaw skills list

🦞 OpenClaw 2026.4.29 (a448042) — Greetings, Professor Falken

21:24:33 [skills] root has many entries, truncating discovery.
Skills (207/251 ready)
┌───────────────┬──────────────────────────────────────────────────────────────┬─────────────────────────────────────────────────────────────────┬────────────────────────┐
│ Status        │ Skill                                                        │ Description                                                     │ Source                 │
├───────────────┼──────────────────────────────────────────────────────────────┼─────────────────────────────────────────────────────────────────┼────────────────────────┤
│ △ needs setup │ 🔐 1password                                                 │ Set up and use 1Password CLI for sign-in, desktop integration,  │ openclaw-bundled       │
│               │                                                              │ and reading or injecting secrets.                               │                        │
│ ✓ ready       │ 📦 add-educational-comments                                  │ Add educational comments to the file specified, or prompt       │ agents-skills-personal │
│               │                                                              │ asking for file to comment if one is not provided.              │                        │
│ ✓ ready       │ 📦 add-rest-endpoint                                         │ Scaffold a new REST endpoint with controller, service, DTO,     │ agents-skills-personal │
│               │                                                              │ tests, and error handling following project conventions         │                        │
│ ✓ ready       │ 📦 add-tests                                                 │ Analyze existing code and generate comprehensive tests with     │ agents-skills-personal │
│               │                                                              │ edge cases, using the project's testing framework and           │                        │
│               │                                                              │ conventions                                                     │                        │
│ ✓ ready       │ 📦 add-webhook                                               │ Add new Modal webhooks for event-driven execution. Use when     │ agents-skills-personal │
│               │                                                              │ user asks to create a webhook, add an endpoint, or set up       │                        │
│               │                                                              │ event triggers.                                                 │                        │
│ ✓ ready       │ 📦 adk-cheatsheet                                            │ MUST READ before writing or modifying ADK agent code. ADK API   │ agents-skills-personal │
│               │                                                              │ quick reference for Python — agent types, tool definitions,     │                        │
│               │                                                              │ orchestration patterns, callbacks, and state management.        │                        │
│               │                                                              │ Includes an index of all ADK documentation pages. Do NOT use    │                        │
│               │                                                              │ for creating new projects (use adk-scaffold).                   │                        │
│ ✓ ready       │ 📦 adk-deploy-guide                                          │ MUST READ before deploying any ADK agent. ADK deployment guide  │ agents-skills-personal │
│               │                                                              │ — Agent Engine, Cloud Run, GKE, CI/CD pipelines, secrets,       │                        │
│               │                                                              │ observability, and production workflows. Use when deploying     │                        │
│               │                                                              │ agents to Google Cloud or troubleshooting deployments. Do NOT   │                        │
│               │                                                              │ use for API code patterns (use adk-cheatsheet), evaluation      │                        │
│               │                                                              │ (use adk-eval-guide), or project scaffolding (use adk-          │                        │
│               │                                                              │ scaffold).                                                      │                        │
│ ✓ ready       │ 📦 adk-dev-guide                                             │ ALWAYS ACTIVE — read at the start of any ADK agent development  │ agents-skills-personal │
│               │                                                              │ session. ADK development lifecycle and mandatory coding         │                        │
│               │                                                              │ guidelines — spec-driven workflow, code preservation rules,     │                        │
│               │                                                              │ model selection, and troubleshooting.                           │                        │
│ ✓ ready       │ 📦 adk-eval-guide                                            │ MUST READ before running any ADK evaluation. ADK evaluation     │ agents-skills-personal │
│               │                                                              │ methodology — eval metrics, evalset schema, LLM-as-judge, tool  │                        │
│               │                                                              │ trajectory scoring, and common failure causes. Use when         │                        │
│               │                                                              │ evaluating agent quality, running adk eval, or debugging eval   │                        │
│               │                                                              │ results. Do NOT use for API code patterns (use adk-             │                        │
│               │                                                              │ cheatsheet), deployment (use adk-deploy-guide), or project      │                        │
│               │                                                              │ scaffolding (use adk-scaffold).                                 │                        │
│ ✓ ready       │ 📦 adk-observability-guide                                   │ MUST READ before setting up observability for ADK agents or     │ agents-skills-personal │
│               │                                                              │ when analyzing production traffic, debugging agent behavior,    │                        │
│               │                                                              │ or improving agent performance. ADK observability guide —       │                        │
│               │                                                              │ Cloud Trace, prompt-response logging, BigQuery Agent            │                        │
│               │                                                              │ Analytics, third-party integrations, and troubleshooting. Use   │                        │
│               │                                                              │ when configuring monitoring, tracing, or logging for agents,    │                        │
│               │                                                              │ or when understanding how a deployed agent handles real         │                        │
│               │                                                              │ traffic.                                                        │                        │
│ ✓ ready       │ 📦 adk-scaffold                                              │ MUST READ before creating or enhancing any ADK agent project.   │ agents-skills-personal │
│               │                                                              │ Use when the user wants to build a new agent (e.g. "build me a  │                        │
│               │                                                              │ search agent") or enhance an existing project (e.g. "add CI/CD  │                        │
│               │                                                              │ to my project", "add RAG").                                     │                        │
│ ✓ ready       │ 📦 agent-builder                                             │ Use when building a new agent harness, designing tool systems,  │ agents-skills-personal │
│               │                                                              │ or structuring multi-agent workflows. Provides patterns,        │                        │
│               │                                                              │ templates, and decision trees for harness engineering.          │                        │
│ ✓ ready       │ 📦 agent-governance                                          │ Patterns and techniques for adding governance, safety, and      │ agents-skills-personal │
│               │                                                              │ trust controls to AI agent systems. Use this skill when:        │                        │
│               │                                                              │ - Building AI agents that call external tools (APIs,            │                        │
│               │                                                              │ databases, file systems)                                        │                        │
│               │                                                              │ - Implementing policy-based access controls for agent tool      │                        │
│               │                                                              │ usage                                                           │                        │
│               │                                                              │ - Adding semantic intent classification to detect dangerous     │                        │
│               │                                                              │ prompts                                                         │                        │
│               │                                                              │ - Creating trust scoring systems for multi-agent workflows      │                        │
│               │                                                              │ - Building audit trails for agent actions and decisions         │                        │
│               │                                                              │ - Enforcing rate limits, content filters, or tool restrictions  │                        │
│               │                                                              │ on agents                                                       │                        │
│               │                                                              │ - Working with any agent framework (PydanticAI, CrewAI, OpenAI  │                        │
│               │                                                              │ Agents, LangChain, AutoGen)                                     │                        │
│ ✓ ready       │ 📦 agentic-eval                                              │ Patterns and techniques for evaluating and improving AI agent   │ agents-skills-personal │
│               │                                                              │ outputs. Use this skill when:                                   │                        │
│               │                                                              │ - Implementing self-critique and reflection loops               │                        │
│               │                                                              │ - Building evaluator-optimizer pipelines for quality-critical   │                        │
│               │                                                              │ generation                                                      │                        │
│               │                                                              │ - Creating test-driven code refinement workflows                │                        │
│               │                                                              │ - Designing rubric-based or LLM-as-judge evaluation systems     │                        │
│               │                                                              │ - Adding iterative improvement to agent outputs (code,          │                        │
│               │                                                              │ reports, analysis)                                              │                        │
│               │                                                              │ - Measuring and improving agent response quality                │                        │
│ ✓ ready       │ 📦 ai-prompt-engineering-safety-review                       │ Comprehensive AI prompt engineering safety review and           │ agents-skills-personal │
│               │                                                              │ improvement prompt. Analyzes prompts for safety, bias,          │                        │
│               │                                                              │ security vulnerabilities, and effectiveness while providing     │                        │
│               │                                                              │ detailed improvement recommendations with extensive             │                        │
│               │                                                              │ frameworks, testing methodologies, and educational content.     │                        │
│ ✓ ready       │ 📦 analyze-csv-files                                         │ Analyze CSV files — load, inspect, clean, filter, aggregate,    │ agents-skills-personal │
│               │                                                              │ and summarize tabular data from CSV and TSV files. Use when     │                        │
│               │                                                              │ the user has a CSV file and wants to understand its contents,   │                        │
│               │                                                              │ find patterns, compute statistics, filter rows, or answer       │                        │
│               │                                                              │ questions about the data, even if they just say "look at this   │                        │
│               │                                                              │ spreadsheet" or "what's in this file."                          │                        │
│ ✓ ready       │ 📦 appinsights-instrumentation                               │ Instrument a webapp to send useful telemetry data to Azure App  │ agents-skills-personal │
│               │                                                              │ Insights                                                        │                        │
│ ✓ ready       │ 📦 apple-appstore-reviewer                                   │ Serves as a reviewer of the codebase with instructions on       │ agents-skills-personal │
│               │                                                              │ looking for Apple App Store optimizations or rejection reasons. │                        │
│ △ needs setup │ 📝 apple-notes                                               │ Create, view, edit, delete, search, move, or export Apple       │ openclaw-bundled       │
│               │                                                              │ Notes via the memo CLI on macOS.                                │                        │
│ △ needs setup │ ⏰ apple-reminders                                           │ List, add, edit, complete, or delete Apple Reminders and        │ openclaw-bundled       │
│               │                                                              │ reminder lists via remindctl.                                   │                        │
│ ✓ ready       │ 📦 arch-linux-triage                                         │ Triage and resolve Arch Linux issues with pacman, systemd, and  │ agents-skills-personal │
│               │                                                              │ rolling-release best practices.                                 │                        │
│ ✓ ready       │ 📦 architecture-blueprint-generator                          │ Comprehensive project architecture blueprint generator that     │ agents-skills-personal │
│               │                                                              │ analyzes codebases to create detailed architectural             │                        │
│               │                                                              │ documentation. Automatically detects technology stacks and      │                        │
│               │                                                              │ architectural patterns, generates visual diagrams, documents    │                        │
│               │                                                              │ implementation patterns, and provides extensible blueprints     │                        │
│               │                                                              │ for maintaining architectural consistency and guiding new       │                        │
│               │                                                              │ development.                                                    │                        │
│ ✓ ready       │ 📦 aspire                                                    │ Aspire skill covering the Aspire CLI, AppHost orchestration,    │ agents-skills-personal │
│               │                                                              │ service discovery, integrations, MCP server, VS Code            │                        │
│               │                                                              │ extension, Dev Containers, GitHub Codespaces, templates,        │                        │
│               │                                                              │ dashboard, and deployment. Use when the user asks to create,    │                        │
│               │                                                              │ run, debug, configure, deploy, or troubleshoot an Aspire        │                        │
│               │                                                              │ distributed application.                                        │                        │
│ ✓ ready       │ 📦 aspnet-minimal-api-openapi                                │ Create ASP.NET Minimal API endpoints with proper OpenAPI        │ agents-skills-personal │
│               │                                                              │ documentation                                                   │                        │
│ ✓ ready       │ 📦 automate-this                                             │ Analyze a screen recording of a manual process and produce      │ agents-skills-personal │
│               │                                                              │ targeted, working automation scripts. Extracts frames and       │                        │
│               │                                                              │ audio narration from video files, reconstructs the step-by-     │                        │
│               │                                                              │ step workflow, and proposes automation at multiple complexity   │                        │
│               │                                                              │ levels using tools already installed on the user machine.       │                        │
│ ✓ ready       │ 📦 autoresearch                                              │ Autonomous iterative experimentation loop for any programming   │ agents-skills-personal │
│               │                                                              │ task. Guides the user through defining goals, measurable        │                        │
│               │                                                              │ metrics, and scope constraints, then runs an autonomous loop    │                        │
│               │                                                              │ of code changes, testing, measuring, and keeping/discarding     │                        │
│               │                                                              │ results. Inspired by Karpathy's autoresearch. USE FOR:          │                        │
│               │                                                              │ autonomous improvement, iterative optimization, experiment      │                        │
│               │                                                              │ loop, auto research, performance tuning, automated              │                        │
│               │                                                              │ experimentation, hill climbing, try things automatically,       │                        │
│               │                                                              │ optimize code, run experiments, autonomous coding loop. DO NOT  │                        │
│               │                                                              │ USE FOR: one-shot tasks, simple bug fixes, code review, or      │                        │
│               │                                                              │ tasks without a measurable metric.                              │                        │
│ ✓ ready       │ 📦 aws-cdk-python-setup                                      │ Setup and initialization guide for developing AWS CDK (Cloud    │ agents-skills-personal │
│               │                                                              │ Development Kit) applications in Python. This skill enables     │                        │
│               │                                                              │ users to configure environment prerequisites, create new CDK    │                        │
│               │                                                              │ projects, manage dependencies, and deploy to AWS.               │                        │
│ ✓ ready       │ 📦 az-cost-optimize                                          │ Analyze Azure resources used in the app (IaC files and/or       │ agents-skills-personal │
│               │                                                              │ resources in a target rg) and optimize costs - creating GitHub  │                        │
│               │                                                              │ issues for identified optimizations.                            │                        │
│ ✓ ready       │ 📦 azure-architecture-autopilot                              │ Design Azure infrastructure using natural language, or analyze  │ agents-skills-personal │
│               │                                                              │ existing Azure resources to auto-generate architecture          │                        │
│               │                                                              │ diagrams, refine them through conversation, and deploy with     │                        │
│               │                                                              │ Bicep.                                                          │                        │
│               │                                                              │ When to use this skill: - "Create X on Azure", "Set up a RAG    │                        │
│               │                                                              │ architecture" (new design) - "Analyze my current Azure          │                        │
│               │                                                              │ infrastructure", "Draw a diagram for rg-xxx" (existing          │                        │
│               │                                                              │ analysis) - "Foundry is slow", "I want to reduce costs",        │                        │
│               │                                                              │ "Strengthen security" (natural language modification) - Azure   │                        │
│               │                                                              │ resource deployment, Bicep template generation, IaC code        │                        │
│               │                                                              │ generation - Microsoft Foundry, AI Search, OpenAI, Fabric,      │                        │
│               │                                                              │ ADLS Gen2, Databricks, and all Azure services                   │                        │
│ ✓ ready       │ 📦 azure-deployment-preflight                                │ Performs comprehensive preflight validation of Bicep            │ agents-skills-personal │
│               │                                                              │ deployments to Azure, including template syntax validation,     │                        │
│               │                                                              │ what-if analysis, and permission checks. Use this skill before  │                        │
│               │                                                              │ any deployment to Azure to preview changes, identify potential  │                        │
│               │                                                              │ issues, and ensure the deployment will succeed. Activate when   │                        │
│               │                                                              │ users mention deploying to Azure, validating Bicep files,       │                        │
│               │                                                              │ checking deployment permissions, previewing infrastructure      │                        │
│               │                                                              │ changes, running what-if, or preparing for azd provision.       │                        │
│ ✓ ready       │ 📦 azure-devops-cli                                          │ Manage Azure DevOps resources via CLI including projects,       │ agents-skills-personal │
│               │                                                              │ repos, pipelines, builds, pull requests, work items,            │                        │
│               │                                                              │ artifacts, and service endpoints. Use when working with Azure   │                        │
│               │                                                              │ DevOps, az commands, devops automation, CI/CD, or when user     │                        │
│               │                                                              │ mentions Azure DevOps CLI.                                      │                        │
│ ✓ ready       │ 📦 azure-pricing                                             │ Fetches real-time Azure retail pricing using the Azure Retail   │ agents-skills-personal │
│               │                                                              │ Prices API (prices.azure.com) and estimates Copilot Studio      │                        │
│               │                                                              │ agent credit consumption. Use when the user asks about the      │                        │
│               │                                                              │ cost of any Azure service, wants to compare SKU prices, needs   │                        │
│               │                                                              │ pricing data for a cost estimate, mentions Azure pricing,       │                        │
│               │                                                              │ Azure costs, Azure billing, or asks about Copilot Studio        │                        │
│               │                                                              │ pricing, Copilot Credits, or agent usage estimation. Covers     │                        │
│               │                                                              │ compute, storage, networking, databases, AI, Copilot Studio,    │                        │
│               │                                                              │ and all other Azure service families.                           │                        │
│ ✓ ready       │ 📦 azure-resource-health-diagnose                            │ Analyze Azure resource health, diagnose issues from logs and    │ agents-skills-personal │
│               │                                                              │ telemetry, and create a remediation plan for identified         │                        │
│               │                                                              │ problems.                                                       │                        │
│ ✓ ready       │ 📦 azure-resource-visualizer                                 │ Analyze Azure resource groups and generate detailed Mermaid     │ agents-skills-personal │
│               │                                                              │ architecture diagrams showing the relationships between         │                        │
│               │                                                              │ individual resources. Use this skill when the user asks for a   │                        │
│               │                                                              │ diagram of their Azure resources or help in understanding how   │                        │
│               │                                                              │ the resources relate to each other.                             │                        │
│ ✓ ready       │ 📦 azure-role-selector                                       │ When user is asking for guidance for which role to assign to    │ agents-skills-personal │
│               │                                                              │ an identity given desired permissions, this agent helps them    │                        │
│               │                                                              │ understand the role that will meet the requirements with least  │                        │
│               │                                                              │ privilege access and how to apply that role.                    │                        │
│ ✓ ready       │ 📦 azure-static-web-apps                                     │ Helps create, configure, and deploy Azure Static Web Apps       │ agents-skills-personal │
│               │                                                              │ using the SWA CLI. Use when deploying static sites to Azure,    │                        │
│               │                                                              │ setting up SWA local development, configuring staticwebapp.     │                        │
│               │                                                              │ config.json, adding Azure Functions APIs to SWA, or setting up  │                        │
│               │                                                              │ GitHub Actions CI/CD for Static Web Apps.                       │                        │
│ △ needs setup │ 🐻 bear-notes                                                │ Create, search, and manage Bear notes via grizzly CLI.          │ openclaw-bundled       │
│ ✓ ready       │ 📦 bigquery-pipeline-audit                                   │ Audits Python + BigQuery pipelines for cost safety,             │ agents-skills-personal │
│               │                                                              │ idempotency, and production readiness. Returns a structured     │                        │
│               │                                                              │ report with exact patch locations.                              │                        │
│ △ needs setup │ 📰 blogwatcher                                               │ Monitor blogs and RSS/Atom feeds for updates using the          │ openclaw-bundled       │
│               │                                                              │ blogwatcher CLI.                                                │                        │
│ △ needs setup │ 🫐 blucli                                                    │ BluOS CLI (blu) for discovery, playback, grouping, and volume.  │ openclaw-bundled       │
│ △ needs setup │ 🫧 bluebubbles                                               │ Send and manage iMessages via BlueBubbles, including            │ openclaw-bundled       │
│               │                                                              │ attachments, tapbacks, edits, replies, and groups.              │                        │
│ ✓ ready       │ 📦 boost-prompt                                              │ Interactive prompt refinement workflow: interrogates scope,     │ agents-skills-personal │
│               │                                                              │ deliverables, constraints; copies final markdown to clipboard;  │                        │
│               │                                                              │ never writes code. Requires the Joyride extension.              │                        │
│ ✓ ready       │ 📦 breakdown-epic-arch                                       │ Prompt for creating the high-level technical architecture for   │ agents-skills-personal │
│               │                                                              │ an Epic, based on a Product Requirements Document.              │                        │
│ ✓ ready       │ 📦 breakdown-epic-pm                                         │ Prompt for creating an Epic Product Requirements Document       │ agents-skills-personal │
│               │                                                              │ (PRD) for a new epic. This PRD will be used as input for        │                        │
│               │                                                              │ generating a technical architecture specification.              │                        │
│ ✓ ready       │ 📦 breakdown-feature-implementation                          │ Prompt for creating detailed feature implementation plans,      │ agents-skills-personal │
│               │                                                              │ following Epoch monorepo structure.                             │                        │
│ ✓ ready       │ 📦 breakdown-feature-prd                                     │ Prompt for creating Product Requirements Documents (PRDs) for   │ agents-skills-personal │
│               │                                                              │ new features, based on an Epic.                                 │                        │
│ ✓ ready       │ 📦 breakdown-plan                                            │ Issue Planning and Automation prompt that generates             │ agents-skills-personal │
│               │                                                              │ comprehensive project plans with Epic > Feature > Story/        │                        │
│               │                                                              │ Enabler > Test hierarchy, dependencies, priorities, and         │                        │
│               │                                                              │ automated tracking.                                             │                        │
│ ✓ ready       │ 📦 breakdown-test                                            │ Test Planning and Quality Assurance prompt that generates       │ agents-skills-personal │
│               │                                                              │ comprehensive test strategies, task breakdowns, and quality     │                        │
│               │                                                              │ validation plans for GitHub projects.                           │                        │
│ △ needs setup │ 📸 camsnap                                                   │ Capture frames or clips from RTSP/ONVIF cameras.                │ openclaw-bundled       │
│ ✓ ready       │ 📦 casualize-names                                           │ Convert formal names to casual versions for cold email          │ agents-skills-personal │
│               │                                                              │ personalization - first names, company names, and city names.   │                        │
│               │                                                              │ Use when user asks to casualize names, make names friendly, or  │                        │
│               │                                                              │ prepare lead data for emails.                                   │                        │
│ ✓ ready       │ 📦 centos-linux-triage                                       │ Triage and resolve CentOS issues using RHEL-compatible          │ agents-skills-personal │
│               │                                                              │ tooling, SELinux-aware practices, and firewalld.                │                        │
│ ✓ ready       │ 📦 chrome-devtools                                           │ Expert-level browser automation, debugging, and performance     │ agents-skills-personal │
│               │                                                              │ analysis using Chrome DevTools MCP. Use for interacting with    │                        │
│               │                                                              │ web pages, capturing screenshots, analyzing network traffic,    │                        │
│               │                                                              │ and profiling performance.                                      │                        │
│ ✓ ready       │ 📦 classify-leads                                            │ Classify leads using LLM for complex distinctions like product  │ agents-skills-personal │
│               │                                                              │ SaaS vs agencies. Use when user asks to classify leads, filter  │                        │
│               │                                                              │ leads by type, or categorize businesses.                        │                        │
│ △ needs setup │ 📦 clawhub                                                   │ Search, install, update, sync, or publish agent skills with     │ openclaw-bundled       │
│               │                                                              │ the ClawHub CLI and registry.                                   │                        │
│ ✓ ready       │ 📦 cli-mastery                                               │ Interactive training for the GitHub Copilot CLI. Guided         │ agents-skills-personal │
│               │                                                              │ lessons, quizzes, scenario challenges, and a full reference     │                        │
│               │                                                              │ covering slash commands, shortcuts, modes, agents, skills,      │                        │
│               │                                                              │ MCP, and configuration. Say "cliexpert" to start.               │                        │
│ ✓ ready       │ 📦 cloud-design-patterns                                     │ Cloud design patterns for distributed systems architecture      │ agents-skills-personal │
│               │                                                              │ covering 42 industry-standard patterns across reliability,      │                        │
│               │                                                              │ performance, messaging, security, and deployment categories.    │                        │
│               │                                                              │ Use when designing, reviewing, or implementing distributed      │                        │
│               │                                                              │ system architectures.                                           │                        │
│ ✓ ready       │ 📦 code-exemplars-blueprint-generator                        │ Technology-agnostic prompt generator that creates customizable  │ agents-skills-personal │
│               │                                                              │ AI prompts for scanning codebases and identifying high-quality  │                        │
│               │                                                              │ code exemplars. Supports multiple programming languages (.NET,  │                        │
│               │                                                              │ Java, JavaScript, TypeScript, React, Angular, Python) with      │                        │
│               │                                                              │ configurable analysis depth, categorization methods, and        │                        │
│               │                                                              │ documentation formats to establish coding standards and         │                        │
│               │                                                              │ maintain consistency across development teams.                  │                        │
│ ✓ ready       │ 📦 code-review                                               │ Use when asked to review code, audit a file for bugs, check     │ agents-skills-personal │
│               │                                                              │ code quality, or suggest improvements. Provides a structured    │                        │
│               │                                                              │ review process and issue categorisation.                        │                        │
│ ✓ ready       │ 📦 codeql                                                    │ Comprehensive guide for setting up and configuring CodeQL code  │ agents-skills-personal │
│               │                                                              │ scanning via GitHub Actions workflows and the CodeQL CLI. This  │                        │
│               │                                                              │ skill should be used when users need help with code scanning    │                        │
│               │                                                              │ configuration, CodeQL workflow files, CodeQL CLI commands,      │                        │
│               │                                                              │ SARIF output, security analysis setup, or troubleshooting       │                        │
│               │                                                              │ CodeQL analysis.                                                │                        │
│ △ needs setup │ 🧩 coding-agent                                              │ Delegate coding tasks to Codex, Claude Code, OpenCode, or Pi    │ openclaw-bundled       │
│               │                                                              │ agents via immediate background processes. Use when: (1)        │                        │
│               │                                                              │ building or creating features/apps, (2) reviewing PRs in a      │                        │
│               │                                                              │ temp clone/worktree, (3) refactoring large codebases, (4)       │                        │
│               │                                                              │ iterative coding that needs file exploration. NOT for: simple   │                        │
│               │                                                              │ one-line fixes (just edit), reading code (use read tool),       │                        │
│               │                                                              │ thread-bound ACP harness requests in chat (use sessions_spawn   │                        │
│               │                                                              │ with runtime:"acp"), or any work in ~/clawd workspace (never    │                        │
│               │                                                              │ spawn agents here). All coding-agent runs start with            │                        │
│               │                                                              │ background:true immediately. Claude Code: use --print --        │                        │
│               │                                                              │ permission-mode bypassPermissions (no PTY). Codex/Pi/OpenCode:  │                        │
│               │                                                              │ pty:true required. Completion notification must use openclaw    │                        │
│               │                                                              │ message send, not system event/heartbeat.                       │                        │
│ ✓ ready       │ 📦 comment-code-generate-a-tutorial                          │ Transform this Python script into a polished, beginner-         │ agents-skills-personal │
│               │                                                              │ friendly project by refactoring the code, adding clear          │                        │
│               │                                                              │ instructional comments, and generating a complete markdown      │                        │
│               │                                                              │ tutorial.                                                       │                        │
│ ✓ ready       │ 📦 containerize-aspnet-framework                             │ Containerize an ASP.NET .NET Framework project by creating      │ agents-skills-personal │
│               │                                                              │ Dockerfile and .dockerfile files customized for the project.    │                        │
│ ✓ ready       │ 📦 containerize-aspnetcore                                   │ Containerize an ASP.NET Core project by creating Dockerfile     │ agents-skills-personal │
│               │                                                              │ and .dockerfile files customized for the project.               │                        │
│ ✓ ready       │ 📦 context-map                                               │ Generate a map of all files relevant to a task before making    │ agents-skills-personal │
│               │                                                              │ changes                                                         │                        │
│ ✓ ready       │ 📦 conventional-commit                                       │ Prompt and workflow for generating conventional commit          │ agents-skills-personal │
│               │                                                              │ messages using a structured XML format. Guides users to create  │                        │
│               │                                                              │ standardized, descriptive commit messages in line with the      │                        │
│               │                                                              │ Conventional Commits specification, including instructions,     │                        │
│               │                                                              │ examples, and validation.                                       │                        │
│ ✓ ready       │ 📦 convert-plaintext-to-md                                   │ Convert a text-based document to markdown following             │ agents-skills-personal │
│               │                                                              │ instructions from prompt, or if a documented option is passed,  │                        │
│               │                                                              │ follow the instructions for that option.                        │                        │
│ ✓ ready       │ 📦 copilot-cli-quickstart                                    │ Use this skill when someone wants to learn GitHub Copilot CLI   │ agents-skills-personal │
│               │                                                              │ from scratch. Offers interactive step-by-step tutorials with    │                        │
│               │                                                              │ separate Developer and Non-Developer tracks, plus on-demand     │                        │
│               │                                                              │ Q&A. Just say "start tutorial" or ask a question! Note: This    │                        │
│               │                                                              │ skill targets GitHub Copilot CLI specifically and uses CLI-     │                        │
│               │                                                              │ specific tools (ask_user, sql, fetch_copilot_cli_               │                        │
│               │                                                              │ documentation).                                                 │                        │
│ ✓ ready       │ 📦 copilot-instructions-blueprint-generator                  │ Technology-agnostic blueprint generator for creating            │ agents-skills-personal │
│               │                                                              │ comprehensive copilot-instructions.md files that guide GitHub   │                        │
│               │                                                              │ Copilot to produce code consistent with project standards,      │                        │
│               │                                                              │ architecture patterns, and exact technology versions by         │                        │
│               │                                                              │ analyzing existing codebase patterns and avoiding assumptions.  │                        │
│ ✓ ready       │ 📦 copilot-sdk                                               │ Build agentic applications with GitHub Copilot SDK. Use when    │ agents-skills-personal │
│               │                                                              │ embedding AI agents in apps, creating custom tools,             │                        │
│               │                                                              │ implementing streaming responses, managing sessions,            │                        │
│               │                                                              │ connecting to MCP servers, or creating custom agents. Triggers  │                        │
│               │                                                              │ on Copilot SDK, GitHub SDK, agentic app, embed Copilot,         │                        │
│               │                                                              │ programmable agent, MCP server, custom agent.                   │                        │
│ ✓ ready       │ 📦 copilot-spaces                                            │ Use Copilot Spaces to provide project-specific context to       │ agents-skills-personal │
│               │                                                              │ conversations. Use this skill when users mention a "Copilot     │                        │
│               │                                                              │ space", want to load context from a shared knowledge base,      │                        │
│               │                                                              │ discover available spaces, or ask questions grounded in         │                        │
│               │                                                              │ curated project documentation, code, and instructions.          │                        │
│ ✓ ready       │ 📦 copilot-usage-metrics                                     │ Retrieve and display GitHub Copilot usage metrics for           │ agents-skills-personal │
│               │                                                              │ organizations and enterprises using the GitHub CLI and REST     │                        │
│               │                                                              │ API.                                                            │                        │
│ ✓ ready       │ 📦 cosmosdb-datamodeling                                     │ Step-by-step guide for capturing key application requirements   │ agents-skills-personal │
│               │                                                              │ for NoSQL use-case and produce Azure Cosmos DB Data NoSQL       │                        │
│               │                                                              │ Model design using best practices and common patterns,          │                        │
│               │                                                              │ artifacts_produced: "cosmosdb_requirements.md" file and         │                        │
│               │                                                              │ "cosmosdb_data_model.md" file                                   │                        │
│ ✓ ready       │ 📦 create-agentsmd                                           │ Prompt for generating an AGENTS.md file for a repository        │ agents-skills-personal │
│ ✓ ready       │ 📦 create-architectural-decision-record                      │ Create an Architectural Decision Record (ADR) document for AI-  │ agents-skills-personal │
│               │                                                              │ optimized decision documentation.                               │                        │
│ ✓ ready       │ 📦 create-github-action-workflow-specification               │ Create a formal specification for an existing GitHub Actions    │ agents-skills-personal │
│               │                                                              │ CI/CD workflow, optimized for AI consumption and workflow       │                        │
│               │                                                              │ maintenance.                                                    │                        │
│ ✓ ready       │ 📦 create-github-issue-feature-from-specification            │ Create GitHub Issue for feature request from specification      │ agents-skills-personal │
│               │                                                              │ file using feature_request.yml template.                        │                        │
│ ✓ ready       │ 📦 create-github-issues-feature-from-implementation-plan     │ Create GitHub Issues from implementation plan phases using      │ agents-skills-personal │
│               │                                                              │ feature_request.yml or chore_request.yml templates.             │                        │
│ ✓ ready       │ 📦 create-github-issues-for-unmet-specification-requirements │ Create GitHub Issues for unimplemented requirements from        │ agents-skills-personal │
│               │                                                              │ specification files using feature_request.yml template.         │                        │
│ ✓ ready       │ 📦 create-github-pull-request-from-specification             │ Create GitHub Pull Request for feature request from             │ agents-skills-personal │
│               │                                                              │ specification file using pull_request_template.md template.     │                        │
│ ✓ ready       │ 📦 create-implementation-plan                                │ Create a new implementation plan file for new features,         │ agents-skills-personal │
│               │                                                              │ refactoring existing code or upgrading packages, design,        │                        │
│               │                                                              │ architecture or infrastructure.                                 │                        │
│ ✓ ready       │ 📦 create-llms                                               │ Create an llms.txt file from scratch based on repository        │ agents-skills-personal │
│               │                                                              │ structure following the llms.txt specification at https://      │                        │
│               │                                                              │ llmstxt.org/                                                    │                        │
│ ✓ ready       │ 📦 create-proposal                                           │ Generate PandaDoc proposals from client information or sales    │ agents-skills-personal │
│               │                                                              │ call transcripts. Use when user asks to create a proposal,      │                        │
│               │                                                              │ generate a quote, draft a contract, or prepare a client         │                        │
│               │                                                              │ document.                                                       │                        │
│ ✓ ready       │ 📦 create-readme                                             │ Create a README.md file for the project                         │ agents-skills-personal │
│ ✓ ready       │ 📦 create-specification                                      │ Create a new specification file for the solution, optimized     │ agents-skills-personal │
│               │                                                              │ for Generative AI consumption.                                  │                        │
│ ✓ ready       │ 📦 create-spring-boot-java-project                           │ Create Spring Boot Java Project Skeleton                        │ agents-skills-personal │
│ ✓ ready       │ 📦 create-spring-boot-kotlin-project                         │ Create Spring Boot Kotlin Project Skeleton                      │ agents-skills-personal │
│ ✓ ready       │ 📦 create-technical-spike                                    │ Create time-boxed technical spike documents for researching     │ agents-skills-personal │
│               │                                                              │ and resolving critical development decisions before             │                        │
│               │                                                              │ implementation.                                                 │                        │
│ ✓ ready       │ 📦 create-tldr-page                                          │ Create a tldr page from documentation URLs and command          │ agents-skills-personal │
│               │                                                              │ examples, requiring both URL and command name.                  │                        │
│ ✓ ready       │ 📦 creating-oracle-to-postgres-master-migration-plan         │ Discovers all projects in a .NET solution, classifies each for  │ agents-skills-personal │
│               │                                                              │ Oracle-to-PostgreSQL migration eligibility, and produces a      │                        │
│               │                                                              │ persistent master migration plan. Use when starting a multi-    │                        │
│               │                                                              │ project Oracle-to-PostgreSQL migration, creating a migration    │                        │
│               │                                                              │ inventory, or assessing which .NET projects contain Oracle      │                        │
│               │                                                              │ dependencies.                                                   │                        │
│ ✓ ready       │ 📦 creating-oracle-to-postgres-migration-bug-report          │ Creates structured bug reports for defects found during Oracle- │ agents-skills-personal │
│               │                                                              │ to-PostgreSQL migration. Use when documenting behavioral        │                        │
│               │                                                              │ differences between Oracle and PostgreSQL as actionable bug     │                        │
│               │                                                              │ reports with severity, root cause, and remediation steps.       │                        │
│ ✓ ready       │ 📦 creating-oracle-to-postgres-migration-integration-tests   │ Creates integration test cases for .NET data access artifacts   │ agents-skills-personal │
│               │                                                              │ during Oracle-to-PostgreSQL database migrations. Generates DB-  │                        │
│               │                                                              │ agnostic xUnit tests with deterministic seed data that          │                        │
│               │                                                              │ validate behavior consistency across both database systems.     │                        │
│               │                                                              │ Use when creating integration tests for a migrated project,     │                        │
│               │                                                              │ generating test coverage for data access layers, or writing     │                        │
│               │                                                              │ Oracle-to-PostgreSQL migration validation tests.                │                        │
│ ✓ ready       │ 📦 cross-niche-outliers                                      │ Find viral YouTube videos from adjacent business niches to      │ agents-skills-personal │
│               │                                                              │ extract content patterns and hooks. Use when user asks to find  │                        │
│               │                                                              │ content inspiration, YouTube outliers, viral video patterns,    │                        │
│               │                                                              │ or cross-niche content ideas.                                   │                        │
│ ✓ ready       │ 📦 csharp-async                                              │ Get best practices for C# async programming                     │ agents-skills-personal │
│ ✓ ready       │ 📦 csharp-docs                                               │ Ensure that C# types are documented with XML comments and       │ agents-skills-personal │
│               │                                                              │ follow best practices for documentation.                        │                        │
│ ✓ ready       │ 📦 csharp-mcp-server-generator                               │ Generate a complete MCP server project in C# with tools,        │ agents-skills-personal │
│               │                                                              │ prompts, and proper configuration                               │                        │
│ ✓ ready       │ 📦 csharp-mstest                                             │ Get best practices for MSTest 3.x/4.x unit testing, including   │ agents-skills-personal │
│               │                                                              │ modern assertion APIs and data-driven tests                     │                        │
│ ✓ ready       │ 📦 csharp-nunit                                              │ Get best practices for NUnit unit testing, including data-      │ agents-skills-personal │
│               │                                                              │ driven tests                                                    │                        │
│ ✓ ready       │ 📦 csharp-tunit                                              │ Get best practices for TUnit unit testing, including data-      │ agents-skills-personal │
│               │                                                              │ driven tests                                                    │                        │
│ ✓ ready       │ 📦 csharp-xunit                                              │ Get best practices for XUnit unit testing, including data-      │ agents-skills-personal │
│               │                                                              │ driven tests                                                    │                        │
│ ✓ ready       │ 📦 csv-analyzer-workspace                                    │ Manage a workspace for evaluating and benchmarking CSV          │ agents-skills-personal │
│               │                                                              │ analysis quality. Use when the user wants to set up eval        │                        │
│               │                                                              │ harnesses, compare analysis outputs with and without skills,    │                        │
│               │                                                              │ grade CSV analysis results, or track analysis accuracy over     │                        │
│               │                                                              │ time.                                                           │                        │
│ ✓ ready       │ 📦 daily-prep                                                │ Prepare for tomorrow's meetings and tasks. Pulls calendar from  │ agents-skills-personal │
│               │                                                              │ Outlook via WorkIQ, cross-references open tasks and workspace   │                        │
│               │                                                              │ context, classifies meetings, detects conflicts and day-fit     │                        │
│               │                                                              │ issues, finds learning and deep-work slots, and generates a     │                        │
│               │                                                              │ structured HTML prep file with productivity recommendations.    │                        │
│ ✓ ready       │ 📦 data-analysis                                             │ Analyze datasets — compute summary statistics, clean messy      │ agents-skills-personal │
│               │                                                              │ data, add derived columns, detect outliers, and generate        │                        │
│               │                                                              │ charts. Use when the user has a CSV, TSV, Excel, or JSON data   │                        │
│               │                                                              │ file and wants to explore, transform, visualize, or understand  │                        │
│               │                                                              │ the data, even if they don't explicitly mention "analysis."     │                        │
│ ✓ ready       │ 📦 datanalysis-credit-risk                                   │ Credit risk data cleaning and variable screening pipeline for   │ agents-skills-personal │
│               │                                                              │ pre-loan modeling. Use when working with raw credit data that   │                        │
│               │                                                              │ needs quality assessment,  missing value analysis, or variable  │                        │
│               │                                                              │ selection before modeling. it covers data loading and           │                        │
│               │                                                              │ formatting, abnormal period filtering, missing rate             │                        │
│               │                                                              │ calculation, high-missing variable removal,low-IV variable      │                        │
│               │                                                              │ filtering, high-PSI variable removal, Null Importance           │                        │
│               │                                                              │ denoising, high-correlation variable removal, and cleaning      │                        │
│               │                                                              │ report generation. Applicable scenarios arecredit risk data     │                        │
│               │                                                              │ cleaning, variable screening, pre-loan modeling preprocessing.  │                        │
│ ✓ ready       │ 📦 dataverse-python-advanced-patterns                        │ Generate production code for Dataverse SDK using advanced       │ agents-skills-personal │
│               │                                                              │ patterns, error handling, and optimization techniques.          │                        │
│ ✓ ready       │ 📦 dataverse-python-production-code                          │ Generate production-ready Python code using Dataverse SDK with  │ agents-skills-personal │
│               │                                                              │ error handling, optimization, and best practices                │                        │
│ ✓ ready       │ 📦 dataverse-python-quickstart                               │ Generate Python SDK setup + CRUD + bulk + paging snippets       │ agents-skills-personal │
│               │                                                              │ using official patterns.                                        │                        │
│ ✓ ready       │ 📦 dataverse-python-usecase-builder                          │ Generate complete solutions for specific Dataverse SDK use      │ agents-skills-personal │
│               │                                                              │ cases with architecture recommendations                         │                        │
│ ✓ ready       │ 📦 debian-linux-triage                                       │ Triage and resolve Debian Linux issues with apt, systemd, and   │ agents-skills-personal │
│               │                                                              │ AppArmor-aware guidance.                                        │                        │
│ ✓ ready       │ 📦 declarative-agents                                        │ Complete development kit for Microsoft 365 Copilot declarative  │ agents-skills-personal │
│               │                                                              │ agents with three comprehensive workflows (basic, advanced,     │                        │
│               │                                                              │ validation), TypeSpec support, and Microsoft 365 Agents         │                        │
│               │                                                              │ Toolkit integration                                             │                        │
│ ✓ ready       │ 📦 dependabot                                                │ Comprehensive guide for configuring and managing GitHub         │ agents-skills-personal │
│               │                                                              │ Dependabot. Use this skill when users ask about creating or     │                        │
│               │                                                              │ optimizing dependabot.yml files, managing Dependabot pull       │                        │
│               │                                                              │ requests, configuring dependency update strategies, setting up  │                        │
│               │                                                              │ grouped updates, monorepo patterns, multi-ecosystem groups,     │                        │
│               │                                                              │ security update configuration, auto-triage rules, or any        │                        │
│               │                                                              │ GitHub Advanced Security (GHAS) supply chain security topic     │                        │
│               │                                                              │ related to Dependabot.                                          │                        │
│ ✓ ready       │ 📦 design-website                                            │ Generate a premium mockup website for a prospect using the      │ agents-skills-personal │
│               │                                                              │ buildinamsterdam.com template style. Use when user asks to      │                        │
│               │                                                              │ design a website, create a mockup, or build a prospect website. │                        │
│ ✓ ready       │ 📦 devops-rollout-plan                                       │ Generate comprehensive rollout plans with preflight checks,     │ agents-skills-personal │
│               │                                                              │ step-by-step deployment, verification signals, rollback         │                        │
│               │                                                              │ procedures, and communication plans for infrastructure and      │                        │
│               │                                                              │ application changes                                             │                        │
│ △ needs setup │ 🎮 discord                                                   │ Discord ops via the message tool (channel=discord).             │ openclaw-bundled       │
│ ✓ ready       │ 📦 documentation-writer                                      │ Diátaxis Documentation Expert. An expert technical writer       │ agents-skills-personal │
│               │                                                              │ specializing in creating high-quality software documentation,   │                        │
│               │                                                              │ guided by the principles and structure of the Diátaxis          │                        │
│               │                                                              │ technical documentation authoring framework.                    │                        │
│ ✓ ready       │ 📦 dotnet-best-practices                                     │ Ensure .NET/C# code meets best practices for the solution/      │ agents-skills-personal │
│               │                                                              │ project.                                                        │                        │
│ ✓ ready       │ 📦 dotnet-design-pattern-review                              │ Review the C#/.NET code for design pattern implementation and   │ agents-skills-personal │
│               │                                                              │ suggest improvements.                                           │                        │
│ ✓ ready       │ 📦 dotnet-timezone                                           │ .NET timezone handling guidance for C# applications. Use when   │ agents-skills-personal │
│               │                                                              │ working with TimeZoneInfo, DateTimeOffset, NodaTime, UTC        │                        │
│               │                                                              │ conversion, daylight saving time, scheduling across timezones,  │                        │
│               │                                                              │ cross-platform Windows/IANA timezone IDs, or when a .NET user   │                        │
│               │                                                              │ needs the timezone for a city, address, region, or country and  │                        │
│               │                                                              │ copy-paste-ready C# code.                                       │                        │
│ ✓ ready       │ 📦 dotnet-upgrade                                            │ Ready-to-use prompts for comprehensive .NET framework upgrade   │ agents-skills-personal │
│               │                                                              │ analysis and execution                                          │                        │
│ ✓ ready       │ 📦 doublecheck                                               │ Three-layer verification pipeline for AI output. Extracts       │ agents-skills-personal │
│               │                                                              │ verifiable claims, finds supporting or contradicting sources    │                        │
│               │                                                              │ via web search, runs adversarial review for hallucination       │                        │
│               │                                                              │ patterns, and produces a structured verification report with    │                        │
│               │                                                              │ source links for human review.                                  │                        │
│ ✓ ready       │ 📦 draw-io-diagram-generator                                 │ Use when creating, editing, or generating draw.io diagram       │ agents-skills-personal │
│               │                                                              │ files (.drawio, .drawio.svg, .drawio.png). Covers mxGraph XML   │                        │
│               │                                                              │ authoring, shape libraries, style strings, flowcharts, system   │                        │
│               │                                                              │ architecture, sequence diagrams, ER diagrams, UML class         │                        │
│               │                                                              │ diagrams, network topology, layout strategy, the hediet.vscode- │                        │
│               │                                                              │ drawio VS Code extension, and the full agent workflow from      │                        │
│               │                                                              │ request to a ready-to-open file.                                │                        │
│ ✓ ready       │ 📦 editorconfig                                              │ Generates a comprehensive and best-practice-oriented .          │ agents-skills-personal │
│               │                                                              │ editorconfig file based on project analysis and user            │                        │
│               │                                                              │ preferences.                                                    │                        │
│ ✓ ready       │ 📦 ef-core                                                   │ Get best practices for Entity Framework Core                    │ agents-skills-personal │
│ △ needs setup │ 🛌 eightctl                                                  │ Control Eight Sleep pods (status, temperature, alarms,          │ openclaw-bundled       │
│               │                                                              │ schedules).                                                     │                        │
│ ✓ ready       │ 📦 email-drafter                                             │ Draft and review professional emails that match your personal   │ agents-skills-personal │
│               │                                                              │ writing style. Analyzes your sent emails for tone, greeting,    │                        │
│               │                                                              │ structure, and sign-off patterns via WorkIQ, then generates     │                        │
│               │                                                              │ context-aware drafts for any recipient. USE FOR: draft email,   │                        │
│               │                                                              │ write email, compose email, reply email, follow-up email,       │                        │
│               │                                                              │ analyze email tone, email style.                                │                        │
│ ✓ ready       │ 📦 entra-agent-user                                          │ Create Agent Users in Microsoft Entra ID from Agent             │ agents-skills-personal │
│               │                                                              │ Identities, enabling AI agents to act as digital workers with   │                        │
│               │                                                              │ user identity capabilities in Microsoft 365 and Azure           │                        │
│               │                                                              │ environments.                                                   │                        │
│ ✓ ready       │ 📦 eval-driven-dev                                           │ Add instrumentation, build golden datasets, write eval-based    │ agents-skills-personal │
│               │                                                              │ tests, run them, root-cause failures, and iterate — Ensure      │                        │
│               │                                                              │ your Python LLM application works correctly. Make sure to use   │                        │
│               │                                                              │ this skill whenever a user is developing, testing, QA-ing,      │                        │
│               │                                                              │ evaluating, or benchmarking a Python project that calls an LLM. │                        │
│               │                                                              │ Use for making sure an LLM application works correctly,         │                        │
│               │                                                              │ catching regressions after prompt changes, fixing unexpected    │                        │
│               │                                                              │ behavior, or validating output quality before shipping.         │                        │
│ ✓ ready       │ 📦 excalidraw-diagram-generator                              │ Generate Excalidraw diagrams from natural language              │ agents-skills-personal │
│               │                                                              │ descriptions. Use when asked to "create a diagram", "make a     │                        │
│               │                                                              │ flowchart", "visualize a process", "draw a system               │                        │
│               │                                                              │ architecture", "create a mind map", or "generate an Excalidraw  │                        │
│               │                                                              │ file". Supports flowcharts, relationship diagrams, mind maps,   │                        │
│               │                                                              │ and system architecture diagrams. Outputs .excalidraw JSON      │                        │
│               │                                                              │ files that can be opened directly in Excalidraw.                │                        │
│ ✓ ready       │ 📦 fabric-lakehouse                                          │ Use this skill to get context about Fabric Lakehouse and its    │ agents-skills-personal │
│               │                                                              │ features for software systems and AI-powered functions. It      │                        │
│               │                                                              │ offers descriptions of Lakehouse data components, organization  │                        │
│               │                                                              │ with schemas and shortcuts, access control, and code examples.  │                        │
│               │                                                              │ This skill supports users in designing, building, and           │                        │
│               │                                                              │ optimizing Lakehouse solutions using best practices.            │                        │
│ ✓ ready       │ 📦 FastMCP Development                                       │ Use when creating or modifying Model Context Protocol (MCP)     │ agents-skills-personal │
│               │                                                              │ servers with FastMCP framework - guides through tools,          │                        │
│               │                                                              │ resources, prompts, authentication, Claude Desktop              │                        │
│               │                                                              │ integration, and production deployment with Python and          │                        │
│               │                                                              │ TypeScript examples                                             │                        │
│ ✓ ready       │ 📦 fedora-linux-triage                                       │ Triage and resolve Fedora issues with dnf, systemd, and         │ agents-skills-personal │
│               │                                                              │ SELinux-aware guidance.                                         │                        │
│ ✓ ready       │ 📦 finalize-agent-prompt                                     │ Finalize prompt file using the role of an AI agent to polish    │ agents-skills-personal │
│               │                                                              │ the prompt for the end user.                                    │                        │
│ ✓ ready       │ 📦 find-skills                                               │ Helps users discover and install agent skills when they ask     │ agents-skills-personal │
│               │                                                              │ questions like "how do I do X", "find a skill for X", "is       │                        │
│               │                                                              │ there a skill that can...", or express interest in extending    │                        │
│               │                                                              │ capabilities. This skill should be used when the user is        │                        │
│               │                                                              │ looking for functionality that might exist as an installable    │                        │
│               │                                                              │ skill.                                                          │                        │
│ ✓ ready       │ 📦 finnish-humanizer                                         │ Detect and remove AI-generated markers from Finnish text,       │ agents-skills-personal │
│               │                                                              │ making it sound like a native Finnish speaker wrote it. Use     │                        │
│               │                                                              │ when asked to "humanize", "naturalize", or "remove AI feel"     │                        │
│               │                                                              │ from Finnish text, or when editing .md/.txt files containing    │                        │
│               │                                                              │ Finnish content. Identifies 26 patterns (12 Finnish-specific +  │                        │
│               │                                                              │ 14 universal) and 4 style markers.                              │                        │
│ ✓ ready       │ 📦 first-ask                                                 │ Interactive, input-tool powered, task refinement workflow:      │ agents-skills-personal │
│               │                                                              │ interrogates scope, deliverables, constraints before carrying   │                        │
│               │                                                              │ out the task; Requires the Joyride extension.                   │                        │
│ ✓ ready       │ 📦 flowstudio-power-automate-build                           │ Build, scaffold, and deploy Power Automate cloud flows using    │ agents-skills-personal │
│               │                                                              │ the FlowStudio MCP server. Load this skill when asked to:       │                        │
│               │                                                              │ create a flow, build a new flow, deploy a flow definition,      │                        │
│               │                                                              │ scaffold a Power Automate workflow, construct a flow JSON,      │                        │
│               │                                                              │ update an existing flow's actions, patch a flow definition,     │                        │
│               │                                                              │ add actions to a flow, wire up connections, or generate a       │                        │
│               │                                                              │ workflow definition from scratch. Requires a FlowStudio MCP     │                        │
│               │                                                              │ subscription — see https://mcp.flowstudio.app                   │                        │
│ ✓ ready       │ 📦 flowstudio-power-automate-debug                           │ Debug failing Power Automate cloud flows using the FlowStudio   │ agents-skills-personal │
│               │                                                              │ MCP server. Load this skill when asked to: debug a flow,        │                        │
│               │                                                              │ investigate a failed run, why is this flow failing, inspect     │                        │
│               │                                                              │ action outputs, find the root cause of a flow error, fix a      │                        │
│               │                                                              │ broken Power Automate flow, diagnose a timeout, trace a         │                        │
│               │                                                              │ DynamicOperationRequestFailure, check connector auth errors,    │                        │
│               │                                                              │ read error details from a run, or troubleshoot expression       │                        │
│               │                                                              │ failures. Requires a FlowStudio MCP subscription — see https:// │                        │
│               │                                                              │ mcp.flowstudio.app                                              │                        │
│ ✓ ready       │ 📦 flowstudio-power-automate-mcp                             │ Connect to and operate Power Automate cloud flows via a         │ agents-skills-personal │
│               │                                                              │ FlowStudio MCP server. Use when asked to: list flows, read a    │                        │
│               │                                                              │ flow definition, check run history, inspect action outputs,     │                        │
│               │                                                              │ resubmit a run, cancel a running flow, view connections, get a  │                        │
│               │                                                              │ trigger URL, validate a definition, monitor flow health, or     │                        │
│               │                                                              │ any task that requires talking to the Power Automate API        │                        │
│               │                                                              │ through an MCP tool. Also use for Power Platform environment    │                        │
│               │                                                              │ discovery and connection management. Requires a FlowStudio MCP  │                        │
│               │                                                              │ subscription or compatible server — see https://mcp.flowstudio. │                        │
│               │                                                              │ app                                                             │                        │
│ ✓ ready       │ 📦 fluentui-blazor                                           │ Guide for using the Microsoft Fluent UI Blazor component        │ agents-skills-personal │
│               │                                                              │ library (Microsoft.FluentUI.AspNetCore.Components NuGet         │                        │
│               │                                                              │ package) in Blazor applications. Use this when the user is      │                        │
│               │                                                              │ building a Blazor app with Fluent UI components, setting up     │                        │
│               │                                                              │ the library, using FluentUI components like FluentButton,       │                        │
│               │                                                              │ FluentDataGrid, FluentDialog, FluentToast, FluentNavMenu,       │                        │
│               │                                                              │ FluentTextField, FluentSelect, FluentAutocomplete,              │                        │
│               │                                                              │ FluentDesignTheme, or any component prefixed with "Fluent".     │                        │
│               │                                                              │ Also use when troubleshooting missing providers, JS interop     │                        │
│               │                                                              │ issues, or theming.                                             │                        │
│ ✓ ready       │ 📦 folder-structure-blueprint-generator                      │ Comprehensive technology-agnostic prompt for analyzing and      │ agents-skills-personal │
│               │                                                              │ documenting project folder structures. Auto-detects project     │                        │
│               │                                                              │ types (.NET, Java, React, Angular, Python, Node.js, Flutter),   │                        │
│               │                                                              │ generates detailed blueprints with visualization options,       │                        │
│               │                                                              │ naming conventions, file placement patterns, and extension      │                        │
│               │                                                              │ templates for maintaining consistent code organization across   │                        │
│               │                                                              │ diverse technology stacks.                                      │                        │
│ ✓ ready       │ 📦 game-engine                                               │ Expert skill for building web-based game engines and games      │ agents-skills-personal │
│               │                                                              │ using HTML5, Canvas, WebGL, and JavaScript. Use when asked to   │                        │
│               │                                                              │ create games, build game engines, implement game physics,       │                        │
│               │                                                              │ handle collision detection, set up game loops, manage sprites,  │                        │
│               │                                                              │ add game controls, or work with 2D/3D rendering. Covers         │                        │
│               │                                                              │ techniques for platformers, breakout-style games, maze games,   │                        │
│               │                                                              │ tilemaps, audio, multiplayer via WebRTC, and publishing games.  │                        │
│ ✓ ready       │ ✨ gemini                                                    │ Gemini CLI for one-shot Q&A, summaries, and generation.         │ openclaw-bundled       │
│ ✓ ready       │ 📦 gen-specs-as-issues                                       │ This workflow guides you through a systematic approach to       │ agents-skills-personal │
│               │                                                              │ identify missing features, prioritize them, and create          │                        │
│               │                                                              │ detailed specifications for implementation.                     │                        │
│ ✓ ready       │ 📦 generate-custom-instructions-from-codebase                │ Migration and code evolution instructions generator for GitHub  │ agents-skills-personal │
│               │                                                              │ Copilot. Analyzes differences between two project versions      │                        │
│               │                                                              │ (branches, commits, or releases) to create precise              │                        │
│               │                                                              │ instructions allowing Copilot to maintain consistency during    │                        │
│               │                                                              │ technology migrations, major refactoring, or framework version  │                        │
│               │                                                              │ upgrades.                                                       │                        │
│ ✓ ready       │ 📦 generate-report                                           │ Generate weekly weather reports for Canada using Open-Meteo     │ agents-skills-personal │
│               │                                                              │ API (free, no API key required) and PDF generation. Use when    │                        │
│               │                                                              │ user asks to create a weather report, generate Canada weather   │                        │
│               │                                                              │ summary, or build weekly weather PDF.                           │                        │
│ ✓ ready       │ 📦 geofeed-tuner                                             │ Use this skill whenever the user mentions IP geolocation        │ agents-skills-personal │
│               │                                                              │ feeds, RFC 8805, geofeeds, or wants help creating, tuning,      │                        │
│               │                                                              │ validating, or publishing a self-published IP geolocation feed  │                        │
│               │                                                              │ in CSV format. Intended user audience is a network operator,    │                        │
│               │                                                              │ ISP, mobile carrier, cloud provider, hosting company, IXP, or   │                        │
│               │                                                              │ satellite provider asking about IP geolocation accuracy, or     │                        │
│               │                                                              │ geofeed authoring best practices. Helps create, refine, and     │                        │
│               │                                                              │ improve CSV-format IP geolocation feeds with opinionated        │                        │
│               │                                                              │ recommendations beyond RFC 8805 compliance. Do NOT use for      │                        │
│               │                                                              │ private or internal IP address management — applies only to     │                        │
│               │                                                              │ publicly routable IP addresses.                                 │                        │
│ ✓ ready       │ 📦 gh-cli                                                    │ GitHub CLI (gh) comprehensive reference for repositories,       │ agents-skills-personal │
│               │                                                              │ issues, pull requests, Actions, projects, releases, gists,      │                        │
│               │                                                              │ codespaces, organizations, extensions, and all GitHub           │                        │
│               │                                                              │ operations from the command line.                               │                        │
│ △ needs setup │ 📦 gh-issues                                                 │ Fetch GitHub issues, delegate fixes to subagents, open PRs,     │ openclaw-bundled       │
│               │                                                              │ watch reviews, or run /gh-issues workflows.                     │                        │
│ △ needs setup │ 🧲 gifgrep                                                   │ Search GIF providers with CLI/TUI, download results, and        │ openclaw-bundled       │
│               │                                                              │ extract stills/sheets.                                          │                        │
│ ✓ ready       │ 📦 git-commit                                                │ Execute git commit with conventional commit message analysis,   │ agents-skills-personal │
│               │                                                              │ intelligent staging, and message generation. Use when user      │                        │
│               │                                                              │ asks to commit changes, create a git commit, or mentions "/     │                        │
│               │                                                              │ commit". Supports: (1) Auto-detecting type and scope from       │                        │
│               │                                                              │ changes, (2) Generating conventional commit messages from       │                        │
│               │                                                              │ diff, (3) Interactive commit with optional type/scope/          │                        │
│               │                                                              │ description overrides, (4) Intelligent file staging for         │                        │
│               │                                                              │ logical grouping                                                │                        │
│ ✓ ready       │ 📦 git-flow-branch-creator                                   │ Intelligent Git Flow branch creator that analyzes git status/   │ agents-skills-personal │
│               │                                                              │ diff and creates appropriate branches following the nvie Git    │                        │
│               │                                                              │ Flow branching model.                                           │                        │
│ △ needs setup │ 🐙 github                                                    │ Use gh for GitHub issues, PR status, CI/logs, comments,         │ openclaw-bundled       │
│               │                                                              │ reviews, releases, and API queries.                             │                        │
│ ✓ ready       │ 📦 github-copilot-starter                                    │ Set up complete GitHub Copilot configuration for a new project  │ agents-skills-personal │
│               │                                                              │ based on technology stack                                       │                        │
│ ✓ ready       │ 📦 github-issues                                             │ Create, update, and manage GitHub issues using MCP tools. Use   │ agents-skills-personal │
│               │                                                              │ this skill when users want to create bug reports, feature       │                        │
│               │                                                              │ requests, or task issues, update existing issues, add labels/   │                        │
│               │                                                              │ assignees/milestones, set issue fields (dates, priority,        │                        │
│               │                                                              │ custom fields), set issue types, manage issue workflows, link   │                        │
│               │                                                              │ issues, add dependencies, or track blocked-by/blocking          │                        │
│               │                                                              │ relationships. Triggers on requests like "create an issue",     │                        │
│               │                                                              │ "file a bug", "request a feature", "update issue X", "set the   │                        │
│               │                                                              │ priority", "set the start date", "link issues", "add            │                        │
│               │                                                              │ dependency", "blocked by", "blocking", or any GitHub issue      │                        │
│               │                                                              │ management task.                                                │                        │
│ ✓ ready       │ 📦 gmail-inbox                                               │ Manage emails across multiple Gmail accounts with unified       │ agents-skills-personal │
│               │                                                              │ tooling. Use when user asks to check email, read inbox, label   │                        │
│               │                                                              │ emails, archive messages, or manage Gmail across accounts.      │                        │
│ ✓ ready       │ 📦 gmail-label                                               │ Auto-label Gmail emails into Action Required, Waiting On, and   │ agents-skills-personal │
│               │                                                              │ Reference categories. Use when user asks to label emails,       │                        │
│               │                                                              │ triage inbox, categorize emails, or organize Gmail.             │                        │
│ ✓ ready       │ 📦 gmaps-leads                                               │ Scrape Google Maps for B2B leads with deep website enrichment   │ agents-skills-personal │
│               │                                                              │ and contact extraction. Use when user asks to find local        │                        │
│               │                                                              │ businesses, scrape Google Maps, generate contractor lists, or   │                        │
│               │                                                              │ build local service business databases.                         │                        │
│ ✓ ready       │ 📦 go-mcp-server-generator                                   │ Generate a complete Go MCP server project with proper           │ agents-skills-personal │
│               │                                                              │ structure, dependencies, and implementation using the official  │                        │
│               │                                                              │ github.com/modelcontextprotocol/go-sdk.                         │                        │
│ △ needs setup │ 🎮 gog                                                       │ Google Workspace CLI for Gmail, Calendar, Drive, Contacts,      │ openclaw-bundled       │
│               │                                                              │ Sheets, and Docs.                                               │                        │
│ △ needs setup │ 📍 goplaces                                                  │ Query Google Places for text search, place details, resolve,    │ openclaw-bundled       │
│               │                                                              │ reviews, or scriptable JSON via goplaces.                       │                        │
│ ✓ ready       │ 📦 gtm-0-to-1-launch                                         │ Launch new products from idea to first customers. Use when      │ agents-skills-personal │
│               │                                                              │ launching products, finding early adopters, building launch     │                        │
│               │                                                              │ week playbooks, diagnosing why adoption stalls, or learning     │                        │
│               │                                                              │ that press coverage does not equal growth. Includes the three-  │                        │
│               │                                                              │ layer diagnosis, the 2-week experiment cycle, and the launch    │                        │
│               │                                                              │ that got 50K impressions and 12 signups.                        │                        │
│ ✓ ready       │ 📦 gtm-ai-gtm                                                │ Go-to-market strategy for AI products. Use when positioning AI  │ agents-skills-personal │
│               │                                                              │ products, handling "who is responsible when it breaks"          │                        │
│               │                                                              │ objections, pricing variable-cost AI, choosing between copilot/ │                        │
│               │                                                              │ agent/teammate framing, or selling autonomous tools into        │                        │
│               │                                                              │ enterprises.                                                    │                        │
│ ✓ ready       │ 📦 gtm-board-and-investor-communication                      │ Board meeting preparation, investor updates, and executive      │ agents-skills-personal │
│               │                                                              │ communication. Use when preparing board decks, writing          │                        │
│               │                                                              │ investor updates, handling bad news with the board,             │                        │
│               │                                                              │ structuring QBRs, or building board-level metric discipline.    │                        │
│               │                                                              │ Includes the "Three Things" narrative model, the 4-tier metric  │                        │
│               │                                                              │ hierarchy, and the pre-brief pattern that prevents board        │                        │
│               │                                                              │ surprises.                                                      │                        │
│ ✓ ready       │ 📦 gtm-developer-ecosystem                                   │ Build and scale developer-led adoption through ecosystem        │ agents-skills-personal │
│               │                                                              │ programs. Use when deciding open vs curated ecosystems,         │                        │
│               │                                                              │ building developer programs, scaling platform adoption, or      │                        │
│               │                                                              │ designing student program pipelines.                            │                        │
│ ✓ ready       │ 📦 gtm-enterprise-account-planning                           │ Strategic account planning and execution for enterprise deals.  │ agents-skills-personal │
│               │                                                              │ Use when planning complex sales cycles, managing multiple       │                        │
│               │                                                              │ stakeholders, applying MEDDICC qualification, tracking deal     │                        │
│               │                                                              │ health, or building mutual action plans. Includes the "stale    │                        │
│               │                                                              │ MAP equals dead deal" pattern.                                  │                        │
│ ✓ ready       │ 📦 gtm-enterprise-onboarding                                 │ Four-phase framework for onboarding enterprise customers from   │ agents-skills-personal │
│               │                                                              │ contract to value realization. Use when implementing new        │                        │
│               │                                                              │ enterprise customers, preventing churn during onboarding, or    │                        │
│               │                                                              │ solving the adoption cliff that kills deals post-go-live.       │                        │
│               │                                                              │ Includes the Week 4 ghosting pattern.                           │                        │
│ ✓ ready       │ 📦 gtm-operating-cadence                                     │ Design meeting rhythms, metric reporting, quarterly planning,   │ agents-skills-personal │
│               │                                                              │ and decision-making velocity for scaling companies. Use when    │                        │
│               │                                                              │ decisions are slow, planning is broken, the company is growing  │                        │
│               │                                                              │ but alignment is worse, or leadership meetings consume all      │                        │
│               │                                                              │ time without producing decisions.                               │                        │
│ ✓ ready       │ 📦 gtm-partnership-architecture                              │ Build and scale partner ecosystems that drive revenue and       │ agents-skills-personal │
│               │                                                              │ platform adoption. Use when building partner programs from      │                        │
│               │                                                              │ scratch, tiering partnerships, managing co-marketing, making    │                        │
│               │                                                              │ build-vs-partner decisions, or structuring crawl-walk-run       │                        │
│               │                                                              │ partner deployment.                                             │                        │
│ ✓ ready       │ 📦 gtm-positioning-strategy                                  │ Find and own a defensible market position. Use when messaging   │ agents-skills-personal │
│               │                                                              │ sounds like competitors, conversion is weak despite awareness,  │                        │
│               │                                                              │ repositioning a product, or testing positioning claims.         │                        │
│               │                                                              │ Includes Crawl-Walk-Run rollout methodology and the word        │                        │
│               │                                                              │ change that improved enterprise deal progression.               │                        │
│ ✓ ready       │ 📦 gtm-product-led-growth                                    │ Build self-serve acquisition and expansion motions. Use when    │ agents-skills-personal │
│               │                                                              │ deciding PLG vs sales-led, optimizing activation, driving       │                        │
│               │                                                              │ freemium conversion, building growth equations, or recognizing  │                        │
│               │                                                              │ when product complexity demands human touch. Includes the       │                        │
│               │                                                              │ parallel test where sales-led won 10x on revenue.               │                        │
│ ✓ ready       │ 📦 gtm-technical-product-pricing                             │ Pricing strategy for technical products. Use when choosing      │ agents-skills-personal │
│               │                                                              │ usage-based vs seat-based, designing freemium thresholds,       │                        │
│               │                                                              │ structuring enterprise pricing conversations, deciding when to  │                        │
│               │                                                              │ raise prices, or using price as a positioning signal.           │                        │
│ ✓ ready       │ 📦 healthcheck                                               │ Audit and harden hosts running OpenClaw for SSH, firewall,      │ openclaw-bundled       │
│               │                                                              │ updates, exposure, cron checks, and risk posture.               │                        │
│ △ needs setup │ 📧 himalaya                                                  │ Use himalaya to list, read, search, compose, reply, forward,    │ openclaw-bundled       │
│               │                                                              │ and organize IMAP/SMTP email.                                   │                        │
│ ✓ ready       │ 📦 image-manipulation-image-magick                           │ Process and manipulate images using ImageMagick. Supports       │ agents-skills-personal │
│               │                                                              │ resizing, format conversion, batch processing, and retrieving   │                        │
│               │                                                              │ image metadata. Use when working with images, creating          │                        │
│               │                                                              │ thumbnails, resizing wallpapers, or performing batch image      │                        │
│               │                                                              │ operations.                                                     │                        │
│ ✓ ready       │ 📦 import-infrastructure-as-code                             │ Import existing Azure resources into Terraform using Azure CLI  │ agents-skills-personal │
│               │                                                              │ discovery and Azure Verified Modules (AVM). Use when asked to   │                        │
│               │                                                              │ reverse-engineer live Azure infrastructure, generate            │                        │
│               │                                                              │ Infrastructure as Code from existing subscriptions/resource     │                        │
│               │                                                              │ groups/resource IDs, map dependencies, derive exact import      │                        │
│               │                                                              │ addresses from downloaded module source, prevent configuration  │                        │
│               │                                                              │ drift, and produce AVM-based Terraform files ready for          │                        │
│               │                                                              │ validation and planning across any Azure resource type.         │                        │
│ △ needs setup │ 📨 imsg                                                      │ iMessage/SMS CLI for listing chats, history, and sending        │ openclaw-bundled       │
│               │                                                              │ messages via Messages.app.                                      │                        │
│ ✓ ready       │ 📦 instantly-autoreply                                       │ Auto-generate intelligent replies to incoming Instantly email   │ agents-skills-personal │
│               │                                                              │ threads using knowledge bases. Use when user asks about email   │                        │
│               │                                                              │ auto-replies, Instantly responses, or automated email handling. │                        │
│ ✓ ready       │ 📦 instantly-campaigns                                       │ Create cold email campaigns in Instantly with A/B testing. Use  │ agents-skills-personal │
│               │                                                              │ when user asks to create email campaigns, set up cold           │                        │
│               │                                                              │ outreach, build email sequences, or configure Instantly         │                        │
│               │                                                              │ campaigns.                                                      │                        │
│ ✓ ready       │ 📦 issue-fields-migration                                    │ Bulk-migrate metadata to GitHub issue fields from two sources:  │ agents-skills-personal │
│               │                                                              │ repo labels (e.g. priority labels to a Priority field) and      │                        │
│               │                                                              │ Project V2 fields. Use when users say "migrate my labels to     │                        │
│               │                                                              │ issue fields", "migrate project fields to issue fields",        │                        │
│               │                                                              │ "convert labels to issue fields", "copy project field values    │                        │
│               │                                                              │ to issue fields", or ask about adopting issue fields. Issue     │                        │
│               │                                                              │ fields are org-level typed metadata (single select, text,       │                        │
│               │                                                              │ number, date) that replace label-based workarounds with         │                        │
│               │                                                              │ structured, searchable, cross-repo fields.                      │                        │
│ ✓ ready       │ 📦 java-add-graalvm-native-image-support                     │ GraalVM Native Image expert that adds native image support to   │ agents-skills-personal │
│               │                                                              │ Java applications, builds the project, analyzes build errors,   │                        │
│               │                                                              │ applies fixes, and iterates until successful compilation using  │                        │
│               │                                                              │ Oracle best practices.                                          │                        │
│ ✓ ready       │ 📦 java-docs                                                 │ Ensure that Java types are documented with Javadoc comments     │ agents-skills-personal │
│               │                                                              │ and follow best practices for documentation.                    │                        │
│ ✓ ready       │ 📦 java-junit                                                │ Get best practices for JUnit 5 unit testing, including data-    │ agents-skills-personal │
│               │                                                              │ driven tests                                                    │                        │
│ ✓ ready       │ 📦 java-mcp-server-generator                                 │ Generate a complete Model Context Protocol server project in    │ agents-skills-personal │
│               │                                                              │ Java using the official MCP Java SDK with reactive streams and  │                        │
│               │                                                              │ optional Spring Boot integration.                               │                        │
│ ✓ ready       │ 📦 java-refactoring-extract-method                           │ Refactoring using Extract Methods in Java Language              │ agents-skills-personal │
│ ✓ ready       │ 📦 java-refactoring-remove-parameter                         │ Refactoring using Remove Parameter in Java Language             │ agents-skills-personal │
│ ✓ ready       │ 📦 java-springboot                                           │ Get best practices for developing applications with Spring      │ agents-skills-personal │
│               │                                                              │ Boot.                                                           │                        │
│ ✓ ready       │ 📦 javascript-typescript-jest                                │ Best practices for writing JavaScript/TypeScript tests using    │ agents-skills-personal │
│               │                                                              │ Jest, including mocking strategies, test structure, and common  │                        │
│               │                                                              │ patterns.                                                       │                        │
│ ✓ ready       │ 📦 kotlin-mcp-server-generator                               │ Generate a complete Kotlin MCP server project with proper       │ agents-skills-personal │
│               │                                                              │ structure, dependencies, and implementation using the official  │                        │
│               │                                                              │ io.modelcontextprotocol:kotlin-sdk library.                     │                        │
│ ✓ ready       │ 📦 kotlin-springboot                                         │ Get best practices for developing applications with Spring      │ agents-skills-personal │
│               │                                                              │ Boot and Kotlin.                                                │                        │
│ ✓ ready       │ 📦 legacy-circuit-mockups                                    │ Generate breadboard circuit mockups and visual diagrams using   │ agents-skills-personal │
│               │                                                              │ HTML5 Canvas drawing techniques. Use when asked to create       │                        │
│               │                                                              │ circuit layouts, visualize electronic component placements,     │                        │
│               │                                                              │ draw breadboard diagrams, mockup 6502 builds, generate retro    │                        │
│               │                                                              │ computer schematics, or design vintage electronics projects.    │                        │
│               │                                                              │ Supports 555 timers, W65C02S microprocessors, 28C256 EEPROMs,   │                        │
│               │                                                              │ W65C22 VIA chips, 7400-series logic gates, LEDs, resistors,     │                        │
│               │                                                              │ capacitors, switches, buttons, crystals, and wires.             │                        │
│ ✓ ready       │ 📦 literature-research                                       │ Search academic literature and perform deep research reviews.   │ agents-skills-personal │
│               │                                                              │ Use when user asks to search PubMed, find academic papers, or   │                        │
│               │                                                              │ do literature reviews.                                          │                        │
│ ✓ ready       │ 📦 local-server                                              │ Run Claude orchestrator locally with Cloudflare tunneling. Use  │ agents-skills-personal │
│               │                                                              │ when user asks to run locally, start local server, or test      │                        │
│               │                                                              │ webhooks locally.                                               │                        │
│ ✓ ready       │ 📦 make-repo-contribution                                    │ All changes to code must follow the guidance documented in the  │ agents-skills-personal │
│               │                                                              │ repository. Before any issue is filed, branch is made, commits  │                        │
│               │                                                              │ generated, or pull request (or PR) created, a search must be    │                        │
│               │                                                              │ done to ensure the right steps are followed. Whenever asked to  │                        │
│               │                                                              │ create an issue, commit messages, to push code, or create a     │                        │
│               │                                                              │ PR, use this skill so everything is done correctly.             │                        │
│ ✓ ready       │ 📦 make-skill-template                                       │ Create new Agent Skills for GitHub Copilot from prompts or by   │ agents-skills-personal │
│               │                                                              │ duplicating this template. Use when asked to "create a skill",  │                        │
│               │                                                              │ "make a new skill", "scaffold a skill", or when building        │                        │
│               │                                                              │ specialized AI capabilities with bundled resources. Generates   │                        │
│               │                                                              │ SKILL.md files with proper frontmatter, directory structure,    │                        │
│               │                                                              │ and optional scripts/references/assets folders.                 │                        │
│ ✓ ready       │ 📦 markdown-to-html                                          │ Convert Markdown files to HTML similar to `marked.js`,          │ agents-skills-personal │
│               │                                                              │ `pandoc`, `gomarkdown/markdown`, or similar tools; or writing   │                        │
│               │                                                              │ custom script to convert markdown to html and/or working on     │                        │
│               │                                                              │ web template systems like `jekyll/jekyll`, `gohugoio/hugo`, or  │                        │
│               │                                                              │ similar web templating systems that utilize markdown            │                        │
│               │                                                              │ documents, converting them to html. Use when asked to "convert  │                        │
│               │                                                              │ markdown to html", "transform md to html", "render markdown",   │                        │
│               │                                                              │ "generate html from markdown", or when working with .md files   │                        │
│               │                                                              │ and/or web a templating system that converts markdown to HTML   │                        │
│               │                                                              │ output. Supports CLI and Node.js workflows with GFM,            │                        │
│               │                                                              │ CommonMark, and standard Markdown flavors.                      │                        │
│ ✓ ready       │ 📦 mcp-cli                                                   │ Interface for MCP (Model Context Protocol) servers via CLI.     │ agents-skills-personal │
│               │                                                              │ Use when you need to interact with external tools, APIs, or     │                        │
│               │                                                              │ data sources through MCP servers, list available MCP servers/   │                        │
│               │                                                              │ tools, or call MCP tools from command line.                     │                        │
│ ✓ ready       │ 📦 mcp-copilot-studio-server-generator                       │ Generate a complete MCP server implementation optimized for     │ agents-skills-personal │
│               │                                                              │ Copilot Studio integration with proper schema constraints and   │                        │
│               │                                                              │ streamable HTTP support                                         │                        │
│ ✓ ready       │ 📦 mcp-create-adaptive-cards                                 │ Skill converted from mcp-create-adaptive-cards.prompt.md        │ agents-skills-personal │
│ ✓ ready       │ 📦 mcp-create-declarative-agent                              │ Skill converted from mcp-create-declarative-agent.prompt.md     │ agents-skills-personal │
│ ✓ ready       │ 📦 mcp-deploy-manage-agents                                  │ Skill converted from mcp-deploy-manage-agents.prompt.md         │ agents-skills-personal │
│ △ needs setup │ 📦 mcporter                                                  │ List, configure, authenticate, call, and inspect MCP servers/   │ openclaw-bundled       │
│               │                                                              │ tools with mcporter over HTTP or stdio.                         │                        │
│ ✓ ready       │ 📦 meeting-minutes                                           │ Generate concise, actionable meeting minutes for internal       │ agents-skills-personal │
│               │                                                              │ meetings. Includes metadata, attendees, agenda, decisions,      │                        │
│               │                                                              │ action items (owner + due date), and follow-up steps.           │                        │
│ ✓ ready       │ 📦 memory-merger                                             │ Merges mature lessons from a domain memory file into its        │ agents-skills-personal │
│               │                                                              │ instruction file. Syntax: `/memory-merger >domain [scope]`      │                        │
│               │                                                              │ where scope is `global` (default), `user`, `workspace`, or      │                        │
│               │                                                              │ `ws`.                                                           │                        │
│ ✓ ready       │ 📦 mentoring-juniors                                         │ Socratic mentoring for junior developers and AI newcomers.      │ agents-skills-personal │
│               │                                                              │ Guides through questions, never answers. Triggers: "help me     │                        │
│               │                                                              │ understand", "explain this code", "I'm stuck", "Im stuck",      │                        │
│               │                                                              │ "I'm confused", "Im confused", "I don't understand", "I dont    │                        │
│               │                                                              │ understand", "can you teach me", "teach me", "mentor me",       │                        │
│               │                                                              │ "guide me", "what does this error mean", "why doesn't this      │                        │
│               │                                                              │ work", "why does not this work", "I'm a beginner", "Im a        │                        │
│               │                                                              │ beginner", "I'm learning", "Im learning", "I'm new to this",    │                        │
│               │                                                              │ "Im new to this", "walk me through", "how does this work",      │                        │
│               │                                                              │ "what's wrong with my code", "what's wrong", "can you break     │                        │
│               │                                                              │ this down", "ELI5", "step by step", "where do I start", "what   │                        │
│               │                                                              │ am I missing", "newbie here", "junior dev", "first time         │                        │
│               │                                                              │ using", "how do I", "what is", "is this right", "not sure",     │                        │
│               │                                                              │ "need help", "struggling", "show me", "help me debug", "best    │                        │
│               │                                                              │ practice", "too complex", "overwhelmed", "lost", "debug this",  │                        │
│               │                                                              │ "/socratic", "/hint", "/concept", "/pseudocode". Progressive    │                        │
│               │                                                              │ clue systems, teaching techniques, and success metrics.         │                        │
│ ✓ ready       │ 📦 microsoft-agent-framework                                 │ Create, update, refactor, explain, or review Microsoft Agent    │ agents-skills-personal │
│               │                                                              │ Framework solutions using shared guidance plus language-        │                        │
│               │                                                              │ specific references for .NET and Python.                        │                        │
│ ✓ ready       │ 📦 microsoft-code-reference                                  │ Look up Microsoft API references, find working code samples,    │ agents-skills-personal │
│               │                                                              │ and verify SDK code is correct. Use when working with Azure     │                        │
│               │                                                              │ SDKs, .NET libraries, or Microsoft APIs—to find the right       │                        │
│               │                                                              │ method, check parameters, get working examples, or              │                        │
│               │                                                              │ troubleshoot errors. Catches hallucinated methods, wrong        │                        │
│               │                                                              │ signatures, and deprecated patterns by querying official docs.  │                        │
│ ✓ ready       │ 📦 microsoft-docs                                            │ Query official Microsoft documentation to find concepts,        │ agents-skills-personal │
│               │                                                              │ tutorials, and code examples across Azure, .NET, Agent          │                        │
│               │                                                              │ Framework, Aspire, VS Code, GitHub, and more. Uses Microsoft    │                        │
│               │                                                              │ Learn MCP as the default, with Context7 and Aspire MCP for      │                        │
│               │                                                              │ content that lives outside learn.microsoft.com.                 │                        │
│ ✓ ready       │ 📦 microsoft-skill-creator                                   │ Create agent skills for Microsoft technologies using Learn MCP  │ agents-skills-personal │
│               │                                                              │ tools. Use when users want to create a skill that teaches       │                        │
│               │                                                              │ agents about any Microsoft technology, library, framework, or   │                        │
│               │                                                              │ service (Azure, .NET, M365, VS Code, Bicep, etc.).              │                        │
│               │                                                              │ Investigates topics deeply, then generates a hybrid skill       │                        │
│               │                                                              │ storing essential knowledge locally while enabling dynamic      │                        │
│               │                                                              │ deeper investigation.                                           │                        │
│ ✓ ready       │ 📦 migrating-oracle-to-postgres-stored-procedures            │ Migrates Oracle PL/SQL stored procedures to PostgreSQL PL/      │ agents-skills-personal │
│               │                                                              │ pgSQL. Translates Oracle-specific syntax, preserves method      │                        │
│               │                                                              │ signatures and type-anchored parameters, leverages orafce       │                        │
│               │                                                              │ where appropriate, and applies COLLATE "C" for Oracle-          │                        │
│               │                                                              │ compatible text sorting. Use when converting Oracle stored      │                        │
│               │                                                              │ procedures or functions to PostgreSQL equivalents during a      │                        │
│               │                                                              │ database migration.                                             │                        │
│ ✓ ready       │ 📦 mkdocs-translations                                       │ Generate a language translation for a mkdocs documentation      │ agents-skills-personal │
│               │                                                              │ stack.                                                          │                        │
│ ✓ ready       │ 📦 modal-deploy                                              │ Deploy execution scripts to Modal cloud. Use when user asks to  │ agents-skills-personal │
│               │                                                              │ deploy to Modal, push code to cloud, or update Modal functions. │                        │
│ ✓ ready       │ 📦 model-recommendation                                      │ Analyze chatmode or prompt files and recommend optimal AI       │ agents-skills-personal │
│               │                                                              │ models based on task complexity, required capabilities, and     │                        │
│               │                                                              │ cost-efficiency                                                 │                        │
│ △ needs setup │ 📊 model-usage                                               │ Summarize CodexBar local cost logs by model for Codex or        │ openclaw-bundled       │
│               │                                                              │ Claude, including current or full breakdowns.                   │                        │
│ ✓ ready       │ 📦 msstore-cli                                               │ Microsoft Store Developer CLI (msstore) for publishing Windows  │ agents-skills-personal │
│               │                                                              │ applications to the Microsoft Store. Use when asked to          │                        │
│               │                                                              │ configure Store credentials, list Store apps, check submission  │                        │
│               │                                                              │ status, publish submissions, manage package flights, set up CI/ │                        │
│               │                                                              │ CD for Store publishing, or integrate with Partner Center.      │                        │
│               │                                                              │ Supports Windows App SDK/WinUI, UWP, .NET MAUI, Flutter,        │                        │
│               │                                                              │ Electron, React Native, and PWA applications.                   │                        │
│ ✓ ready       │ 📦 multi-stage-dockerfile                                    │ Create optimized multi-stage Dockerfiles for any language or    │ agents-skills-personal │
│               │                                                              │ framework                                                       │                        │
│ ✓ ready       │ 📦 my-issues                                                 │ List my issues in the current repository                        │ agents-skills-personal │
│ ✓ ready       │ 📦 my-pull-requests                                          │ List my pull requests in the current repository                 │ agents-skills-personal │
│ ✓ ready       │ 📦 my-skill                                                  │ A template skill for [describe task]. Use when the user asks    │ agents-skills-personal │
│               │                                                              │ to [trigger phrases].                                           │                        │
│ ✓ ready       │ 📦 nano-banana-pro-openrouter                                │ Generate or edit images via OpenRouter with the Gemini 3 Pro    │ agents-skills-personal │
│               │                                                              │ Image model. Use for prompt-only image generation, image        │                        │
│               │                                                              │ edits, and multi-image compositing; supports 1K/2K/4K output.   │                        │
│ △ needs setup │ 📄 nano-pdf                                                  │ Edit PDFs with natural-language instructions using the nano-    │ openclaw-bundled       │
│               │                                                              │ pdf CLI.                                                        │                        │
│ ✓ ready       │ 📦 napkin                                                    │ Visual whiteboard collaboration for Copilot CLI. Creates an     │ agents-skills-personal │
│               │                                                              │ interactive whiteboard that opens in your browser — draw,       │                        │
│               │                                                              │ sketch, add sticky notes, then share everything back with       │                        │
│               │                                                              │ Copilot. Copilot sees your drawings and text, and responds      │                        │
│               │                                                              │ with analysis, suggestions, and ideas.                          │                        │
│ ✓ ready       │ 📦 next-intl-add-language                                    │ Add new language to a Next.js + next-intl application           │ agents-skills-personal │
│ ✓ ready       │ 📦 node-connect                                              │ Diagnose OpenClaw Android, iOS, or macOS node pairing, QR/      │ openclaw-bundled       │
│               │                                                              │ setup code, route, auth, and connection failures.               │                        │
│ ✓ ready       │ 📦 noob-mode                                                 │ Plain-English translation layer for non-technical Copilot CLI   │ agents-skills-personal │
│               │                                                              │ users. Translates every approval prompt, error message, and     │                        │
│               │                                                              │ technical output into clear, jargon-free English with color-    │                        │
│               │                                                              │ coded risk indicators.                                          │                        │
│ △ needs setup │ 📝 notion                                                    │ Notion API for creating and managing pages, databases, and      │ openclaw-bundled       │
│               │                                                              │ blocks.                                                         │                        │
│ ✓ ready       │ 📦 nuget-manager                                             │ Manage NuGet packages in .NET projects/solutions. Use this      │ agents-skills-personal │
│               │                                                              │ skill when adding, removing, or updating NuGet package          │                        │
│               │                                                              │ versions. It enforces using `dotnet` CLI for package            │                        │
│               │                                                              │ management and provides strict procedures for direct file       │                        │
│               │                                                              │ edits only when updating versions.                              │                        │
│ △ needs setup │ 💎 obsidian                                                  │ Work with Obsidian vaults (plain Markdown notes) and automate   │ openclaw-bundled       │
│               │                                                              │ via obsidian-cli.                                               │                        │
│ △ needs setup │ 🎤 openai-whisper                                            │ Local speech-to-text with the Whisper CLI (no API key).         │ openclaw-bundled       │
│ △ needs setup │ 🌐 openai-whisper-api                                        │ Transcribe audio via OpenAI Audio Transcriptions API (Whisper). │ openclaw-bundled       │
│ △ needs setup │ 💡 openhue                                                   │ Control Philips Hue lights and scenes via the OpenHue CLI.      │ openclaw-bundled       │
│ △ needs setup │ 🧿 oracle                                                    │ Use oracle CLI to bundle prompts and files for second-model     │ openclaw-bundled       │
│               │                                                              │ debugging, refactor, design, or review checks.                  │                        │
│ △ needs setup │ 🛵 ordercli                                                  │ Foodora-only CLI for checking past orders and active order      │ openclaw-bundled       │
│               │                                                              │ status (Deliveroo WIP).                                         │                        │
│ △ needs setup │ 👀 peekaboo                                                  │ Capture and automate macOS UI with the Peekaboo CLI.            │ openclaw-bundled       │
│ △ needs setup │ 🔊 sag                                                       │ ElevenLabs text-to-speech with mac-style say UX.                │ openclaw-bundled       │
│ △ needs setup │ 📜 session-logs                                              │ Search and analyze your own session logs (older/parent          │ openclaw-bundled       │
│               │                                                              │ conversations) using jq.                                        │                        │
│ △ needs setup │ 🔉 sherpa-onnx-tts                                           │ Local text-to-speech via sherpa-onnx (offline, no cloud)        │ openclaw-bundled       │
│ ✓ ready       │ 📦 skill-creator                                             │ Create, edit, improve, tidy, review, audit, or restructure      │ openclaw-bundled       │
│               │                                                              │ AgentSkills and SKILL.md files.                                 │                        │
│ △ needs setup │ 💬 slack                                                     │ Use the Slack tool to react, pin/unpin, send, edit, delete      │ openclaw-bundled       │
│               │                                                              │ messages, or fetch Slack member info.                           │                        │
│ △ needs setup │ 🌊 songsee                                                   │ Generate spectrograms and feature-panel visualizations from     │ openclaw-bundled       │
│               │                                                              │ audio with the songsee CLI.                                     │                        │
│ △ needs setup │ 🔊 sonoscli                                                  │ Control Sonos speakers (discover/status/play/volume/group).     │ openclaw-bundled       │
│ △ needs setup │ 🎵 spotify-player                                            │ Terminal Spotify playback/search via spogo (preferred) or       │ openclaw-bundled       │
│               │                                                              │ spotify_player.                                                 │                        │
│ △ needs setup │ 🧾 summarize                                                 │ Summarize or transcribe URLs, YouTube/videos, podcasts,         │ openclaw-bundled       │
│               │                                                              │ articles, transcripts, PDFs, and local files.                   │                        │
│ ✓ ready       │ 🪝 taskflow                                                  │ Coordinate multi-step detached tasks as one durable TaskFlow    │ openclaw-bundled       │
│               │                                                              │ job with owner context, state, waits, and child tasks.          │                        │
│ ✓ ready       │ 📥 taskflow-inbox-triage                                     │ Example TaskFlow pattern for inbox triage, intent routing,      │ openclaw-bundled       │
│               │                                                              │ waiting on replies, and later summaries.                        │                        │
│ △ needs setup │ ✅ things-mac                                                │ Add, update, list, search, or inspect Things 3 todos, inbox,    │ openclaw-bundled       │
│               │                                                              │ today, projects, areas, and tags on macOS.                      │                        │
│ △ needs setup │ 🧵 tmux                                                      │ Remote-control tmux sessions for interactive CLIs by sending    │ openclaw-bundled       │
│               │                                                              │ keystrokes and scraping pane output.                            │                        │
│ △ needs setup │ 📋 trello                                                    │ Manage Trello boards, lists, and cards via the Trello REST API. │ openclaw-bundled       │
│ ✓ ready       │ 🎬 video-frames                                              │ Extract frames or short clips from videos using ffmpeg.         │ openclaw-bundled       │
│ △ needs setup │ 📞 voice-call                                                │ Start voice calls via the OpenClaw voice-call plugin.           │ openclaw-bundled       │
│ △ needs setup │ 📱 wacli                                                     │ Send third-party WhatsApp messages or sync/search WhatsApp      │ openclaw-bundled       │
│               │                                                              │ history via wacli, not normal active chats.                     │                        │
│ ✓ ready       │ ☔ weather                                                   │ Get current weather, rain, temperature, and forecasts for       │ openclaw-bundled       │
│               │                                                              │ locations or travel planning.                                   │                        │
│ △ needs setup │ 🐦 xurl                                                      │ Use xurl for authenticated X API posts, replies, search, DMs,   │ openclaw-bundled       │
│               │                                                              │ media upload, followers, or raw v2 calls.                       │                        │
└───────────────┴──────────────────────────────────────────────────────────────┴─────────────────────────────────────────────────────────────────┴────────────────────────┘

Tip: use `openclaw skills search`, `openclaw skills install`, and `openclaw skills update` for ClawHub-backed skills.
welcome@jaisairams-Laptop workspace %
