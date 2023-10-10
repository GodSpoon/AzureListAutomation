## Azure List Automation Template 

Intended for Creating Automations in a Similar Fashion to MozzieMozz's "Teams Phone Automation" project

Original Author: Martin Heusser | M365 Apps & Services MVP

Please check out his [blog post](https://medium.com/@mozzeph/teams-phone-number-management-on-a-budget-e25d53f65caf) and [Github Repository](https://github.com/mozziemozz/TeamsPhoneAutomation)!

---

### Overview

#### Project Structure

- `.git` and `.gitignore`: For version control.
- `.vscode`: IDE-specific settings (optional).
- `Deploy.ps1`: Main deployment script.
- `Functions`: Contains helper functions for Microsoft Graph.
- `Modules`: Holds reusable PowerShell modules.
- `Resources`: Contains environment configurations and resources.
- `Scripts`: Holds auxiliary scripts.
- `Setup`: Contains setup scripts and configurations.

#### Templated Modifications

a. Deployment Script (`Deploy.ps1`)

- Utilize parameterized or relative paths instead of hard-coded paths like `C:\\Temp`.
- Integrate CLI for Microsoft 365 commands where applicable.

b. Setup Script (`Setup.ps1`)

- Ensure essential variables (Tenant ID, Automation Account Name, etc.) are parameterized.
- Make the path for `Resources\\Environment.json` parameterized or relative.
- Use CLI for Microsoft 365 commands for interactions with Microsoft 365 services, where possible.

c. Environment Configuration (`Resources\\Environment.json`)

- Ensure all environment-specific configurations are isolated to this JSON file.
- Provide a sample configuration with placeholder values and clear documentation for each attribute.

d. Functions

- Ensure functions, especially those interacting with Microsoft Graph, are modular and documented.
- Use CLI for Microsoft 365 commands for Microsoft 365 service interactions, where possible.

e. Documentation

- Updated README.md
   -  Document the purpose of each script, order of execution, prerequisites, and assumptions.
   - Provide a step-by-step setup and usage guide.

- In-Script Documentation
   - Include comments explaining the purpose, input parameters, and expected output of each script.

f. Integration with CLI for Microsoft 365

- Replace PowerShell logic with CLI for Microsoft 365 commands for interactions with Microsoft 365 services.

