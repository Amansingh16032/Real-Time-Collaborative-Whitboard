# 🧑‍🎨 Real-Time Collaborative Whiteboard

A real-time collaborative whiteboard that allows multiple users to draw, write, and interact on a shared canvas simultaneously. Ideal for remote teams, classrooms, or workshops.

## 🚀 Features

- ✏️ Real-time multi-user drawing
- 🧑‍🤝‍🧑 WebSocket-powered live collaboration
- 🖼️ Canvas with pen, shapes, colors, and erase tools
- 🔒 User authentication (JWT-based)
- 🕒 Session management with reconnect and sync
- 💾 Save and load whiteboard sessions
- 📦 Dockerized deployment

## 🛠️ Tech Stack

| Layer              | Stack                                 |
|--------------------|----------------------------------------|
| Frontend           | React.js, HTML5 Canvas, Tailwind CSS   |
| Backend            | Node.js, Express.js                    |
| Real-time Sync     | Socket.IO                              |
| Authentication     | JWT, bcrypt                            |
| Database           | MongoDB (Mongoose)                     |
| Deployment         | Docker, Render / Vercel                |

## 🧩 System Design

```plaintext
+------------+     WebSocket      +------------+     DB Calls     +------------+
|  Browser A | <================> |  Node.js    | <=============> |   MongoDB   |
+------------+                    +------------+                 +------------+
       ▲                                ▲
       | REST API                       |
       ▼                                ▼
+------------+                    +------------+
|  Browser B | <================> |  Node.js    |
+------------+     WebSocket      +------------+
