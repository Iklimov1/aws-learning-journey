# A & AAAA records
- A records: they map a hostname like www.gooogle.com to an IPV4 address
- AAAA records: similar to the A records but map to a IPV6 address
# CNAME record
- CNAME acts as an alias. It allows one domain to point to another without the use of IP.
- It MUST point to another domain NOT an IP

# MX record
- mail exchange directs email to a mail server
- It includes a priority value(lower num= higher delivery priority) and the mail server hostname
- A trailing dot marks the fully qualified domain name

# NS record
- Name server designates which DNS servers have authority for a domain/subdomain allowing delegation within the hierarchy

# TXT record 
- Text records allow arbitrary text strings in DNS entries

# TTL
- Time to live filed specifies how long a resolver should cache the DNS record (measured in seconds)
- A shorter TTL value allows faster updates but it increases lookup frequency so longer TTL values reduce query traffic