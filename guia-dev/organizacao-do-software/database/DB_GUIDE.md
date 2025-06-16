# 📚 Banco de Dados - Projeto X

## 🛠️ Requisitos

- **MySQL 8+**
- **DBeaver**, **DataGrip** ou outro cliente SQL (opcional)

---

## 📂 Estrutura de Pastas

```bash
banco-de-dados/
├── README.md
├── ddl/ # Data Definition Language - Criação de estruturas
│   ├── 01_create_schema.sql # CREATE DATABASE, USE ...
│   ├── 02_create_tables.sql # Criação de todas as tabelas
│   ├── 03_constraints.sql # Chaves primárias, estrangeiras, unique, etc
│   └── 04_indexes.sql # Criação de índices (se necessário)
├── dml/ # Data Manipulation Language - Inserção e atualização de dados
│   ├── inserts/
│   │   ├── insert_usuarios.sql
│   │   ├── insert_produtos.sql
│   │   └── ...
│   ├── updates/
│   │   ├── update_usuarios.sql
│   │   └── ...
│   └── deletes/
│       ├── delete_usuarios.sql
│       └── ...
├── consultas/ # SELECTs úteis, exemplos de uso
│   ├── select_usuarios.sql
│   ├── relatorios.sql
│   └── ...
└── scripts_completos/
    ├── banco_completo.sql # Contém todos os comandos acima, em ordem
    └── popular_base_completa.sql # Todos os INSERTs e dados iniciais
```

---

## 📌 Sobre cada pasta:

### ✅ `ddl/`
Scripts responsáveis pela **estrutura do banco**:

- Criação de schemas
- Tabelas
- Constraints (chaves primárias, estrangeiras, unique)
- Índices

> 💡 **Por que separado?**  
Facilita alterações pontuais, como adicionar apenas uma FK sem precisar recriar tudo.

---

### ✅ `dml/`
Scripts de **manipulação de dados**, separados por tipo:

- **Inserts:** Popular dados iniciais ou de teste
- **Updates:** Atualizações de registros
- **Deletes:** Exclusões específicas

> 💡 Útil para manter controle de todos os dados manipulados durante o desenvolvimento.

---

### ✅ `consultas/`
Aqui ficam os **SELECTs mais usados**, como:

- Consultas de exemplo
- Relatórios
- Queries para debug

> 💡 Serve também como repositório de exemplos para a equipe.

---

### ✅ `scripts_completos/`
Scripts que **juntam tudo de forma sequencial**:

- **banco_completo.sql:**  
Cria o banco do zero (schema + tabelas + constraints + índices)

- **popular_base_completa.sql:**  
Popula o banco com dados de exemplo.

> 💡 Útil para quem for clonar o projeto e quiser um ambiente pronto rapidamente.

---

## 📝 Como criar o banco de dados

1. Executar o schema:

```bash
ddl/01_create_schema.sql
```

Criar as tabelas:

```bash
ddl/02_create_tables.sql
```

Adicionar constraints:

```bash
ddl/03_constraints.sql
```

(Opcional) Criar índices:

```bash
ddl/04_indexes.sql
```

Popular o banco com dados de teste:

```bash
dml/inserts/*
```

👤 Usuários padrão (Exemplo)
|Usuário |	Senha  |
|--------|---------|
|admin	 |admin123 |
|user	 |user123  |
⚠️ Dicas de Segurança

- Nunca adicione ao repositório:
    - Dumps com dados reais
    - Arquivos de configuração com senhas (.env, .my.cnf)
    - Senhas em texto aberto

🔒 Se precisar de dados sensíveis, armazene-os em ambientes seguros ou variáveis de ambiente.

