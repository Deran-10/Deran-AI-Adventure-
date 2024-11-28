
```python
import nltk
from nltk.chat.util import Chat, reflections

# Define pairs of patterns and responses
pairs = [
    [
        r"my name is (.*)",
        ["Hello %1, how can I help you today?",]
    ],
    [
        r"hi|hello|hey",
        ["Hello!", "Hi there!",]
    ],
    [
        r"what is your name?",
        ["I am a chatbot created to assist you.",]
    ],
    [
        r"how are you?",
        ["I'm just a bunch of code, but thanks for asking!",]
    ],
    [
        r"(.*) (location|city) ?",
        ["I'm not sure where you are, but I hope it's nice!",]
    ],
    [
        r"quit",
        ["Bye! Take care!"]
    ],
]

# Create the chatbot
def chatbot():
    print("Hi! I'm a chatbot. Type 'quit' to exit.")
    chat = Chat(pairs, reflections)
    chat.converse()

# Start the chatbot
if __name__ == "__main__":
    chatbot()
```
