
# 🔵 Nível 4 – Tópico 1: Criação e Uso de Funções

---

## 📖 1. Por que usar funções?

Funções tornam seus scripts:

✅ **Mais organizados** — Dividem o código em blocos lógicos  
✅ **Reutilizáveis** — Evitam repetição  
✅ **Fáceis de manter** — Melhor leitura e manutenção

---

## 📚 2. Como declarar funções (revisão)

### Sintaxe recomendada:

```bash
minha_funcao() {
    comandos
}
```

### Chamando a função:

```bash
minha_funcao
```

---

## 🧠 3. Funções com parâmetros

Você pode passar dados para funções:

```bash
dizer_ola() {
    echo "Olá, $1!"
}

dizer_ola "Peterson"
```

| Parâmetro | Significado |
|:---|:---|
| `$1` | Primeiro argumento |
| `$2` | Segundo argumento |
| `$@` | Todos os argumentos |
| `$#` | Número de argumentos |

---

## 📦 4. Retornando valores

### 🔧 Usando `return` (apenas para códigos numéricos)

```bash
soma() {
    return $(( $1 + $2 ))
}

soma 5 3
resultado=$?
echo "Resultado: $resultado"
```

> ⚡ Limite: `return` só aceita números (0 a 255).

---

### 🧹 Usando `echo` (forma recomendada)

```bash
soma() {
    echo $(( $1 + $2 ))
}

resultado=$(soma 5 3)
echo "Resultado: $resultado"
```

> Essa é a maneira mais flexível, inclusive para textos.

---

## 🚨 5. Funções que verificam erro e retornam status

Funções podem usar `return` para indicar sucesso ou erro:

```bash
verificar_usuario() {
    if id "$1" &>/dev/null; then
        echo "Usuário $1 existe."
        return 0
    else
        echo "Usuário $1 não encontrado."
        return 1
    fi
}

verificar_usuario "root"

if [ $? -eq 0 ]; then
    echo "Tudo certo!"
else
    echo "Algo deu errado."
fi
```

---

## 📌 6. Boas práticas

- Use nomes descritivos para funções.
- Deixe funções pequenas e focadas em uma única tarefa.
- Use `return` para **status de erro/sucesso** e `echo` para **dados e resultados**.
- Sempre comente funções que forem complexas.

---

## 📚 7. Exemplo completo

```bash
#!/bin/bash

mostrar_mensagem() {
    echo "Mensagem: $1"
}

somar() {
    echo $(( $1 + $2 ))
}

mostrar_mensagem "Iniciando o script..."

resultado=$(somar 10 5)
echo "Soma: $resultado"

mostrar_mensagem "Fim do script."
```

---
