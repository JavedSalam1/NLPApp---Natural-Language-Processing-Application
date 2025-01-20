# NLPApp---Natural-Language-Processing-Application
This Python-based app lets users perform NLP tasks like:  Sentiment Analysis: Detect emotions using pre-trained models from NLPCloud. User Authentication: Secure login and registration.
NLPApp - Natural Language Processing Application
This is an interactive Python application that allows users to perform various Natural Language Processing (NLP) tasks, such as Named Entity Recognition (NER), Language Detection, and Sentiment Analysis. The application uses the nlpcloud API for NLP tasks and stores user credentials in an in-memory database.

Features
User Authentication:
Users can register or log in to the application.
Registration requires a name, email, and password.
Login requires a registered email and password.
NLP Tasks:
Named Entity Recognition (NER): (Currently not implemented in the provided code but can be added later).
Language Detection: (Feature can be added later).
Sentiment Analysis: Uses a pre-trained sentiment analysis model to analyze text and detect emotions.
Exit Option: Users can exit the application at any time.
Getting Started
Prerequisites
To run this application, you need to have Python 3.x installed. You also need to install the nlpcloud library and other dependencies.

Install dependencies: In your terminal, run:

bash
Copy
Edit
pip install nlpcloud emoji
Ensure you have a valid nlpcloud API key: You will need to replace the API key used in the code ("2b58d7fb9af09e617ee525e78c7766b6d8c5bb61") with your own API key from nlpcloud.io.

Running the Application
Once all dependencies are installed, you can run the application by simply executing the NLPApp class. In your terminal, navigate to the folder containing the nlp_app.py file and run:

bash
Copy
Edit
python nlp_app.py
You will be prompted to register or log in. After successfully logging in, you can go ahead and use the available NLP tasks.

Using the Application
Register:

Choose 1 to register a new user.
Enter your name, email, and password. (Email is used as the username).
Login:

Choose 2 to login with an existing account.
Enter your registered email and password.
Perform NLP Tasks:

After successful login, choose from the following tasks:
1: NER (Not implemented yet)
2: Language Detection (Can be added later)
3: Sentiment Analysis (Current feature)
Enter a paragraph, and the app will analyze the sentiment of the text.
The app uses the distilbert-base-uncased-emotion model from nlpcloud to determine the emotion in the text.
Exit: If you wish to exit, you can simply choose option 3 on any menu.

Code Explanation
Class: NLPApp: The main class that handles user authentication and NLP tasks.

Methods:

__init__(self): Initializes the app and prompts the first menu for registration/login.
__first_menu(self): Prompts the user to choose to register, login, or exit.
__second_menu(self): Prompts the user to choose from NLP tasks (NER, Language Detection, Sentiment Analysis).
__register(self): Registers a new user by adding them to the __database dictionary.
__login(self): Logs an existing user in by verifying their credentials.
__sentiment_analysis(self): Performs sentiment analysis using the nlpcloud API.
Sentiment Analysis:

The sentiment analysis is powered by the nlpcloud API.
After the user inputs a paragraph, the app uses the "distilbert-base-uncased-emotion" model to predict the sentiment of the text.
It ranks emotions and returns the most likely emotion based on the input.
Emoji Support:

The app supports displaying emojis using the emoji library. This can be useful when adding or displaying emotive text.
Example Output
Menu Example:
css
Copy
Edit
Hi! how would you like to proceed?
1. Not a member? Register
2. Already a member? Login
3. Galti se aa gaye? Exit
Login Example:
yaml
Copy
Edit
enter email: test@example.com
enter password: password123
login successful
Sentiment Analysis Example:
vb net
Copy
Edit
enter the paragraph: I love programming, it's so much fun!
Emotion: Joy
Future Improvements
NER (Named Entity Recognition): Add functionality to perform NER using a pre-trained model.
Language Detection: Integrate a language detection model to identify the language of the input text.
User Data Persistence: Instead of storing user data in memory (lost after the program exits), store user data in a database (e.g., SQLite or JSON file) for persistence.
