
# 🟣 Nível 2 – Tópico 4: Exibir Informações com `echo`

---

## 📖 1. O que é o comando `echo`?

O `echo` é um dos comandos mais básicos e importantes no Shell Script.  
Ele **exibe mensagens na tela** ou **escreve conteúdo em arquivos**.

É usado para:

- Mostrar informações para o usuário
- Exibir resultados de variáveis
- Imprimir mensagens de status em scripts
- Criar ou modificar arquivos (com redirecionamento)

---

## ⚙️ 2. Como usar o `echo`

### Exibir uma mensagem simples:

```bash
echo "Olá, mundo!"
```

> Saída:
```
Olá, mundo!
```

---

### Exibir o valor de uma variável:

```bash
nome="Peterson"
echo "Bem-vindo, $nome!"
```

> Saída:
```
Bem-vindo, Peterson!
```

---

## 📋 3. Opções (flags) úteis do `echo`

| Flag        | Função                             |
|:------------|:-----------------------------------|
| `-n`        | Não adicionar nova linha no final  |
| `-e`        | Interpretar sequências especiais (`\n`, `\t`, etc.) |

---

### Exemplo com `-n` (sem nova linha):

```bash
echo -n "Digite seu nome: "
```
> O cursor fica na mesma linha.

---

### Exemplo com `-e` (permitir caracteres especiais):

```bash
echo -e "Primeira linha\nSegunda linha"
```
> Saída:
```
Primeira linha
Segunda linha
```

---

### Sequências especiais usadas com `-e`:

| Sequência | Função                  |
|:----------|:------------------------|
| `\n`      | Nova linha                |
| `\t`      | Tabulação (tab)           |
| `\\`      | Exibe uma barra invertida |
| `\"`      | Exibe aspas duplas        |

---

## 🛠️ 4. Redirecionar a saída do `echo` para um arquivo

Você pode usar o `>` ou `>>` para criar ou adicionar conteúdo a arquivos.

### Criar um novo arquivo (ou sobrescrever):
```bash
echo "Primeira linha" > arquivo.txt
```

---

### Adicionar uma linha ao final de um arquivo existente:
```bash
echo "Mais uma linha" >> arquivo.txt
```

---

## 📚 5. Exemplo completo

```bash
#!/bin/bash

echo "Iniciando o script..."
nome="Peterson"
echo "Usuário logado: $nome"
echo -e "Operação concluída!\nObrigado por usar o sistema."
```

---

## 🎯 Boas práticas ao usar `echo`

- Sempre use aspas duplas ao redor dos textos para evitar erros com espaços ou variáveis.
- Se o texto tiver sequências especiais como `\n`, lembre de usar `-e`.
- Para mensagens sem quebrar linha, use `-n` de forma consciente.

---
