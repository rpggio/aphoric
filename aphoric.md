# Aphoric Form

From aphorism — compact, sequential, one thought per line  
High-context, for communicating with humans  
Not for agent-targed prose  

## Line

One line, one thought  
No compound claims  
No connective filler  
Density is a goal, not a constraint  

## Stanza

One focus per stanza  
Break when focus shifts  
Stanzas stand alone and compose  

## Titles

Name what you're thinking about, not what you're doing  
Titles must identify their own context  
A reader scanning titles alone should follow the thread  

Two levels: chapters and sections  
A section may contain one stanza or several  
Not every stanza needs a title  

## Sequence

Each line relates to its neighbors  
Juxtaposition and accumulation both valid  
Order implies relation  
Omit transitions  

## Epistemic state

Hedges mark uncertainty  
Questions mark open tension  
When a question is genuinely unresolved, leave it unresolved  
Don't paper over epistemic tension with false conclusions  

## Density

Every word earns its place  
Cut adjectives first, then linking verbs  
Nouns and verbs carry weight  
Compact, not compressed — lines vary in length  

## Line feeds

Use double space to delimit lines  
To prevent collapse in rendered markdown

## As example

This pattern is written in its own form  

---

## Example

```
# Auth token refresh race in PR #4412

## Bug report: 401s after idle sessions

Token refresh fires on 15-min interval  
Refresh endpoint is not idempotent  
Two users report spurious 401s  

## Multi-tab race condition

Tab A refreshes, succeeds, rotates the token  
Tab B refreshes simultaneously with the stale token  
Server rejects — token already rotated  

## Fix options: client vs server

Mutex the refresh per-tab — only fixes single-tab  
BroadcastChannel for cross-tab — Safari 14 lacks it  
Make refresh idempotent server-side  

Server-side idempotency absorbs the most risk  
Client complexity stays flat  
Need buy-in from platform team  
Draft RFC or just start the conversation?  
```
