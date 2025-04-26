
# 🟣 Nível 2 – Tópico 3: Variáveis Simples no Shell

---

## 📖 1. O que são variáveis no Shell?

Variáveis no Shell são **espaços de memória reservados** para **armazenar valores temporários** como:

- Textos (strings)
- Números
- Resultados de comandos
- Caminhos de arquivos

Assim como em outras linguagens de programação, variáveis no Bash servem para **guardar e manipular dados**.

---

## 📋 2. Como declarar variáveis

### Sintaxe:
```bash
nome_variavel=valor
```

⚠️ **Muito importante: NÃO pode haver espaços antes ou depois do sinal `=`.**

---

### Exemplos:

```bash
nome="Peterson"
idade=35
cidade="São Paulo"
```

Correto:
```bash
nome="Peterson"
```

Incorreto:
```bash
nome = "Peterson"
```

---

## 📖 3. Como acessar o valor de uma variável

Para usar uma variável, **coloque o símbolo `$`** na frente do nome.

### Exemplo:
```bash
echo $nome
```
> Saída:
```
Peterson
```

---

## 📚 4. Exemplo completo

```bash
#!/bin/bash

nome="Peterson"
echo "Olá, $nome! Bem-vindo ao Bash!"
```

---

## 🛠️ 5. Variáveis com comandos (`command substitution`)

Você também pode **guardar o resultado de comandos** em variáveis usando crase (`` ` ``) ou `$(...)`.

### Exemplo:

```bash
data=$(date)
echo "A data de hoje é: $data"
```

---

## 🧠 6. Convenções e boas práticas

| Boa prática | Descrição |
|:---|:---|
| Nomes em minúsculo ou com _ | Evitar espaços e letras maiúsculas |
| Descritivos | Escolha nomes que indiquem o que armazenam |
| Constantes em maiúsculo | Variáveis que não mudam devem ser em caixa alta (ex: `PI=3.14`) |

---

### Exemplos de boas práticas:

```bash
meu_nome="Peterson"
total_usuarios=5
ARQUIVO_LOG="/var/log/syslog"
```

---

## 🧹 7. Apagando variáveis

Você pode "destruir" uma variável usando o comando `unset`:

```bash
unset nome
```

Depois disso, a variável `nome` não existirá mais.

---

## 📜 8. Tipos de dados em Bash

No Shell Script:

- **Tudo é tratado como texto.**
- Não existe diferenciação direta entre número, texto ou booleano (como em linguagens mais complexas).

O Bash interpreta **conforme o contexto** (exemplo: quando você compara dois valores ou faz operações aritméticas, ele trata como número).

---
