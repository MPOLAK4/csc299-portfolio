# Reflection

## In the project you developed further, what did a fresh session get wrong or ask about that an earlier round had already settled? What was missing from the repository that would have prevented it?

I had claude.md prompt setup to use pytest; README.md instead asked for unittest, round 1's attempt for the web app wireframe model had to ask me which implementation was preferred due to the conflict.


## In the round that changed an earlier requirement, what broke? Did the tests catch it, and does the decision record explain the change to someone who was not there?

Didn't recall any round doing any changes to the requirement. The decision didn't record anything regarding the change.


## Name one test that caught a real problem, or one test the assistant wrote that checked nothing useful. Quote it.

Didn't recall any round doing any changes to the requirement. Some test kept breaking due to the bug involving server return type (404 VS 405 response).


## Choose one commit you would now write differently, and say how.

In hindsight, 5b4ccd9 was something that should've been remade to be more descriptive; "Round 6 + claude" doesn't translate into a CLAUDE.md and handoff change.


## Choose one function in the project you developed further that you did not read while building it. Without an assistant open, read it and write what you think it does, in two or three sentences. Then ask an assistant, and say what you got right and wrong.


Doublechecked "standin(key)", based off of a required feature I requested, this effectively replaces a code variable access (user.key) with a standin that is more suitable for being viewed in the wireframe viewer for evaluation (user.key => [the user's key, localized])

I'm not proficient with regex so I didn't understood it, but just enough to know that ``re`` is the python library for regex. This specific code takes whatever was detected by the regex, then strips it from the key, then sets words to key. 

AI model explained it further by giving an explanation of the regex scope; it seeks to remove the . - _ of a key to translate it into readable text, I probably would've preferred that it used a key-value localization hash table to do this rather than just simple regex, albeit still works.



