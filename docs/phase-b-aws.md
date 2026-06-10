# Phase B1 — Week 3 (AWS architecture, VM not required)

## Diagram

(Drawing or ASCII: Internet → security group → EC2 → nginx or Docker)

## Inbound ports (security group)

| Port | Protocol | Source | Usage |
|------|----------|--------|--------|
| 22 | TCP |Your IP-adresse only | SSH |
| 80 or 5000 | TCP |everyone | HTTP |

**Why is opening SSH (22) to 0.0.0.0/0 dangerous in production?**

0.0.0.0/0 means 'allow connections from ANYONE on the internet.' This is extremely dangerous for SSH because:
•Bots and hackers constantly scan the internet for open port 22. If found, they attempt thousands of password or key combinations per second (brute-force attack).
•Even with a strong password, an exposed SSH port is a high-value attack target.

## Commands you would run on the VM

```bash
ssh -i key.pem ubuntu@PUBLIC_IP
sudo apt update && sudo apt install -y nginx
curl http://localhost
```

Explain the role of: **SSH key**, **public IP**, **security group**.

 SSH key; You use it to connect securely without a password. Only someone with the private key can log in.

 public IP;the public IP changes every time the instance restarts unless you use an Elastic IP.

 security group; It controls which ports and IP addresses are allowed to send traffic to your server.

## Technical choices

- AWS region and why:
- Instance type (e.g. t2.micro):
- Why **terminate** the instance after a lab:
