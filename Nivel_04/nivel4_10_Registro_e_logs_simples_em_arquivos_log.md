
# 🔵 Nível 4 — Tópico 10: Registro e Logs Simples em Arquivos `.log`

---

## 📖 1. O que são logs e por que usá-los?

Logs são registros das ações que o script executa.  
São extremamente úteis para:

✅ Saber o que aconteceu durante a execução  
✅ Depurar e corrigir erros  
✅ Auditar atividades realizadas

> Um script sem logs é como um carro sem painel: você não sabe o que está acontecendo.

---

## 📚 2. Como registrar logs em arquivos simples

O método mais direto para registrar é redirecionar a saída com `>>`.

```bash
echo "Iniciando o script em $(date)" >> script.log
```

> `>>` → Adiciona ao final do arquivo sem apagar o conteúdo anterior.

---

## 📦 3. Exemplo de script simples com log

```bash
#!/bin/bash

LOG="meuscript.log"

echo "[$(date)] Script iniciado" >> "$LOG"

# Simular atividade
echo "[$(date)] Processando arquivos..." >> "$LOG"
sleep 2

echo "[$(date)] Script finalizado com sucesso" >> "$LOG"
```

> O arquivo `meuscript.log` terá todos os registros.

---

## 🧹 4. Função para registrar logs (padrão recomendado)

```bash
logar() {
    local mensagem="$1"
    echo "[$(date '+%Y-%m-%d %H:%M:%S')] $mensagem" >> "$LOG"
}

LOG="meuscript.log"

logar "Iniciando script"
logar "Processando dados"
logar "Finalizado com sucesso"
```

> Organiza melhor e padroniza o formato do log.

---

## 🚦 5. Níveis de log (avançado)

Para scripts maiores, é possível adicionar **níveis de log**:

```bash
logar() {
    local nivel="$1"
    local mensagem="$2"
    echo "[$(date '+%Y-%m-%d %H:%M:%S')] [$nivel] $mensagem" >> "$LOG"
}

LOG="meuscript.log"

logar "INFO" "Iniciando script"
logar "WARN" "Aviso sobre dados incompletos"
logar "ERROR" "Erro crítico encontrado"
```

> Permite classificar registros como INFO, WARN, ERROR.

---

## 🚨 6. Boas práticas

- Inclua **timestamp (data e hora)** nas mensagens  
- Padronize o formato dos registros  
- Crie uma função para centralizar a gravação do log  
- Sempre registre erros e ações importantes

---

## 🎯 Conclusão

- Logs são essenciais para rastrear a execução dos scripts  
- Simples de implementar com `echo` + `>>`  
- Funções de log deixam o script mais limpo e organizado  
- Níveis de log permitem categorizar e melhorar a análise posterior

---
