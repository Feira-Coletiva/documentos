# 🌐 Estrutura de Pastas - Frontend

## 📁 Estrutura Recomendada

```bash
frontend/
│
├── index.html                      # Página inicial
├── login.html                      # Outras páginas principais...
│
├── assets/                         # Arquivos estáticos (CSS, JS, imagens)
│   ├── css/
│   │   ├── style.css               # Estilos globais
│   │   ├── reset.css               # Reset de estilos (opcional)
│   │   └── [tela].css              # Estilos específicos por tela
│   │
│   ├── js/
│   │   ├── main.js                 # JS principal / inicialização
│   │   ├── api.js                  # Comunicação com a API (fetch)
│   │   ├── utils.js                # Funções utilitárias
│   │   └── controllers/
│   │       ├── loginController.js
│   │       ├── cadastroController.js
│   │       └── ...                 # Um controller por tela ou funcionalidade
│   │
│   └── img/
│       ├── logo.png
│       └── ...                     # Imagens do sistema
│
├── pages/                          # Telas separadas (HTML)
│   ├── dashboard.html
│   ├── cadastroCliente.html
│   └── ...
│
└── README.md                       # Explicação da estrutura (este arquivo)
```

## 📝 Finalidade de Cada Pasta/Arquivo

| 📂 Pasta/Arquivo       | 🎯 Função                                                 |
| ---------------------- | --------------------------------------------------------- |
| `index.html`, `pages/` | Cada tela em um arquivo separado → Facilita manutenção    |
| `assets/css/`          | Organização de estilos globais e por tela                 |
| `assets/js/`           | Scripts organizados por responsabilidade                  |
| `controllers/`         | JavaScript orientado por tela ou funcionalidade           |
| `api.js`               | Centralização de chamadas para o backend (ex.: `fetch`)   |
| `utils.js`             | Funções utilitárias (validação, máscaras, formatação etc) |
| `img/`                 | Organização de imagens do sistema                         |

## 💡 Boas Práticas e Dicas Extras

- 🔧 Nomeação descritiva
Dê nomes claros aos arquivos:
Exemplos:
cadastroProduto.html, produtoController.js, dashboard.css

- 🧪 Estrutura para testes (se crescer)
Se o projeto for expandido, crie uma pasta:
frontend/tests/ → Para scripts de teste em JS.

- 🌐 Padronização visual (CSS)
Considere criar um arquivo como:
variables.css ou theme.css → Para centralizar cores, fontes e espaçamentos.

- 🧼 Configuração do Git
- Se for versionar o frontend no Git:
    - 👉 Inclua um .gitignore na raiz, especialmente se no futuro usar npm ou outras ferramentas (ex.: ignorar node_modules/).

- 📏 Organização por responsabilidade
    - 👉 Cada arquivo .js deve ter uma responsabilidade clara:

    - Controle de uma tela específica

    - Comunicação com API

    - Funções auxiliares

## 🚀 Sugestões Futuras

- Utilizar frameworks modernos (ex.: Vue, Angular, React)

- Implementar um sistema de roteamento SPA

- Adicionar automações com Webpack ou Vite (se migrar para frameworks JS)

- Aplicar validações mais avançadas com bibliotecas JS
