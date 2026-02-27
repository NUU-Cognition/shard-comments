# Workflow: Respond to Comments

Read inline comments in a document, respond to each, and revise the document.

# Input

- Path to the document containing `%%...%%` comments

# Actions

## Stage 1: Extract Comments

1. Read the target document
2. Find all comments matching:
   - `%%? ...%%` — questions requiring answers
   - `%%...%%` — general comments requiring responses
3. List each comment with its context (surrounding text)

## Stage 2: Respond

1. For each comment, provide a response:
   - Questions (`%%?...%%`): Give a direct answer
   - Comments (`%%...%%`): Acknowledge or address the point
2. Present all responses to the user for review
3. Iterate based on user feedback until satisfied

## Stage 3: Revise Document

1. Replace each `%%...%%` block with the agreed response
2. Remove all `%%` markers
3. Ensure the responses flow naturally with surrounding text
4. Present the revised document for final confirmation

# Output

- Revised document with all comments resolved and markers removed
