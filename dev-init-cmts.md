# Comments Shard

A headless shard for inline document comments that agents can respond to.

## Syntax

| Pattern | Purpose |
|---------|---------|
| `%%comment%%` | General comment requiring a response |
| `%%? question%%` | Question requiring an answer |

## Usage

Add comments anywhere in a document using the `%%...%%` syntax. Then run the respond workflow to have the agent read, respond, and optionally revise the document.

## Workflow

- **respond** — Read all comments, respond to each, then revise document removing markers

## Example

Before:
```markdown
# My Document

This section explains the architecture. %%is this clear enough?%%

The system uses a pub/sub model. %%? what are the tradeoffs of this approach?%%
```

After running respond workflow:
```markdown
# My Document

This section explains the architecture. Yes, the explanation is clear and covers the key points.

The system uses a pub/sub model. The main tradeoffs are: pros include loose coupling and scalability; cons include eventual consistency and debugging complexity.
```
