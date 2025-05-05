
# 🔵 Nível 4 — Tópico 6: Funções Utilitárias e Reutilizáveis (Exemplos Práticos)

---

## 📖 1. O que são funções utilitárias?

São funções **genéricas** que podem ser reutilizadas em diferentes scripts e situações.

✅ Tornam o script mais organizado  
✅ Evitam repetição de código  
✅ Facilitam manutenção e leitura

**Exemplos clássicos**:

- Funções para exibir mensagens
- Funções para validar entrada de dados
- Funções para verificar se arquivos existem

---

## 📚 2. Exemplo: Função para exibir mensagens formatadas

```bash
exibir_mensagem() {
    echo "====================="
    echo "$1"
    echo "====================="
}

# Uso
exibir_mensagem "Iniciando o script..."
```

> Ajuda a padronizar a saída visual dos scripts.

---

## 📦 3. Exemplo: Função para verificar se arquivo existe

```bash
arquivo_existe() {
    if [ -f "$1" ]; then
        echo "Arquivo encontrado: $1"
        return 0
    else
        echo "Arquivo não encontrado: $1"
        return 1
    fi
}

# Uso
arquivo_existe "/etc/passwd"
```

> Útil para scripts que manipulam arquivos.

---

## 🧹 4. Exemplo: Função para validar entrada

```bash
validar_entrada() {
    if [ -z "$1" ]; then
        echo "Nenhum argumento fornecido!"
        return 1
    fi
    return 0
}

# Uso
validar_entrada "$1" || exit 1
```

> Pode ser usada para garantir que o usuário forneça parâmetros obrigatórios.

---

## 🧠 5. Exemplo: Função para pausar o script

```bash
pausar() {
    read -p "Pressione Enter para continuar..."
}

# Uso
pausar
```

> Útil para scripts interativos ou para dar tempo de leitura.

---

## 🚦 6. Boas práticas para funções utilitárias

- Mantenha funções **curtas e objetivas**
- Use nomes descritivos
- Documente o que cada função faz
- Armazene funções comuns em arquivos como `utils.sh` e carregue com `source`

---

## 🎯 Conclusão

- Funções utilitárias reduzem repetição e aumentam a clareza dos scripts.
- São ideais para projetos que compartilham rotinas.
- Devem ser bem organizadas e documentadas para reutilização.

---
