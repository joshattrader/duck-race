# Duck Race

## Prompt

```txt
  THE JOB
  Build a duck race game as a single self-contained index.html in this folder. The team enters duck names, the ducks race, and the finishing order is shown as the result.

  THE WHY
  I'm building this for my team's daily standup. We screen-share it to pick a random, fair speaking order, so it has to be quick to run every day, readable over a screen share, and fun enough to
  watch for 10 seconds.

  HOW IT SHOULD WORK
  - Setup screen: a textarea with one duck name per line, prefilled from the last roster saved in localStorage. Ignore blank lines, trimwhitespace, and handle duplicate names so no two ducks
  look identical. Support about 2–20 ducks, and block Start Race with a clear message if there are fewer than 2.
  - Start Race: save the roster, create one lane per duck, show a 3-2-1 countdown, then run the race for exactly 5 seconds.
  - Fairness: pick the finishing order with an unbiased shuffle (Fisher–Yates with crypto.getRandomValues) before the race starts. This decides who speaks first, so every order must be equally
  likely.
  - Race feel: each duck gets a varied pace curve, so positions visibly swap during the race while still ending in the pre-chosen order and crossing the line by the 5-second mark. Show each
  duck's progress continuously all the way to the finish.
  - Results: a large numbered list from 1st to last (this is the speaking order), confetti on the winner, and a "Copy order" button thatcopies the list as plain text for Slack or Teams.
  - Race Again reruns with the same names and a new random order. Setup Race goes back to the setup screen with the names still filled in.
  - Visuals: simple inline SVG ducks, each a distinct color with its name on it, in water lanes with a clear finish line. Size text and lanes so they stay legible on a shared screen with up to
  20 ducks.

  THE GUARDRAILS
  - Keep it to one index.html with inline CSS and JS, and no external libraries, CDNs or build step. It has to work by double-clicking the file or dropping it on any static host.
  - Wrap localStorage access in try/catch so the game still works when storage is blocked. It just won't remember names.
  - Make routine design and implementation calls yourself. Ask me only if something in this spec contradicts itself.

  DONE MEANS
  - Opening index.html in a browser runs the full flow (setup → countdown → 5 s race → results → Race Again / Setup Race) with no console errors.
  - Race Again produces different orders across runs, and the finish order always matches the displayed results.
  - When you finish, tell me the file path and give me 3 short bullets on how the race animation and the randomness work. Nothing more.

  Before reporting progress, audit each claim against a tool result from this session. Only report work you can point to evidence for; if something is not yet verified, say so explicitly. Report
  outcomes faithfully: if tests fail, say so with the output; if a step was skipped, say that; when something is done and verified, state it plainly without hedging.
```
