# ◈ CRM Pipeline Flow

> A professional desktop CRM application for managing sales leads through a dynamic Kanban board.

[![Java](https://img.shields.io/badge/Java-21%20LTS-blue?logo=openjdk&logoColor=white)](https://openjdk.org/)
[![JavaFX](https://img.shields.io/badge/JavaFX-21-007396?logo=java&logoColor=white)](https://openjdk.org/projects/openjfx/)
[![Maven](https://img.shields.io/badge/Maven-3.9+-C71A36?logo=apachemaven&logoColor=white)](https://maven.apache.org/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

<p align="center">
  <img src="screenshot.png" alt="CRM Pipeline Flow Screenshot" width="800">
</p>

## ✨ Features

| Feature | Description |
|---------|-------------|
| **📋 Kanban Board** | Visual pipeline with 5 customizable stages |
| **🖱️ Drag & Drop** | Move deals between columns effortlessly |
| **📊 Real-time Stats** | Dashboard with total leads, pipeline value, conversion rate |
| **➕ Add/Edit Leads** | Full modal form with all contact details |
| **🖱️ Right-click Menu** | Edit, move, or delete leads instantly |
| **🔍 Search & Filter** | Filter cards by name, company or email in real-time |
| **🎯 Priority System** | HIGH / MEDIUM / LOW with color indicators |
| **💾 Data Persistence** | Auto-saves to local JSON on every change |
| **🌙 Dark UI** | Clean, modern dark theme with color-coded columns |

## 🗂️ Pipeline Stages
┌─────────────┐    ┌─────────────┐    ┌──────────────┐    ┌─────────────┐    ┌─────────────┐
│  New Lead   │ →  │  Contacted  │ →  │Proposal Sent │ →  │   Closed    │ →  │    Lost     │
│   Purple    │    │    Blue     │    │    Orange    │    │    Green    │    │     Red     │
└─────────────┘    └─────────────┘    └──────────────┘    └─────────────┘    └─────────────┘
plain
Copy

## 🚀 Quick Start

### Prerequisites
- Java JDK 21+
- Apache Maven 3.9+

### Installation

```bash
# Clone the repository
git clone https://github.com/ChristopherDond/CRM-Pipeline-Flow.git

# Navigate to project
cd CRM-Pipeline-Flow/crm-pipeline

# Run the application
mvn javafx:run
⚠️ Note: On first run, Maven will download JavaFX and Gson dependencies (1-2 minutes).
🏗️ Architecture
plain
Copy
crm-pipeline/
├── pom.xml
└── src/main/java/com/crm/
    ├── Main.java                 # Application entry point
    ├── model/
    │   └── Lead.java             # Lead data model
    ├── service/
    │   └── LeadService.java      # Business logic + JSON persistence
    └── view/
        ├── KanbanBoard.java      # Main Kanban UI
        └── LeadFormDialog.java   # Add/Edit lead modal
Pattern: MSV (Model-Service-View)
📋 Lead Data Model
Table
Field	Type	Description
name	String	Full name (required)
email	String	Contact email
phone	String	Phone number
company	String	Company name
value	Double	Deal value in USD
priority	Enum	HIGH / MEDIUM / LOW
stage	String	Current pipeline stage
notes	String	Internal observations
created	Date	Auto-set on creation
⌨️ Keyboard Shortcuts
Table
Key	Action
Enter	Save form (when open)
Esc	Close modal
Double-click	Open edit form
Right-click	Context menu
💾 Data Storage
All leads are automatically saved to crm_data.json in the project root. The file updates on every action (add, edit, move, delete) and restores automatically on next launch.
🛠️ Tech Stack
Java 21 (LTS) - Core language
JavaFX 21 - UI framework
Gson 2.10.1 - JSON persistence
Maven 3.9+ - Build tool
🤝 Contributing
Fork the project
Create your feature branch: git checkout -b feature/AmazingFeature
Commit your changes: git commit -m 'Add AmazingFeature'
Push to the branch: git push origin feature/AmazingFeature
Open a Pull Request
📄 License
Distributed under the MIT License. See LICENSE for more information.
<p align="center">
  Built with ☕ and JavaFX by <strong>Christopher Dondé</strong>
</p>
```
