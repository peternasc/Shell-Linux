
# 🟠 Nível 3 – Tópico 5: Menus com `select`

---

## 📖 1. O que é o `select`?

O `select` é uma estrutura do Bash para:

- Criar **menus interativos simples e rápidos**
- Exibir opções numeradas para o usuário
- Capturar a escolha do usuário de forma fácil

É muito útil para **scripts de automação**, instaladores e ferramentas que exigem que o usuário faça uma escolha.

---

## 📚 2. Sintaxe do `select`

```bash
select variavel in op1 op2 op3
do
    comandos
done
```

### Explicação:

| Parte | Descrição |
|:---|:---|
| `select` | Inicia o menu |
| `variavel` | Guarda a opção escolhida |
| `in` | Lista de opções |
| `do` ... `done` | Comandos a serem executados |

---

## 🛠️ 3. Exemplo básico

```bash
#!/bin/bash

PS3="Escolha uma fruta: "

select fruta in Maçã Banana Laranja Sair
do
    case $fruta in
        "Maçã")
            echo "Você escolheu Maçã."
            ;;
        "Banana")
            echo "Você escolheu Banana."
            ;;
        "Laranja")
            echo "Você escolheu Laranja."
            ;;
        "Sair")
            echo "Saindo..."
            break
            ;;
        *)
            echo "Opção inválida."
            ;;
    esac
done
```

> PS3 → Define o texto que será exibido antes da seleção.

> `break` → Sai do menu.

---

## 🎨 4. Exemplo com números automáticos

```bash
#!/bin/bash

select opcao in "Iniciar" "Parar" "Sair"
do
    echo "Você escolheu a opção $REPLY: $opcao"
    
    if [ "$opcao" == "Sair" ]; then
        break
    fi
done
```

- `$REPLY`: Variável automática que contém **o número digitado** pelo usuário.

---

## 🔑 5. Notas importantes

- O menu continua em **loop até que o comando `break` seja usado**.
- O `select` é **ótimo para menus simples**, mas não é muito personalizável.
- Para menus complexos, pode ser necessário usar `while` + `case` (níveis mais avançados).

---

## 🎯 Boas práticas

- Sempre use `PS3` para personalizar a mensagem de seleção.
- Use `case` junto com `select` para lidar com as opções escolhidas.
- Adicione uma opção de **sair** para evitar loops infinitos.

---
