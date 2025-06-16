# 📌 Principais comandos Git utilizados no desenvolvimento

## ✅ Inicialização e configuração

```bash
git init                      # Inicializa um repositório local
git config --global user.name "Seu Nome"
git config --global user.email "seu@email.com"
git config --list             # Ver configurações atuais
```

## ✅ Clonando repositórios

```bash
git clone <url>               # Clona um repositório remoto para sua máquina
```

## ✅ Trabalhando com arquivos

```bash
git status                    # Mostra os arquivos modificados
git add <arquivo>             # Adiciona um arquivo específico
git add .                     # Adiciona todas as modificações
git commit -m "mensagem"      # Cria um commit com mensagem
git restore <arquivo>         # Desfaz alterações locais não commitadas
git rm <arquivo>              # Remove arquivo do Git e do projeto
```

## ✅ Branches (ramificações)

```bash
git branch                    # Lista branches locais
git checkout -b nova-branch   # Cria e muda para uma nova branch
git checkout main             # Muda para a branch main
git merge <branch>            # Mescla uma branch na atual
git branch -d <branch>        # Apaga uma branch local

```

## ✅ Enviando para o GitHub

```bash
git push origin <branch>      # Envia commits da branch atual
git push -u origin <branch>   # Envia e define como branch padrão de push
```

## ✅ Atualizando o repositório local

```bash
git pull                      # Puxa atualizações do repositório remoto
git fetch                     # Puxa atualizações sem mesclar
```

## ✅ Correções e histórico

```bash
git log                       # Mostra o histórico de commits
git diff                      # Mostra as diferenças ainda não adicionadas
git reset --soft HEAD~1       # Remove o último commit, mas mantém alterações
git revert <commit>           # Reverte um commit específico
```

## ✅ Comandos úteis

```bash
git stash                     # Salva alterações não commitadas para depois
git stash apply               # Recupera o que foi salvo no stash
git clean -f                  # Remove arquivos não rastreados
```

## ✅ Extras

```bash
git remote -v                 # Mostra os repositórios remotos
git remote add origin <url>   # Conecta um repositório local a um remoto
```

## 📝 Observações importantes:
- Sempre use git status antes de qualquer ação.
- Use git pull antes de um git push para evitar conflitos.
- Os commits devem seguir a padronização definida no arquivo de convenção de commits deste projeto.