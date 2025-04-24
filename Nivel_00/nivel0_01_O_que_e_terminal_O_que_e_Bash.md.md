
# 🟤 Nível 0 – O que é Terminal? O que é Bash?

Este é o início do meu guia de estudos de Bash para administração de sistemas **sem interface gráfica**. Aqui você vai entender o que é o terminal, o shell e o Bash — fundamentos essenciais para tudo que vem depois.

---

## 🧠 1. O que é o Terminal?

O **terminal** é uma interface de texto que permite interagir com o sistema operacional usando comandos.  
Em ambientes sem interface gráfica, como servidores ou sistemas minimalistas, ele é a principal (e muitas vezes única) forma de controle.

### Exemplos de comandos básicos:
```bash
ls        # Lista arquivos e diretórios
pwd       # Mostra o diretório atual
cd /etc   # Muda para o diretório /etc
```

---

## 🧩 2. Por que usar o terminal?

Mesmo em sistemas com interface gráfica, administradores usam o terminal porque ele permite:

- Automatizar tarefas repetitivas
- Administrar servidores remotos via SSH
- Ter acesso a recursos que não aparecem em interfaces gráficas
- Trabalhar com mais agilidade e controle

---

## 🧪 3. O que é o Shell?

O **shell** é o programa que interpreta os comandos que você digita no terminal.

### Shells populares:
- `sh` – Shell original
- `bash` – Bourne Again Shell (o mais comum no Linux)
- `zsh`, `fish`, `dash` – Outras opções

---

## 🐚 4. O que é Bash?

O **Bash** (Bourne Again Shell) é o shell mais usado nos sistemas Linux.  
Ele permite executar comandos, criar variáveis, estruturas condicionais, loops e **automatizar qualquer processo** do sistema.

---

## 📟 5. Estou usando Bash?

Digite o comando:
```bash
echo $SHELL
```

Se o resultado for algo como `/bin/bash`, então você está usando o Bash.

---

## 🔄 6. Diferença entre Terminal, Shell e Bash

| Componente | Descrição |
|------------|-----------|
| Terminal   | Interface onde você digita comandos |
| Shell      | O interpretador que executa os comandos |
| Bash       | Um dos tipos de shell mais usados |

---

## 📝 Teste de fixação

Responda às perguntas abaixo **com base no conteúdo acima**:

### ❓1. O que é o terminal e para que ele serve?

---

### ❓2. O que é o shell?

---

### ❓3. Qual a diferença entre terminal, shell e Bash?

---

### ❓4. Como verificar qual shell está em uso no seu sistema?

---

### ❓5. Por que o terminal é tão utilizado em servidores?

---

Pronto! Agora que você entendeu o ambiente, podemos seguir para comandos e navegação básica no sistema de arquivos!
