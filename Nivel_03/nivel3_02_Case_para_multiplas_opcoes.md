
# 🟠 Nível 3 – Tópico 2: `case` para Múltiplas Opções

---

## 📖 1. O que é o `case` no Bash?

O comando `case` é uma estrutura de decisão usada para:

- **Verificar múltiplas possibilidades** sem precisar de muitos `if` e `elif`.
- Deixar o script **mais limpo e fácil de ler** quando existem **muitas opções possíveis**.

É uma alternativa mais elegante ao uso excessivo de `if/elif/else`.

---

## 📚 2. Sintaxe do `case`

```bash
case variavel in
    padrão1)
        comandos
        ;;
    padrão2)
        comandos
        ;;
    *)
        comandos padrão (opcional)
        ;;
esac
```

| Parte | Significado |
|:--|:--|
| `case` | Inicia o bloco |
| `variavel` | Valor a ser comparado |
| `padrão)` | Valor esperado para executar os comandos abaixo |
| `;;` | Fim do bloco de comandos daquela opção |
| `*` | Opcional - Valor padrão caso nenhum dos anteriores seja atendido |
| `esac` | Fim do bloco `case` (leia-se "case" ao contrário) |

---

## 🛠️ 3. Exemplo básico de `case`

```bash
#!/bin/bash

read -p "Digite uma letra (a, b ou c): " letra

case $letra in
    a)
        echo "Você escolheu A."
        ;;
    b)
        echo "Você escolheu B."
        ;;
    c)
        echo "Você escolheu C."
        ;;
    *)
        echo "Opção inválida."
        ;;
esac
```

---

## 🧠 4. Quando usar o `case`?

- Quando você precisa **testar várias opções específicas**.
- Quando há **muitas alternativas**, o que deixaria o `if/elif` bagunçado.

**Exemplos comuns:**
- Menus interativos
- Verificar tipos de arquivos/extensões
- Escolha de modos em scripts

---

## 📌 5. Exemplo com valores compostos

```bash
#!/bin/bash

read -p "Digite o nome do dia da semana: " dia

case $dia in
    "sábado" | "domingo")
        echo "É fim de semana!"
        ;;
    "segunda" | "terça" | "quarta" | "quinta" | "sexta")
        echo "É dia útil."
        ;;
    *)
        echo "Dia inválido."
        ;;
esac
```

> Note que `|` pode ser usado para **combinar múltiplos padrões**.

---

## ⚡ 6. Exemplo: Menu interativo

```bash
#!/bin/bash

echo "Escolha uma opção:"
echo "1 - Exibir data"
echo "2 - Listar arquivos"
echo "3 - Sair"

read opcao

case $opcao in
    1)
        date
        ;;
    2)
        ls
        ;;
    3)
        echo "Saindo..."
        ;;
    *)
        echo "Opção inválida"
        ;;
esac
```

---
