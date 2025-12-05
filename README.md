# Reddit MCP Server

A Model Context Protocol (MCP) server that enables AI agents and developer tools
(such as Continue.dev or VS Code MCP clients) to interact with Reddit securely
through the official Reddit API.

This server supports authenticated user workflows for reading subreddit content
and optionally drafting posts/comments with explicit user approval.

---

## ✨ Features

| Capability | Status |
|----------|--------|
| User authentication via Reddit OAuth2 | ✅ |
| Search subreddit posts | ✅ |
| Retrieve post details + comments | ✅ |
| Filter by keywords, flair, or timeframe | 🚧 |
| Draft posts/comments (user-triggered only) | 🚧 |
| Moderator assistance (fetch reports, queues) | Planned |

> 🔐 This project enforces **human-in-the-loop** actions.  
> No automated posting, voting, or bulk scraping.

---

## 🔄 Architecture Overview
MCP Client (VS Code / CLI / Agent) ──► Reddit MCP Server ──► Reddit API
│
└──► Secure User OAuth


- Built using **Node.js / TypeScript**
- Integrates with Reddit via **OAuth2 + scoped API permissions**
- MCP interface exposes Reddit actions as structured tools

---

## 🛠 Tech Stack

- **Node.js** – Server runtime
- **Express** – API routing (optional)
- **Reddit OAuth2 API** – Auth + data access
- **Model Context Protocol (MCP)** – Tooling interface

---

## 🔐 Reddit API Scopes Used

| Scope | Purpose |
|-------|---------|
| `read` | Retrieve posts, comments, subreddit info |
| `identity` | Identify and authenticate the user |
| `submit` (Optional) | Create posts/comments only with human confirmation |

> Additional scopes will only be added with user consent.

---

## 🚀 Getting Started

```bash
git clone https://github.com/<your-username>/reddit-mcp-server
cd reddit-mcp-server
npm install
npm start

🧩 MCP Tools (Example)
Tool	Description
search_posts	Search posts by subreddit + keywords
get_comments	Fetch comments for a given post ID
create_post	Start a draft post (manual user submit required)

Example prompt:

"Search r/kubernetes for posts about 'autoscaling' in the past week"

