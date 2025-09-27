You are a senior DevOps engineer. I want a detailed, phased implementation plan to deploy a secure home lab stack consisting of WireGuard (VPN), Pi-hole (DNS filtering), and Unbound (recursive DNS) from initial setup to production readiness.

Please break it down into phases:

1. **Planning & Requirements**
   - Define project goals (remote secure access, DNS filtering, privacy)
   - Identify hardware (Raspberry Pi 5 4GB and Docker host)
   - Network prerequisites (ports, NAT, DDNS if needed)

2. **Design & Architecture**
   - High-level network topology (VPN clients, server, DNS flow)
   - Security considerations (firewall rules, key management)
   - Decision on deployment style: bare metal, Docker

3. **Environment Setup**
   - Install OS (Raspberry Pi OS recommended)
   - Update & harden system
   - Prepare prerequisites (Docker, systemd, or packages)

4. **Implementation (Service Setup)**
   - Install & configure WireGuard
   - Install & configure Pi-hole
   - Configure Pi-hole to use Unbound as upstream DNS
   - Test locally before exposing externally

5. **Testing & QA**
   - Verify VPN connectivity (client ↔ server)
   - Verify DNS filtering works via Pi-hole logs
   - Verify Unbound resolves directly via root servers
   - Test performance & stability (latency, throughput)

6. **Deployment Preparation**
   - Configure port forwarding on router/firewall
   - Secure WireGuard (non-standard UDP port, key rotation)
   - Setup dynamic DNS if ISP IP is dynamic
   - Backup configs & keys

7. **Production Go-Live**
   - Connect external client (mobile/laptop outside LAN)
   - Force DNS to Pi-hole via VPN config
   - Verify secure remote access + DNS filtering works
   - Document credentials and topology

8. **Post-Production (Maintenance)**
   - Monitoring: Pi-hole dashboard, WireGuard peers, logs
   - Patch management (system updates, Pi-hole/Unbound updates)
   - Backup & disaster recovery plan (config snapshots)
   - Continuous improvement (add more clients, automate with Ansible/Terraform)

For each phase:
- Suggest best practices
- Provide example configs/checklists
- Recommend common tools (e.g., UFW, Docker Compose, Portainer)

Make the guide clear, concise, and structured as a professional roadmap for production.
