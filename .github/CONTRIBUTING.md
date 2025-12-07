# Contributing to PageSculpt-Web-To-PDF-Converter-Python-CLI-Tool

We welcome contributions to `PageSculpt-Web-To-PDF-Converter-Python-CLI-Tool`! To ensure a smooth and collaborative development process, please adhere to the following guidelines.

## 1. Code of Conduct

This project adheres to the Contributor Covenant Code of Conduct. Please ensure your contributions are respectful and inclusive.

## 2. Project Philosophy & Architecture (Late 2025 Standards)

This project is built on the principles of **Zero-Defect, High-Velocity, and Future-Proof development**. We leverage a **Modular Monolith** architecture for our Python CLI tool, prioritizing clear separation of concerns, maintainability, and robust performance. The core toolchain includes **Python 3.10+**, **uv** for package management, **Ruff** for lightning-fast linting/formatting, and **Pytest** for comprehensive testing.

## 3. Development Workflow

Our workflow is designed for efficiency and quality:

1.  **Fork the Repository:** Create your own fork of the `chirag127/PageSculpt-Web-To-PDF-Converter-Python-CLI-Tool` repository.
2.  **Clone Your Fork:** Clone your forked repository to your local machine.
    bash
    git clone https://github.com/YOUR_USERNAME/PageSculpt-Web-To-PDF-Converter-Python-CLI-Tool.git
    cd PageSculpt-Web-To-PDF-Converter-Python-CLI-Tool
    
3.  **Set Up Development Environment:**
    *   Ensure you have Python 3.10+ installed.
    *   Install the project's dependencies using `uv`:
        bash
        uv venv  # Or your preferred virtual environment tool
        source .venv/bin/activate # On Windows use `source .venv/Scripts/activate`
        uv pip install -e .[dev]
        
4.  **Create a New Branch:** Create a descriptive branch for your changes.
    bash
    git checkout -b feature/your-feature-name
    
5.  **Make Your Changes:** Implement your feature or bug fix.
6.  **Lint & Format:** Ensure your code adheres to our standards.
    bash
    ruff check .
    ruff format .
    
7.  **Run Tests:** Execute the test suite to ensure no regressions.
    bash
    pytest
    
8.  **Commit Your Changes:** Commit your changes with clear and concise messages.
    bash
    git add .
    git commit -m "feat: Add descriptive commit message"
    
9.  **Push to Your Fork:** Push your branch to your fork on GitHub.
    bash
    git push origin feature/your-feature-name
    
10. **Open a Pull Request:** Create a Pull Request from your fork to the `main` branch of the `chirag127/PageSculpt-Web-To-PDF-Converter-Python-CLI-Tool` repository.

## 4. Pull Request Guidelines

*   **Descriptive Title & Body:** Provide a clear title summarizing your changes and a detailed body explaining the 'why' and 'how'. Reference any related issues.
*   **Single Responsibility:** Each PR should ideally address one specific issue or feature.
*   **Testing:** Ensure all new code is accompanied by appropriate unit or integration tests.
*   **Code Review:** Be prepared to address feedback from reviewers.

## 5. Reporting Issues

*   **Use the Issue Template:** Please use the provided bug report template (`.github/ISSUE_TEMPLATE/bug_report.md`) when reporting issues.
*   **Provide Details:** Include clear steps to reproduce, expected vs. actual behavior, environment details (Python version, OS), and any relevant logs or screenshots.

## 6. Feature Requests

*   **Open an Issue:** For feature requests, open a new issue and clearly describe the proposed feature and its benefits.

## 7. Dependencies

*   **Python Package Management:** We use `uv` for managing dependencies. Please ensure any new dependencies are added to `pyproject.toml` and installed correctly.
*   **Virtual Environments:** Always work within a dedicated virtual environment.

## 8. Architectural Principles

*   **SOLID:** Adhere to the SOLID principles of object-oriented design.
*   **DRY:** Don't Repeat Yourself.
*   **YAGNI:** You Ain't Gonna Need It.
*   **Modularity:** Favor small, independent modules.

Thank you for contributing to `PageSculpt-Web-To-PDF-Converter-Python-CLI-Tool`!
