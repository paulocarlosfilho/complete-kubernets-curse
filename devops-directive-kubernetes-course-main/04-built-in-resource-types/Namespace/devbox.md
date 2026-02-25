# 📦 Devbox - Guia Prático (Java, Spring & Postgres)

Ambiente isolado para o curso de Kubernetes e Desenvolvimento Java.

---

## 🛠️ Comandos Corriqueiros

### 1. Banco de Dados (Postgres 16)
O Devbox já criou as variáveis de ambiente. Siga estes passos:

* **Inicializar o Banco (Só a primeira vez):**
  `initdb`
* **Subir o Banco (Serviço):**
  `devbox services start postgresql`
* **Entrar no Console do Postgres:**
  `psql postgres`
* **Parar o Banco:**
  `devbox services stop postgresql`

### 2. Java & Spring Boot
* **Verificar Versões:**
  `java -version` && `spring --version`
* **Criar novo projeto Spring:**
  `spring init --dependencies=web,data-jpa,postgresql --language=java --build=maven minha-api`
* **Compilar e Rodar:**
  `./mvnw spring-boot:run`

### 3. Kubernetes & Infra (Seu curso)
* **Subir Cluster local:** `kind create cluster --name meu-cluster`
* **Ver Nodes:** `kubectl get nodes`
* **Interface Visual:** `k9s`

---

## 🚀 Fluxo Profissional Git/Github
1. **Nova Branch:** `git checkout -b feature-minha-api`
2. **Edite o código**
3. **Commit:** `git add .` -> `git commit -m "feat: setup inicial spring e postgres"`
4. **Push:** `git push origin feature-minha-api`

---
## 💡 Dicas de Sobrevivência
- **Sair do shell:** `exit`
- **Tudo sumiu?** `devbox shell` (volta tudo ao normal)
- **Erro de TLS/Rede?** Reinicie o terminal e tente `devbox shell` novamente.