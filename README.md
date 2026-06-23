# 🎮 Game Glitch Investigator: The Impossible Guesser

## 🚨 The Situation

You asked an AI to build a simple "Number Guessing Game" using Streamlit.
It wrote the code, ran away, and now the game is unplayable. 

- You can't win.
- The hints lie to you.
- The secret number seems to have commitment issues.

## 🛠️ Setup

1. Install dependencies: `pip install -r requirements.txt`
2. Run the broken app: `python -m streamlit run app.py`

## 🕵️‍♂️ Your Mission

1. **Play the game.** Open the "Developer Debug Info" tab in the app to see the secret number. Try to win.
2. **Find the State Bug.** Why does the secret number change every time you click "Submit"? Ask ChatGPT: *"How do I keep a variable from resetting in Streamlit when I click a button?"*
3. **Fix the Logic.** The hints ("Higher/Lower") are wrong. Fix them.
4. **Refactor & Test.** - Move the logic into `logic_utils.py`.
   - Run `pytest` in your terminal.
   - Keep fixing until all tests pass!

## 📝 Document Your Experience

- [x] The game is a Streamlit number guessing game where the player tries to guess a secret number.
- [x] I found bugs where the hints were reversed, the secret number was changed into a string, and the New Game button did not fully reset the game.
- [x] I fixed the hint logic, refactored the logic into `logic_utils.py`, removed the string conversion bug, and reset the game state correctly.

## 📸 Demo Walkthrough

1. The game starts with a random secret number.
2. The user enters a guess that is too low.
3. The game responds with "GO HIGHER!"
4. The user enters a guess that is too high.
5. The game responds with "GO LOWER!"
6. The user enters the correct guess.
7. The game displays a win message and final score.
8. The user clicks "New Game" and the game resets correctly.

**Screenshot** *(optional)*: <!-- Insert a screenshot of your fixed, winning game here -->

## 🧪 Test Results

```text
============================== 3 passed ==============================

