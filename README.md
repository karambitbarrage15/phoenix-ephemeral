# 🔥 Phoenix Ephemeral

Phoenix Ephemeral is a real-time anonymous chat application that allows users to create and join chat rooms without requiring signup or authentication.

The application is built around the idea of quick and simple communication. A user can create a secure chat room, receive a unique Room ID, and share that ID with another person. The other person can then use the same Room ID to join the conversation.

This project focuses on building a complete full-stack application involving a modern frontend, backend APIs, database integration, real-time communication, and deployment.

---

## 🚀 Live Demo

🔗 **Live Application:**  
https://phoenix-ephemeral-git-main-kalejrbrownboy-3210s-projects.vercel.app/

🔗 **GitHub Repository:**  
https://github.com/karambitbarrage15/phoenix-ephemeral

---

## ✨ Features

- 🔐 Create secure anonymous chat rooms
- 👤 No signup or authentication required
- 🆔 Unique Room ID for every chat room
- 👥 Join an existing chat room using its Room ID
- 💬 Send and receive messages in real time
- ⚡ Instant message updates without refreshing the page
- 🗄️ Database integration for managing application data
- 📱 Responsive user interface
- 🌐 Deployed and accessible online

---

# 🛠️ Tech Stack

## Frontend

- Next.js
- React
- TypeScript
- Tailwind CSS

## Backend

- Node.js
- REST APIs
- Real-time communication

## Database

- PostgreSQL
- Prisma ORM

## Deployment

- Vercel

---

# 🏗️ How It Works

The application follows a simple workflow.

## 1. Create a Secure Room

The user enters an anonymous identity and creates a new chat room.

```text
Enter Identity
      │
      ▼
CREATE SECURE ROOM
      │
      ▼
Generate Unique Room ID
```

For example:

```text
Room ID: phoenix-8f4k2
```

The Room ID acts as the identifier for the chat room.

---

## 2. Share the Room ID

The person who creates the room can copy the Room ID and send it to another person.

For example:

```text
phoenix-8f4k2
```

The Room ID can be shared through:

- WhatsApp
- Discord
- Telegram
- Email
- Instagram
- Any other messaging platform

---

## 3. Join the Same Room

The second person enters the same Room ID.

```text
User 1 ───────┐
              │
              ▼
       ┌─────────────┐
       │   ROOM ID   │
       │ phoenix-8f4k2│
       └─────────────┘
              ▲
              │
User 2 ───────┘
```

Once both users are connected to the same Room ID, they can communicate with each other.

---

## 4. Start Chatting

Messages sent by users inside the same room are delivered to the other participants.

```text
User 1
   │
   │ Sends Message
   ▼
Backend / API
   │
   │ Processes Message
   ▼
Chat Room
   │
   ├────────────► User 1
   │
   └────────────► User 2
```

This allows users in the same room to exchange messages through the application.

---

# 🧩 Application Architecture

The overall architecture of Phoenix Ephemeral can be represented as:

```text
                    ┌─────────────────┐
                    │     User 1      │
                    └────────┬────────┘
                             │
                             ▼
                    ┌─────────────────┐
                    │   Next.js App   │
                    │    Frontend     │
                    └────────┬────────┘
                             │
                         API Requests
                             │
                             ▼
                    ┌─────────────────┐
                    │     Backend     │
                    │                 │
                    │ Room Management │
                    │ Message Handling│
                    └────────┬────────┘
                             │
                             ▼
                    ┌─────────────────┐
                    │   PostgreSQL    │
                    │      Prisma     │
                    └─────────────────┘
```

Multiple users can connect to the same room using the Room ID.

```text
        User 1
           │
           ▼
      ┌───────────┐
      │ Chat Room │
      │ Room ID   │
      └───────────┘
           ▲
           │
        User 2
```

---

# 💻 Getting Started

Follow these steps to run the project locally.

## 1. Clone the Repository

```bash
git clone https://github.com/karambitbarrage15/phoenix-ephemeral.git
```

## 2. Navigate to the Project

```bash
cd phoenix-ephemeral
```

## 3. Install Dependencies

```bash
npm install
```

## 4. Configure Environment Variables

