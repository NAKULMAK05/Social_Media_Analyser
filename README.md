## Social Media Analyzer Application 

This project demonstrates a workflow that integrates **Astra DB** with a chat-based interface to analyze social media data. It leverages tools like the **Groq API** to process user queries and generate insightful responses.<br/>   
 
 
You can also checkout the youtube video for detailed review  : https://youtu.be/HdfA5NL12KU?si=rCPU_4jkk9nL9iWc
<br/>   
### Workflow Overview   
   
1. **Astra DB Connection**:
    - **Purpose**: Establish a connection to the Astra DB instance and access the `Social_Media_Data` collection. 
    - **Components**:   
        - **Tool Name**: `data_insights`. 
        - **Tool Description**: Tool for generating insights from social media data. 
        - **Collection**: `Social_Media_Data`.
        - **Database**: `social_media_insights`.
        - **Astra DB Application Token**: Authentication token to securely access the database. 
        - **Tool Parameters**:
            - Parameter: `post_type` (to filter or specify data types).
 
2. **Chat Input**: 
    - **Purpose**: Capture the user query dynamically in natural language.
    - **Example Query**: `What is the maximum number of likes for a post?`. 

3. **Agent (Language Model Integration)**:
    - **Purpose**: Process user input using a language model to generate actionable instructions for querying the database.
    - **Details**:
        - **Language Model**: `Groq`.
        - **Model**: `gemma2-9b-it`.
        - **Agent Instructions**:
            - Example: `Extract the post type with the highest likes`.

4. **Tool Integration**: 
    - The agent sends the instructions to the Astra DB tool. 
    - The tool fetches the requested data from the specified collection and database.

5. **Output Generation**:
    - **Component**: Chat Output.
    - **Purpose**: Display the result of the query in a user-friendly manner.
    - Example Response: `The post type with the highest likes is "Image Post"`.

---

### Step-by-Step Process

1. **Configure Astra DB**:
   - Set up an Astra DB instance and load your social media data into the `Social_Media_Data` collection.
   - Obtain the Astra DB Application Token for secure access.

2. **Integrate Chat Input**:
   - Use the Chat Input component to allow users to input their queries.

3. **Setup Groq Agent**:
   - Configure the Groq API with appropriate models and instructions to process user queries.

4. **Define Tool Parameters**:
   - Pass parameters (e.g., `post_type`) to the Astra DB tool for focused data retrieval.

5. **Connect Workflow**:
   - Link the Chat Input, Astra DB tool, and Chat Output components via the Groq Agent.

6. **Generate Insights**:
   - Process the data and display the insights in the Chat Output.

---

### Technologies Used

- **Astra DB**: For managing and querying social media data.
- **Groq API**: For natural language processing and intelligent query handling.
- **Workflow Builder**: To design and connect the components visually.

### Installation and Setup

1. Clone the repository:
   ```bash
   git clone <repository-url>
   ```
2. Configure Astra DB:
   - Add your Astra DB Application Token in the tool configuration.
   - Specify your database and collection.
3. Configure Groq API:
   - Add your Groq API Key and select the desired model.
4. Run the workflow:
   - Use the visual builder to simulate or execute the workflow.

---

