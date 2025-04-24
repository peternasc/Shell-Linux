
# 🟤 Nível 0 – Tópico 4: Como digitar comandos corretamente

---

## ⌨️ 1. O terminal é sensível a maiúsculas e minúsculas

No Linux, **comandos e nomes de arquivos são case-sensitive**:

```bash
ls      # funciona
LS      # ERRO: comando não encontrado
```

```bash
cd /home/peterson
cd /Home/Peterson  # ERRO se o caminho não existir com letras maiúsculas
```

---

## 🧱 2. Um comando pode ter três partes

Geralmente um comando no Bash segue essa estrutura:

```
[comando] [opções] [argumentos]
```

Exemplo:
```bash
ls -l /etc
```

| Parte     | Significado                      |
|-----------|----------------------------------|
| `ls`      | O comando                        |
| `-l`      | A opção (lista detalhada)        |
| `/etc`    | O argumento (diretório a listar) |

---

## ⚠️ 3. Espaços fazem diferença!

**Não coloque espaços onde não deve:**

```bash
ls-l        # ERRO
ls -l       # CERTO
```

```bash
cd ..       # CERTO
cd..        # ERRO
```

---

## 🗂 4. Caminhos com espaços precisam de aspas

```bash
cd "Meus Documentos"
```

Ou com **escape**:
```bash
cd Meus\ Documentos
```

---

## 📛 5. Erros comuns ao digitar comandos

| Erro | Correção |
|------|----------|
| `LS` | `ls` |
| `cd..` | `cd ..` |
| `mkdirmeupasta` | `mkdir meupasta` |
| `rm-arquivo.txt` | `rm arquivo.txt` |

---

## ✅ 6. Boas práticas ao digitar comandos

- Use **seta ↑** para repetir o último comando
- Use **Tab** para completar nomes automaticamente
- Evite usar nomes com espaços em arquivos e pastas
- Sempre revise o comando antes de apertar **Enter**, principalmente com `rm`

---

## 📝 Teste de fixação

### ❓1. O que acontece se você digitar `LS` em vez de `ls`?

---

### ❓2. Qual a diferença entre `cd ..` e `cd..`?

---

### ❓3. Como navegar até uma pasta chamada `Arquivos de Texto`?

---

### ❓4. Qual parte do comando `ls -a /etc` representa o argumento?

---
