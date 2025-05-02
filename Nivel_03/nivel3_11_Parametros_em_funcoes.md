
# 🟠 Nível 3 – Tópico 11: Parâmetros em Funções (`$1`, `$2`, `$@`, `$#`)

---

## 📖 1. O que são parâmetros em funções?

Funções no Bash podem receber informações **no momento da chamada**, exatamente como os scripts recebem argumentos na linha de comando.

Isso é útil para:

- **Reutilizar funções para diferentes dados**
- **Tornar o script mais flexível e dinâmico**

---

## 📚 2. Como passar parâmetros para uma função

### 📌 Exemplo simples

```bash
#!/bin/bash

dizer_ola() {
    echo "Olá, $1!"
}

dizer_ola "Peterson"
dizer_ola "Maria"
```

> Saída:
```
Olá, Peterson!
Olá, Maria!
```

---

## 🧠 3. Acessando os parâmetros dentro da função

| Parâmetro | O que representa |
|:---|:---|
| `$1` | Primeiro argumento |
| `$2` | Segundo argumento |
| `$@` | Todos os argumentos |
| `$#` | Quantidade de argumentos |

---

### 📌 Exemplo com múltiplos argumentos

```bash
#!/bin/bash

mostrar_dados() {
    echo "Nome: $1"
    echo "Idade: $2"
}

mostrar_dados "Peterson" "35"
```

> Saída:
```
Nome: Peterson
Idade: 35
```

---

## 📦 4. Usando `$@` para listar todos os argumentos

```bash
#!/bin/bash

listar() {
    echo "Você passou $# argumentos."

    for argumento in "$@"
    do
        echo "Argumento: $argumento"
    done
}

listar "Ana" "Bruno" "Carlos"
```

> Saída:
```
Você passou 3 argumentos.
Argumento: Ana
Argumento: Bruno
Argumento: Carlos
```

---

## 📌 5. Quando `$@` e `$#` são úteis

- `$@` → Para **percorrer todos os argumentos**
- `$#` → Para **validar quantos argumentos foram passados**

### 📌 Exemplo validando argumentos:

```bash
#!/bin/bash

validar() {
    if [ "$#" -lt 2 ]
    then
        echo "Uso correto: validar arg1 arg2"
        return 1
    fi

    echo "Parâmetros ok: $1 e $2"
}

validar "Peterson"
validar "Peterson" "35"
```

> O primeiro chamará o aviso, o segundo passará normalmente.

---

## 🎯 Boas práticas

- Sempre valide a quantidade de parâmetros com `$#` para evitar erros.
- Use nomes claros para funções que recebem parâmetros.
- Utilize `$@` quando quiser repassar ou iterar todos os parâmetros.

---
