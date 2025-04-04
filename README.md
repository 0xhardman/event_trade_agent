# News Quantar

## Background

Cryptocurrency markets are highly responsive to social media statements from influential figures like Vitalik Buterin or Donald Trump. For instance, on April 3, 2025, when Justin Sun criticized FUSDT, it triggered significant de-pegging. However, once the FUSDT team provided clarification, the price quickly returned to its pegged value. This volatility creates substantial arbitrage opportunities for traders who can quickly react to key opinion leaders' (KOLs) statements.

The challenge is that a single person cannot effectively monitor all relevant KOLs across various platforms, leading to missed trading opportunities.

## Introduction

AI Event Trader is a sophisticated solution that leverages AI agents to monitor influential figures' statements on social media and automatically execute trading decisions on the Polygon blockchain. By combining natural language processing with blockchain technology, the system can identify market-moving statements and execute trades faster than human traders.

## Key Features

- **Real-time KOL Monitoring**: Continuously tracks statements from key opinion leaders on platforms like Farcaster
- **Sentiment Analysis**: Uses advanced AI to determine if statements are bullish or bearish for specific tokens
- **Autonomous Trading**: Makes independent decisions to long or short tokens based on analyzed sentiment
- **Polygon Integration**: Executes all transactions on Polygon PoS for fast, low-cost trading
- **Risk Management**: Implements safeguards to limit potential losses and optimize capital efficiency

## Technology Stack

### Polygon MCP

The core of AI Event Trader is built on the Polygon Model Context Protocol (MCP), which provides:

- Seamless blockchain interaction for AI agents
- Reliable on-chain data access
- Low-cost, high-speed transaction execution
- Smart contract deployment for automated trading strategies

### 1inch Integration

The platform leverages 1inch's powerful APIs to:

- Execute optimal token swaps with minimal slippage
- Query real-time token prices and account balances
- Track transaction history for performance analysis
- Monitor market liquidity to optimize trade timing and size

### Farcaster Integration

The platform utilizes NEYNAR webhooks for immediate market response:

- Real-time Webhook Monitoring: Leverages NEYNAR webhooks to listen for cast creation events from key Farcaster users
- Instant Trade Execution: Triggers buy/sell decisions within milliseconds of detecting relevant casts

## Core Components

### polygon-mcp

A TypeScript implementation of the Polygon Model Context Protocol that enables:

- Direct blockchain interaction from AI agents
- Token balance checking and transfers
- Smart contract deployment and interaction
- Gas price optimization
- **1inch swap** integration for efficient token exchanges
- Secure wallet management through seed phrases

### webhook-sdk

A Python SDK for Farcaster event monitoring that provides:

- Creation and management of Neynar webhooks
- Real-time event reception for Farcaster casts
- Filtering capabilities to focus on specific content or users
- Event deduplication to prevent duplicate trade execution
- Seamless integration with the trading engine

### chat.py

A standalone interactive CLI for blockchain operations that:

- Provides a conversational interface to the Polygon blockchain
- Allows manual querying of wallet addresses, gas prices, and token balances
- Supports manual token swaps and transfers for testing
- Serves as a development and debugging tool for the trading system
- Uses the Fast-Agent framework for natural language blockchain interaction

### quantar.py

The core trading engine that:

- Connects the webhook system to the trading infrastructure
- Analyzes Farcaster messages for trading signals
- Implements strict trading limits and security measures
- Executes trades through the Polygon MCP
- Supports multiple token types with proper decimal handling
- Restricts trading to authorized users only
- Ensures proper token address usage (e.g., native USDC vs USDC.e)

## Installation

```bash
git clone https://github.com/your-username/ai-event-trader.git
cd ai-event-trader
npm install
