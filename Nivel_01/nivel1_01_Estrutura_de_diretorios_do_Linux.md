
# 🟢 Nível 1 – Tópico 1: Estrutura de diretórios do Linux

---

## 🧱 1. O que é o sistema de arquivos no Linux?

No Linux, **tudo começa na raiz do sistema**, representada por uma única barra:

```
/
```

A partir daí, tudo se ramifica como em uma **árvore de diretórios**.

---

## 🌳 2. Diretórios principais

| Diretório | Função |
|----------|--------|
| `/`      | Raiz do sistema (tudo começa aqui) |
| `/bin`   | Binários essenciais (ex: `ls`, `cp`, `mv`) |
| `/sbin`  | Binários administrativos (ex: `reboot`, `shutdown`) |
| `/etc`   | Arquivos de configuração |
| `/home`  | Diretórios pessoais dos usuários |
| `/root`  | Diretório pessoal do superusuário (root) |
| `/var`   | Arquivos variáveis (logs, fila de email, cache) |
| `/tmp`   | Arquivos temporários (apagados após reinício) |
| `/usr`   | Programas e arquivos de usuários (não críticos) |
| `/lib`   | Bibliotecas usadas pelos binários |
| `/dev`   | Dispositivos do sistema (HD, teclado, etc) |
| `/proc`  | Informações sobre processos ativos (virtual) |
| `/mnt` e `/media` | Pontos de montagem (pendrives, HDs externos) |

---

## 🏠 3. Diretório pessoal (`/home`)

Cada usuário tem seu próprio espaço:

```bash
/home/peterson
```

Lá ficam seus arquivos, configurações pessoais e pastas.

---

## ⚙️ 4. Diretório `/etc`

Contém **arquivos de configuração do sistema**:

- `/etc/passwd` – informações dos usuários
- `/etc/hostname` – nome da máquina
- `/etc/apt/` – repositórios de pacotes

⚠️ Alterar arquivos aqui pode afetar o funcionamento do sistema!

---

## 🔧 5. Diretório `/var`

Contém arquivos que **mudam constantemente**, como:

- Logs: `/var/log`
- Fila de e-mails: `/var/spool`
- Dados de serviços: `/var/lib`

---

## 🕵️ 6. Comandos úteis para explorar

```bash
cd /          # Vai para a raiz
ls /etc       # Lista arquivos de configuração
ls /home      # Mostra os diretórios de usuários
ls -lh /var/log  # Visualiza os logs do sistema
```

---

## 📝 Teste de fixação

### ❓1. Qual é o diretório raiz no Linux?

---

### ❓2. Para que serve o diretório `/etc`?

---

### ❓3. Onde ficam os arquivos pessoais dos usuários?

---

### ❓4. O que você encontra dentro de `/var/log`?

---

### ❓5. Qual a diferença entre `/bin` e `/usr/bin`?

---
