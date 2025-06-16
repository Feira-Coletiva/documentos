# 📌 Convenção de Commits

## ✅ Boas práticas de mensagens de commit

- **Seja claro e objetivo:**  
  Evite mensagens genéricas como `update`, `ajustes`, `finalizado`.

- **Use o tempo verbal imperativo:**  
  Exemplo de mensagens corretas:  
  - `Adiciona tela de login`  
  - `Corrige validação de formulário`  
  - `Remove endpoint obsoleto`

- **Commits pequenos e frequentes:**  
  Mantenha os commits **atômicos**, ou seja, uma mudança clara por commit.

- **Evite arquivos desnecessários:**  
  Não comite arquivos como:
  - `.class`
  - `node_modules/`
  - `.env`
  - Arquivos com senhas
  - Arquivos pessoais e configurações de IDE

---

## ✅ Padrão: Conventional Commits (adaptado)

Adotaremos uma estrutura baseada no padrão **[Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/)**.

### 🔎 Formato básico:

`<tipo>(escopo): mensagem`
---

## ✅ Tipos mais comuns

| Tipo      | Uso                                 |
|---------- |------------------------------------ |
| **feat**  | Nova funcionalidade                 |
| **fix**   | Correção de bug                     |
| **docs**  | Documentação apenas (README, comentários, etc) |
| **style** | Estilo (formatação, indentação, etc – sem alterar lógica) |
| **refactor** | Refatoração de código (sem mudar comportamento) |
| **test**  | Adição ou modificação de testes     |
| **chore** | Tarefas diversas (build, configs, scripts) |
| **perf**  | Melhorias de performance            |

---

## ✅ Exemplos práticos de commits:

```bash
feat(login): adiciona tela de login com validação

fix(usuario): corrige bug ao salvar usuário sem e-mail

docs(readme): atualiza instruções de execução local

style(css): melhora indentação do arquivo de estilos

refactor(api): separa lógica de serviço em novo arquivo

test(usuario): adiciona teste para criação de usuário

chore(gitignore): adiciona node_modules ao .gitignore
```

## ✅ Dicas finais:
- Mantenha a consistência durante todo o desenvolvimento.
- Se tiver dúvida sobre o tipo, priorize feat, fix ou docs.
- Para mudanças muito pequenas e técnicas (que não se encaixam nos tipos principais), use chore.