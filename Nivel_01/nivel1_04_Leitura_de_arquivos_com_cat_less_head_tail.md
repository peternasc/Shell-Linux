
# 🟢 Nível 1 – Tópico 4: Leitura de Arquivos com `cat`, `less`, `head`, `tail`

---

## 📄 1. `cat` – Exibir conteúdo completo

O comando `cat` (de *concatenate*) serve para:

- Exibir o conteúdo **completo** de um ou mais arquivos diretamente no terminal
- Juntar arquivos
- Criar arquivos simples (com redirecionamento)

### Sintaxe:
```bash
cat nome_do_arquivo
```

### Exemplo:
```bash
cat texto.txt
```

### Com vários arquivos:
```bash
cat parte1.txt parte2.txt > completo.txt
```

> Dica: evite usar `cat` com arquivos muito grandes, pois ele despeja tudo de uma vez.

---

## 📜 2. `less` – Visualizar arquivos paginados

O comando `less` é usado para **navegar confortavelmente** por arquivos longos.

- Permite rolar para cima/baixo
- Não carrega tudo de uma vez
- Pode pesquisar dentro do conteúdo

### Sintaxe:
```bash
less nome_do_arquivo
```

### Navegação dentro do `less`:
| Tecla | Ação                       |
|-------|----------------------------|
| `Espaço` | Avança uma página        |
| `↑`/`↓` | Sobe ou desce linha      |
| `q`   | Sai do `less`              |
| `/palavra` | Busca por uma palavra  |
| `n`   | Próxima ocorrência da busca |

### Exemplo:
```bash
less /etc/passwd
```

---

## 🔝 3. `head` – Mostrar o início de um arquivo

Exibe as **primeiras linhas** de um arquivo.

### Sintaxe:
```bash
head nome_do_arquivo
```

Por padrão, exibe **as 10 primeiras linhas**.

### Para definir o número de linhas:
```bash
head -n 5 relatorio.txt
```

---

## 🔚 4. `tail` – Mostrar o fim de um arquivo

Exibe as **últimas linhas** de um arquivo.

### Sintaxe:
```bash
tail nome_do_arquivo
```

Também mostra **10 linhas por padrão**.

### Para ver mais/menos linhas:
```bash
tail -n 15 log.txt
```

### Modo de monitoramento contínuo (modo ao vivo):
```bash
tail -f /var/log/syslog
```

> Muito útil para **ver logs em tempo real**!

---

## 🧠 5. Comparativo entre os comandos

| Comando | Uso principal                  | Quando usar                           |
|---------|--------------------------------|----------------------------------------|
| `cat`   | Mostrar tudo de uma vez        | Arquivos pequenos                      |
| `less`  | Ler arquivos longos com rolagem| Arquivos grandes, navegação interativa|
| `head`  | Ver o início do arquivo        | Conferir título ou cabeçalho          |
| `tail`  | Ver o final do arquivo         | Ver rodapé ou logs recentes           |

---

## 🔍 6. Dicas práticas

- Combine com `grep` para filtrar enquanto lê:
```bash
cat arquivo.txt | grep "erro"
```

- Combine `tail` com `-f` para monitorar arquivos:
```bash
tail -f /var/log/auth.log
```

- Veja só as 3 primeiras linhas:
```bash
head -n 3 arquivo.txt
```

- Veja só as 5 últimas:
```bash
tail -n 5 arquivo.txt
```

---

## 📝 Teste de fixação

### ❓1. Qual comando é mais indicado para arquivos muito grandes: `cat` ou `less`?

---

### ❓2. Como exibir apenas as primeiras 7 linhas de `resumo.txt`?

---

### ❓3. Qual comando mostra as 10 últimas linhas de `mensagens.log`?

---

### ❓4. O que faz `tail -f /var/log/syslog`?

---

### ❓5. Como navegar no conteúdo de um arquivo com `less` e buscar uma palavra?

---
