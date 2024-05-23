# llama3-70B Using Akash

- Llama 3 70B with 16-bit quantization on Akash Network intented for Akash Zealy Quest.
- For this we need acces to Huggingface llama models.
- Access can ge gained by requesting access from the repo's authors and by sharing your info.
- After gaining the access to the repo create an access token by clicking [here](https://huggingface.co/settings/tokens).

# Steps to Deploy Application ON Akash Network

- Create and fund a Keplr or Leap wallet
  - [Keplr wallet](https://akash.network/docs/getting-started/token-and-wallets/#keplr-wallet)
  - [Leap wallet](https://akash.network/docs/getting-started/token-and-wallets/#leap-cosmos-wallet)
- Visit https://deploy.cloudmos.io/
- Connect your wallet
  - You need to have at least 0.5 AKT in your wallet
- Press the deploy button
- Select "Build your template"
- (Optional) Name your deployment
- Select YAML and paste the [deploy.yaml](https://github.com/Lukewarmer6969/llama3-akash/blob/main/deploy.yaml) contents
- Replace "hf_token" with your huggingface access token.
- Press "Create Deployment"
- click wallet transaction
- Review bids and select provider
- Preferably select the provider who is audited.
- Accept provider transaction
- Go to LEASES and press the URI
- Wait for 30 mins for the model weight's to be downloaded.
- Then Use Postman or CMD to interact with the llama model.


# Test The deployed model.

 - Use the following api call in CMD or terminal (for UNIX)

```
curl -X POST http://<host>/v1/chat/completions -H "Content-Type: application/json" -d "{\"model\": \"meta-llama/Meta-Llama-3-70B-Instruct\", \"messages\": [{\"role\": \"system\", \"content\": \"You are a helpful assistant.\"}, {\"role\": \"user\", \"content\": \"Tell me a joke.\"}], \"max_tokens\": 50, \"temperature\": 0.7}"
```
- Replace the <host> with the url in leases.
- Set `max_tokens` value of your choice.
- Now you can chat With llama-3-70B and ask questions.
