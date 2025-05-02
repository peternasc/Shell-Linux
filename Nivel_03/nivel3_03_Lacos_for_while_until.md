
# 🟠 Nível 3 – Tópico 3: Laços de Repetição — `for`, `while`, `until`

---

## 📖 1. O que são laços de repetição?

Laços (ou loops) são usados para:

- **Executar comandos repetidamente** enquanto uma condição for verdadeira (ou até que seja).
- Automatizar tarefas que precisam ser repetidas.

No Bash, os principais tipos de laços são:

| Laço | Quando usar |
|:---|:---|
| `for` | Quando já se sabe **quantas vezes** executar |
| `while` | Quando precisa repetir **enquanto uma condição for verdadeira** |
| `until` | Quando precisa repetir **até que uma condição se torne verdadeira** |

---

## 🔄 2. Laço `for`

### 📚 Sintaxe básica:

```bash
for variavel in lista
do
    comandos
done
```

### 📌 Exemplo:

```bash
#!/bin/bash

for nome in Ana Bruno Carlos
do
    echo "Olá, $nome!"
done
```

> Saída:
```
Olá, Ana!
Olá, Bruno!
Olá, Carlos!
```

---

### 📌 Exemplo com sequência numérica:

```bash
for numero in {1..5}
do
    echo "Número: $numero"
done
```

> Saída:
```
Número: 1
Número: 2
...
Número: 5
```

---

## 🔁 3. Laço `while`

### 📚 Sintaxe:

```bash
while [ condição ]
do
    comandos
done
```

### 📌 Exemplo:

```bash
#!/bin/bash

contador=1

while [ $contador -le 5 ]
do
    echo "Contador: $contador"
    contador=$((contador + 1))
done
```

> Executa enquanto o contador for menor ou igual a 5.

---

## ⬇️ 4. Laço `until`

### 📚 Sintaxe:

```bash
until [ condição ]
do
    comandos
done
```

- Funciona **ao contrário do while**.
- Executa **enquanto a condição for falsa**.

### 📌 Exemplo:

```bash
#!/bin/bash

contador=1

until [ $contador -gt 5 ]
do
    echo "Contador: $contador"
    contador=$((contador + 1))
done
```

> Executa **até que o contador seja maior que 5**.

---

## 🚦 5. Diferenças entre `while` e `until`

| Laço | Quando termina |
|:---|:---|
| `while` | Quando a condição se torna falsa |
| `until` | Quando a condição se torna verdadeira |

Ou seja:
- `while`: "Faça enquanto for VERDADEIRO"
- `until`: "Faça até que fique VERDADEIRO"

---

## 🎯 Boas práticas com laços

- Evitar loops infinitos (a menos que seja intencional)
- Garantir que a condição **vai mudar** para não travar o script
- Usar `break` e `continue` para maior controle (veremos no próximo tópico)

---
