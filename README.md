# MCP Server Example

This project demonstrates a simple client-server application using the Model Context Protocol (MCP) with Google Gemini AI and Twitter API integration.

## Features
- **Server**: Exposes tools via MCP, including:
  - `addTwoNumbers`: Adds two numbers.
  - `createPost`: Posts a status to X (formerly Twitter).
- **Client**: Connects to the MCP server, lists available tools, and interacts with Gemini AI to call tools.

## Prerequisites
- Node.js v18 or higher
- npm
- Twitter Developer credentials (for posting to X)
- Google Gemini API key

## Setup

1. **Clone the repository**
   ```sh
   git clone <your-repo-url>
   cd <repo-folder>
   ```

2. **Install dependencies**
   ```sh
   cd server
   npm install
   cd ../client
   npm install
   ```

3. **Environment Variables**
   Create a `.env` file in both `server/` and `client/` directories with the following variables:
cles
   **server/.env**
   ```env
   TWITTER_API_KEY=your_twitter_api_key
   TWITTER_API_SECRET=your_twitter_api_secret
   TWITTER_ACCESS_TOKEN=your_twitter_access_token
   TWITTER_ACCESS_TOKEN_SECRET=your_twitter_access_token_secret
   ```

   **client/.env**
   ```env
   GEMINI_API_KEY=your_gemini_api_key
   ```

## Running the Project

1. **Start the server**
   ```sh
   cd server
   node index.js
   ```
   The server will run at `http://localhost:3001`.

2. **Start the client**
   In a new terminal:
   ```sh
   cd client
   node index.js
   ```

3. **Usage**
   - The client will connect to the server and prompt you for input.
   - You can ask questions or trigger tool calls (e.g., add two numbers, post a status to X).

## Project Structure
```
client/
  index.js
  package.json
server/
  index.js
  mcp.tool.js
  package.json
```

## Notes
- Ensure your Twitter and Gemini API credentials are valid.
- The server must be running before starting the client.
- For production, secure your environment variables and API keys.

## License
MIT
