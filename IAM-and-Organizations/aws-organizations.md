# AWS Organizations

**AWS Organizations** helps manage **multiple AWS accounts** in a **cost-effective** and **centrally governed** way.

## Key Concepts

- **Management account** (formerly called the "Master" account):
  - The account that **creates and manages** the organization.
  - It contains the **payment method** and is also referred to as the **payer account**.

- **Member accounts**:
  - Other AWS accounts that are part of the organization.
  - These accounts are managed by the management account.

- **Organizational Root**:
  - The **top-most node** in the organization’s hierarchy.
  - Not to be confused with the **AWS account root user**.

- **Organizational Units (OUs)**:
  - Allow for **nesting** of accounts into groups under the root.
  - You can apply **Service Control Policies (SCPs)** at the root or OU level to enforce permission boundaries.

## Account Creation

- You **can create new accounts** within AWS Organizations using the console or API.
- Each account must have a **unique email address**.
- Alternatively, you can **invite existing accounts** to join your organization.

## Benefits

- **Centralized billing**: All charges roll up to the management account.
- **Policy-based management**: Use SCPs to set permission guardrails.
- **Account isolation**: Helps apply the principle of least privilege by separating workloads.

> Best Practice: Use **OUs and SCPs** to structure your accounts by function (e.g., dev, test, prod) and control access from a central location.

