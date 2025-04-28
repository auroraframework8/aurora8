
# Cartilha Git - Fluxo entre `main` e `dev`

## 1. Introdução ao Git

O **Git** é um sistema de controle de versão distribuído que permite gerenciar o histórico de alterações em arquivos, facilitando o trabalho em equipe e o versionamento de código.

### Benefícios:
- Histórico completo de mudanças.
- Possibilidade de trabalhar em **branches** para isolar desenvolvimentos.
- Trabalho offline com repositórios locais.

---

## 2. Estrutura do Git

- **Working Directory**: Diretório onde os arquivos são editados.
- **Staging Area**: Área de preparação dos arquivos para commit.
- **Local Repository**: Banco de dados de commits no computador local.
- **Remote Repository**: Repositório na nuvem (ex: GitHub, GitLab).

### Fluxo de Arquivo no Git:

```plaintext
Working Directory -> Staging Area -> Local Repository -> Remote Repository
```

---

## 3. Conceito de Branches (`main` e `dev`)

- **main**: Linha principal de produção (código estável).
- **dev**: Linha de desenvolvimento (novas features).

### Por que usar branches?

- Isola funcionalidades.
- Facilita revisões antes de integrar no `main`.

---

## 4. Comandos Essenciais

```bash
git init                             # Inicializa o repositório Git
git remote add origin <URL>          # Adiciona o repositório remoto
git checkout -b dev                  # Cria e muda para a branch dev
git status                           # Verifica o status dos arquivos
git add .                            # Adiciona todos os arquivos para staging
git commit -m 'Mensagem'             # Realiza o commit com uma mensagem
git push origin dev                  # Envia a branch dev para o repositório remoto
```

---

## 5. Integrando `dev` no `main` (merge)

```bash
git checkout main                    # Muda para a branch main
git pull origin main                 # Atualiza a main com o remoto
git merge dev                        # Faz o merge das mudanças da dev
git push origin main                 # Envia para o repositório remoto
```
