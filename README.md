# fastapi-nextjs-dev-container

A fully containerized development environment for building modern full-stack web applications using Next.js and FastAPI.

---

## ✨ Features

- ⚡️ Fast tooling via `Bun` and `uv`
- 🧠 Linting with `ESLint` and `ruff`
- 💄 Formatting with `Prettier` and `ruff`
- 🔍 Static type checking with `TypeScript` and `ty`
- 🎨 Frontend styling with `Tailwind CSS`
- 🛠️ Simple developer workflow via `Makefile`
- 🐳 Docker-in-Docker support
- 🔁 Persistent shell history across container rebuilds

## 🚀 Getting Started

### Prerequisites

Make sure you have the following dependencies installed:

- Docker
- VS Code with the "Dev Containers" extension

> **Note:** This dev container is made specifically for VS Code, but it should work with any IDE that has a "Dev Containers" plugin.

### Setup

1.  Clone the repo

```bash
git clone https://github.com/rdguzman-swe/fastapi-nextjs-dev-container.git <your-project>
```

2. Open in VS Code

```bash
code <your-project>
```

3. Reopen in container
   - `Cmd/Ctrl + Shift + P`
   - Select `Dev Containers: Reopen in Container`

4. Initialize the project

```bash
make init
```

---

## 📁 Project Structure

```diff
.
├── .devcontainer/       # Dev container config
├── backend/             # FastAPI app (created on scaffold)
├── frontend/            # Next.js app (created on scaffold)
├── .gitignore
├── .python-version
├── Makefile             # Developer commands
└── README.md
```

---

## 🛠️ Developer Commands

Run `make help` to see a list of all available commands:

```bash
make help
```

| Command            | Description                          |
| ------------------ | ------------------------------------ |
| `make init`        | Full setup (scaffold + install)      |
| `make scaffold`    | Create backend & frontend if missing |
| `make backend`     | Run FastAPI server                   |
| `make frontend`    | Run Next.js development server       |
| `make post-create` | Re-run container setup script        |

---

## ▶️ Running the App

### Start Frontend

```bash
make frontend
```

- Runs on port 3000

### Start Backend

```bash
make backend
```

- Runs on port 8000

---

## ⚙️ Dev Container Details

### Preinstalled Tools

- Bun
- uv
- Python
- Git
- curl
- Build tools

### VS Code Extensions

- Tailwind CSS
- ESLint
- Prettier
- Python
- Pylance
- Ruff
- ty
- Docker
