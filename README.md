
# 📘 Git Tips

## 📌 Comandos Básicos do Git e GitHub

### Sumário

<!--ts-->
- [Antes de Começar](#antes-de-começar)
- [Principais Comandos do Git](#principais-comandos-do-git)
- [Gerenciamento de Branches](#gerenciamento-de-branches)
- [Tags](#tags)
- [Outros Comandos Úteis](#outros-comandos-úteis)
<!--te-->

---

## 🔧 Antes de Começar

1. Vá até a pasta onde deseja clonar o projeto.
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

