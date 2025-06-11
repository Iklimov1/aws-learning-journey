# IAM Users

An **IAM User** is an identity used for anything requiring **long-term AWS access**, such as:

- Humans (e.g., developers, admins)
- Applications
- Service accounts

## Credentials

IAM Users can be configured with:

- **Username + password** for AWS Management Console access
- **Access key ID + secret access key** for CLI, SDK, or API access

> Avoid hardcoding access keys. Use environment variables or services like AWS Secrets Manager.
## Permissions

IAM Users have **no permissions by default**. Permissions can be granted via:

- **IAM policies attached to the user** (not recommended)
- **Group memberships** (preferred)
- **Assuming IAM roles** for temporary or cross-account access
## Important IAM User Limits

- Maximum **5,000 IAM users** per account
- Each user can be in up to **10 groups**
- Account-wide **password policy** can enforce:
  - Minimum length
  - Complexity rules
  - Password rotation
  - Preventing password reuse

# ARN: Amazon Resource Name

Uniquely identifies AWS resources.

**Format:**  
`arn:partition:service:region:account-id:resource`

**Example (IAM User ARN):**  
`arn:aws:iam::123456789012:user/inna`

## Best Practices

- Enable **MFA (Multi-Factor Authentication)** for all users
- Use **groups** to manage permissions rather than attaching them directly to users
- Prefer **IAM roles** over users for applications and services
- Apply the **principle of least privilege** when assigning permissions
