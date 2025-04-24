
# 🟤 Nível 0 – Tópico 6: Como sair de comandos travados (Ctrl + C)

---

## 🧨 1. O que são comandos “travados”?

Alguns comandos podem **ficar rodando indefinidamente** ou esperar uma entrada que você não percebeu.

### Exemplos:
```bash
ping google.com     # continua pingando até você parar
cat                 # espera você digitar algo
```

---

## ⛔ 2. Como interromper esses comandos?

### Use o atalho de teclado:
```
Ctrl + C
```

Este atalho **envia um sinal de interrupção (SIGINT)** para o processo em execução, dizendo:  
> “Pare agora!”

---

## 📌 3. Quando usar o Ctrl + C?

Use `Ctrl + C` quando:

- Um comando **não está terminando**
- Você quer **cancelar** algo que digitou errado
- Está em um comando como `cat`, `ping`, ou `top` e quer sair

---

## ⚠️ 4. O que acontece depois?

- O comando é interrompido
- Você volta imediatamente ao prompt
- Nenhum dado é salvo (por isso, cuidado!)

---

## 🧠 5. Diferença entre Ctrl + C e Ctrl + Z

| Atalho     | O que faz                                 |
|------------|--------------------------------------------|
| `Ctrl + C` | **Interrompe** e encerra o processo        |
| `Ctrl + Z` | **Suspende** temporariamente o processo    |

---

## 📝 Teste de fixação

### ❓1. Qual atalho de teclado usamos para interromper comandos que não terminam?

---

### ❓2. O que acontece se você digitar `cat` e não fizer mais nada?

---

### ❓3. Qual a diferença entre `Ctrl + C` e `Ctrl + Z`?

---
