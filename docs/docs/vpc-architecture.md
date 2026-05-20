# VPC Architecture Documentation

```text
AWS Cloud
│
└── VPC
    │
    ├── Public Subnet
    │     │
    │     ├── EC2 Instance
    │     │      ├── Jenkins
    │     │      ├── Docker
    │     │      └── Application
    │     │
    │     └── Internet Gateway
    │
    └── Security Group
          ├── Port 22  (SSH)
          ├── Port 80  (HTTP)
          ├── Port 443 (HTTPS)
          └── Port 8080 (Jenkins)
```

## VPC Components
- VPC
- Public Subnet
- Internet Gateway
- EC2 Instance
- Security Group

## Open Ports
- 22 → SSH
- 80 → HTTP
- 443 → HTTPS
- 8080 → Jenkins

## Security Improvements
- Disabled unused ports
- Restricted inbound access
- IAM MFA enabled
- Password policy enabled
