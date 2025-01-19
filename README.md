# langchain-poc

For any Langchain GenAI application, there are 2 steps:
1. Data Ingestion
2. Data Splitting
3. Data Embeddings
4. Storing Embeddings in Vector DB 
5. Retrieving information from that data using LLMs

1. Data Ingestion
Data is ingested through langchain

2. Data Splitting
For various LLMs, data cannot be provided in one go since LLMs have context size restrictions. To overcome this, we have split data into text chunks.

3. Data Embeddings
Once the data is split into text chunks, text chunks are converted into embeddings which basically are vectors

4. Storing Embeddings in Vector DB
Once the embeddings are created, they can be stored as vectors in vector db. Vector DB usually return Context information which can be used along with prompts for better equip chatbots to provide relevant information from data ingested

5. Retrieving information from that data using LLMs
Now when the data is ingested, it is ready to be used in GenAI application. A general GenAI application is a chatbot which retrieves information from data ingested.
For retrieving info, langchain uses document stuff load chain which uses interface to vector db to get context info.
Once the context info is retrieved from vector db, it is combined with ai assistant info and passed to LLM which provides response according to it

