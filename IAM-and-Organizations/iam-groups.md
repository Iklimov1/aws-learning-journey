# IAM Groups
- **IAM Groups** are **containers** for IAM users.
- They are **not identities** themselves:
  - You **cannot log in** as a group.
  - They **cannot be assigned an ARN** directly or referred to as a principal.
- **Purpose**: To simplify permission management by assigning policies to a group of users.
- **Permissions** applied to a group are **inherited** by all its members.
- **No group nesting**: You cannot put a group inside another group.
- **Limit**: A maximum of **300 IAM Groups** per AWS account (without special support).

> Best Practice: Attach permissions to **groups**, not directly to users, for easier management and auditing.
