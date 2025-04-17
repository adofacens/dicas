### 📄 `GIT_TIPS.md`

```markdown
# 📘 Git Tips

## 📌 Comandos Básicos do Git e GitHub

### Sumário

<!--ts-->
- [Antes de Começar](#antes-de-começar)
- [Principais Comandos do Git](#principais-comandos-do-git)
- [Gerenciamento de Branches](#gerenciamento-de-branches)
- [Tags](#tags)
- [Outros Comandos Úteis](#outros-comandos-úteis)
- [Jornada Git + GitHub no VS Code](#jornada-git--github-no-vs-code)
<!--te-->

---

## 🔧 Antes de Começar

1. Vá até a pasta onde deseja clonar ou iniciar o projeto.
2. Abra o terminal dentro dessa pasta.

---

## 👑 Principais Comandos do Git

### Configuração Inicial

```bash
git config --global user.name "Seu Nome"
git config --global user.email "seu@email.com"
```

### Clonar Repositório

```bash
git clone -b <branch> <URL_do_repositório>
```

### Acessar a pasta do projeto

```bash
cd <nome_da_pasta>
```

### Inicializar Repositório Git (caso necessário)

```bash
git init
```

### Verificar o estado dos arquivos

```bash
git status
```

### Adicionar arquivos à *staging area*

```bash
git add .
# ou para adicionar arquivos específicos
git add nome_do_arquivo
```

### Fazer Commit

```bash
git commit -m "mensagem do commit"
```

### Verificar repositório remoto

```bash
git remote -v
```

### Adicionar repositório remoto (HTTPS ou SSH)

```bash
# Via HTTPS
git remote add origin https://github.com/usuario/repositorio.git

# Via SSH
git remote add origin git@github.com:usuario/repositorio.git
```

### Puxar alterações do repositório remoto

```bash
git pull origin main
```

### Enviar alterações para o repositório remoto

```bash
git push origin main
```

### Forçar push inicial (caso necessário)

```bash
git push -u origin main
```

---

## 🌿 Gerenciamento de Branches

### Alterar nome da branch principal para `main`

```bash
git branch -M main
```

### Criar nova branch

```bash
git checkout -b nome-da-branch
```

### Mudar para uma branch existente

```bash
git checkout nome-da-branch
```

### Enviar nova branch para o remoto

```bash
git push origin nome-da-branch
```

### Fazer merge de outra branch

```bash
git merge nome-da-branch
```

---

## 🏷️ Tags

### Criar uma tag

```bash
git tag -a <nome-da-tag> -m "comentário"
```

### Enviar tags para o repositório remoto

```bash
git push origin --tags
```

---

## 🛠️ Outros Comandos Úteis

### Resolver erro: `fatal: refusing to merge unrelated histories`

```bash
git pull origin main --allow-unrelated-histories
```

### Baixar atualizações do repositório remoto

```bash
git pull
```

### Redefinir histórico do projeto (limpar commits anteriores)

```bash
# Criar nova branch órfã
git checkout --orphan new_branch

# Adicionar todos os arquivos
git add -A

# Fazer um commit "limpo"
git commit -m "limpando commits anteriores"

# Excluir a branch antiga
git branch -D main

# Renomear nova branch para main
git branch -m main

# Forçar push para o repositório remoto
git push -f origin main
```

---

## 🚀 Jornada Git + GitHub no VS Code

### 📁 1. Criar Projeto Localmente

```bash
mkdir nome-do-projeto
cd nome-do-projeto
code .
```

> O comando `code .` abre o VS Code diretamente na pasta.

---

### 🛠️ 2. Inicializar Git no projeto

```bash
git init
```

---

### ⚙️ 3. Configurar seu usuário (caso ainda não tenha feito)

```bash
git config --global user.name "Seu Nome"
git config --global user.email "seu@email.com"
```

---

### 📄 4. Criar o primeiro arquivo (ex: README)

```bash
echo "# Meu Projeto" > README.md
```

---

### ➕ 5. Adicionar os arquivos ao Git

```bash
git add .
```

---

### 📝 6. Fazer o primeiro commit

```bash
git commit -m "primeiro commit"
```

---

### 🌐 7. Criar um repositório no GitHub

- Acesse [https://github.com](https://github.com)
- Clique em "New Repository"
- Dê um nome ao repositório (ex: `meu-projeto`)
- Não selecione nenhum template/README
- Clique em "Create repository"

---

### 🔗 8. Conectar repositório local ao GitHub

```bash
# HTTPS
git remote add origin https://github.com/seuusuario/meu-projeto.git

# ou via SSH
git remote add origin git@github.com:seuusuario/meu-projeto.git
```

---

### ☁️ 9. Enviar o projeto local para o GitHub

```bash
git branch -M main
git push -u origin main
```

---

### 🔄 10. Clonar um projeto existente do GitHub

```bash
git clone https://github.com/usuario/repositorio.git
cd repositorio
code .
```

---

### 🔁 11. Fluxo diário de uso no VS Code

1. Faça alterações nos arquivos.
2. Use os seguintes comandos no terminal do VS Code:

```bash
git status                    # Verificar alterações
git add .                     # Adicionar todas as mudanças
git commit -m "descrição"     # Criar commit
git pull origin main          # Puxar alterações mais recentes
git push origin main          # Enviar alterações
```

---

### ✅ Dica final

Use a aba **Source Control** (Ctrl+Shift+G) no VS Code para gerenciar seus commits de forma visual.  
Mas lembre-se: o terminal sempre será seu melhor aliado!

---

## 🧠 Recomendações Finais

- Sempre use `git pull` antes de começar a trabalhar para evitar conflitos.
- Crie branches para funcionalidades novas (`feature/nome`).
- Prefira commits pequenos e com mensagens claras.
- Faça `push` com frequência para evitar perda de progresso.
- Evite resolver conflitos direto no GitHub, prefira o VS Code.

---

## 💡 Sugestão de nome para este repositório

**`git-cheatsheet-br`**  
> Um guia simples, direto e em português com os principais comandos do Git e GitHub.

```
