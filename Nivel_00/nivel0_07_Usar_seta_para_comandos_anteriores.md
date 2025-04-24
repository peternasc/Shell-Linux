
# 🟤 Nível 0 – Tópico 7: Usar seta ↑ para comandos anteriores

---

## ⏫ 1. O que é o histórico de comandos?

O Bash mantém um **histórico automático de todos os comandos** que você digita.  
Esse histórico é salvo mesmo após reiniciar o terminal!

---

## 🔁 2. Como navegar no histórico?

### Use as **setas do teclado**:

- `↑` – Mostra o comando anterior
- `↓` – Volta para o próximo (caso tenha recuado demais)

---

## 💡 3. Por que isso é útil?

Você pode:

- **Repetir comandos** longos sem digitar tudo de novo
- **Corrigir um erro** em um comando já digitado
- **Testar variações** de um mesmo comando

---

## 🧠 4. Dica: edite o comando ao reaproveitar

```bash
ls -l /etc
```

Se você quiser reaproveitar esse comando, pressione `↑` e altere para:

```bash
ls -l /var
```

Isso evita digitar tudo novamente.

---

## 📁 5. Onde o histórico é armazenado?

O histórico geralmente fica no arquivo oculto:
```bash
~/.bash_history
```

Você pode visualizá-lo com:
```bash
cat ~/.bash_history
```

---

## 🛠 6. Comando `history`

Você também pode listar os últimos comandos digitados com:

```bash
history
```

E para repetir um comando específico:
```bash
!42
```
> Isso executa o comando número 42 da lista.

---

## 📝 Teste de fixação

### ❓1. O que acontece quando você pressiona a tecla seta `↑` no terminal?

---

### ❓2. Qual o nome do comando que exibe todos os comandos anteriores?

---

### ❓3. Onde o histórico de comandos do Bash é armazenado?

---

### ❓4. Como repetir rapidamente o comando número 20 do histórico?

---
