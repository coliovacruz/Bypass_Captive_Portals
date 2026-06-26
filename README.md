# 🔐 Bypassing Wi-Fi Captive Portals — Curso Completo

Curso técnico interativo sobre segurança ofensiva e defensiva de captive portals Wi-Fi. Baseado no módulo do **Hack The Box Academy** e na palestra **DEF CON 24 — Grant Bugher**. Inclui teoria, laboratórios Docker funcionais, CTF challenges e módulos de blue team / hardening.

---

## 📚 Conteúdo do Curso

### Módulos teóricos (38 seções)

| Seção | Tópicos |
|---|---|
| Introdução | Como funcionam captive portals, Chilispot, CoovaChilli, RADIUS, UAM |
| Indirect Exploitation | MAC Spoofing, VPN Bypass, ARP Spoofing, Credential Interception, Session Interception, DNS Tunneling |
| Client Hijacking | Hostile Portal (Evil Twin), Hijacking via Serviço Vulnerável (LLMNR/NBT-NS), HTTPS Downgrade (SSLstrip+), Malware Injection |
| Direct Exploitation | Brute Force, XSS, Command Injection, Host Header, File Upload, LFI/RFI, Granting Own Exception |
| Dispositivos Sem Portal | MAC Authentication Bypass (MAB) — impressoras, câmeras IP, VoIP |
| Perspectiva DEF CON 24 | Chilispot & Sputnik, Ethernet Captive Portals, Preparação Antecipada, MAC Spoofing de Sessões Expiradas |
| Skills Assessment | Metodologia completa, fluxograma de decisão, template de relatório |

### 🧪 Laboratórios Docker (4 labs)

| Lab | Descrição |
|---|---|
| Lab 1 — Portal Básico | CoovaChilli + FreeRADIUS + PHP. Brute force, MAB, reconhecimento |
| Lab 2 — DNS Tunneling | Gateway restrito (UDP 53 only) + servidor iodine pré-configurado |
| Lab 3 — Portal Vulnerável | PHP com SQLi, XSS e file upload sem validação |
| Lab 4 — MAB | Gateway com whitelist de MAC, impressora simulada, atacante isolado |

### 🚩 CTF Challenges

- 4 challenges individuais com flags reais nos labs Docker
- Cenário encadeado **Hotel Paradiso** — 4 etapas do recon ao MAC spoofing

### 🛡️ Blue Team / Hardening

- Anti MAC Spoofing (arpwatch, DHCP binding)
- Bloqueio de DNS Tunneling (rate limiting, filtragem por tipo de registro)
- Hardening do portal web (CSP, fail2ban, PDO, validação de upload)
- Hardening do MAB (DHCP fingerprinting, port binding, monitoramento comportamental)

---

## 🚀 Como usar

### Pré-requisitos

- Docker + Docker Compose instalados
- Browser moderno para abrir o curso

### Abrir o curso

```bash
git clone https://github.com/coliovacruz/Bypass_Captive_Portals.git)
cd captive-portal-course
open index.html   # ou abra o arquivo no browser manualmente
```

### Subir o Lab 1 (Portal Básico)

```bash
cd labs/captive-lab
docker compose up -d
# Acessar o portal: http://localhost:8080
# Container atacante: docker exec -it lab-attacker bash
```

### Subir o Lab 2 (DNS Tunneling)

```bash
cd labs/dns-lab
docker compose up -d
# Container cliente: docker exec -it dns-client bash
```

### Subir o Lab 4 (MAB)

```bash
cd labs/mab-lab
docker compose up -d
# Container atacante: docker exec -it mab-attacker bash
```

---

## 🗂️ Estrutura do Repositório

```
captive-portal-course/
├── captive-portal-course.html              # Curso completo (abrir no browser)
├── README.md

```

---

## 📖 Referências

- [HTB Academy — Bypassing Wi-Fi Captive Portals](https://academy.hackthebox.com/course/preview/bypassing-wi-fi-captive-portals)
- [DEF CON 24 — Grant Bugher: Bypassing Captive Portals](https://www.youtube.com/watch?v=GhUUzGBjhXQ)
- [CoovaChilli Documentation](https://coova.github.io/CoovaChilli/)
- [FreeRADIUS Documentation](https://freeradius.org/documentation/)

---

## ⚠️ Aviso Legal

Este curso é para fins **educacionais e de pentest autorizado** exclusivamente. Nunca aplique estas técnicas em redes sem permissão explícita por escrito. O uso não autorizado das técnicas aqui descritas pode configurar crime conforme a legislação vigente.

---

## 📝 Licença

MIT License — use, adapte e compartilhe com os devidos créditos.
