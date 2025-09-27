Professor Recommendation Agent
This project implements an agent to assist prospective graduate students in finding potential professors based on their research interests and application qualifications. The agent utilizes data scraped from a public spreadsheet containing information about university faculty, their research interests, application requirements, and contact details.

Data Source
The data used in this project is sourced from a Google Spreadsheet: https://docs.google.com/spreadsheets/d/1vcEUT_5bXYFQgIzVKpsMQlYmV2xv15VtLXq2rvXZqRk/edit?gid=0#gid=0

The code first loads this data into a pandas DataFrame.

Functionalities
The integrated agent combines the following functionalities:

Professor Recommendation: Matches user-provided research interests with the 'Research Interests' of professors in the dataset using TF-IDF vectorization and cosine similarity.
Application Requirements Check: Checks if a professor's stated requirements are met by a user's qualifications.
Contact Strategy: Extracts and presents the preferred method of contact and homepage for the recommended professors.
Implementation Details
Data Loading and Preprocessing: The data is loaded from the Google Spreadsheet. Relevant columns ('Research Interests', 'Requirements', 'How to Reach out') are cleaned by handling missing values, converting to lowercase, and removing whitespace.
Research Interest Matching: TF-IDF (Term Frequency-Inverse Document Frequency) is used to vectorize the research interests. Cosine similarity is then calculated between the user's interests and the professors' interests to find the most similar matches.
Requirements Check: A basic function is implemented to check if key requirements mentioned by a professor are met by the user's qualifications. This part can be extended for more sophisticated parsing and matching.
Contact Strategy: The agent retrieves the 'How to Reach out' and 'Homepage' information for the recommended professors.
Integrated Agent: A main function professor_agent orchestrates the above functionalities, taking user interests and qualifications as input and printing the recommendations, requirements status, and contact information.
How to Use
Ensure you have the necessary libraries installed (pandas, scikit-learn).
Run the code cells in the notebook sequentially to load data, preprocess it, and define the matching and agent functions.
Provide your research interests as a string and your application qualifications as a dictionary to the professor_agent function.
The agent will print the top recommended professors, whether you meet their listed requirements (based on the simplified check), and how to contact them.# PhD-RA-Interns-Opening-2026-data-science-project--agent
