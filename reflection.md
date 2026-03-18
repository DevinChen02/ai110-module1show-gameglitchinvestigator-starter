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
  I ran the game and tested the specific functionality that was related to the bug. For example, when I fixed the bug that the hints were not working correctly, I entered different guesses and checked if the hints were giving me the correct feedback (higher or lower). If the hints were consistent with the expected behavior based on my guesses, then I considered the bug to be fixed.
- Describe at least one test you ran (manual or using pytest)  
  and what it showed you about your code.
  I ran a manual test for the bug that the prompt in the input box did not update according to the difficulty level. I changed the difficulty level to easy mode and checked if the prompt updated to "Guess a number between 1 and 20". Then I changed it to hard mode and checked if the prompt updated to "Guess a number between 1 and 200". This test showed me that my code was not correctly updating the prompt based on the difficulty level, which indicated that there was still a bug in my code that I needed to fix.
- Did AI help you design or understand any tests? How?
  Yes, AI helped me design tests by suggesting specific scenarios to test based on the bugs I was trying to fix. For example, when I was trying to fix the bug with the hints, AI suggested that I test with guesses that are both higher and lower than the secret number to ensure that the hints are working correctly in all cases. This helped me understand the importance of testing different scenarios to fully verify that a bug is fixed.

---

## 4. What did you learn about Streamlit and state?

- How would you explain Streamlit "reruns" and session state to a friend who has never used Streamlit?
  Streamlit "reruns" means that every time you interact with the app (like clicking a button or changing a dropdown), Streamlit will rerun the entire script from top to bottom. This can cause issues if you have variables that are supposed to keep their values across interactions, because they will reset every time the script reruns. To solve this problem, Streamlit provides a feature called "session state", which allows you to store variables that persist across reruns. You can use session state to keep track of things like the secret number, the number of attempts left, or any other information that needs to be retained while the user interacts with the app.

---

## 5. Looking ahead: your developer habits

- What is one habit or strategy from this project that you want to reuse in future labs or projects?
  - This could be a testing habit, a prompting strategy, or a way you used Git.
  One habit that I want to reuse in future labs or projects is the practice of writing clear and specific prompts when asking AI for help. I found that when I provided detailed information about the issue I was facing and what I had already tried, I received more accurate and helpful suggestions from the AI. This habit of crafting well-thought-out prompts can save time and lead to better results when working with AI tools in the future.
- What is one thing you would do differently next time you work with AI on a coding task?
  One thing I would do differently next time is to be more critical of the AI's suggestions and not take them at face value. I realized that while AI can provide useful insights and code snippets, it can also make mistakes or suggest solutions that are not optimal for my specific use case. In the future, I will make sure to thoroughly review and test any AI-generated code before implementing it, and I will also consider multiple suggestions from the AI rather than relying on just one.
- In one or two sentences, describe how this project changed the way you think about AI generated code.
This project made me realize that AI-generated code can be a powerful tool for debugging and improving my code, but it is not infallible. It has taught me to approach AI suggestions with a critical eye and to always verify the results through testing, rather than blindly trusting the AI's output.
