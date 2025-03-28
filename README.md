# SS AI Agent

## Main Components of the Project
![SS AI Agent](ss-ai-agent.jpeg)

- **Eliza-starter** as the framework
- **Openrouter** as the model provider
- **EVM plugin** for transactions
- **MetaMask** account as the wallet
- **Infura** as the service host
- **Sepolia** as the Ethereum testnet

## Pre-requisites for Setting Up Eliza Starter
- **Node.js 23+** (Recommended: Set the version to exactly 23.3 using `nvm use 23.3` in Git Bash to avoid setup issues.)
- **PNPM**
- **Python 2.7+**
- **Tools Used:** VS Code and Git Bash

## Workflow
### 1. Set Up Eliza Starter
Run the following commands:
```sh
cd eliza-starter
cp .env.example .env
pnpm i && pnpm build && pnpm start
```
**Note:** Initially starting Eliza will only give an idea of the interaction experience. The `pnpm build` command may require running `pnpm approve-builds` to avoid ignoring all buildables.

### 2. Create an OpenRouter Account and Generate a Key
- Sign up at OpenRouter and obtain an API key.

### 3. Edit the `.env` File
- Navigate to the `eliza-starter` folder.
- Assign the OpenRouter key to the `OPENROUTER_API_KEY` variable in `.env`.

### 4. Install the EVM Plugin
```sh
pnpm install @elizaos/plugin-evm -w
```

### 5. Check if the Agent is Alive
```sh
pnpm start
```

### 6. Create a Wallet Account
- Use **MetaMask** to create a wallet.
- Copy the private key and assign it to `EVM_PRIVATE_KEY` in `.env`.
- Ensure your key is prefixed with `0x`.

### 7. Set Up an RPC Provider
- Use **Infura** and navigate to **Active Endpoints**.
- Look for **Ethereum Sepolia**.
- Copy its contents and assign it to `EVM_PROVIDER_URL` in `.env`.

### 8. Start the Agent
```sh
pnpm start
```
If needed, rebuild before starting:
```sh
pnpm build
```

### 9. Interact with the Agent
- Start chatting with your agent using human-like prompts and start transacting!
- Please refer to the Screenshots folder to check how the prompts work and also to check transaction signature.
- More transaction signature: 0xc41d801d065ce57a87cb6b6413ef7ac9a76000e7fde6ad0e1d5255d6df3ee004

## License
Specify the license under which the project is distributed.

## Contact
Provide contact information or links to relevant documentation.

