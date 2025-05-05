
# 🔵 Nível 4 — Tópico 8: Tratamento de Erros em Funções (return, exit, traps)

---

## 📖 1. Por que tratar erros?

Em scripts profissionais é importante:

✅ Detectar quando algo deu errado  
✅ Interromper a execução ou reagir  
✅ Registrar ou informar o problema

> Sem tratamento de erros, o script pode continuar mesmo com falhas críticas.

---

## 📚 2. Usando `return` em funções

`return` é usado para devolver códigos de status de uma função.

```bash
verificar_arquivo() {
    if [ -f "$1" ]; then
        echo "Arquivo encontrado!"
        return 0
    else
        echo "Arquivo não existe."
        return 1
    fi
}

verificar_arquivo "meuarquivo.txt"
echo "Status da função: $?"
```

> O comando `$?` retorna o código da última execução (0 = sucesso, diferente de 0 = erro).

---

## 🚦 3. Usando `exit` para encerrar o script

`exit` é usado para encerrar **todo o script** imediatamente.

```bash
checar_usuario() {
    if [ "$USER" != "root" ]; then
        echo "Você precisa ser root."
        exit 1
    fi
}

checar_usuario
echo "Isso não será exibido se não for root."
```

> `exit` termina tudo, diferente de `return` que só sai da função.

---

## 📌 4. Combinando `return` e `exit`

**Boa prática**:

- Use `return` para funções → informar sucesso/erro
- Use `exit` somente no script principal → encerrar execução

```bash
executar_comando() {
    comando_inexistente
    return $?
}

executar_comando || exit 1
```

> Se a função falhar, o script termina.

---

## 🧠 5. Usando `trap` para capturar sinais e falhas

`trap` captura eventos (ex: encerramento inesperado, CTRL+C):

```bash
trap "echo 'Encerrando script...'" EXIT

echo "Executando..."
sleep 2
echo "Finalizado."
```

> Quando o script termina (normal ou não), o comando do `trap` é executado.

### 📌 Exemplo: Capturar interrupção

```bash
trap "echo 'Script interrompido!'" SIGINT

echo "Pressione CTRL+C para interromper..."
sleep 10
```

> SIGINT é o sinal enviado ao usar CTRL+C.

---

## 🚨 6. Boas práticas no tratamento de erros

- Sempre retorne códigos claros nas funções (0 para sucesso, diferente de 0 para erro).
- Evite `exit` dentro de funções → prefira `return` para informar falhas.
- Use `trap` para limpar ou registrar ações quando o script terminar ou for interrompido.

---

## 🎯 Conclusão

- `return`: Sair da função e informar status.
- `exit`: Encerrar imediatamente o script.
- `trap`: Capturar sinais para responder eventos (encerramento, interrupção).

Scripts robustos precisam de tratamento de erros para garantir que funcionem de maneira previsível e segura.

---
