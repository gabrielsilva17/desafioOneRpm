# Music Tracks API — Laravel + Docker + MySQL + Swagger

Esta é uma API RESTful para importar e expor **faixas musicais** via código ISRC, integrada com a **Spotify Web API**, construída com **Laravel 10**, Docker e MySQL, e documentada via **Swagger**.

---

## 🚀 Getting Started

### 1. Clone o repositório

```bash
git clone https://github.com/gabrielsilva17/oneRpm.git
cd oneRpm
```
### 2. Crie a network Docker

```bash
docker network create gateway_net
```

### 3. Levante os containers

```bash
docker-compose up --build -d
```

Isto irá:

1. **Composer install**
2. **Migrations & seeders**
3. **Gerar APP\_KEY**
4. Ajustar permissões de `storage/` e `bootstrap/cache`

### 4. Acesse

* **API**: `API: http://localhost:9002`
* **Swagger UI**: `http://localhost:9002/api/documentation`
* **Web pública (lista de faixas)**: `http://localhost:9002/tracks`

---

## 📦 Endpoints principais

* **Tracks**

> Consulte o Swagger UI para todos os detalhes desta rota.

---

## 🧪 Testes

>  **Atenção: rodar os testes resetará o banco de dados.**

Dentro do container **app**:

```bash
docker-compose exec app bash
vendor/bin/phpunit --coverage-html coverage
```

* Relatórios de cobertura em `coverage/`.

## 🎯 Requisitos atendidos

* Integração com Spotify Web API (Client Credentials Flow)
* **Importação de faixas por ISRC e persistência no MySQL**
* **API pública com filtros, paginação e ordenação**
* **Documentação via Swagger (L5‑Swagger)**
* **Dockerização completa (PHP, Nginx, MySQL) na porta 9002**
* **Testes unitários e feature tests cobrindo fluxos críticos**
* **Padrões PSR‑12, SOLID e Clean Code**

---

## 🌐 Tecnologias

* **Laravel 10** & PHP 8.2+
* **Docker & Docker Compose**
* **MySQL 8**
* **Swagger / L5‑Swagger**
* **PHPUnit** + Mockery
* **Laravel Pint** (PSR‑12)

---

## 📝 Licença

MIT — veja [LICENSE](LICENSE).
