
# 🟠 Nível 3 – Tópico 4: Controle de Fluxo — `break` e `continue`

---

## 📖 1. O que é controle de fluxo?

Em loops (laços), nem sempre você quer que o ciclo siga até o final naturalmente.  
Às vezes é necessário:

- **Parar o loop imediatamente** → `break`
- **Pular uma iteração e continuar com a próxima** → `continue`

---

## 🚪 2. O que é `break`?

O comando `break` é usado para:

- **Encerrar completamente o loop atual** (for, while ou until).
- Ignorar todas as próximas iterações.

### 📌 Exemplo com `break`:

```bash
#!/bin/bash

for numero in {1..10}
do
    if [ "$numero" -eq 5 ]
    then
        echo "Número 5 encontrado, saindo do loop!"
        break
    fi

    echo "Número: $numero"
done
```

> O loop para assim que o número 5 é encontrado.

---

## 🔁 3. O que é `continue`?

O comando `continue` é usado para:

- **Pular a iteração atual** e continuar com a próxima.
- Ignorar apenas o restante do bloco naquela rodada.

### 📌 Exemplo com `continue`:

```bash
#!/bin/bash

for numero in {1..5}
do
    if [ "$numero" -eq 3 ]
    then
        echo "Pulando o número 3"
        continue
    fi

    echo "Número: $numero"
done
```

> O número 3 não será exibido, mas o loop continuará normalmente.

---

## 🔎 4. Quando usar cada um?

| Comando | Quando usar |
|:---|:---|
| `break` | Quando quiser **interromper totalmente** o loop |
| `continue` | Quando quiser **pular uma iteração específica** e seguir normalmente |

---

## 📚 5. Exemplo prático completo

```bash
#!/bin/bash

contador=0

while true
do
    contador=$((contador + 1))

    if [ "$contador" -eq 3 ]
    then
        echo "Pulando o número 3"
        continue
    fi

    if [ "$contador" -gt 5 ]
    then
        echo "Contador maior que 5, saindo..."
        break
    fi

    echo "Contador: $contador"
done
```

> Exemplo que usa **continue** para pular e **break** para sair.

---

## 🎯 Boas práticas

- Use `break` com cuidado → loops podem terminar antes do esperado.
- Use `continue` para melhorar a clareza ao pular etapas específicas.
- Evite abusar de `break` e `continue` → pode tornar o script confuso.

---
