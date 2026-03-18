# 💭 Reflection: Game Glitch Investigator

Answer each question in 3 to 5 sentences. Be specific and honest about what actually happened while you worked. This is about your process, not trying to sound perfect.

## 1. What was broken when you started?

- What did the game look like the first time you ran it?
  When I ran the game, there is a setting menu on the left that allows me to choose the difficulty level (easy, normal, hard). On the right side of the web page, I can play the game "Make a guess". There is a dropdown menu called "Developer Debug Info" keeping track of the history and my score. I can enter any number in the input box, click "Submit Guess", "New Game", or "Show hint". On the top right corner, I can click on three dots symbol to change the setting like theme color.

- List at least two concrete bugs you noticed at the start  
  (for example: "the hints were backwards").
  1.When I play normal mode (1 to 100), I enter 50, the hint says "GO HIGHER", then I enter 100, the hints still says "GO HIGHER" while 100 is already the highest number. It seems that the hints are not working correctly.
  2.When I change the difficulty level to easy mode, the prompt in the blus box still says "Guess a number between 1 and 100" instead of "Guess a number between 1 and 20". This bug also exists when I changed the difficulty to Hard.
  3.After I used all the attempts and I clicked "New Game", the game should be reset, but then I type in my guess and clicked "Submit Guess", the hint still says "Game Over" and the hint did not update to the new guess. 
---

## 2. How did you use AI as a teammate?

- Which AI tools did you use on this project (for example: ChatGPT, Gemini, Copilot)?
  I used VS Code Copilot.
- Give one example of an AI suggestion that was correct (including what the AI suggested and how you verified the result).
  When I was trying to fix the bug that the hints were not working correctly, I asked Copilot "How to fix the hint in the number guessing game?" Then it suggested me to check the logic of the hint and make sure it is comparing the guess with the secret number correctly. I verified the result by testing the game after I made the changes, and I found that the hints were working correctly now.

- Give one example of an AI suggestion that was incorrect or misleading (including what the AI suggested and how you verified the result).
  When I was trying to fix the bug that the prompt in the input box did not update according to the difficulty level, I asked Copilot "How to update the prompt in the input box according to the difficulty level?" Then it suggested me to use an if statement to check the difficulty level and update the prompt accordingly. However, this suggestion was incorrect because it did not take into account the fact that the prompt should be updated every time the difficulty level changes, not just when the game starts. I verified the result by testing the game after I made the changes, and I found that the prompt still did not update correctly when I changed the difficulty level.

---

## 3. Debugging and testing your fixes

- How did you decide whether a bug was really fixed?
- Describe at least one test you ran (manual or using pytest)  
  and what it showed you about your code.
- Did AI help you design or understand any tests? How?

---

## 4. What did you learn about Streamlit and state?

- How would you explain Streamlit "reruns" and session state to a friend who has never used Streamlit?

---

## 5. Looking ahead: your developer habits

- What is one habit or strategy from this project that you want to reuse in future labs or projects?
  - This could be a testing habit, a prompting strategy, or a way you used Git.
- What is one thing you would do differently next time you work with AI on a coding task?
- In one or two sentences, describe how this project changed the way you think about AI generated code.
