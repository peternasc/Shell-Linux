
# 🟠 Nível 3 – Tópico 1: Condicionais completas – `if`, `elif`, `else`

---

## 📖 1. O que são estruturas condicionais completas?

As estruturas `if`, `elif` e `else` permitem ao script **tomar decisões com múltiplos caminhos**.  
Enquanto o `if` sozinho testa **uma única condição**, o uso de `elif` e `else` permite:

- Verificar **múltiplas condições**
- Executar **diferentes blocos de código**
- Criar **fluxos mais inteligentes** e interativos

---

## 🛠️ 2. Estrutura geral do `if/elif/else`

```bash
if [ condição1 ]
then
    # comandos se condição1 for verdadeira
elif [ condição2 ]
then
    # comandos se condição1 for falsa e condição2 for verdadeira
else
    # comandos se nenhuma das condições for verdadeira
fi
```

---

## 📋 3. Exemplo prático

```bash
#!/bin/bash

read -p "Digite sua idade: " idade

if [ "$idade" -lt 18 ]
then
    echo "Você é menor de idade."
elif [ "$idade" -ge 18 ] && [ "$idade" -lt 60 ]
then
    echo "Você é adulto."
else
    echo "Você é idoso."
fi
```

---

## 🔎 4. Observações importantes

- O `elif` significa "**else if**", ou seja, uma nova condição se a anterior falhar.
- O `else` **não recebe nenhuma condição** – ele é executado quando **nenhuma das condições anteriores for verdadeira**.
- Você pode usar **vários `elif` seguidos**, mas **apenas um `else`** por bloco.

---

## 🧠 5. Exemplo com múltiplos `elif`

```bash
#!/bin/bash

read -p "Digite a nota (0-10): " nota

if [ "$nota" -ge 9 ]
then
    echo "Excelente!"
elif [ "$nota" -ge 7 ]
then
    echo "Bom."
elif [ "$nota" -ge 5 ]
then
    echo "Regular."
else
    echo "Insuficiente."
fi
```

---

## 📌 6. Dica: combine `if/elif/else` com operadores lógicos

```bash
if [ "$idade" -ge 18 ] && [ "$idade" -le 30 ]
then
    echo "Você tem entre 18 e 30 anos."
fi
```

---

## ⚠️ 7. Erros comuns

❌ Esquecer de fechar com `fi`  
❌ Usar `else if` em vez de `elif`  
❌ Não usar espaço entre colchetes `[` e os argumentos

---
