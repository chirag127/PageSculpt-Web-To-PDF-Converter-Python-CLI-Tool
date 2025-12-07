# ⛓️ PageSculpt Security Policy

The `PageSculpt-Web-To-PDF-Converter-Python-CLI-Tool` project is built with security and reliability as top priorities. Given its function of fetching and rendering external web content, we emphasize robust input validation, dependency management, and secure execution environments.

We adhere to the highest industry standards (OWASP Top 10, CWE principles) to protect users against vulnerabilities, particularly Remote Code Execution (RCE) and Local File Inclusion (LFI) risks associated with CLI tools handling external data.

## 1. Reporting a Vulnerability

We sincerely appreciate the efforts of security researchers and the community in disclosing vulnerabilities responsibly.

**DO NOT** open a public GitHub issue.

Please report security issues using the private vulnerability reporting mechanism offered by GitHub:

1.  Navigate to the security tab of the repository: [https://github.com/chirag127/PageSculpt-Web-To-PDF-Converter-Python-CLI-Tool/security](https://github.com/chirag127/PageSculpt-Web-To-PDF-Converter-Python-CLI-Tool/security)
2.  Click "Report a vulnerability."
3.  Provide a detailed description of the vulnerability, including steps to reproduce, potential impact, and suggested mitigations.

### Response Timeline

We aim to acknowledge receipt of vulnerability reports within **48 hours**. Critical vulnerabilities will be addressed via a patch release within **7 days** of verification.

## 2. Supported Versions

Only the latest stable release of `PageSculpt` is actively supported and receives security updates.

| Version | Supported |
| :---: | :---: |
| Latest Stable (e.g., 1.x) | ✅ Yes |
| Older Versions | ❌ No |

Users are strongly encouraged to always use the latest release to ensure they have the most recent security patches.

## 3. General Security Practices

As a high-velocity Python CLI tool, we enforce the following security directives:

### 3.1 Dependency Auditing (Supply Chain Security)

We utilize the `uv` package manager for deterministic and secure dependency resolution.
*   All dependencies are audited upon inclusion.
*   We regularly run automated checks for known CVEs using tools like Dependabot and GitHub Security Advisories.
*   Dependencies with known security flaws are promptly updated or replaced.

### 3.2 Input and URL Validation

Since PageSculpt fetches external content, strict input validation is critical:
*   All user-provided URLs and file paths are sanitized, normalized, and validated against allowed schemes (HTTP/HTTPS) to prevent URI attacks.
*   Execution of arbitrary code or injection into the underlying rendering engine (e.g., system calls to `wkhtmltopdf` or browser automation libraries) is strictly prohibited and shielded by API abstractions.

### 3.3 File System Interaction (LFI Prevention)

When handling output paths via the CLI:
*   Absolute paths are preferred, and any relative path manipulation is strictly contained within the project's working directory context.
*   We use Python's `pathlib` for safe, cross-platform file path management, actively preventing directory traversal (`..`) attacks in user input designated for file output.

## 4. Responsible Disclosure Policy

By submitting a vulnerability report, you agree to our responsible disclosure policy, which requires you to keep all information regarding the vulnerability confidential until we have released an official fix. We commit to crediting responsible reporters in our release notes unless anonymity is explicitly requested.