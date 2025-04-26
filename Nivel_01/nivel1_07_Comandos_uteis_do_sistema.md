
# 🟢 Nível 1 – Tópico 7: Comandos Úteis do Sistema

---

## 👤 1. [`whoami`](../Apendice/apendice_whoami.md) – Quem está logado?

Exibe o **nome do usuário atual** (aquele que executa o comando).

### Exemplo:
```bash
whoami
```

> Saída:
```
peterson
```

---

## 🧼 2. `clear` – Limpar o terminal

Apaga o conteúdo visível do terminal, sem encerrar sua sessão.

### Exemplo:
```bash
clear
```

> Atalho equivalente:
```
Ctrl + L
```

---

## 🕓 3. `history` – Histórico de comandos

Exibe todos os comandos já digitados na sessão ou no passado.

### Exemplo:
```bash
history
```

> Saída:
```
123  ls -l
124  cd projetos
125  cat relatorio.txt
```

### Reexecutar comando anterior:
```bash
!123
```

### Ver últimos 10 comandos:
```bash
history | tail -n 10
```

---

## 📂 4. `file` – Descobrir o tipo de arquivo

Identifica o **conteúdo e tipo real** de um arquivo, mesmo sem extensão.

### Exemplo:
```bash
file imagem.jpg
```

> Saída:
```
imagem.jpg: JPEG image data
```

```bash
file script
```

> Saída:
```
script: Bourne-Again shell script text executable
```

---

## 🧠 5. Dicas extras

| Comando         | Função                         |
|----------------|---------------------------------|
| `whoami`       | Exibe o usuário atual           |
| `clear`        | Limpa a tela do terminal        |
| `history`      | Mostra todos os comandos digitados |
| `!número`      | Executa comando anterior do histórico |
| `file nome`    | Descobre o tipo real de um arquivo |

---

## 📝 Teste de fixação

### ❓1. Qual comando mostra qual usuário está atualmente logado?

---

### ❓2. Como limpar rapidamente o terminal sem fechar a sessão?

---

### ❓3. Qual comando mostra o tipo de um arquivo mesmo sem extensão?

---

### ❓4. O que acontece ao digitar `!100`?

---

### ❓5. Como exibir os últimos 5 comandos executados?

---
