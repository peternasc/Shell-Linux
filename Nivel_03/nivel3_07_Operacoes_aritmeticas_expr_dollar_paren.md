
# 🟠 Nível 3 – Tópico 7: Operações Aritméticas — `expr` e `$(( ))`

---

## 📖 1. O que são operações aritméticas no Bash?

O Bash, por padrão, trata **tudo como texto**.  
Mas é possível realizar **operações com números inteiros** usando:

- **`expr`** → Comando externo, mais antigo.
- **`$(( ))`** → Forma moderna e preferida.

---

## 📌 2. Usando `expr`

### 📚 Sintaxe:

```bash
expr VALOR1 OPERADOR VALOR2
```

- Os valores e operadores **devem ter espaços entre eles**.
- Não pode operar diretamente com variáveis sem espaços.

### 📌 Exemplos:

```bash
expr 5 + 3
```

> Saída:
```
8
```

```bash
a=10
b=2
expr $a / $b
```

> Saída:
```
5
```

⚠️ **Importante:** O operador `*` precisa ser **escapado** com `\`:

```bash
expr 5 \* 3
```

> Saída:
```
15
```

---

## 💡 3. Usando `$(( ))` → Forma moderna e preferida

### 📚 Sintaxe:

```bash
$(( expressao ))
```

- Mais elegante e **sem necessidade de espaços**.
- Muito mais usado em scripts modernos.

### 📌 Exemplos:

```bash
echo $((5 + 3))
```

> Saída:
```
8
```

```bash
a=7
b=3
echo $((a * b))
```

> Saída:
```
21
```

```bash
echo $((10 / 2))
```

> Saída:
```
5
```

---

## 🔢 4. Operadores disponíveis

| Operador | Função |
|:---|:---|
| `+` | Soma |
| `-` | Subtração |
| `*` | Multiplicação |
| `/` | Divisão |
| `%` | Módulo (resto da divisão) |

---

## 🚀 5. Exemplo prático completo

```bash
#!/bin/bash

read -p "Digite o primeiro número: " num1
read -p "Digite o segundo número: " num2

echo "Soma: $((num1 + num2))"
echo "Subtração: $((num1 - num2))"
echo "Multiplicação: $((num1 * num2))"

if [ "$num2" -ne 0 ]; then
    echo "Divisão: $((num1 / num2))"
    echo "Resto: $((num1 % num2))"
else
    echo "Divisão por zero não permitida."
fi
```

---

## 🎯 Boas práticas

- Prefira **`$(( ))` sempre que possível** (mais claro e rápido).
- Use `expr` apenas em casos onde for absolutamente necessário (muito raro hoje).
- Sempre valide entradas para evitar divisões por zero.

---
