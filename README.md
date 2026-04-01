![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Status](https://img.shields.io/badge/status-active-success.svg)
![Built With](https://img.shields.io/badge/built%20with-Web3%20%2B%20AI-purple.svg)
# Eigen Trustless Agents: Building Verifiable AI with ERC-8004 and EigenCloud

> Build verifiable AI agents with deterministic inference, on-chain identity, and cryptographic reputation.

## Overview
## Quick Start

### Clone the Repository

```bash
git clone https://github.com/your-username/eigen-trustless-agents.git
cd eigen-trustless-agents
```

### Full Setup Guide

For a complete walkthrough, refer to the guide below:

[View Full Implementation Guide](https://chatgpt.com/s/m_69ccc9804fac8191a4dead73d307bae8)
This repository demonstrates how to build trust-minimized AI agents using ERC-8004, EigenAI, EigenCompute, and the Agent0 SDK.

The system ensures:
- Deterministic AI outputs
- Verifiable execution
- On-chain identity
- Cryptographic reputation

No trust in the agent operator is required.

## Architecture


User
↓
EigenAI (deterministic inference)
↓
EigenCompute (TEE execution + wallet)
↓
ERC-8004 (on-chain identity + reputation)
↓
Agent0 SDK (registration, discovery, feedback)


## Core Components

| Component     | Description |
|---------------|-------------|
| EigenAI       | Deterministic AI inference with signatures |
| EigenCompute  | Secure execution in Trusted Execution Environments |
| ERC-8004      | NFT-based identity and reputation system |
| Agent0 SDK    | Agent registration, discovery, and feedback |

## Quick Start

### 1. Deterministic Inference

```python
from openai import OpenAI

client = OpenAI(
    base_url="https://eigenai.eigencloud.xyz/v1",
    default_headers={"x-api-key": eigenai_api_key}
)

response = client.chat.completions.create(
    model="gpt-oss-120b-f16",
    seed=42,
    messages=[{"role": "user", "content": "Should I buy or sell?"}]
)

print(response.signature)
```

### 2. Register Agent

```python
from agent0_sdk import SDK

sdk = SDK(
    chain_id=11155111,
    rpc_url="https://sepolia.infura.io/v3/YOUR_PROJECT_ID",
    signer=your_private_key
)

agent = sdk.create_agent(
    name="EigenAI Agent",
    description="Deterministic AI agent"
)

agent_id = agent.register()
```

### 3. Deploy to EigenCompute

```bash
ecloud compute app deploy --image-ref myagent:latest
```

## Features

- Deterministic AI outputs
- Cryptographic verification
- TEE-secured execution
- On-chain agent identity
- Transparent reputation system

## Use Case: Trading Agent

A trading agent can:
- Make deterministic decisions
- Run in secure TEE infrastructure
- Maintain on-chain identity
- Build verifiable reputation

## Roadmap

- [ ] Full SDK integration examples
- [ ] UI dashboard
- [ ] Multi-agent coordination
- [ ] Cross-chain identity support

## License

MIT License
