# 📌 Boas práticas de Pull Request (PR)

## ✅ Antes de abrir um PR:

- Revise seu código.
- Garanta que o projeto está compilando / funcionando.
- Verifique se seguiu a convenção de commits.
- Dê uma olhada nos arquivos modificados (para evitar subir algo por engano).

## ✅ Título do PR

Siga o mesmo formato da sua convenção de commits:

```bash
feat: adiciona tela de login
fix: corrige validação de usuário
docs: atualiza documentação
```
## ✅ Corpo do PR (Descrição)

Inclua no corpo:

- O que foi feito
- Por que foi feito
- Passos para testar
- Se o PR resolve algum issue, adicione:
```
Closes #número_do_issue
```

Exemplo de descrição:

```shell
### O que foi feito
Adicionada a tela de login com validação de campos obrigatórios.

### Por que foi feito
Parte da primeira entrega de funcionalidades.

### Como testar
Executar o projeto, acessar rota `/login` e tentar fazer login sem preencher campos.

Closes #12
```

## ✅ Revisão do PR

Se o projeto tiver política de revisão:

## ✅ Confira:

- Organização de código
- Nome de variáveis
- Seguiu padrões do projeto
- Testes realizados

Depois: Aprove ou solicite mudanças.