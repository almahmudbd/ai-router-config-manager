# Provider Manager — Codex & Claude

A unified, secure configuration manager for managing multiple API providers for **Claude** and **Codex**. This tool allows you to store, organize, and switch between different AI provider configurations through a simple GUI.

## ✨ Features

- **Encrypted Database**: All provider information (API keys, models, URLs) is stored in an encrypted file (`providers.enc`) protected by a password of your choice.
- **Unified Management**: Manage both Claude and Codex providers in a single application.
- **Automatic Config Generation**:
  - **Claude**: Generates `settings.json` with your API keys and environment settings.
  - **Codex**: Generates `auth.json` and `config.toml` files automatically.
- **Easy Import**: Import existing configurations from `settings.json`, `auth.json`, `.toml` files, or Codex backups.
- **Provider Switching**: Quickly set an "Active" provider to generate configurations instantly.
- **Security First**: Uses `cryptography` (Fernet) with PBKDF2 key derivation to ensure your secrets remain safe.

## 🚀 Getting Started

### Prerequisites

- **Python 3.x** installed on your system.
- A terminal or command prompt.

### Installation

1. **Clone or download** this repository to your local machine.
2. **Install dependencies** using `pip`:

   ```bash
   pip install -r requirements.txt
   ```

### Usage

#### Running the application

On **Windows**, you can simply run:

```cmd
run.bat
```

Or via **Python**:

```bash
python manager.py
```

#### Using the tool

1. **Set a Password**: Upon first launch, you will be prompted to create a new database password. **Do not forget this password**, as it is required to access your providers.
2. **Add Providers**: Click **Add** to create a new provider entry for either Claude or Codex.
3. **Configure Details**: Enter the Name, API Key, Base URL, and Model.
4. **Generate Configs**:
   - Select your desired Claude/Codex settings path.
   - Select the provider you want to use.
   - Click **Set Active**.
   - Click **Generate Config**.
5. **Importing**: Use the **Import** button to bring in existing configurations from your current setup.

## 🛠️ Technical Details

- **GUI Framework**: `tkinter`
- **Encryption**: `cryptography` (Fernet symmetric encryption)
- **Storage Format**: Encrypted JSON

## 🛡️ Security & Sharing

**IMPORTANT: Never share your `providers.enc` file with anyone!** It contains your encrypted provider data.

If you want to share this project (e.g., on GitHub), ensure you only include the following files:

- `manager.py` (The main application)
- `requirements.txt` (Dependency list)
- `run.bat` (Windows launcher)
- `run.sh` (Linux launcher)
- `README.md` (Documentation)

### 🚫 DO NOT SHARE:
- `providers.enc` (Contains your encrypted database)
- Any generated `settings.json`, `auth.json`, or `config.toml` files.
- `__pycache__/` directories.