Create a `.env` file in the root directory of the project.

Add the required environment variables.

Example:

```env
DATABASE_URL=your_database_connection_url
```

Add any additional environment variables required by the application.

> Do not commit your `.env` file to GitHub.

---

## 5. Generate Prisma Client

Run:

```bash
npx prisma generate
```

---

## 6. Run the Development Server

```bash
npm run dev
```

The application should now be available at:

```text
http://localhost:3000
```

---

# 🧠 What I Learned

Building Phoenix Ephemeral helped me gain practical experience with several important full-stack development concepts.

## Full-Stack Application Development

I worked on connecting the frontend with backend APIs and managing communication between different parts of the application.

```text
Frontend
   │
   ▼
API / Backend
   │
   ▼
Database
```

---

## Room-Based Architecture

The application uses unique Room IDs to separate conversations.

For example:

```text
Room A
├── User 1
└── User 2


Room B
├── User 3
└── User 4
```

Users in one room should only interact with messages associated with that room.

---

## Database Management with Prisma

The project uses Prisma as an ORM for interacting with the PostgreSQL database.

This involved working with concepts such as:

- Database schemas
- Models
- Queries
- Prisma Client
- Database connections
- Environment variables
- Production database configuration

---

## Frontend and Backend Integration

Building this project involved handling communication between the frontend and backend.

This included:

- Sending API requests
- Handling responses
- Managing room creation
- Joining chat rooms
- Sending messages
- Fetching application data
- Handling errors

---

## Deployment and Debugging

While deploying the application, I encountered real-world development challenges involving:

- CORS configuration
- Frontend and backend communication
- Local vs production environments
- Environment variables
- Prisma Client generation
- TypeScript errors
- Build failures
- Vercel deployment issues

Working through these issues provided practical experience in debugging and deploying a full-stack application.

---

# 🔮 Future Improvements

Some features planned for future versions include:

- [ ] 🔗 Generate shareable room links
- [ ] 📋 One-click Room ID copy button
- [ ] ⏳ Automatically expire inactive rooms
- [ ] 🗑️ Automatically delete messages after a specified period
- [ ] ⌨️ Typing indicators
- [ ] 🟢 Online user indicators
- [ ] 👥 Display the number of active users in a room
- [ ] 📎 File and image sharing
- [ ] 🔐 End-to-end encryption
- [ ] 🔔 Message notifications
- [ ] 📱 Improved mobile responsiveness

---

# 🔗 Future Room Sharing System

Currently, a user can share the Room ID manually.

For example:

```text
Room ID: phoenix-8f4k2
```

A future improvement would be to generate a direct invite link.

For example:

```text
https://your-domain.com/room/phoenix-8f4k2
```

The workflow would then become:

```text
Create Room
     │
     ▼
Generate Room ID
     │
     ▼
Generate Shareable Link
     │
     ▼
Copy & Share Link
     │
     ▼
Friend Opens Link
     │
     ▼
Automatically Joins Room
     │
     ▼
Start Chatting
```

This would make joining a room faster and improve the overall user experience.

---

# 📂 Project Structure

A simplified version of the project structure:

```text
phoenix-ephemeral/
│
├── src/
│   ├── app/
│   ├── components/
│   ├── lib/
│   └── ...
│
├── prisma/
│   └── schema.prisma
│
├── public/
│
├── package.json
├── package-lock.json
├── next.config.ts
└── README.md
```

---

# 🤝 Contributing

Contributions, issues, and feature requests are welcome.

If you would like to contribute:

1. Fork this repository.
2. Create a new branch.

```bash
git checkout -b feature/new-feature
```

3. Make your changes.
4. Commit your changes.

```bash
git commit -m "Add new feature"
```

5. Push the branch.

```bash
git push origin feature/new-feature
```

6. Open a Pull Request.

---

# 👨‍💻 Author

**Aditya Chaturvedi**

- GitHub: https://github.com/karambitbarrage15
- Project Repository: https://github.com/karambitbarrage15/phoenix-ephemeral

---

## ⭐ Support

If you found this project interesting or useful, consider giving the repository a **star** ⭐.

It helps others discover the project and motivates further development.