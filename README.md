# n8n-workflow

This repository contains local n8n workflows exported as JSON files. Follow the instructions below to set up n8n locally and import the workflows.

## Prerequisites

Before getting started, ensure you have the following installed on your local machine:
* [Node.js](https://nodejs.org) (v18 or higher recommended) OR [Docker](https://docker.com)
* A terminal or command prompt

## Getting Started

### 1. Running n8n Locally

Choose **one** of the methods below to run n8n on your computer:

#### Option A: Using NPM (Fastest)
Run the following command in your terminal:
```bash
npx n8n
```

#### Option B: Using Docker
Run this command to pull and start the n8n container:
```bash
docker run -it --rm --name n8n -p 5678:5678 n8nio/n8n
```

Once started, open your browser and navigate to: `http://localhost:5678`

---

## How to Import Workflows from this Repository

To use the workflows (`.json` files) provided in this repository, follow these steps:

1. **Download the Workflow**: Clone this repository or download the specific `.json` file you want to use to your local computer.
2. **Open n8n**: Go to your local n8n dashboard (`http://localhost:5678`).
3. **Create New Workflow**: Click on **Workflows** > **Add Workflow** (or open an empty canvas).
4. **Import File**: 
   * Click on the **Menu icon** (three dots) or the **Workflows** dropdown menu at the top right/left of the editor canvas.
   * Select **Import from File**.
   * Choose the downloaded `.json` file from your local machine.
5. **Configure Credentials**: 
   * *Note:* For security reasons, API keys and credentials are not included in the exported files. 
   * Double-click any nodes that require authentication (e.g., Gmail, database, or external APIs) and add your own credentials.
6. **Save and Activate**: Click **Save** in the top right corner, and toggle the **Active** switch if you want the workflow to run automatically.

---

## Contributing
If you want to add new workflows to this repository:
1. Export your workflow from the n8n UI (**Workflows** > **Download**).
2. Save the `.json` file into this directory.
3. Commit and push your changes to GitHub.
