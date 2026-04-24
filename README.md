# 🚀 AI-Driven HR Workflow Designer

A scalable, production-style **HR Workflow Designer** built using **React, TypeScript, React Flow, Zustand, and Tailwind CSS**.
This application allows HR teams to visually design, configure, validate, and simulate workflows such as onboarding, approvals, and automated processes.

---

## 🎯 Key Features

### 🧩 Visual Workflow Builder

* Drag-and-drop interface using **React Flow**
* Supports multiple node types:

  * Start Node
  * Task Node
  * Approval Node
  * Automated Node
  * End Node
* Connect nodes to form custom workflows

---

### ⚙️ Dynamic Node Configuration

* Context-aware **Properties Panel**
* Each node type has custom editable fields:

  * **Task Node:** Title, Description, Assignee, Due Date
  * **Approval Node:** Approver Role, Threshold
  * **Automated Node:** Action selection with dynamic parameters
* Fully controlled and type-safe forms

---

### 🔌 Mock API Integration

* Simulated backend using async functions:

  * `GET /automations` → Fetch available automation actions
  * `POST /simulate` → Execute workflow simulation
* Models real-world API interactions

---

### 🧪 Workflow Simulation Engine

* Executes workflows using **graph traversal (BFS)**
* Displays step-by-step execution logs
* Provides clear insight into workflow behavior

---

### ✅ Advanced Validation System

* Detects:

  * Missing Start/End nodes
  * Disconnected nodes
  * Cycles in workflow
  * Incomplete configurations (e.g., missing assignee)
* Errors are:

  * Highlighted directly on nodes
  * Summarized in the sandbox panel

---

### ⭐ Bonus Features

* Export / Import workflow as JSON
* Undo / Redo functionality (history-based)
* MiniMap and zoom controls
* Reset workflow option
* Dynamic parameter rendering for automation actions

---

## 🏗️ Architecture

```
src/features/workflow/
├── components/
│   ├── Canvas.tsx          # React Flow canvas & interactions
│   ├── Sidebar.tsx         # Node palette
│   ├── WorkflowNode.tsx    # Custom node renderer
│   ├── PropertiesPanel.tsx # Dynamic configuration panel
│   ├── SandboxPanel.tsx    # Simulation & validation
│   └── Toolbar.tsx         # Controls (undo/redo/import/export)
├── store.ts                # Zustand global state management
├── types.ts                # Type-safe node definitions
├── validation.ts           # Workflow validation logic
└── mockApi.ts              # Mock API layer
```

---

## 🧠 Design Decisions

* **Zustand for State Management:**
  Chosen for simplicity, performance, and clean separation from UI components.

* **Discriminated Unions (TypeScript):**
  Ensures type safety and scalability when adding new node types.

* **Single Custom Node Renderer:**
  Simplifies React Flow integration while supporting multiple node types.

* **Separation of Concerns:**
  Clear division between UI, state, validation, and API layers.

* **Graph-Based Execution:**
  BFS traversal ensures logical and sequential workflow simulation.

---

## ⚡ Why This Approach?

This system is designed with **scalability, extensibility, and real-world workflow modeling** in mind.
It mimics how enterprise workflow engines operate, making it adaptable for future enhancements like real-time collaboration, backend integration, and automation pipelines.

---

## ▶️ How to Run

```bash
npm install
npm run dev
```

---

## 📈 Future Improvements

* Real-time collaboration (WebSockets / Yjs)
* Backend integration with persistent storage
* Auto-layout using DAG algorithms (e.g., Dagre)
* Unit & E2E testing (Vitest, Playwright)
* Workflow templates and reusable components
* Role-based access control

---

## 👩‍💻 Author

[Your Name]

---

## 📌 Submission Details

* Role: Full Stack Engineering Intern
* Organization: Tredence Studio
* Case Study: HR Workflow Designer

---
