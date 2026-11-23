# multiAgent
Agentic AI: From Zero to Build with Google ADK

A hands-on, one-hour workshop notebook for building agents with Google's Agent Development Kit (ADK). You start with a model that can only talk and finish with a multi-agent system that calls your own tools, searches the web, remembers context, enforces guardrails, and is measured by an eval suite.

Open In Colab

What you build
Part	Topic	You build
0	Setup	Install ADK, wire an API key
1	The agent loop	Your first LlmAgent and a run harness
2	Tools	Python functions the model can call
3	Built-in tools	Grounded answers with google_search
4	Sessions, state, memory	An agent that remembers
5	Structured output	Typed results with Pydantic
6	Multi-agent	Delegation via sub_agents and AgentTool
7	Orchestration	A deterministic Workflow graph
8	Guardrails	Callbacks that intercept the model and tools
9	Evaluation	An eval set you can run in CI
10	Capstone	One agent that uses all of it

Deployment is intentionally out of scope.

Quick start (Google Colab)
Click the Open in Colab badge above.
Get a free API key at https://aistudio.google.com/apikey.
In Colab, open the key icon in the left sidebar, add a secret named GOOGLE_API_KEY, and enable notebook access.
Run the notebook top to bottom.
Run locally
bash
git clone https://github.com/akajammythakkar/agentic-ai-google-adk.git
cd agentic-ai-google-adk
python -m venv .venv && source .venv/bin/activate   # Windows: .venv\Scripts\activate
pip install -r requirements.txt
pip install jupyterlab
jupyter lab

When prompted for GOOGLE_API_KEY, paste your key, or export it first:

bash
export GOOGLE_API_KEY="your_key_here"

Never commit your key. .env files are git-ignored; use .env.example as a template.

Notes
Rate limits. The Gemini free tier has low per-minute quotas. If you see 429 RESOURCE_EXHAUSTED, wait about 30 seconds or set MODEL = "gemini-3.5-flash-lite" in Part 0.
Version. Tested with google-adk==2.7.1. ADK moves quickly, so the pin avoids surprises.
Generated files. Part 9 creates shop_app/ and eval/ at runtime. They are git-ignored, and the notebook can recreate them.
Outputs are cleared. Run the notebook to see results.
Resources
ADK docs: https://google.github.io/adk-docs/
ADK on GitHub: https://github.com/google/adk-python
ADK samples: https://github.com/google/adk-samples
License

MIT. See LICENSE.
