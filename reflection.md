# 💭 Reflection: Game Glitch Investigator

Answer each question in 3 to 5 sentences. Be specific and honest about what actually happened while you worked. This is about your process, not trying to sound perfect.

## 1. What was broken when you started?

- What did the game look like the first time you ran it?
It showed up as a buggy looking website with my secret number being 53. I chose a number higher than it and it told me to go higher while simultanesly chose a number lower and it said go lower
- List at least two concrete bugs you noticed at the start  
  (for example: "the hints were backwards").
Hint directions are reversed
- Guess above the secret → game says go higher.
- Guess below the secret → game says go lower.

History does not clear when starting a New Game
- Expected: a new game should start with an empty guess history.
- Actual: guesses from the previous game remain.

New Game generates a secret outside the selected difficulty range
- Expected: the new secret should stay inside that difficulty’s displayed range.
- Actual: the new secret can fall outside that range.

**Bug Reproduction Log**

Document at least 3 bugs you found. Add rows as needed.

| Input | Expected Behavior | Actual Behavior | Console Output / Error |
|-------|-------------------|-----------------|------------------------|
| | | | |
| | | | |
| | | | |
| Input | Expected Behavior | Actual Behavior | Console Output / Error |
|-------|-------------------|-----------------|------------------------|
| Guess higher/lower than the secret number | A high guess should tell me to go lower, and a low guess should tell me to go higher | The hint directions were reversed | No console error |
| Click New Game after making guesses | Guess history should clear for the new game | Previous guesses remained in History | No console error |
| Click New Game while using a difficulty with a limited range | New secret number should stay inside the selected difficulty range | New secret number was generated outside the difficulty range | No console error |


---

## 2. How did you use AI as a teammate?

- Which AI tools did you use on this project (for example: ChatGPT, Gemini, Copilot)?
- Give one example of an AI suggestion that was correct (including what the AI suggested and how you verified the result).
- Give one example of an AI suggestion you did not accept as written (including what the AI suggested, why you rejected or changed it, and how you verified your version). It does not have to be a suggestion that was wrong: over-engineered, out of scope, harder to read, or a poor fit for this codebase all count.

---

## 3. Debugging and testing your fixes

- How did you decide whether a bug was really fixed?
if it worked as i wanted it to
- Describe at least one test you ran (manual or using pytest)  
  and what it showed you about your code.
  pytest
- Did AI help you design or understand any tests? How?
yes, just describing what terminolgy meant
---

## 4. What did you learn about Streamlit and state?

- How would you explain Streamlit "reruns" and session state to a friend who has never used Streamlit?
Streamlit reruns the Python script from top to bottom whenever the user interacts with the app, such as clicking a button or entering a guess. Because the script reruns, normal variables can be recreated or reset each time. Session state is a way to save important values, like the secret number, score, attempts, or guess history, so they stay available between reruns. I would describe it like the app is restarting its instructions after every interaction, while session state acts like a small memory box that keeps track of the information the game still needs.
---

## 5. Looking ahead: your developer habits

- What is one habit or strategy from this project that you want to reuse in future labs or projects?
make sure I read all direction
  - This could be a testing habit, a prompting strategy, or a way you used Git.
- What is one thing you would do differently next time you work with AI on a coding task?
nothing
- In one or two sentences, describe how this project changed the way you think about AI generated code.
I realized that using ai can completely mess up thee code
