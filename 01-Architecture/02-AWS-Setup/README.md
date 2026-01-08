# ☁️ AWS Setup

Ce dossier décrit la configuration AWS utilisée pour déployer le laboratoire SOC.

---

## 🔹 Instances EC2

| Instance | OS | Rôle |
|--------|----|-----|
| EC2-1 | Ubuntu 22.04 | Wazuh Server |
| EC2-2 | Ubuntu 22.04 | Linux Client |
| EC2-3 | Windows Server 2022 | Windows Client |

---

## 🔹 Security Groups

| Port | Source | Usage |
|-----|------|-----|
| 443 | Internet | Accès Wazuh Dashboard |
| 1515 | VPC | Enrollment agents |
| 1514 | VPC | Logs & Events |
| 22 | Admin IP | SSH Linux |
| 3389 | Admin IP | RDP Windows |

---

## 🔐 Sécurité

- Instances isolées dans un VPC dédié
- Accès administrateur limité par IP
- Communication interne sécurisée
