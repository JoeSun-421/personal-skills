# Source Reading and Recipe Fidelity

## Source Record

For each main paper, retain its title, authors, original release, fixed version, primary link and the method/appendix locations used. Keep the record outside the article when it would interrupt reading. Verify versions rather than mixing older numerical results with newer mechanisms.

## Reconstruct the Actual Recipe

Read these questions as an evidence checklist, not headings to copy into the article:

- What state or history is available at the decision point?
- What does the model generate, and what actually executes?
- Which parameters are frozen and which receive updates?
- How are data, labels, successful trajectories and negative examples obtained?
- Does scoring use a fixed reference action, a new sampled continuation or an environment rerun?
- What is the reward, its unit, and the time at which it becomes available?
- Over which queries, trajectories, steps, modes or tokens are statistics calculated?
- Which tokens enter policy loss, closure supervision or value learning?
- Does the method use a critic and GAE, group-relative advantages, supervised classification, or no training?
- Is cross-segment credit exact or approximate?

Preserve source distinctions such as allocated budget versus consumed tokens, action likelihood versus execution success, summary generation versus answer generation from a provided prefix, and original token positions versus loss normalization counts.

## Evidence and Costs

Identify the matched comparison and what it supports: bounded context, task quality, token use, FLOPs, training throughput, request latency, or complete task time. Keep estimates separate from measurements. Include routers, probes, summaries, rejected drafts, repairs and retries within the relevant cost boundary.

Method names and acceptance status do not establish resource efficiency. If a context manager explicitly increases wall time, describe it as context/quality evidence and do not promote it as demonstrated acceleration. State the benchmark and model scope of measured gains.

## Paragraph-Level Review

A paper section should let the reader reconstruct the operation order without reading a generic RL tutorial. Use a method figure near the data flow and an evidence figure near the result. Keep experimental facts separate from transfer design. Put target-domain adaptations in the requested final section.

## Template Provenance

This personal pattern was distilled from an annotated Markdown review: target-system motivation, a numbered mechanism map, grouped original-paper explanations, source-critical RL formulas, clean original figures, and one final robot-use discussion. Topic names, particular papers, counts and algorithms remain replaceable by the user's current instructions.
