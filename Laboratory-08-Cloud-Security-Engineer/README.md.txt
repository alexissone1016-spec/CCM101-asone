
### `README.md`
```markdown
# Laboratory 08 — Cloud Security Engineer

## Mission Overview
Deployed a vulnerable Nginx web application, audited open ports, and hardened an Ubuntu server with UFW using a Default Deny policy plus granular allow rules for SSH and HTTP/8080.

## Objectives
- Apply the Principle of Least Privilege and reduce attack surface
- Audit listening ports on a Linux host
- Enforce a UFW Default Deny incoming policy
- Selectively allow SSH and TCP 8080
- Document rules and rationale in Markdown

## Commands Executed
```bash
docker run -d --name secure-web-app -p 8080:80 nginx
curl -i http://localhost:8080
sudo ss -tulpn
sudo ufw allow ssh
sudo ufw default deny incoming
sudo ufw default allow outgoing
sudo ufw enable
sudo ufw status verbose
sudo ufw allow 8080/tcp
sudo ufw status numbered
curl -i http://localhost:8080