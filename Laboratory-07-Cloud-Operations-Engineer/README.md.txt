
### 📄 `README.md`
```markdown
# Laboratory 07 – Cloud Operations Engineer

## Mission Overview
This laboratory activity transitions from deployment to operations (SRE). Using a KillerCoda Ubuntu Playground, I established a baseline for server health, deployed a containerized Nginx web server, generated web traffic, and used Docker logs and metrics to verify the application's health.

## Objectives
- Utilize native Linux CLI tools to monitor host CPU, Memory, and Disk capacity.
- Deploy a web container and track its real-time performance using Docker metrics.
- Generate web traffic and extract application access logs for analysis.
- Translate raw performance data into a readable technical report using Markdown.

## Monitoring Commands Executed
```bash
# Host Baseline
free -h
df -h /
top

# Deploy Nginx
docker run -d --name client-website -p 8080:80 nginx

# Generate Traffic
curl http://localhost:8080
curl http://localhost:8080/hidden-admin-page

# Observability
docker logs client-website
docker stats