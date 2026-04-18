🚀 BrifAI - Intelligent Briefing AgentBrifAI is an automated system designed to generate personalized news briefings and distribute them via Email and Discord using AI Agents. This project follows the Spec-Driven Development (SDD) methodology to ensure high-quality code and seamless integration between team members. 🛠️ Tech StackLanguage: Python 3.12+ Framework: Agno (AI Orchestration) Environment Manager: uv Key Libraries: discord.py, newsapi-python, apscheduler, smtplib. 📂 Project StructureFollowing the Clean Architecture and SOLID principles:Plaintextsrc/
├── agent/            # M3: AI Agent logic (Agno) [cite: 421]
├── bot/              # M2: Conversational onboarding (discord.py) [cite: 417]
├── core/             # M1: Domain models (Dataclasses) [cite: 405]
├── interfaces/       # M1: Abstract Base Classes (Contracts) [cite: 408]
├── services/         # M4: Infrastructure (NewsAPI, SMTP, Scheduler) [cite: 425]
├── storage/          # M1: Data persistence (JSON) [cite: 431]
└── main.py           # M1: Dependency injection and entry point 
⚙️ Setup & Installation1. PrerequisitesEnsure you have uv installed. If not, install it via PowerShell:PowerShellpowershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex"
2. ConfigurationClone the repository and navigate to the root folder.Create a .env file from the template:PowerShellcp .env.example .env
Fill in your credentials: DISCORD_BOT_TOKEN, NEWS_API_KEY, and SMTP settings. 3. Install DependenciesPowerShelluv sync
🚀 Running the ProjectTo start the system (Onboarding and Scheduler):PowerShelluv run python src/main.py
🤖 Development Protocol (For the Team)All members must follow the Spec-Driven Development rules:English Only: All code, variables, and docs must be in English. 20-Line Rule: No method or function shall exceed 20 lines of code. DIP: Depend on abstractions (interfaces), never on concrete implementations. AI Usage: Always use the Base Prompt provided in the [Protocolo de Desenvolvimento PDF] before generating code.
