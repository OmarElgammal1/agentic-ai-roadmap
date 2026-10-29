# Agentic AI Roadmap

The path I'd follow if I were learning to build AI agents from scratch today, from "what even is an agent" to running one in production.

**[View the roadmap →](https://omarelgammal1.github.io/agentic-ai-roadmap/)**

## Why I made this

When I started, the hard part wasn't finding resources. It was knowing which ones to skip and what order to do the rest in. This is my answer to that: one path, in order, with a small project at the end of most steps so you're building as you go.

Everything is free except two books in the last section, and those are clearly marked.

## The path

| Step | Topic | What's in it |
|------|-------|--------------|
| 01 | The mental model | Three short videos, then Anthropic's *Building Effective Agents*, Chip Huyen's *Agents* essay and Google's design pattern guide |
| 02 | A structured course *(optional)* | DeepLearning.AI or the Hugging Face Agents Course |
| 03 | LangGraph & Deep Agents | The freeCodeCamp LangGraph course, then LangChain's Deep Agents library |
| 04 | MCP & Agent Skills | The MCP docs, FastMCP, and how Agent Skills work |
| 05 | Tracing & evals | LangSmith (with Phoenix and Langfuse as open-source options), plus metrics like groundedness, relevance and coherence |
| 06 | Shipping it | FastAPI, Postgres/pgvector or MongoDB, Streamlit or Chainlit, Docker, and Azure or AWS |
| 07 | Safety & governance | Prompt injection, the OWASP lists, NIST AI RMF, and what governance looks like in practice |
| 08 | Two more frameworks | Pydantic AI and Agno |
| ·· | Visual builders *(optional)* | n8n and Langflow |
| ·· | Going further | CrewAI, framework comparisons, distributed systems, and two books worth buying |

## Building as you go

Most steps end with a "build it" task. Each task finishes with you writing an [Agent Skill](https://agentskills.io): a `SKILL.md` file that teaches a coding agent how to do what you just learned. By the end you have a set of skills you actually use, and writing them is a good way to check you understood the step.

The [`skills/`](skills/) folder has a template to start from and one worked example.

## Running it locally

It's one `index.html` file with no build step.

```bash
git clone https://github.com/omarelgammal1/agentic-ai-roadmap.git
```

Open `index.html` in a browser. To host your own copy, turn on GitHub Pages under Settings → Pages and point it at `main`.

## Contributing

If you find a dead link or know something that belongs here, open an issue or a PR. The bar: it should be free (or very clearly worth paying for), good, and still current.

## License

MIT

— [Omar Elgammal](https://github.com/omarelgammal1)
