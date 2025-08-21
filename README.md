# 🎮 DSList API  

[![Java](https://img.shields.io/badge/Java-17-red?logo=openjdk)](https://adoptium.net/)  
[![Spring Boot](https://img.shields.io/badge/Spring%20Boot-3.0-brightgreen?logo=springboot)](https://spring.io/projects/spring-boot)  
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-15-blue?logo=postgresql)](https://www.postgresql.org/)  
[![Docker](https://img.shields.io/badge/Docker-Enabled-2496ED?logo=docker)](https://www.docker.com/)  
[![License: GPL](https://img.shields.io/badge/License-GPL-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)  

API Backend desenvolvida durante o **Intensivão Java Spring** da [DevSuperior](https://devsuperior.com.br/).  
O projeto consiste em uma aplicação para gerenciamento de **listas de jogos**, com operações de consulta e alteração de posições.  

> 📌 Créditos: DevSuperior, mantenedora do treinamento.  

---

## 🚀 Tecnologias utilizadas
- **Java 17**  
- **Spring Boot 3**  
- **PostgreSQL 15**  
- **Docker**  
- **Git**  

---

## 📂 Arquitetura
O projeto segue o padrão **MVC (Model–View–Controller)**:
- **Entities e DTOs** → abstração dos dados  
- **Controllers** → exposição de endpoints REST  
- **Services** → regras de negócio  
- **Repositories** → integração com o banco de dados  
- **Projections** → consultas otimizadas  

---

## 🛠️ Como executar localmente

### Pré-requisitos
- [Docker](https://www.docker.com/) instalado  
- [Java 17+](https://adoptium.net/)  
- [Maven](https://maven.apache.org/)  

---

## 🌐 Endpoints principais

| Método | Endpoint                  | Descrição                                |
|--------|----------------------------|------------------------------------------|
| GET    | `/games`                  | Lista todos os jogos                     |
| GET    | `/games/{id}`             | Retorna informações de um único jogo     |
| GET    | `/lists`                  | Lista todas as coleções                  |
| GET    | `/lists/{id}/games`       | Lista os jogos de uma coleção específica |
| POST   | `/lists/{id}/replacement` | Altera posição de jogo em uma coleção    |

### 🔎 Exemplo de resposta JSON
**GET** `/games/1`
```json
{
  "id": 1,
  "title": "The Witcher 3",
  "platform": "PC",
  "score": 9.7,
  "year": 2015,
  "genre": "RPG"
}
```

---

## 📊 Base de dados
O projeto utiliza **PostgreSQL**.  
O repositório contém o script `create.sql` com a estrutura e dados iniciais.  

---

## ⚙️ Configurações adicionais
- Configurações de **CORS** e **profiles** estão em `application-*.properties`.  
- Profiles disponíveis: `dev`, `test`, `prod`.  

---

## 📌 Status
🚧 Projeto em desenvolvimento — baseado no **Intensivão Java Spring da DevSuperior**.  

---

## 🤝 Contribuição
Contribuições são sempre bem-vindas!  

1. Faça um fork do projeto  
2. Crie uma branch (`git checkout -b feature/nova-feature`)  
3. Commit suas alterações (`git commit -m 'Adiciona nova feature'`)  
4. Faça o push para a branch (`git push origin feature/nova-feature`)  
5. Abra um Pull Request 🚀  

---

## 📜 Licença
Este projeto está licenciado sob a **GNU General Public License (GPL)**.  
