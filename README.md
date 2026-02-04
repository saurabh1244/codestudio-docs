# CodeStudio – Developer Social & Coding Platform

**CodeStudio** is a project where developers can run code, challenge others, and share their knowledge in a social feed. I built this to combine a coding playground with a community platform.

**Live Link:** [codestudio.appnity.cloud](https://codestudio.appnity.cloud)

---

## 🐍 Python Execution Environment
Since this project allows users to write and run Python code in the browser, handling the execution environment was the most critical part.

*   **Sandboxed Execution:** When a user writes Python code, it runs inside a secure engine (Piston) to prevent it from harming the server.
*   **Real-time Output:** It captures the print statements (stdout) and errors (stderr) and shows them instantly in the browser terminal.
*   **Libraries:** Supports standard Python libraries for algorithm practice.

---

## ⚙️ Execution Flow Chart
Here is how the code travels from the user's browser to the server and back:

```mermaid
graph TD
    User([User]) -->|Types Python Code| Frontend[React Frontend]
    Frontend -- "State (Zustand)" --> Frontend
    Frontend -->|Clicks Run| API[Backend API]
    API -->|Sends Script| Piston[Piston Engine (Sandbox)]
    API -->|JSON Response| Frontend
    Frontend -->|Displays Output| User
```

---

## 🧩 Tech Stack
I used a simple and modern stack to build this:

| Category | Technology | Usage in Project |
| :--- | :--- | :--- |
| **Frontend** | **React.js** | Building the Editor, Feed, and UI Components |
| **State Management** | **Zustand** | Handling global state (much simpler than Redux) |
| **Styling** | **Tailwind CSS** | Quick, responsive styling for mobile & desktop |
| **Code Execution** | **Piston** | The engine that runs Python/Rust code safely |
| **Backend** | **Node.js** | Handling API requests and user data |

---

## 🚀 Key Features

### 1. The Arena (Coding Practice)
This is where users solve problems.
*   Supports **Python**, Node.js, and Rust.
*   Users get instant feedback on their code (Pass/Fail).

### 2. Social Feed & Sharing
*   Developers can share their code snippets as posts.
*   Other users can view, like, and try running those snippets themselves.

### 3. Leaderboard & XP System
*   To make it engaging, users earn **XP (Experience Points)** for solving problems.
*   The global leaderboard ranks users based on their activity.

### 4. Code Converter
*   An integrated tool that helps users understand code by converting logic between different languages.

### 5. Developer Identity (Profile)
*   Every user has a dedicated public profile showing their:
    *   **Activity Graph:** Similar to GitHub, showing contribution frequency.
    *   **Badges:** Achievements unlocked (e.g., "Algorithm Guru").
    *   **Reputation:** A score reflecting their helpfulness in the community.
    *   **Social Graph:** Followers and following connections.

### 6. The Studio (Snippet Creation)
*   A dedicated creative space where users can:
    *   Write code in various languages (Python, Rust, JS).
    *   Run it instantly to verify output.
    *   Publish it to the public feed for others to see and fork.

### 7. Discover & Roadmaps
*   **Search**: Users can find specific code snippets or problems.
*   **Roadmaps**: Curated learning paths for developers to master new skills.
