# IAM policies (policy documents)
- It is a set of security statements to AWS
- It grants or denies access to AWS products/features to any identity which uses that policy
- can have 1+ statements
## consistent rules: DENY ALLOW DENY
- explicit denies: overrules ALL other rules
- explicit allows: these take affect unless there is an explicit deny
- implicit deny (default): REMEMBER: if they're not allowed access they're not allowed!
## 2 main types of policies
Inline & Managed: the same thing technically but handled differently
Inline:
- applying JSON to each account individually
- isolated bits of JSON
- best if used for exceptions/special occasions
Managed:
- created as its own object
- reusable
