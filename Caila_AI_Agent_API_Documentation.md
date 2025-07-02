
# Caila AI Agent API Documentation

## Introduction
Caila is a powerful AI Agent designed for cryptocurrency market analysis, weather & location services, and comprehensive blockchain analytics. Through simple RESTful APIs, you can easily integrate Caila's intelligent conversational capabilities into your applications.

## Core Features
- **Intelligent Conversation System**
- **Real-time Streaming Response**: Supports Server-Sent Events (SSE) and streaming transmission
- **Multi-user Management**: Supports username, display name, and room ID management
- **Context Memory**: Remembers conversation history and provides coherent responses

### Professional Service Domains
- **Cryptocurrency Market Analysis**: DeFi navigation, token market predictions, yield farming recommendations
- **Weather & Location Services**: Real-time weather queries with location-based business recommendations and travel advice
- **BNB MCP Integration**: Access to BNB MCP (Multi-Chain Protocol) data for smart contract analysis and token insights
- **Real-time DeFi Protocol Analytics**: Cross-chain APY analysis, liquidity tracking, and yield optimization
- **Personalized Responses**: Customized responses based on user preferences and conversation history

---

## API Endpoints Overview
| Method | Endpoint | Function |
|--------|----------|----------|
| GET | /agents | Retrieve available Agent ID list |
| GET | /agents/:agentId/channels | Get Caila's current Discord channels |
| POST | /:agentId/message | Send message and receive SSE streaming response |
| POST | /:agentId/message-stream | Send message and receive real-time streaming response |

---

## Use Cases

### 1. Weather & Travel Planning with Local Recommendations
```json
{
  "userName": "traveler_alice",
  "userId": "alice001",
  "roomId": "travel_chat",
  "text": "What's the weather like in Bali this week? Recommend the best beaches for surfing and nearby restaurants"
}
```
**Expected Response**: Weather forecast, surf conditions, beach recommendations, crypto-friendly local businesses, and optimal travel timing.

### 2. BNB Chain Token Contract Analysis
```json
{
  "userName": "contract_analyst",
  "userId": "analyst123",
  "roomId": "bnb_research",
  "text": "Analyze the PancakeSwap (CAKE) token contract on BNB Chain"
}
```
**Expected Response**: Contract address verification, holder analytics, transaction volume, liquidity metrics, security audit status, and tokenomics breakdown.

### 3. DeFi Protocol APY Analysis
```json
{
  "userName": "yield_farmer",
  "userId": "farmer001",
  "roomId": "defi_yields",
  "text": "Compare current APY rates across major DeFi protocols - show me the best yield farming opportunities on Ethereum, BNB Chain, and Polygon"
}
```
**Expected Response**: Real-time APY comparison, risk assessment, impermanent loss calculations, gas fee considerations, and optimized yield strategies.

### 4. Location-Based Crypto Services (Upcoming)
```json
{
  "userName": "crypto_nomad",
  "userId": "nomad123",
  "roomId": "travel_crypto",
  "text": "I'm in Tokyo and it's raining. Find indoor crypto meetups, Bitcoin ATMs, and cafes that accept cryptocurrency payments"
}
```
**Expected Response**: Weather-appropriate indoor activities, crypto ATM locations, merchant directories, and local crypto community events.

---

## Response Features
- **Streaming Transmission**: Real-time reception of AI-generated content for enhanced user experience
- **Structured Data**: Complete metadata including message ID, response analysis, user information
- **Personalized Replies**: Caila remembers user query history for more relevant suggestions
- **Multi-chain Data**: Integrated BNB MCP data for comprehensive blockchain analytics
- **Weather Intelligence**: Real-time weather data combined with location-based recommendations
- **Contract Analytics**: Deep smart contract analysis and token metrics
- **Multimedia Support**: Supports emojis and formatted text for more engaging conversations

---

## Quick Start

### 🔧 Get Agent ID
```bash
curl 'https://caila.api.iotex.ai/agents'
```

### ✉️ Send Your First Message
```bash
curl -X POST 'https://caila.api.iotex.ai/:agentId/message' \
  -H 'Content-Type: application/json' \
  -d '{"userName": "your_name", "userId": "your_id", "text": "Hello Caila!"}'
```

### 📡 Handle Streaming Response
Listen for SSE events or parse streaming JSON data

---

## Advanced Capabilities

### Weather & Location Intelligence
- Hyper-local real-time weather (accurate to block-level precision)
- Real-time weather forecasting with travel recommendations
- Location-based business discovery
- Geo-targeted travel advice and activity suggestions

### BNB Chain Contract Analysis
- Smart contract security assessment
- Token holder distribution analysis
- Transaction pattern recognition

### DeFi Protocol Analytics
- Real-time APY monitoring across multiple chains
- Risk-adjusted yield calculations
- Impermanent loss projections
- Gas fee optimization strategies
- Liquidity migration recommendations
