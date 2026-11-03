# AWS Security Group Configuration

## Project: Highly Available Web Application

Security Groups act as virtual firewalls that control inbound and outbound traffic.

## 1. Load Balancer Security Group

| Type | Protocol | Port | Source |
|---|---|---:|---|
| HTTP | TCP | 80 | 0.0.0.0/0 |
| HTTPS | TCP | 443 | 0.0.0.0/0 |

## 2. EC2 Web Server Security Group

| Type | Protocol | Port | Source |
|---|---|---:|---|
| HTTP | TCP | 80 | Load Balancer Security Group |
| SSH | TCP | 22 | Your trusted IP address |

## 3. Security Best Practices

- Allow only required ports.
- Restrict SSH access to trusted IP addresses.
- Allow web traffic from the Load Balancer security group.
- Avoid opening all ports to the internet.
- Review security rules regularly.

**Note:** These are example rules. Update them to match your actual AWS configuration.