# CopilotStudioSNOWAgent
Accelerator for Copilot Studio ServiceNow Agent


# ⚠️ Disclaimer

This repository contains **demonstration / sample code** intended for
educational and illustrative purposes only.

- ❌ Not production-ready
- ❌ No security hardening
- ❌ No SLA or support commitment

Use at your own risk. The authors assume no responsibility for use of this
code in production environments.

# CopilotStudioSNOWAgent
Accelerator for Copilot Studio ServiceNow Agent


# ⚠️ Disclaimer

This repository contains **demonstration / sample code** intended for
educational and illustrative purposes only.

- ❌ Not production-ready
- ❌ No security hardening
- ❌ No SLA or support commitment

Use at your own risk. The authors assume no responsibility for use of this
code in production environments.


## Prerequisites

Before importing this solution, ensure the following managed solution is installed in the target Power Platform environment.

| Requirement | Value |
|------------|-------|
| Managed Solution Name | AI Solution default templates |
| Unique Name | msdyn_AISolutionDefaultTemplates |
| Minimum Version | ${AI_SOLUTION_DEFAULT_TEMPLATES_VERSION} |

> ⚠️ **Important**  
> Import will fail if this managed solution is not present in the environment.

### Version Parameters

```text
AI_SOLUTION_DEFAULT_TEMPLATES_VERSION=202601.2.6.1

> ✅ **Deployment Note**
> The `AI Solution default templates` managed solution is automatically available in environments where Copilot Studio is enabled.  
> If importing into a restricted or newly provisioned environment, verify that Copilot Studio has been initialized before importing this solution.
``
