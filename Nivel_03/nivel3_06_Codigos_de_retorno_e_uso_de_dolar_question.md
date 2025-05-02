
# 🟠 Nível 3 – Tópico 6: Códigos de Retorno e Uso de `$?`

---

## 📖 1. O que são códigos de retorno (exit status)?

Todo comando no Linux/Bash **termina com um status de saída** (exit status), que é um **número que indica o resultado da execução**.

| Código | Significado |
|:--|:--|
| `0` | Sucesso |
| Diferente de `0` | Algum tipo de erro ocorreu |

Esse valor é **muito importante para verificar se um comando funcionou ou falhou**.

---

## 📚 2. Como capturar o código de retorno?

Logo após executar um comando, o código de retorno fica armazenado na **variável especial `$?`**.

```bash
comando
echo $?
```

> Mostra o status da última execução.

---

## 🛠️ 3. Exemplo básico:

```bash
#!/bin/bash

ls /etc
echo "O comando ls retornou: $?"

ls /pasta/nao/existe
echo "O comando ls retornou: $?"
```

> Saída:
```
O comando ls retornou: 0
ls: cannot access '/pasta/nao/existe': No such file or directory
O comando ls retornou: 2
```

---

## 🧠 4. Usando `$?` em scripts para validar comandos

```bash
#!/bin/bash

echo "Tentando criar diretório..."
mkdir /algum/diretorio

if [ $? -eq 0 ]
then
    echo "Diretório criado com sucesso."
else
    echo "Falha ao criar diretório."
fi
```

---

## 🔧 5. O comando `exit` e códigos personalizados

Você pode usar `exit` para:

- **Finalizar um script** com um código específico

```bash
#!/bin/bash

read -p "Digite sua idade: " idade

if [ "$idade" -lt 18 ]
then
    echo "Acesso negado."
    exit 1
fi

echo "Acesso permitido."
exit 0
```

> Saída do script será 0 ou 1, dependendo da idade.

---

## 📌 6. Tabela de códigos de retorno comuns

| Código | Significado |
|:--|:--|
| 0 | Sucesso |
| 1 | Falha geral / erro genérico |
| 2 | Uso incorreto do comando |
| 126 | Comando encontrado, mas não executável |
| 127 | Comando não encontrado |
| 128+N | Comando finalizado por sinal |

---

## 🎯 Boas práticas

- Verifique sempre o código de retorno para capturar erros críticos.
- Use códigos de saída **consistentes e documentados** em scripts que serão chamados por outros.
- Em scripts pequenos, `$?` é suficiente; em scripts maiores, prefira `exit` com códigos bem definidos.

---
