
# 🟣 Nível 2 – Tópico 7: Condições Simples com `if`, `then`, `fi`

---

## 📖 1. O que é uma condição em Shell Script?

Condições são usadas para **tomar decisões** nos scripts:

- Executar comandos **apenas se** uma condição for verdadeira
- Criar comportamentos **diferentes** dependendo do que acontecer
- Deixar o script **mais inteligente** e **dinâmico**

---

## 🛠️ 2. Estrutura básica do `if`

```bash
if [ condição ]
then
    comandos
fi
```

- `if` → Inicia a condição
- `[ condição ]` → Avalia uma expressão (como uma comparação)
- `then` → Define o que fazer **se** a condição for verdadeira
- `fi` → Finaliza o bloco `if` (lembre: `fi` é `if` ao contrário)

---

## 📋 3. Exemplo básico

```bash
#!/bin/bash

echo "Digite um número:"
read numero

if [ $numero -gt 10 ]
then
    echo "O número é maior que 10!"
fi
```

---

## 🧠 4. Operadores comuns usados em condições

| Operador | Significado |
|:---------|:------------|
| `-eq` | Igual (`==`) |
| `-ne` | Diferente (`!=`) |
| `-gt` | Maior que (`>`) |
| `-lt` | Menor que (`<`) |
| `-ge` | Maior ou igual (`>=`) |
| `-le` | Menor ou igual (`<=`) |

---

### Exemplos:

```bash
if [ $idade -eq 18 ]
then
    echo "Você tem 18 anos!"
fi
```

```bash
if [ $idade -ge 60 ]
then
    echo "Você é idoso segundo a legislação."
fi
```

---

## 📚 5. Comparações de texto

| Operador | Significado |
|:---------|:------------|
| `=`      | Igual        |
| `!=`     | Diferente    |
| `-z`     | Verifica se a string é vazia |

---

### Exemplo:

```bash
#!/bin/bash

read -p "Digite seu nome: " nome

if [ "$nome" = "Peterson" ]
then
    echo "Bem-vindo, Peterson!"
fi
```

---

## ⚙️ 6. Atenção: espaços são obrigatórios!

**No Bash**, é obrigatório:

- Espaço **entre `[` e a condição** e `]`
- Espaço **entre variáveis, operadores e valores**

✅ Correto:
```bash
if [ $numero -gt 10 ]
```

❌ Errado:
```bash
if [$numero-gt10]
```

---

## 📈 7. Exemplo completo

```bash
#!/bin/bash

read -p "Digite sua idade: " idade

if [ $idade -ge 18 ]
then
    echo "Você é maior de idade!"
fi
```
