# 🚩 Workflow Git - Como trabalhar em equipe

## ✅ Fluxo básico de trabalho

### 1. Antes de começar: atualize sua branch local

Sempre que for iniciar um novo trabalho:

```bash
git checkout main
git pull origin main
```

### 2. Crie uma nova branch para cada tarefa

Nomeie sua branch de forma descritiva:

```bash
git checkout -b tipo/nome-da-tarefa
```

Exemplos:

```bash
git checkout -b feat/tela-login
git checkout -b fix/cadastro-cliente
git checkout -b docs/atualiza-readme
```
Dica: Use o mesmo tipo da sua convenção de commits (feat, fix, docs, etc).

### 3. Faça commits pequenos e com mensagens padronizadas

Sempre siga a nossa convenção de commits.

### 4. Envie sua branch para o GitHub

```bash
git push origin nome-da-sua-branch
```
Exemplo:

```bash
git push origin feat/tela-login
```
### 5. Crie um Pull Request (PR)

- Acesse o GitHub.
- Abra um Pull Request da sua branch em direção à main.
- Adicione uma descrição clara sobre o que foi feito.
- Peça revisão de alguém do time (se aplicável).

### 6. Aguarde aprovação (se houver revisão)

- Se o time adotar revisões, aguarde aprovação antes de dar merge.
- Se for liberado, siga para o próximo passo.

### 7. Faça o merge na main

Após aprovado:

```bash
git checkout main
git pull origin main
git merge nome-da-sua-branch
git push origin main
```
### 8. Após o merge: delete sua branch (opcional, mas recomendado)

```bash
git branch -d nome-da-sua-branch      # Local
git push origin --delete nome-da-sua-branch  # Remoto
```
## ✅ Fluxo visual simplificado:

```bash
main → cria branch → faz commits → push → PR → revisão → merge → deleta branch
```

## ✅ Boas práticas gerais:

- Nunca trabalhe direto na main.
- Sempre puxe atualizações antes de iniciar.
- Mantenha suas branches organizadas.
- Nomeie suas branches de forma clara e curta.
- Prefira várias branches pequenas ao invés de uma enorme.

## ✅ Comandos úteis de revisão:

```bash
git log --oneline --graph --all
git diff main nome-da-sua-branch
```

