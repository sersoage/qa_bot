# QA BOT

* Support for loading documents from local data sources and web urls
* Support for persona and message tone
* AI qa limited to knowledge sources
* Text splitting to optimize indexing and similarity search
* NLTK support for text processing and tokenization
Support for OpenAI embeddings and vector stores, including Chroma
* Logging support for troubleshooting and analysis
* TODO PERSIST DB

## Configuration

Before you can use the utility, you need to set up the configuration file. The configuration file is a YAML file that contains the following options:

* openai_api_key: Your OpenAI API key.
* data_directory: The directory where your local data sources are located.
* data_files_glob: A glob pattern that specifies which files in data_directory to use as data sources.
* webpages: A list of URLs of webpages to use as data sources.
* tone: The tone to use for the chatbot's responses (e.g., "formal", "informal", "friendly", etc.).
* persona: The persona to use for the chatbot.
* You can copy the config.example.yaml file to config.yaml and modify the options as needed.

## Getting Started
To use this utility:
```
2. Build the Docker image by running the following command in the terminal:
```
docker build -t qa_chat_web:latest .
```
3. Once the image is built, run the Docker container using the following command:
```
docker run -p 5001:5001 qa_chat_web
```
4. Use curl/postman for API call
```
curl --header "Content-Type: application/json" \
     --request POST \
     --data '{"question": "como receber pagamento"}' \
     http://<pods-ip-address>:5001/api/chat
```
