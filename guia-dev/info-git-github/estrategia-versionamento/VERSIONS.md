# 📌 Estratégia de Versionamento (SemVer + Tags)

Vamos utilizar Semantic Versioning (SemVer) e as Releases do GitHub para organizar as versões oficiais do projeto.

## ✅ O que é SemVer?
SemVer (Versionamento Semântico) segue o formato:

```bash
MAJOR.MINOR.PATCH
```

Exemplo:

```bash 
1.4.2
```

## ✅ Significado de cada parte:

| Parte     | Quando aumentar                              | Exemplo      |
|---------- |----------------------------------------------|--------------|
| **MAJOR** | Mudanças incompatíveis na API ou no projeto  |1.0.0 → 2.0.0 |
| **MINOR** | Nova funcionalidade, mas compatível          |1.1.0 → 1.2.0 |
| **PATCH** | Correções de bugs pequenas                   |1.2.1 → 1.2.2 |

## ✅ Como criar uma nova versão (tag) no Git

1. Primeiro, finalize as alterações na main.
2. Depois, crie a tag:

```bash
git tag -a v1.0.0 -m "Primeira versão estável"
git push origin v1.0.0
```

## ✅ Releases no GitHub

Depois de criar a tag, vá até o repositório no GitHub:

1. Acesse a aba "Releases"
2. Clique em "Draft a new release"
3. Selecione a tag criada
4. Adicione um changelog (lista de alterações daquela versão)
5. Publique a Release.

Dica: Use as releases para marcar milestones importantes (ex: MVP, Versão Estável, etc).