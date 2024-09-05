The LangChain Summarizer is a Streamlit application designed to extract and summarize text content from YouTube videos and web pages. 
Leveraging the powerful capabilities of the LangChain framework and Groq's ChatGroq model, this tool provides users with concise summaries, making it easier to grasp essential information quickly.

Features:

User Interface:

A user-friendly Streamlit interface allows users to enter a URL from either YouTube or a website.
The sidebar provides a secure input for the Groq API key, essential for accessing the ChatGroq model.
Input Validation:

The application includes input validation to ensure that the API key and URL are correctly provided and formatted.
Users are prompted with error messages if inputs are missing or invalid, guiding them to correct their entries.
Content Loading:

For YouTube URLs, the YoutubeLoader from LangChain Community is used to fetch and process video content.
For web URLs, the UnstructuredURLLoader is employed to handle text extraction from web pages, including the necessary headers for proper content retrieval.
Text Summarization:

The application utilizes the ChatGroq model with the Llama3-8b-8192 configuration to generate summaries.
The PromptTemplate defines the structure for the summarization task, instructing the model to condense the content into a 500-word summary.
Error Handling:

Comprehensive error handling ensures that users are informed of any issues encountered during the summarization process, maintaining a smooth user experience.
How It Works:

Users enter the Groq API key and URL into the Streamlit app.
Upon pressing the "Summarize the Content from YT or Website" button, the app validates the inputs.
If valid, the app loads content from the provided URL using the appropriate loader based on the URL type (YouTube or web).
The loaded content is then processed by the ChatGroq model to generate a summary.
The summary is displayed to the user, providing a concise overview of the original content.
