# 💭 Reflection: Game Glitch Investigator

Answer each question in 3 to 5 sentences. Be specific and honest about what actually happened while you worked. This is about your process, not trying to sound perfect.

## 1. What was broken when you started?

The game looked normal when it first loaded, but the hints were incorrect. When the secret number was 76 and I guessed 10, the game told me to go lower instead of higher. When I guessed numbers above 76, such as 80 and 99, it told me to go higher. This made the game impossible to play correctly.

**Bug Reproduction Log**

Document at least 3 bugs you found. Add rows as needed.
  
| Input | Expected Behavior | Actual Behavior | Console Output / Error |
|-------|-------------------|-----------------|------------------------|
| | | | |
| | | | |
| | | | |

---

## 2. How did you use AI as a teammate?

I used ChatGPT as my AI teammate. I described the bug I found and asked why the hints were incorrect. ChatGPT suggested that the comparison logic for the hints might be reversed, which matched the behavior I observed. I verified this by testing multiple guesses above and below the secret number.

---

## 3. Debugging and testing your fixes

I checked whether a bug was fixed by rerunning the game and repeating the same guesses. I used the Developer Debug Info section to compare my guesses to the secret number. If the hint matched the correct direction, I considered the bug fixed. AI helped me think of test cases to try.

I verified the fixes by running `python3 -m pytest`, and all 3 tests passed. I also ran the Streamlit app and tested guesses below and above the secret number to confirm the hints were correct. After that, I found another bug where New Game did not fully reset the game. I fixed it by resetting attempts, score, status, history, and the secret number.
---

## 4. What did you learn about Streamlit and state?

I learned that Streamlit reruns the script every time a user interacts with the app. Because of this, variables can reset unless they are stored in session state. Session state allows information such as attempts, scores, and the secret number to persist between interactions. This helps the game keep track of progress correctly.

---

## 5. Looking ahead: your developer habits

One habit I want to keep is documenting bugs before trying to fix them. Writing down the expected and actual behavior made debugging easier. Next time I work with AI, I will verify its suggestions with tests before trusting them. This project showed me that AI-generated code still needs careful testing and review.