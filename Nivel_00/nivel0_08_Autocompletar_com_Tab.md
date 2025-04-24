
# 🟤 Nível 0 – Tópico 8: Autocompletar com Tab

---

## ⌨️ 1. O que é autocompletar?

O Bash permite **completar automaticamente comandos, nomes de arquivos, pastas e usuários** com a tecla:

```
Tab
```

---

## 💡 2. Por que usar?

- **Evita erros de digitação**
- **Economiza tempo**
- **Ajuda a lembrar nomes longos**
- **Mostra opções disponíveis**

---

## 🛠 3. Como funciona?

### Exemplos:

```bash
cd Docu[Tab]
```
> Se existir uma pasta chamada `Documentos`, o Bash completa automaticamente:

```bash
cd Documentos
```

---

```bash
nano scr[Tab]
```
> Se houver um arquivo chamado `script.sh`, o terminal completa:

```bash
nano script.sh
```

---

## 🔁 4. Se houver mais de uma opção?

Se o que você digitou pode se referir a **vários arquivos ou pastas**, o Bash **não completa imediatamente**, mas você pode pressionar `Tab` duas vezes para ver as opções.

### Exemplo:
```bash
cd D[Tab][Tab]
```

Saída:
```
Desktop/  Downloads/  Documentos/
```

---

## 🔍 5. Completar comandos também funciona

Se você começar a digitar um comando e não lembrar o final:

```bash
uni[Tab]
```

Se `uniq` estiver instalado, o Bash completa:
```bash
uniq
```

---

## 🔄 6. Completar nomes de usuários

Você pode usar `~` seguido de `Tab` para ver usuários (em alguns sistemas):

```bash
cd ~[Tab][Tab]
```

---

## 📝 Teste de fixação

### ❓1. Qual tecla usamos para ativar o recurso de autocompletar no Bash?

---

### ❓2. O que acontece se houver mais de uma opção ao autocompletar?

---

### ❓3. Como o autocompletar pode ajudar na hora de digitar comandos ou caminhos?

---

### ❓4. O que acontece se você digitar `cd D` e pressionar `Tab` duas vezes?

---
