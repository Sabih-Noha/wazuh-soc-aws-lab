# 🧱 Architecture Cloud SOC – Wazuh on AWS

Ce dossier décrit l’architecture complète du laboratoire SOC déployé sur Amazon Web Services.

---

## 🔹 Infrastructure

| Composant | Description |
|---------|------------|
| VPC | 10.0.0.0/16 |
| Subnet | Public Subnet 10.0.1.0/24 |
| Wazuh Server | EC2 Ubuntu 22.04 |
| Linux Client | EC2 Ubuntu 22.04 |
| Windows Client | EC2 Windows Server 2022 |

---

## 🔹 Flux réseau

| Port | Usage |
|-----|-----|
| 443 | Accès au dashboard Wazuh |
| 1515/TCP | Enrôlement des agents |
| 1514/TCP | Logs & événements sécurité |
| 22 | SSH Linux |
| 3389 | RDP Windows |

---

## 🔹 Fonctionnement

- Les agents Linux et Windows envoient leurs logs vers le serveur Wazuh
- Wazuh agit comme SIEM + EDR
- Toutes les attaques sont détectées et journalisées

---

## 🎯 Objectif

Mettre en place une architecture SOC Cloud sécurisée simulant un environnement réel de supervision de sécurité.
