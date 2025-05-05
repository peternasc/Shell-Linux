
# 🔵 Nível 4 — Tópico 4: Boas Práticas e Cabeçalhos de Script

---

## 📖 1. Por que usar cabeçalhos?

Cabeçalhos em scripts são fundamentais para:

✅ Explicar o propósito do script  
✅ Identificar autor e data de criação  
✅ Informar como o script deve ser utilizado  
✅ Facilitar manutenção futura

Sem cabeçalho, entender scripts antigos ou de terceiros pode ser um pesadelo.

---

## 📚 2. Como criar um cabeçalho padrão

### 📌 Exemplo de cabeçalho

```bash
#!/bin/bash
#
# Nome do Script: backup.sh
# Descrição: Realiza backup de arquivos importantes
# Autor: Peterson Nascimento
# Data de criação: 05/2025
# Uso: ./backup.sh /caminho/do/arquivo
#
```

> Dica: Comece sempre seus scripts com cabeçalhos claros.

Campos comuns:

- **Nome do script**
- **Descrição do que ele faz**
- **Autor**
- **Data de criação**
- **Como usar**

---

## 🧠 3. Organização e boas práticas no corpo do script

- **Declare variáveis no início do script**

```bash
DIRETORIO_BACKUP="/backup"
```

- **Comente trechos importantes**

```bash
# Verifica se o diretório existe
if [ -d "$DIRETORIO_BACKUP" ]; then
```

- **Use indentação consistente**

```bash
if [ condição ]; then
    comando
else
    comando
fi
```

- **Evite nomes de variáveis genéricos**

```bash
# Ruim
a=10

# Melhor
quantidade_arquivos=10
```

- **Trate possíveis erros**

```bash
if [ ! -d "$DIRETORIO" ]; then
    echo "Diretório não encontrado!"
    exit 1
fi
```

---

## 📦 4. Exemplo completo com boas práticas

```bash
#!/bin/bash
#
# Nome do Script: verifica_usuario.sh
# Descrição: Verifica se um usuário existe no sistema
# Autor: Peterson Nascimento
# Data de criação: 05/2025
# Uso: ./verifica_usuario.sh <usuario>
#

USUARIO="$1"

# Verifica se um usuário foi informado
if [ -z "$USUARIO" ]; then
    echo "Uso: $0 <usuario>"
    exit 1
fi

# Verifica se o usuário existe
if id "$USUARIO" &>/dev/null; then
    echo "Usuário $USUARIO existe."
else
    echo "Usuário $USUARIO não encontrado."
fi
```

---

## 🎯 Conclusão

- Sempre adicione um cabeçalho em seus scripts.
- Comente seções importantes do código.
- Nomeie variáveis de forma descritiva.
- Trate erros e situações inesperadas.
- Prefira organização e clareza à complexidade.

---
