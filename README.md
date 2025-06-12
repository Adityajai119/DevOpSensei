# DevOpSensei

DevOpSensei is a full-stack DevOps assistant designed to help teams automate, visualize, and manage their development pipelines. It provides actionable insights, requirement tracking, plugin-based extensions, and a user-friendly interface for both developers and operations engineers.

## Table of Contents

- [Features](#features)
- [Architecture](#architecture)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Configuration](#configuration)
- [Running the Application](#running-the-application)
- [Folder Structure](#folder-structure)
- [Testing](#testing)


## Features

- **Requirement Management**: Track and manage project requirements.
- **Pipeline Visualization**: View and analyze DevOps pipeline steps.
- **Plugin Architecture**: Extend functionality via custom plugins.
- **User Authentication**: Secure user login and registration flows.
- **Multi-language Support**: Built-in internationalization (i18n) support.

## Architecture

DevOpSensei is composed of two main components:

1. **Backend (Flask)**
   - RESTful API endpoints for data management (`backend/app/`)
   - SQLite database for persistence (`app.db`, `database.db`)
   - Configuration managed via `config.py`

2. **Frontend (Semantic UI)**
   - Static HTML pages and Semantic UI assets (`frontend/`)
   - Responsive layouts for different DevOps views

## Prerequisites

- Python 3.8+
- pip (Python package manager)
- (Optional) virtualenv or conda for isolated environments

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/Adityajai119/DevOpSensei.git
   cd DevOpSensei
   ```

2. Create and activate a virtual environment (recommended):
   ```bash
   python3 -m venv venv
   source venv/bin/activate
   ```

3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## Configuration

1. Copy the template config file and update values:
   ```bash
   cp env.yaml.tpl env.yaml
   # Edit env.yaml with your settings
   ```

2. (Optional) Modify `backend/config.py` for advanced options.

## Running the Application

### Local Development (Unix)

```bash
# Start the backend server
bash run.sh

# Open http://localhost:5000 in your browser
``` 

### Windows (via run.bat)

```batch
run.bat
``` 

## Folder Structure

```plaintext
/DevOpSensei
├── backend/           # Flask application and API
├── frontend/          # HTML views and Semantic UI assets
├── db/                # Database files and migration scripts
├── static/            # Static assets (CSS, JS, images)
├── i18n/              # Internationalization files
├── Dockerfile         # Docker image definition
├── build.sh           # Build automation script
├── requirements.txt   # Python dependencies
└── README.md          # Project overview and setup instructions
```

## Testing

Run unit tests for the backend:

```bash
python backend/test.py
```

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/your-feature`)
3. Commit your changes
4. Open a pull request

Please refer to `CONTRIBUTING.md` (if provided) for detailed guidelines.
