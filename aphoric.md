# Aphoric Form

From aphorism — compact, sequential, one thought per line  

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

End non-heading lines with double space  
For markdown rendering  

## As example

This pattern is written in its own form  

---

## Example: technical reasoning

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

## Example: product design discourse

# Onboarding drop-off at team invite

## Completion data

60% of signups never finish setup  
The setup flow has 7 steps  
Completion correlates with step 3: "invite team"  

## Why "invite team" stalls users

Solo users see no value yet at step 3  
The product is collaborative but onboarding is solo  
Inviting a team is commitment before payoff  

## Reducing steps vs reducing friction

Cutting steps treats the symptom  
Users who complete all 7 retain well  
The 7 steps aren't the problem — the order might be  

## Reordering the flow around early value

Move value demonstration before team invite  
Let users see sample data, a populated workspace  
Invite becomes pull ("share this") not push ("add your team")  

Does sample data create false expectations?  
Do solo users ever convert to team use organically?  
We're guessing at motivation — instrument the funnel first  

## Possible move: A/B test reordered flow

Test reordered flow against current  
Measure completion rate and 7-day retention  
Hold off on cutting steps until data arrives  