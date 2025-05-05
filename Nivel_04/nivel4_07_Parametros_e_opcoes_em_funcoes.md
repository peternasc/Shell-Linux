
# 🔵 Nível 4 — Tópico 7: Parâmetros e Opções em Funções (Argumentos Nomeados e Posicionais)

---

## 📖 1. O que são parâmetros e argumentos?

Quando chamamos funções em shell, podemos:

✅ Passar **valores posicionais** (exemplo: `$1`, `$2`, `$3`)  
✅ Tratar esses valores dentro da função para torná-la flexível  
✅ Também aceitar **opções nomeadas** (usando flags ou argumentos específicos)

---

## 📚 2. Parâmetros posicionais simples

Funções recebem argumentos pela ordem que são passados:

```bash
saudacao() {
    echo "Olá, $1!"
}

saudacao "Peterson"
```

> `$1` é o primeiro argumento passado para a função.

Você pode acessar:

- `$1`, `$2`, `$3` ... → até o 9º argumento direto  
- `${10}`, `${11}` → para argumentos acima do 9º

### 📌 Todos os argumentos

```bash
exibir_todos() {
    echo "Todos os argumentos: $@"
}

exibir_todos "um" "dois" "três"
```

> `$@` contém todos os argumentos como lista.

---

## 🧹 3. Quantidade de argumentos

```bash
quantidade() {
    echo "Foram passados $# argumentos."
}

quantidade "um" "dois"
```

> `$#` é o número de argumentos recebidos.

---

## 📦 4. Exemplo prático com validação

```bash
ola_usuario() {
    if [ -z "$1" ]; then
        echo "Você precisa informar seu nome!"
        return 1
    fi

    echo "Bem-vindo, $1!"
}

ola_usuario "Peterson"
ola_usuario
```

> Validação de argumento obrigatório com `-z`.

---

## 🧠 5. Trabalhando com argumentos nomeados (opções)

Argumentos nomeados não são automáticos, você cria a lógica para interpretar:

```bash
executar_acao() {
    while [[ "$#" -gt 0 ]]; do
        case $1 in
            --start)
                echo "Iniciando..."
                ;;
            --stop)
                echo "Parando..."
                ;;
            *)
                echo "Opção desconhecida: $1"
                ;;
        esac
        shift
    done
}

executar_acao --start --stop --foo
```

> `shift` move os argumentos ($1 vira $2, $2 vira $3...).

---

## 🚦 6. Boas práticas

- Valide todos os parâmetros necessários
- Dê feedback claro para opções desconhecidas
- Use `shift` para processar listas de argumentos
- Combine parâmetros posicionais e nomeados para flexibilidade

---

## 🎯 Conclusão

- Parâmetros posicionais são fáceis e rápidos
- Argumentos nomeados (flags) tornam funções mais robustas
- Boas práticas evitam erros e tornam o script mais profissional

---
