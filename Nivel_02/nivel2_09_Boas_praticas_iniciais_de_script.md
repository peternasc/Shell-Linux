
# 🟡 Nível 2 – Tópico 9: Boas Práticas Iniciais de Script

---

## 📖 1. Por que boas práticas são importantes?

- Melhoram a **legibilidade** do seu código
- Facilitam a **manutenção** e **atualização** dos scripts
- Evitam **erros difíceis de encontrar** (bugs)
- Deixam o trabalho mais **profissional e organizado**

---

## 📋 2. Boas práticas iniciais essenciais

### 🛡️ Sempre iniciar o script com o **shebang**

O **shebang** (`#!/bin/bash`) define qual interpretador será usado para rodar o script.

```bash
#!/bin/bash
```

---

### 📚 Nomeie seus scripts e variáveis de forma clara

- Evite nomes genéricos como `teste.sh`, `script1.sh`.
- Prefira nomes que expliquem o que o script faz, como `backup_diario.sh`, `monitorar_usuarios.sh`.

Para variáveis:
```bash
usuario_logado="Peterson"
```

---

### 🧹 Mantenha seu código limpo e organizado

- Use **comentários** para explicar trechos importantes.
- Separe blocos de código com linhas em branco para melhorar a visualização.

---

### 📦 Trate entradas de usuário

Sempre valide o que o usuário digita para evitar erros:

```bash
read -p "Digite sua idade: " idade

if [ -z "$idade" ]; then
  echo "Erro: você não digitou nada!"
  exit 1
fi
```

---

### 🔐 Evite códigos desnecessariamente complexos

Prefira scripts simples e diretos, principalmente em ambientes de produção.

---

### 📈 Utilize padrões de indentação

Mantenha o alinhamento do código para facilitar a leitura:

```bash
if [ "$opcao" = "1" ]; then
    echo "Você escolheu a opção 1"
fi
```

---

### 🧠 Sempre use aspas em variáveis

Isso evita problemas com espaços em nomes ou entradas:

```bash
echo "Bem-vindo, $usuario"
```

---

## 📂 3. Exemplo de boas práticas aplicadas

```bash
#!/bin/bash

# Script para saudação personalizada

read -p "Digite seu nome: " nome

if [ -z "$nome" ]; then
    echo "Você não digitou seu nome!"
    exit 1
fi

echo "Bem-vindo, $nome!"
```

---

## 🎯 Resumo final

| Boa prática | Por que usar |
|:---|:---|
| Shebang (`#!/bin/bash`) | Define o interpretador correto |
| Comentários (`#`) | Facilita entender o código |
| Nomes claros | Ajuda a manter a organização |
| Aspas em variáveis | Evita erros com espaços e vazios |
| Tratamento de entrada | Previne falhas inesperadas |
| Indentação | Facilita a leitura e manutenção |

---
