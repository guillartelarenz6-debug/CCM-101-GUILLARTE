# CloudNova Enterprise Cloud Infrastructure Operational Manual

## 1. System Overview & Deployment
This document outlines operational workflows for managing the CloudNova multi-tier application stack.

### Launching the Stack
To deploy or start all containerized services:



bash
cd ~/cloudnova-stack
docker compose up -d



bash
docker compose down



bash
sudo ufw default deny incoming
sudo ufw default allow outgoing
sudo ufw allow 22/tcp comment 'SSH Access'
sudo ufw allow 80/tcp comment 'Web Traffic'
sudo ufw allow 8080/tcp comment 'WordPress Port'
sudo ufw enable




bash
sudo ufw status verbose



bash
./automation-script.sh
cat /home/admin1/backups/backup.log
ls -lh /home/admin1/backups/
