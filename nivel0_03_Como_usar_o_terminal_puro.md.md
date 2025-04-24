
# 🟤 Nível 0 – Tópico 2: Como usar o terminal puro (sem interface gráfica)

---

## 🧠 1. Quando você está em um sistema sem interface gráfica

Em um sistema Linux **sem interface gráfica (sem GUI)**, o **terminal é tudo que você tem**.  
Você interage com o sistema diretamente após o login — e esse ambiente é chamado de **modo texto** ou **modo console**.

---

## 🔐 2. Login no terminal puro

Ao iniciar o sistema, você verá algo como:

```
Debian GNU/Linux 12 debian tty1

debian login:
```

Você deve digitar seu **nome de usuário** e, em seguida, sua **senha**. A senha não aparece enquanto você digita — isso é normal por segurança.

---

## 🧭 3. O que aparece após o login?

Logo após o login, você verá uma **linha de comando** como esta:

```
peterson@debian:~$
```

Essa linha é chamada de **prompt**. Ela mostra que o shell está esperando por um comando seu.

---

## 🧪 4. Exemplos práticos de comandos para começar

Aqui estão alguns comandos básicos que funcionam **em qualquer terminal puro**:

```bash
pwd          # Mostra onde você está (diretório atual)
ls           # Lista arquivos e pastas
cd /etc      # Entra na pasta /etc
cd           # Volta para seu diretório pessoal
clear        # Limpa a tela do terminal
```

---

## 🧱 5. Informações úteis que você pode obter com comandos simples

```bash
whoami       # Mostra seu nome de usuário
hostname     # Mostra o nome da máquina
date         # Mostra a data e hora atuais
uptime       # Mostra há quanto tempo o sistema está ligado
```

---

## ⚠️ 6. Algumas diferenças importantes no modo texto

- **Você não pode usar o mouse** (tudo é com o teclado)
- **Você não pode abrir arquivos com duplo clique**
- **Não há janelas nem ícones**
- **Tudo acontece com comandos e arquivos de configuração**

---

## 🧭 7. Dicas para navegar mais fácil

- Use a tecla **↑** para ver comandos anteriores
- Use **Tab** para completar nomes de arquivos ou pastas
- Use **Ctrl + C** para cancelar um comando travado
- Use **Ctrl + L** (ou `clear`) para limpar a tela

---

## 📝 Teste de fixação

Responda com base no que aprendeu:

### ❓1. O que acontece após o login em um sistema Linux sem interface gráfica?

---

### ❓2. O que é o prompt?

---

### ❓3. Qual comando mostra onde você está no sistema de arquivos?

---

### ❓4. Quais atalhos de teclado ajudam na navegação no terminal?

---

### ❓5. O que significa quando você digita a senha e nada aparece?

---

Pronto! Agora que você está à vontade no terminal puro, podemos partir para o próximo tópico: **Navegação e estrutura de diretórios**.
