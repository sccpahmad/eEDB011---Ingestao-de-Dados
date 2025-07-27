# Projeto: Ingestão de Dados com KNIME + PostgreSQL

Este projeto foi desenvolvido como parte da disciplina **eEDB011 - Ingestão de Dados** do curso de pós-graduação em Engenharia de Dados e Big Data.

- Objetivo
Demonstrar um fluxo completo de ingestão, transformação e consolidação de dados utilizando:

- **KNIME** para orquestração dos fluxos
- **PostgreSQL** como base de dados relacional
- **Docker** para garantir reprodutibilidade do ambiente

---

- Estrutura do Projeto
workflow_knime/ → Fluxo KNIME exportado (.knwf)
init/ → Scripts de inicialização do banco
docker-compose.yml → Container com PostgreSQL configurado
ingestao_dados.sql → Dump SQL com dados populados
README.md → Este documento

---

- Como Executar
1. Clonar o repositório:
```bash
git clone https://github.com/seuusuario/eEDB011---Ingest-o-de-Dados.git
cd eEDB011---Ingest-o-de-Dados

2. Subir o container Docker com PostgreSQL:
docker compose up --build
Isso irá iniciar o banco de dados e criar as tabelas com os dados previamente populados.

3. Abrir o fluxo no KNIME:
Abra o KNIME Analytics Platform
Vá em File > Import KNIME Workflow...
Selecione o arquivo .knwf localizado na pasta workflow_knime/
Execute o fluxo.

---

- Observações
O KNIME não está incluído no container, apenas o PostgreSQL e os dados.
É necessário ter o Docker instalado na sua máquina.

O script ingestao_dados.sql contém as instruções de criação e inserção dos dados.