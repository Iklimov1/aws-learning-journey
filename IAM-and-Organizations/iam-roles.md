# IAM Roles

- An **IAM Role** is an identity that is **assumed** by a principal (user, application, device, or service).
- It is **not associated with a specific user** or group.
- Best used for **temporary access** and **cross-account access**.

## Key Concepts

- **Principal**: A trusted entity (e.g., IAM user, AWS service, federated identity) that can assume the role.
- **STS (Security Token Service)**: Issues **temporary credentials** when a principal **assumes** a role.
  - Example API operation: `AssumeRole`
- **IAM Role ARN**: Roles have ARNs and policies but **no password or long-term credentials**.

## Common Use Cases

- **AWS Lambda (function as a service) functions**: Assume a role to access AWS services (e.g., S3, DynamoDB).
- **EC2 instances**: Use an instance profile (a container for a role) to access AWS resources securely.
- **Cross-account access**: Roles allow trusted external accounts to access resources via role assumption.
- **Federated access**: IAM roles are used with **identity federation** to allow SSO from external identity providers (e.g., Active Directory, Google Workspace).

## Notes

- Roles **cannot be deleted** if they are still **attached to active resources** (e.g., EC2 instance profiles).
- **Service-linked roles**: Specific roles created and managed by AWS services. Cannot be manually edited or deleted unless the service is removed.

> ✅ Best Practice: Use **IAM roles** for all machine-to-machine interactions or cross-account access. Never use static credentials in code.

