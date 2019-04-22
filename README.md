

# ChatBot

This ChatBot is a machine-learning based conversational dialog engine build in
C which makes it possible to generate responses based on collections of
known conversations.


An example of typical input would be something like this:

> **user:** Good morning! How are you doing?  
> **bot:**  I am doing very well, thank you for asking.  
> **user:** You're welcome.  
> **bot:** Do you like hats?  

## How it works

An untrained instance of ChatterBot starts off with no knowledge of how to communicate. Each time a user enters a statement, the library saves the text that they entered and the text that the statement was in response to. As ChatterBot receives more input the number of responses that it can reply and the accuracy of each response in relation to the input statement increase. The program selects the closest matching response by searching for the closest matching known statement that matches the input, it then returns the most likely response to that statement based on how frequently each response is issued by the people the bot communicates with.





# Training data

ChatterBot comes with a data utility module that can be used to train chat bots.
At the moment there is training data for over a dozen languages in this module.
Contributions of additional training data or training data
in other languages would be greatly appreciated. Take a look at the data files
in the [chatterbot-corpus](https://github.com/gunthercox/chatterbot-corpus)
package if you are interested in contributing.

```
from chatterbot.trainers import ChatterBotCorpusTrainer

# Create a new trainer for the chatbot
trainer = ChatterBotCorpusTrainer(chatbot)

# Train based on the english corpus
trainer.train("chatterbot.corpus.english")

# Train based on english greetings corpus
trainer.train("chatterbot.corpus.english.greetings")

# Train based on the english conversations corpus
trainer.train("chatterbot.corpus.english.conversations")
```

**Corpus contributions are welcome! Please make a pull request.**



# History

See release notes for changes https://github.com/gunthercox/ChatterBot/releases

