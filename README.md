# Midline-AMD-Slingshot
Tailwind AI is an AI-powered no-code business launcher. Type your idea — get a validated concept, landing page, legal framework, 90-day game plan, and lead list in under 5 minutes. Powered by Claude API on AMD MI300X.
The AI-Powered No-Code Business Launcher

Type your idea. Get a validated concept, landing page, legal framework, 90-day game plan, and lead list — in under 5 minutes.


What is Tailwind AI?
Tailwind AI is an end-to-end business launcher built for first-time founders, solopreneurs, and aspiring entrepreneurs who lack the technical skills or capital to launch a business traditionally.
Instead of juggling 10+ tools across strategy, design, legal, and marketing — you type your idea in plain English, and Tailwind's AI does the rest.

Features
Module What it does 
Idea Validation
5 AI-generated questions
stress-test your concept. Get a 0–100 score with strengths, risks, and market size.Offer CreationHormozi-inspired 6-question framework crafts your pricing, positioning, and messaging.Landing Page GeneratorProduces a complete, production-ready HTML landing page — hero, social proof, pricing, CTA — live in seconds.90-Day Game PlanPhase-by-phase execution roadmap with tasks, KPIs, and revenue targets.Legal Framework KitBusiness structure recommendation + 6-category compliance checklist, downloadable as PDF.Marketing & Lead List5 marketing channels with ROI ratings, 5 sample leads with contact info, and outreach templates.

How It Works
1. Enter Idea       →  Describe your business in plain English
2. Validate         →  Answer 5 AI questions, receive a scored report
3. Build Offer      →  Answer 6 offer-shaping questions
4. AI Generation    →  4 parallel Claude API calls build your full kit (~60s)
5. Launch Dashboard →  Access all outputs — landing page, game plan, legal kit, leads

Tech Stack
LayerTechnologyFrontendNana Banana Pro, AntigravityAI / LLMAnthropic Claude API (claude-sonnet-4)Inference HardwareAMD Instinct MI300XCompute StackAMD ROCm 6.xCloud DeploymentKoyeb (AMD GPU instances)Frontend HostingVercelAsset StorageCloudflare R2AnalyticsPostHog

AMD Integration
Tailwind AI leverages AMD hardware throughout its inference pipeline:

AMD Instinct MI300X — 192 GB HBM3 memory handles 4 simultaneous large-context generation jobs per user session without bottlenecks
AMD ROCm 6.x — Open-source compute stack for running and fine-tuning domain-specific models (offer strategy, legal classification) at reduced cost
Koyeb AMD Cloud — MI300X-backed inference endpoints deliver sub-200ms time-to-first-token for real-time streaming UI


Prerequisites

Node.js 18+
Anthropic API key

Installation
bashgit clone https://github.com/midlane/tailwind-ai.git
cd tailwind-ai
npm install
Environment Variables
bashcp .env.example .env
envANTHROPIC_API_KEY=your_key_here
Run Locally
bashnpm run dev
Open http://localhost:3000
Deploy
bashnpm run build
vercel deploy

Project Structure
tailwind-ai/
├── src/
│   ├── components/
│   │   ├── IdeaScreen.jsx
│   │   ├── ValidationScreen.jsx
│   │   ├── OfferScreen.jsx
│   │   ├── GeneratingScreen.jsx
│   │   └── Dashboard/
│   │       ├── Overview.jsx
│   │       ├── LandingPage.jsx
│   │       ├── GamePlan.jsx
│   │       ├── Legal.jsx
│   │       └── Marketing.jsx
│   ├── utils/
│   │   └── claude.js        # Claude API helpers
│   └── App.jsx
├── public/
├── .env.example
└── README.md

Cost Estimate
ItemMonthlyAnnualAnthropic Claude API₹14,940₹1,79,280AMD ROCm cloud (Koyeb)₹9,960₹1,19,520Vercel Pro₹1,660₹19,920Cloudflare R2₹415₹4,980PostHog₹0₹0Domain + SSL₹166₹1,992Total₹27,141/mo₹3,25,692/yr

Break-even at ~500 users on a ₹1,577/month subscription plan.


Team
Team Midlane — AMD Slingshot 2025
Name                   RoleTeam Leader
Swastik Samal          Team Leader
Aadish Kaushik         Member
Vedhaanthh             Member
