
# 🟣 Nível 2 – Tópico 8: Comentários com `#`

---

## 📖 1. O que são comentários em Shell Script?

Comentários são **linhas ignoradas** pelo interpretador Bash na hora de rodar o script.

- **Não são comandos.**
- Servem para **explicar o que o script ou trecho de código faz**.
- **Melhoram a legibilidade** e **facilitam a manutenção** do script.

---

## 🛠️ 2. Como criar um comentário

### Basta começar a linha com o símbolo `#`.

```bash
# Isso é um comentário
```

---

## 📋 3. Exemplos práticos

### Comentário de linha única:

```bash
#!/bin/bash

# Script para exibir uma saudação
echo "Olá, mundo!"
```

---

### Comentários após comandos:

```bash
echo "Executando..." # Mensagem de status
```

---

## 📚 4. Atenção!

- Tudo o que estiver **depois do `#`** na linha é ignorado.
- Se você quiser usar o caractere `#` em um texto exibido, ele precisa estar dentro de **aspas**.

### Exemplo correto:

```bash
echo "O símbolo # é usado para comentários."
```

---

## 🧠 5. Boas práticas para comentários

| Dica | Descrição |
|:---|:---|
| Seja claro | Comente **o que** e **por quê**, não apenas **o óbvio** |
| Não comente cada linha | Comente apenas **trechos relevantes** ou **lógicas importantes** |
| Atualize comentários | Se mudar o script, atualize o comentário para não confundir quem ler |
| Prefira frases curtas | Comentários rápidos e diretos são mais fáceis de entender |

---

### Exemplo de boas práticas:

```bash
#!/bin/bash

# Verifica se o usuário digitou um nome
read -p "Digite seu nome: " nome

# Exibe a saudação personalizada
echo "Bem-vindo, $nome!"
```
