# smart_easy_chat_bot

This chatbot runs using PyCharm and python 3.11, it learns by taking every answer and saves it into file: "knowledge_base.json"
then gains the ability to answer these questions if asked again. 

Bot Demo:

https://github.com/Inguzz15/smart_easy_chat_bot/assets/107085915/8d69afd6-0a00-4323-a531-51ba2e1ff8ab

This Python code defines a simple command-line chatbot that interacts with users to answer questions or learn new responses. Here's a summary of its main components and functionality:

1. Importing Libraries:
   - The code imports the `json` module for handling JSON files and the `get_close_matches` function from the `difflib` library for finding similar strings.

2. Constants:
   - It defines two constants:
     - `KNOWLEDGE_BASE_FILE`: The name of a JSON file where the chatbot's knowledge base is stored.
     - `CUTOFF_THRESHOLD`: A threshold value for string similarity when searching for the best match to a user's question.

3. Functions:
   - `load_knowledge_base(file_path: str) -> dict`: Loads the chatbot's knowledge base from a JSON file. If the file doesn't exist, it returns an empty knowledge base.

   - `save_knowledge_base(file_path: str, data: dict)`: Saves the knowledge base to a JSON file.

   - `find_best_match(user_question: str, questions: list[str]) -> str | None`: Finds the best match for a user's question in a list of known questions using string similarity. If a match is found above the cutoff threshold, it returns the best match; otherwise, it returns `None`.

   - `get_answer_for_question(question: str, knowledge_base: dict) -> str | None`: Retrieves the answer associated with a specific question from the knowledge base.

   - `chat_bot()`: The main function that drives the chatbot's interaction with the user. It loads the knowledge base, repeatedly takes user input, and responds accordingly. If the user enters "quit," the chatbot exits. If a similar question is found in the knowledge base, it provides the corresponding answer. If not, it prompts the user to provide an answer to the question and adds it to the knowledge base.

4. Main Execution:
   - The code begins by printing a welcome message.
   - It then calls the `chat_bot()` function to start the interaction.

In summary, this code implements a basic chatbot that can answer questions based on a knowledge base stored in a JSON file. It uses string similarity to find the best-matching question in the knowledge base and allows users to teach the chatbot new responses for questions it doesn't know.

