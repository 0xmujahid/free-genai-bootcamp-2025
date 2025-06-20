   ## running ollama third-party service


   ## choosing a model
   https://ollama.com/library/llama3.2:1b

   ## API documentation of Ollama
   https://github.com/ollama/ollama/blob/main/docs/api.md

   ## Download  (Pull) a model 
   curl http://localhost:8008/api/pull -d '{
  "model": "llama3.2:1b"
}'

## Generate a ollama Model
curl http://localhost:8008/api/generate -d '{
  "model": "llama3.2:1b",
  "prompt": "Why is the sky blue?"
}'


  
## run this in terrminal to up and running
 LLM_ENDPOINT_PORT=8008 no_proxy=localhost LLM_MODEL_ID=llama3.2.1b host_ip=$(hostname -I | awk '{print $1}') docker compose up -d