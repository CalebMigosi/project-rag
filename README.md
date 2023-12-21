# project-rag
We wanted to use this project to show an example production ready setup for a small company with little resources wishing to use Retrieval Augmented Generation in their applications with considerations to GDPR regulations on Personal Identifying Information (PII data.)

We run the main LLM locally because of cost concerns. It was just easier to predict how much we would spend on a graphics card vs having to contend with unexpected costs of using a cloud provider. Of course if we get good traction on this we'll just move the project to a CSP. 

## Disclaimer
By no means are we experts in any of these fields. We're just guys playing around with what's out there. There will likely be security issues (potentially serious ones) somewhere and we would definitely appreciate you letting us know where.

## Important repos

1. rag-fe: Front end logic (We decided to go with React for obvious community and popularity reasons.)
2. rag-be: Backend logic (TBD. Could be python or dotnet)
3. rag-etl: ETL logic. Processing incoming data into vector embeddings. (Obvious choice is python here. But considering doing a separate repo using mlnet in C#)
4. rag-model: Model logic. Allows for the application and data store to interact with the LLM.

# LLM choice
We chose [Mistral-7B-Instruct-v0.2](https://docs.mistral.ai/models) because of the recent hype surrounding the performance of the model. (Also where in the world are we going to get 100gb worth of GPU by ourselves?)

# Data store choice
We've had quite a bit of experience with Elasticsearch and decided to go with version 8 because of the recent (end 2023) news that vector embeddings are now available in v8.
