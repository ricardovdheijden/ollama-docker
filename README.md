### Start container
```shell
docker compose up -d
```
The container creates a `ollama` folder in this project folder and contains public and private keys as well as the downloaded models

### Pull the llama3 model
```shell
curl -X POST http://localhost:7869/api/pull -d '{"model":"llama3"}'
```
Note: it will be stored in the `ollama` folder in the project

### Test the API
```shell
curl -X POST http://localhost:7869/api/generate -d '{ "model": "llama3", "prompt":"Can you tell me your best dad joke?", "stream": false }'
```
