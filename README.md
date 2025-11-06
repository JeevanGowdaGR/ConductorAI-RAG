ConductorAI-RAG

A Dynamic Multi-Agent AI Research Assistant built with LangGraph and LangChain
This repository implements a modular, LLM-powered multi-agent system for complex query workflows. Each agent specializes in a distinct role and is orchestrated by a Coordinator agent, enabling iterative reasoning, retrieval, critique and synthesis.

Overview
	•	Graph-based orchestration via LangGraph for flexibility and clarity in workflow routing. ￼
	  Multi-agent architecture including:
	•	Coordinator Agent: Evaluates the input query and chooses whether to answer directly or trigger a full workflow.
	•	Researcher Agent: Retrieves and structures knowledge from documents API, tools.
	•	Critic Agent: Validates research output, highlights gaps, bias and weaknesses.
	•	Writer Agent: Produces a polished response combining validated research.
	•	Conditional routing allows loops and deeper analysis when needed.
	•	Easy to extend: add new agents, tools, memory layers.
	•	Modular, deployable system suitable for AI-research assistants, domain-specific Q&A, knowledge-driven workflows.

Features
	•	Built with the latest LangGraph and LangChain APIs.
	•	Fully dynamic graph execution with conditional edges for adaptive workflows.
	•	Powered by OpenAI GPT-4o.
	•	Uses modern TypedDict structures for type-safe shared state management.
	•	Modular agents: Coordinator, Researcher, Critic, Writer.
	•	Customizable system prompts for each agent.
	•	Easily extendable to additional agents, tools, retrieval modules, memory layers.
	•	Clear logging and traceability of each agent’s role in the reasoning chain.


The system will:

  •	Start at the Coordinator Agent to analyze the query.
	•	Decide whether to return an immediate answer or trigger a full multi-agent workflow
	•	If needed, route the query through Researcher > Critic > Writer.
	•	Return to the Coordinator for another cycle or finalize the output.
	•	Output a complete, polished response.


##Project Structure
 ConductorAI-RAG/
 
|--main.py           # Main execution of script

|-- requirements.txt  # Python dependencies

|-- .env              # API key configuration

|-- README.md         # Documentation
