
# 🟠 Nível 3 – Tópico 10: Funções no Bash

---

## 📖 1. O que são funções?

Funções são blocos de código que podem ser:

- **Definidos uma vez e reutilizados várias vezes**
- **Organizados para melhorar a leitura e manutenção do script**
- **Chamados a qualquer momento durante a execução**

---

## 📚 2. Por que usar funções?

- Evitam repetição de código (DRY — Don't Repeat Yourself)
- Melhoram a organização e clareza
- Facilitam manutenção e atualizações futuras
- Tornam o script mais modular

---

## 📌 3. Como declarar funções no Bash

### Sintaxe 1 (Recomendada)

```bash
minha_funcao() {
    comandos
}
```

### Sintaxe 2 (Alternativa)

```bash
function minha_funcao {
    comandos
}
```

---

## 🛠️ 4. Exemplo básico

```bash
#!/bin/bash

dizer_ola() {
    echo "Olá, bem-vindo!"
}

# Chamando a função
dizer_ola
```

> Saída:
```
Olá, bem-vindo!
```

---

## 🎒 5. Funções com parâmetros

- As funções podem receber parâmetros como se fossem scripts.

```bash
minha_funcao() {
    echo "Olá, $1!"
}

minha_funcao "Peterson"
```

> Saída:
```
Olá, Peterson!
```

| Parâmetro | Descrição |
|:---|:---|
| `$1` | Primeiro parâmetro |
| `$2` | Segundo parâmetro |
| `$@` | Todos os parâmetros |

---

## 📦 6. Retornando valores (usando `return` ou `echo`)

### Usando `return` (apenas números)

```bash
soma() {
    return $(( $1 + $2 ))
}

soma 5 3
resultado=$?
echo "Resultado: $resultado"
```

> `return` só pode retornar números (0 a 255).

---

### Usando `echo` (recomendado para textos e números):

```bash
soma() {
    echo $(( $1 + $2 ))
}

resultado=$(soma 5 3)
echo "Resultado: $resultado"
```

> Usar `echo` é a maneira mais flexível para capturar valores.

---

## 🧠 7. Exemplo completo

```bash
#!/bin/bash

boas_vindas() {
    echo "Olá, $1! Seja bem-vindo(a)."
}

soma() {
    echo $(( $1 + $2 ))
}

boas_vindas "Peterson"

resultado=$(soma 10 20)
echo "A soma é: $resultado"
```

---

## 🎯 Boas práticas

- Use nomes descritivos para funções.
- Mantenha as funções focadas em **uma única responsabilidade**.
- Comente funções complexas para explicar o propósito.
- Prefira `echo` para retornar valores dinâmicos.

---
