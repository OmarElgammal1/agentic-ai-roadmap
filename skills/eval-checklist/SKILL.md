---
name: eval-checklist
description: Use before calling any change to an agent's prompt, tools, model or retrieval "done". Runs the agent against its eval dataset in LangSmith and compares the scores to the last good run.
---

# Eval checklist

## When to use this

Any change that could affect what the agent says or does: prompt edits, new or changed tools, switching models, changing chunking or retrieval. You can skip it for pure refactors that don't touch the agent, like logging or config plumbing.

## Steps

1. **Make sure the dataset is still representative.** It should have at least 20 examples taken from real usage, not invented ones. If the change adds a new capability, add 3–5 examples that cover it first.
2. **Run the evaluation** against the dataset in LangSmith with these evaluators:
   - **Groundedness**: is every claim supported by the retrieved context or tool output?
   - **Relevance**: does the answer address the question?
   - **Tool use**: for examples with an expected tool call, did it call the right tool with sensible arguments?
3. **Compare with the last good run** (the experiment tagged `baseline`).
   - If groundedness drops by more than 5 points, stop. That usually means the prompt is encouraging the model to answer without sources.
   - If relevance drops, read the 3 lowest-scoring traces before changing anything else.
4. **Read at least 5 traces by hand**, including at least one that passed. Scores miss things like the agent making a pointless extra tool call.
5. **If it's better or the same**, tag the new experiment as `baseline` and note what changed in the commit message.

## Gotchas

- LLM-as-judge scores vary from run to run. Don't react to a 1–2 point change. Run it twice if you're unsure.
- If the judge and the agent use the same model, the judge tends to go easy on it. Use a different model for judging where you can.
- A rising score on a dataset that hasn't changed in months is a warning sign. You might be overfitting to it, so add fresh examples.

## Reference

- LangSmith evaluation docs: https://docs.langchain.com/langsmith/home
- Metric definitions: https://learn.microsoft.com/en-us/azure/ai-foundry/concepts/evaluation-evaluators/rag-evaluators
