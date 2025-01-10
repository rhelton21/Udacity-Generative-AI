# HomeMatch Application
HomeMatch is an innovative application developed for "Future Homes Realty." It leverages Large Language Models (LLMs) and vector databases to personalize real estate listings for potential buyers based on their preferences.

## Features
1. **Generate Listings**:
   - Uses a Large Language Model (LLM) to create synthetic real estate listings with details such as neighborhood, price, bedrooms, bathrooms, and a descriptive summary.
2. **Store Listings in a Vector Database**:
   - Converts listings into vector embeddings and stores them in a vector database (using ChromaDB).
3. **Parse Buyer Preferences**:
   - Accepts buyer preferences in natural language and structures them into a query format for effective searching.
4. **Semantic Search**:
   - Matches listings with buyer preferences using semantic embeddings, ensuring relevant results based on user input.
5. **Personalized Descriptions**:
   - Enhances listings by highlighting specific property features that align with buyer preferences, ensuring factual accuracy.
6. **Comprehensive Testing and Debugging**:
   - Implements detailed logging and debugging to track each step of the workflow.
7. **End-to-End Workflow**:
   - Integrates all steps into a seamless pipeline for generating, storing, searching, and displaying personalized listings.

## Prerequisites
- Python 3.7 or above
- Installed packages:
  - `langchain`
  - `openai`
  - `chromadb`
  - `pandas`
  - `numpy`
  - `tenacity` (for retry mechanisms)
- OpenAI API Key (for GPT functionality)

## How to Run the Code
1. Clone or download the project repository.
2. Navigate to the project directory and install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Set up environment variables for OpenAI API access:
   ```bash
   export OPENAI_API_KEY="your_openai_api_key"
   ```

4. Open the Jupyter Notebook or Python script:
   - Run the notebook cells sequentially, starting from Step 1 (Setting up the environment).

## Project Steps
1. **Step 1: Setting Up the Python Application**
   - Initializes the environment and imports necessary libraries.
   - Connects to the vector database (ChromaDB).
2. **Step 2: Generating Real Estate Listings**
   - Generates 10 diverse and realistic real estate listings using GPT-based prompts.
   - Each listing includes a neighborhood description, price, number of rooms, and unique features.
3. **Step 3: Storing Listings in ChromaDB**
   - Embeds the listing descriptions into 300-dimensional vectors.
   - Stores the embeddings in ChromaDB with metadata for querying.
4. **Step 4: Collecting Buyer Preferences**
   - Collects user preferences such as location, property type, features, and lifestyle.
   - Parses the preferences into structured input for semantic search.
5. **Step 5: Searching Based on Preferences**
   - Performs semantic searches using the vector database.
   - Retrieves listings that match the buyer’s requirements based on the closeness of embeddings.
6. **Step 6: Personalizing Listing Descriptions**
   - Uses an LLM to tailor listing descriptions to emphasize features relevant to the buyer.
   - Maintains factual integrity while making descriptions more engaging.
7. **Step 7: Testing and Debugging**
   - Includes robust logging at each step to identify errors or gaps.
   - Example outputs show how user preferences influence listing generation and personalization.

## Example Output
- Example 1:
  **Input Preferences:**
  - Property Type: House
  - Bedrooms: 3
  - Neighborhood: Quiet
  - Feature: Backyard
  **Generated Listing:**
  - *"Welcome to this charming 3-bedroom house nestled in a serene, family-friendly neighborhood with a spacious backyard perfect for relaxation."*

## Optional Extensions
- Add CLIP-based multimodal capabilities to incorporate image-based embeddings for richer, visual property matching.
- Implement more diverse datasets for synthetic listing generation to expand property features and geographic variety.

## Notes
- Ensure that you have a valid OpenAI API key and sufficient usage quota to run the LLM-based tasks.
- You can modify the prompts in the listing generation step to customize the style or tone of the descriptions.

## Troubleshooting
- **Model Deprecation Issue:** If you encounter an error like `The model text-davinci-003 is deprecated`, switch to newer models such as `gpt-3.5-turbo` or `gpt-4`.
- **ChromaDB Connection Errors:** Ensure ChromaDB is installed and that dependencies are properly set up.

## Deliverables
- **Generated Listings File:** A file containing at least 10 synthetically generated listings.
- **Documentation:** A README file with instructions on how to run the code and interpret the output.
- **Submission:** Submit the notebook along with generated listings and the README in a zip file.

By following this guide, you can ensure the "HomeMatch" application is fully functional and meets all requirements for personalized real estate matching.
