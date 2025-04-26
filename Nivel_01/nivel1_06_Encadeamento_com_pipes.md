
# 🟢 Nível 1 – Tópico 6: Encadeamento com Pipes – `|`

---

## 🔗 1. O que é um pipe (`|`)?

Um **pipe** redireciona a **saída (`stdout`) de um comando como entrada (`stdin`) para outro comando**.

### Sintaxe:
```bash
comando1 | comando2
```

> Lê-se: "comando1 **pipe** comando2"

---

## ⚙️ 2. Como funciona na prática?

Quando você usa `|`, o Bash:

1. Executa o `comando1`
2. Pega a saída gerada
3. Envia essa saída diretamente como **entrada do `comando2`**

---

## 📌 3. Exemplo básico

```bash
ls | sort
```
> Lista os arquivos e envia essa lista para o comando `sort`, que ordena alfabeticamente.

---

## 🔍 4. Usando com `grep` para filtrar resultados

```bash
dmesg | grep usb
```
> Mostra apenas as linhas do log do sistema que contêm a palavra “usb”.

```bash
cat /etc/passwd | grep root
```
> Filtra as linhas do arquivo que contêm o termo "root".

---

## 📄 5. Pipe com `wc` – contar linhas, palavras, caracteres

```bash
ls /etc | wc -l
```
> Conta **quantos arquivos ou pastas** existem no diretório `/etc`.

```bash
ps aux | grep bash | wc -l
```
> Conta quantos processos relacionados ao `bash` estão ativos.

---

## 📜 6. Pipe com `head`, `tail`, `cut`, `awk`

```bash
ls -lh /var/log | head -n 5
```
> Mostra os 5 primeiros arquivos da listagem de logs.

```bash
df -h | grep sda | awk '{print $5}'
```
> Mostra apenas a **porcentagem de uso do disco** com nome "sda".

---

## 🧠 7. Comparação: Pipe vs Redirecionamento

| Operador | Função                           |
|----------|----------------------------------|
| `>`      | Envia a saída para um arquivo    |
| `<`      | Usa um arquivo como entrada      |
| `|`      | Envia a saída para **outro comando** |

---

## 🧪 8. Exemplos úteis com pipe

```bash
ps aux | grep firefox
```

```bash
cat arquivo.txt | grep "falha" | wc -l
```
> Conta quantas falhas existem no arquivo.

```bash
ls -lh /etc | grep ".conf" | sort
```

---

## 📝 Teste de fixação

### ❓1. Para que serve o operador `|`?

---

### ❓2. O que o comando `ls /etc | grep conf` faz?

---

### ❓3. Como usar `wc` com pipe para contar quantas linhas existem em `ls /bin`?

---

### ❓4. Qual comando mostra apenas os 5 primeiros resultados da listagem de `/var`?

---

### ❓5. Qual a diferença entre usar `>` e `|`?

---
