<p align="center">
  <img src="https://blog.rosnertech.com.br/wp-content/uploads/2023/08/RosnerTech.png" alt="RosnerTech Logo" width="180"/>
</p>

<h1 align="center">legolas-n8n</h1>

<p align="center">
  <img src="https://img.shields.io/badge/n8n-automation-FF6D00?logo=n8n&logoColor=white"/>
  <img src="https://img.shields.io/badge/Docker-✔-2496ED?logo=docker&logoColor=white"/>
  <img src="https://img.shields.io/badge/PostgreSQL-15-336791?logo=postgresql&logoColor=white"/>
  <img src="https://img.shields.io/badge/Redis-7-DC382D?logo=redis&logoColor=white"/>
  <img src="https://img.shields.io/badge/NPM-Reverse%20Proxy-009639"/>
  <img src="https://img.shields.io/badge/License-MIT-green"/>
</p>

<p align="center">
Stack n8n em Docker com PostgreSQL e Redis, integrada ao Nginx Proxy Manager, preparada para homelab e produção.
</p>

---

## 📌 Visão Geral

Este repositório documenta a implantação de um **n8n self-hosted**, com:

- Execução em fila (Redis)
- Banco PostgreSQL dedicado
- Reverse proxy via Nginx Proxy Manager
- Persistência via bind mounts
- Boas práticas de segurança

---

## 🧰 Stack & Ferramentas

- 🐳 Docker + Docker Compose (v2)
- ⚙️ n8n
- 🛢️ PostgreSQL 15
- 🚀 Redis 7
- 🔐 Nginx Proxy Manager
- 🐧 Linux (VPS / HomeLab)

---

## 📂 Estrutura do Projeto

```bash
.
├── docker-compose.yml
├── .env              # NÃO versionado
├── example.env
├── n8n-data/
├── postgres-data/
├── redis-data/
└── README.md
```

---

## 🚀 Subir o n8n

```bash
cp example.env .env
docker compose up -d
```

---

## 🌐 Acesso

O acesso é feito exclusivamente via **Nginx Proxy Manager**, sem portas expostas no host.

```
https://legolas.seudominio.com.br
```

---

## 🔐 Segurança

- Sem portas abertas diretamente
- Variáveis sensíveis fora do Git
- Permissões reforçadas no volume do n8n
- TLS encerrado no NPM

---

## 👨‍💻 Autor

**RosnerTech**  
📧 rosnertech@rosnertech.com.br  
🌐 https://blog.rosnertech.com.br

---

## 📜 Licença

MIT License
