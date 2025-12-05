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

