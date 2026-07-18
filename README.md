#  MeetNest

A real-time video conferencing application built using **React**, **WebRTC**, and **Socket.IO**, enabling seamless peer-to-peer audio and video communication. MeetNest allows users to create or join meeting rooms instantly using a unique room ID while maintaining low-latency communication through direct browser-to-browser connections.


---

## ✨ Features

- 🎥 Real-time video and audio communication
- 🔗 Create and join meeting rooms using unique Room IDs
- 🤝 Peer-to-peer communication using WebRTC
- ⚡ Low-latency media streaming
- 📡 Socket.IO based signaling server
- 🔄 Automatic WebRTC offer/answer negotiation
- 🌍 ICE Candidate exchange for NAT traversal
- 📱 Responsive user interface
- 🎯 Clean and intuitive meeting experience

---

## 🛠️ Tech Stack

### Frontend
- React.js
- HTML5
- CSS3
- JavaScript

### Backend
- Node.js
- Express.js
- Socket.IO

### Real-Time Communication
- WebRTC
- STUN Servers

---

# 📈 Application Workflow

```mermaid
flowchart TD

A[User Opens MeetNest] --> B{Create or Join Room}

B -->|Create| C[Generate Room ID]
B -->|Join| D[Enter Existing Room ID]

C --> E[Connect to Socket.IO Server]
D --> E

E --> F[Join Signaling Room]

F --> G[Exchange SDP Offer & Answer]
G --> H[Exchange ICE Candidates]
H --> I[Establish WebRTC Peer Connection]

I --> J[Real-Time Audio & Video Streaming]
```

---

# 🏗️ System Architecture

```mermaid
flowchart LR

subgraph Client A
React1[React App]
WebRTC1[WebRTC]
end

subgraph Signaling Server
Socket[Socket.IO Server]
end

subgraph Client B
React2[React App]
WebRTC2[WebRTC]
end

React1 --> Socket
React2 --> Socket

Socket --> React1
Socket --> React2

WebRTC1 <------ Peer-to-Peer ------> WebRTC2
```

---

## 📁 Project Structure

```
MeetNest/
│
├── backend/
│   ├── controllers/
│   ├── models/
│   ├── routes/
│   ├── middleware/
│   ├── app.js
│   ├── server.js
│   └── package.json
│
├── frontend/
│   ├── public/
│   ├── src/
│   │   ├── contexts/
│   │   ├── pages/
│   │   ├── controllers/      
│   │   ├── App.jsx
│   │   └── main.jsx
│   └── package.json
│
└── README.md
```
