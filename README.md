# one-docs (One Suite Documentation)

Welcome to the official documentation for One Suite, which includes the following products:
- **OneLead** - A Frappe-based app for Meta and Google integration. [OneLead Repository](https://github.com/redsoftware-hq/onelead)
- **OneInbox** - A unified inbox solution. [OneInbox Repository](https://github.com/redsoftware-hq/oneinbox)
- **OneInbox_WhatsApp** - WhatsApp integration for seamless communication. [(Forked frappe_whatsapp)](https://github.com/shridarpatil/frappe_whatsapp)

This repository contains the documentation for these products, built using **MkDocs** with the Material theme. The documentation is hosted on GitHub Pages.

## Local Setup

To run the documentation locally and make changes, follow these steps:

### Prerequisites
Ensure you have the following installed:
- **Python (3.x)**: [Download here](https://www.python.org/downloads/)
- **Git**: [Download here](https://git-scm.com/downloads)


### Installation Steps
1. **Clone the Repository**
   ```bash
   git clone https://github.com/YOUR_GITHUB_USERNAME/one-docs.git
   cd one-docs
   ```
2. **(Optional) Virtual Environment**
   ```bash
    python -m venv venv
    source venv/bin/activate  # On Mac/Linux
    venv\Scripts\activate     # On Windows
   ```

3. **Install Dependencies**
   ```bash
   pip install mkdocs-material
   ```
   or
  ```bash
  pip install -r requirements.txt
  ```

4. **Run Locally**
   ```bash
   mkdocs serve
   ```
   This will start a local server at:
   ```bash
   http://127.0.0.1:8000/
   ```
   Open this link in your browser to preview the documentation.

5. **Stop the Server**
   To stop the local server, press **Ctrl + C** in the terminal.

---

## Contribution Guide

We welcome contributions to improve this documentation. Follow these guidelines to contribute:

### 1. If You Make Changes in OneLead or OneInbox
- If you **raise a Pull Request (PR) in OneLead or OneInbox**, please ensure that you **also update the relevant documentation in this repository**.
- Attach the **OneLead/OneInbox PR** to the **documentation PR** for reference.
- Ensure that the documentation clearly explains any new features, API changes, or installation steps.

### 2. Make Your Changes
- Edit Markdown files in the `docs/` directory.
- Follow the existing structure when adding new documentation.
- Use **clear and concise language**.
- Include **code snippets, screenshots, or examples** where relevant.
- Run `mkdocs serve` to preview your changes before submitting a PR.

### 3. Follow Contribution Guidelines
- Ensure documentation is **accurate and up to date**.
- Use **proper formatting and Markdown syntax**.
- Keep descriptions **clear and user-friendly**.
- For API changes, **include request and response examples**.
- If adding a new section, update `mkdocs.yml` for navigation.


## Deployment  (restricted to maintainers and auto-deploy on PR merge)

To deploy updates to GitHub Pages, run:
```bash
mkdocs gh-deploy
```
This will build and publish the documentation at:
```
https://yourusername.github.io/one-docs/
```


## License
This documentation is released under the **MIT License**.

For any questions or feedback, feel free to open an issue in this repository.
