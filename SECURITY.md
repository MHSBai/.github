# Security Policy for MHSB Solutions

As a forward-deployed engineering firm operating in the legal vertical, MHSB Solutions treats security, data provenance, and confidentiality as foundational infrastructure, not afterthoughts. 

Our systems handle intake routing, conflict screening, and drafting pipelines for regulated organizations. We operate under the assumption that all data flowing through our architecture may be subject to attorney-client privilege, work-product doctrine, or strict PII/PHI regulations.

We take all security vulnerabilities seriously and are committed to a Coordinated Vulnerability Disclosure (CVD) process.

## Supported Versions

We provide security updates for the latest major versions of our active open-source and proprietary tools. If you are operating a legacy deployment, please consult your MatterCare Optimization SLA or contact your MHSB integration lead.

| Version | Supported          | Notes |
| ------- | ------------------ | ----- |
| `1.x`   | :white_check_mark: | Active development and security patches |
| `< 1.0` | :x:                | Deprecated. Please upgrade to latest stable release |

## Reporting a Vulnerability

**Do not report security vulnerabilities through public GitHub issues, discussions, or pull requests.** 

Public disclosure of a vulnerability before a patch is deployed puts our law firm partners and their clients at risk. 

If you believe you have found a security vulnerability in any MHSB Solutions repository, system, or Lawmatics integration engine, please email us immediately at:

📧 **security@mhsbsolutions.com**

### What to include in your report:
To help us triage and resolve the issue quickly, please include:
*   **Target:** The specific repository, MCP server, or integration flow affected.
*   **Type:** The class of vulnerability (e.g., Prompt Injection, IDOR, SSRF, Authorization Bypass).
*   **Steps to Reproduce:** A benign, non-destructive proof of concept (PoC) or explicit steps to recreate the issue.
*   **Impact:** Your assessment of how this could be exploited (e.g., "Allows bypass of the deterministic conflict-check gate," or "Permits cross-tenant data leakage in the LLM context window").

## Our Response Process (SLA)

When you submit a vulnerability report, you can expect the following operational cadence:

1.  **Acknowledgment (Within 24 Hours):** We will acknowledge receipt of your report and begin our triage process.
2.  **Triage & Verification (Within 48 Hours):** We will confirm the vulnerability and assess its severity (CVSS) and potential impact on attorney-client data.
3.  **Remediation & Patching:** We will develop, test, and deploy a patch. The timeline depends on severity, but critical vulnerabilities affecting data isolation or prompt integrity are treated as drop-everything emergencies.
4.  **Coordinated Disclosure:** Once the vulnerability is mitigated and our partners are secured, we will coordinate with you on public disclosure (and attribution, if desired).

## Legal AI Threat Models

Because we build deterministic, human-in-the-loop AI systems for the legal profession, we are particularly interested in vulnerability reports concerning:
*   **Prompt Injection / Jailbreaking:** Attempts to force our MCP servers or LLM integrations to bypass hard gates or execute unauthorized tool calls.
*   **Data Exfiltration:** Mechanisms that could trick an AI agent into summarizing or exposing confidential matter data to unauthorized endpoints.
*   **Role-Based Access Control (RBAC) Bypass:** Flaws that would allow an associate or paralegal to view partner-level dashboards or sealed matter records.
*   **Lawmatics API Abuse:** Misconfigurations or flaws that could result in unauthorized pipeline movement, data overwrites, or webhook manipulation.

## Safe Harbor

MHSB Solutions supports safe harbor for security researchers. We will not pursue legal action against researchers who discover and report vulnerabilities in good faith, provided they adhere to this policy, do not exploit the vulnerability beyond what is necessary to prove its existence, and do not compromise, alter, or expose live client data.

---
*For general inquiries, workflow audits, or ABA Formal Opinion 512 readiness diagnostics, please visit [efficient.esq](https://efficient.esq) or [mhsbsolutions.com](https://mhsbsolutions.com).*
