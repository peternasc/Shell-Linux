
# 🟣 Nível 2 – Tópico 5: Leitura de Entrada com `read`

---

## 📖 1. O que é o comando `read`?

O `read` é o comando usado em Shell Script para:

- **Ler dados digitados pelo usuário** no terminal
- **Armazenar esses dados em variáveis** para uso posterior no script

É uma ferramenta essencial para criar scripts **interativos**, onde o usuário precisa informar dados em tempo real.

---

## ⚙️ 2. Como usar o `read`

### Sintaxe básica:

```bash
read variavel
```

---

### Exemplo básico:

```bash
#!/bin/bash

echo "Digite seu nome:"
read nome
echo "Olá, $nome!"
```

> Saída (após digitar "Peterson"):
```
Digite seu nome:
Olá, Peterson!
```

---

## 📋 3. Ler várias variáveis de uma vez

Você pode ler **vários valores** de uma vez usando múltiplas variáveis.

```bash
read nome idade cidade
```

Se o usuário digitar:

```
Peterson 35 "São Paulo"
```

As variáveis ficam:

| Variável | Valor        |
|:---------|:-------------|
| `nome`   | Peterson     |
| `idade`  | 35           |
| `cidade` | São Paulo    |

---

## 🧠 4. Flags e opções úteis do `read`

| Flag       | Função |
|:-----------|:-------|
| `-p`       | Exibe uma mensagem antes de ler |
| `-s`       | Oculta o que é digitado (ideal para senhas) |
| `-t SEGUNDOS` | Define um tempo limite para a resposta |
| `-n NUM`   | Lê apenas `NUM` caracteres |

---

### Exemplos:

#### `-p` para exibir mensagem:

```bash
read -p "Digite seu nome: " nome
```

---

#### `-s` para esconder o que o usuário digita:

```bash
read -s -p "Digite sua senha: " senha
echo
echo "Senha recebida!"
```

---

#### `-t` para tempo limite:

```bash
read -t 5 -p "Digite algo em até 5 segundos: " resposta
echo "Você digitou: $resposta"
```

---

#### `-n` para número fixo de caracteres:

```bash
read -n 1 -p "Digite S para continuar: " escolha
echo
echo "Você escolheu: $escolha"
```

---

## 📂 5. Exemplo completo

```bash
#!/bin/bash

read -p "Qual seu nome? " nome
read -p "Qual sua idade? " idade

echo "Seja bem-vindo(a), $nome! Você tem $idade anos."
```

---

## 🎯 Boas práticas com `read`

- Sempre informar ao usuário o que se espera dele (`-p`).
- Usar `-s` quando for pedir informações sensíveis (senhas).
- Validar se o usuário realmente digitou algo (em níveis mais avançados).

---
