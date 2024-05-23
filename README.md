# llama3-70B Using Akash

- Llama 3 70B with 16-bit quantization on Akash Network intented for Akash Zealy Quest.
- For this we need acces to Huggingface llama models.


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
- Select YAML and paste the [deploy.yaml](deploy.yaml) contents
- Press "Create Deployment"
- click wallet transaction
- Review bids and select provider
- Preferably select the provider who is audited.
- Accept provider transaction
- Go to LEASES and press the URI
- Wait for 30 mins for the model weight's to be downloaded.
- Then Use Postman or CMD to interact with the llama model.
