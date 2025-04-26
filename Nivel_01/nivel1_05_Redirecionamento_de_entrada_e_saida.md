
# 🟢 Nível 1 – Tópico 5: Redirecionamento de Entrada e Saída – `>`, `>>`, `<`

---

## 🧠 1. O que são `stdin`, `stdout` e `stderr`

No Linux, comandos trabalham com **três canais de dados**:

| Nome     | Número | Função                                  |
|----------|--------|------------------------------------------|
| `stdin`  | 0      | Entrada padrão – normalmente o teclado   |
| `stdout` | 1      | Saída padrão – normalmente a tela        |
| `stderr` | 2      | Saída de erro – mensagens de falha       |

Você pode **redirecionar** esses fluxos para ler de arquivos ou gravar saídas em arquivos.

---

## 📤 2. Redirecionar a saída padrão (`stdout`) com `>`

Substitui o conteúdo do arquivo com o resultado do comando.  
**Se o arquivo não existir, será criado. Se existir, será sobrescrito.**

### Exemplo:
```bash
echo "Relatório gerado com sucesso" > log.txt
ls /etc > lista_etc.txt
```

---

## 📥 3. Adicionar à saída com `>>`

**Anexa** conteúdo ao final de um arquivo **sem apagar o que já estava lá**.

### Exemplo:
```bash
echo "Nova linha" >> log.txt
date >> acessos.log
```

---

## 📩 4. Redirecionar a entrada padrão (`stdin`) com `<`

Permite que um comando leia sua entrada de um arquivo, em vez do teclado.

### Exemplo:
```bash
wc -l < texto.txt
sort < nomes.txt
```

---

## ❌ 5. Redirecionar erros com `2>`

Captura mensagens de erro (`stderr`) separadas da saída normal (`stdout`).

### Exemplo:
```bash
ls /inexistente 2> erro.txt
```

---

## 🌀 6. Redirecionar saída **e** erro juntos

Use `2>&1` para combinar `stderr` com `stdout` em um único arquivo:

### Exemplo:
```bash
ls /etc /invalido > resultado.txt 2>&1
```

---

## 🗑️ 7. Ignorar mensagens de erro com `/dev/null`

### Exemplo:
```bash
comando 2>/dev/null
```

> Redireciona os erros para o "buraco negro" do sistema. Nada será mostrado.

---

## 🔎 8. Contexto: o que é o `grep`?

O comando `grep` é usado para **buscar padrões de texto** dentro de arquivos ou saídas de outros comandos.

### Exemplo:
```bash
grep "erro" log.txt
```

Com redirecionamentos:
```bash
cat arquivo.txt | grep "falha" > apenas_falhas.txt
```

---

## 🔄 9. Exemplos combinados

```bash
echo "Relatório 1" > relatorios.txt
echo "Relatório 2" >> relatorios.txt
cat relatorios.txt
```

```bash
grep "root" < /etc/passwd > usuarios_root.txt
```

```bash
ls /naoexiste > saida.txt 2> erro.txt
comando > /dev/null 2>&1
```

---

## 📝 Teste de fixação

### ❓1. Qual a diferença entre `>` e `>>`?

---

### ❓2. O que significa `2> erro.txt`?

---

### ❓3. Como enviar a saída normal e os erros para o mesmo arquivo?

---

### ❓4. O que o comando `wc -l < arquivo.txt` faz?

---

### ❓5. Para que serve `/dev/null` em redirecionamento?

---
