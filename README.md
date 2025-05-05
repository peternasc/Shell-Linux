
# 🐧 Bash para Gerenciamento de Sistemas e Aplicações (Modo Terminal Puro)

Este repositório é meu guia definitivo de estudos em Bash, com foco total em **administração de sistemas**, **automação de tarefas**, **monitoramento**, **segurança**, e **integração com aplicações e serviços** — **tudo isso 100% em terminal, sem interface gráfica**.  
O plano vai do nível **mais básico possível** até o **super hiper mega avançado**. 🚀

---

## 📘 Estrutura dos Estudos

- ✅ Estilo checklist: cada item pode ser marcado conforme for estudado
- 🔁 Dividido por níveis: do zero ao lendário
- 💻 Foco total em administração de sistemas com Bash
- 🧱 Compatível com servidores, máquinas virtuais, Raspberry Pi headless e sistemas Linux sem GUI

---

## 🟤 Nível 0 – Pré-Básico: Primeiros Passos no Terminal

- [x] [O que é terminal? O que é Bash?](Nivel_00/nivel0_01_O_que_e_terminal_O_que_e_Bash.md.md)
- [x] [Entendendo o shell e seu papel no sistema](Nivel_00/nivel0_02_Entendendo_o_shell_e_seu_papel_no_sistema.md)
- [x] [Como usar o terminal puro (sem interface gráfica)](Nivel_00/nivel0_03_Como_usar_o_terminal_puro.md)
- [x] [Como digitar comandos corretamente](Nivel_00/nivel0_04_Como_digitar_comandos_corretamente.md)
- [x] [Navegação básica: `pwd`, `cd`, `ls`](Nivel_00/nivel0_05_Navegacao_basica_pwd_cd_ls.md)
- [x] [Como sair de comandos travados (`Ctrl + C`)](Nivel_00/nivel0_06_Como_sair_de_comandos_travados.md)
- [x] [Usar seta ↑ para comandos anteriores](Nivel_00/nivel0_07_Usar_seta_para_comandos_anteriores.md)
- [x] [Autocompletar com `Tab`](Nivel_00/nivel0_08_Autocompletar_com_Tab.md)

---

## 🟢 Nível 1 – Básico: Comandos Essenciais e Estrutura de Arquivos

- [x] [Estrutura de diretórios do Linux (`/home`, `/etc`, `/var`, etc.)](Nivel_01/nivel1_01_Estrutura_de_diretorios_do_Linux.md)
- [x] [Criação e manipulação de arquivos e pastas: `touch`, `mkdir`, `cp`, `mv`, `rm`](Nivel_01/nivel1_02_Criacao_e_manipulacao_de_arquivos_e_pastas.md)
- [x] [Permissões e propriedade de arquivos: `chmod`, `chown`, `ls -l`](Nivel_01/nivel1_03_Permissoes_e_propriedade_de_arquivos.md)
- [x] [Leitura de arquivos com `cat`, `less`, `head`, `tail`](Nivel_01/nivel1_04_Leitura_de_arquivos_com_cat_less_head_tail.md)
- [x] [Redirecionamento de entrada e saída: `>`, `>>`, `<`](Nivel_01/nivel1_05_Redirecionamento_de_entrada_e_saida.md)
- [x] [Encadeamento com pipes: `|`](Nivel_01/nivel1_06_Encadeamento_com_pipes.md)
- [x] [Comandos úteis do sistema: `whoami`, `clear`, `history`, `file`](Nivel_01/nivel1_07_Comandos_uteis_do_sistema.md)

---

## 🟡 Nível 2 – Bash Script Iniciante

- [x] [Introdução ao Shell Script](Nivel_02/nivel2_01_Introducao_ao_shell_script.md)
- [x] [Criar e executar scripts (`.sh`, `chmod +x`)](Nivel_02/nivel2_02_Criar_e_executar_scripts.md)
- [x] [Variáveis simples no Shell](Nivel_02/nivel2_03_Variaveis_simples_no_shell.md)
- [x] [Exibir informações com `echo`](Nivel_02/nivel2_04_Exibir_informacoes_com_echo.md)
- [x] [Leitura de entrada com `read`](Nivel_02/nivel2_05_Leitura_de_entrada_com_read.md)
- [x] [Uso de parâmetros (`$1`, `$@`, `$#`)](Nivel_02/nivel2_06_Uso_de_parametros.md)
- [x] [Condições simples com `if`, `then`, `fi`](Nivel_02/nivel2_07_Condicoes_simples_com_if_then_fi.md)
- [x] [Comentários com `#`](Nivel_02/nivel2_08_Comentarios_com_sharp.md)
- [x] [Boas práticas iniciais de script](Nivel_02/nivel2_09_Boas_praticas_iniciais_de_script.md)

---

## 🟠 Nível 3 – Bash Script Estruturado

- [x] [Condicionais completas – `if`, `elif`, `else`](Nivel_03/nivel3_01_Condicionais_completas_if_elif_else.md)
- [x] [`case` para Múltiplas Opções](Nivel_03/nivel3_02_Case_para_multiplas_opcoes.md)
- [x] [Laços de Repetição — `for`, `while`, `until`](Nivel_03/nivel3_03_Lacos_for_while_until.md)
- [x] [Controle de Fluxo — `break` e `continue`](NIvel_03/nivel3_04_Controle_de_fluxo_break_continue.md)
- [x] [Menus com `select`](Nivel_03/nivel3_05_Menus_com_select.md)
- [x] [Códigos de Retorno e Uso de `$?`](Nivel_03/nivel3_06_Codigos_de_retorno_e_uso_de_dolar_question.md)
- [x] [Operações Aritméticas — `expr` e `$(( ))`](Nivel_03/nivel3_07_Operacoes_aritmeticas_expr_dollar_paren.md)
- [x] [Leitura de Arquivos Linha a Linha com `while read`](Nivel_03/nivel3_08_Leitura_de_arquivos_com_while_read.md)
- [x] [Testes de Arquivos — `-f`, `-d`, `-e` e outros](Nivel_03/nivel3_09_Testes_de_arquivos.md)
- [x] [Funções no Bash](Nivel_03/nivel3_10_Funcoes_no_bash.md)
- [x] [Parâmetros em Funções (`$1`, `$2`, `$@`, `$#`)](Nivel_03/nivel3_11_Parametros_em_funcoes.md)
- [x] [Desafios do Nível 3](Nivel_03/nivel3_desafios.md)

---

## 🔵 Nível 4 – Organização e Modularização de Scripts

- [x] [Criação e Uso de Funções](Nivel_04/nivel4_01_Criacao_e_uso_de_funcoes.md)
- [x] [Escopo — Variáveis Locais e Globais](Nivel_04/nivel4_02_Escopo_variaveis_locais_e_globais.md)
- [x] [Reaproveitamento com `source`](Nivel_04/nivel4_03_Reaproveitamento_com_source.md)
- [x] [Boas Práticas e Cabeçalhos de Script](Nivel_04/nivel4_04_Boas_praticas_e_cabecalhos_de_script.md)
- [x] [Estrutura modular de scripts grandes](Nivel_04/nivel4_05_Estrutura_modular_de_scripts_grandes.md)
- [x] [Funções Utilitárias e Reutilizáveis (Exemplos Práticos)](Nivel_04/nivel4_06_Funcoes_utilitarias_e_reutilizaveis.md)
- [x] [Parâmetros e Opções em Funções](Nivel_04/nivel4_07_Parametros_e_opcoes_em_funcoes.md)
- [x] [Tratamento de Erros em Funções](Nivel_04/nivel4_08_Tratamento_de_erros_em_funcoes.md)
- [x] [Funções em Arquivos Separados](Nivel_04/nivel4_09_Funcoes_em_arquivos_separados_bibliotecas_de_funcoes.md)
- [x] [Registro e Logs Simples em Arquivos `.log`](Nivel_04/nivel4_10_Registro_e_logs_simples_em_arquivos_log.md)

---

## 🟣 Nível 5 – Administração de Sistemas Automatizada

- [ ] Verificar espaço em disco: `df`, `du`, `ncdu`
- [ ] Monitoramento de RAM e CPU: `free`, `top`, `htop`, `uptime`
- [ ] Gerenciar processos: `ps`, `kill`, `nice`, `renice`
- [ ] Agendando tarefas: `cron`, `at`, `anacron`
- [ ] Automatizar atualizações com `apt`, `yum`, `dnf`
- [ ] Backups com `tar`, `gzip`, `rsync`
- [ ] Menus interativos em terminal com `dialog` e `whiptail` (modo texto)

---

## 🟥 Nível 6 – Manipulação de Dados e Logs com Bash

- [ ] `grep`, `cut`, `sort`, `uniq`, `xargs`
- [ ] `awk` básico e intermediário
- [ ] `sed` para substituições e transformações
- [ ] Utilitários: `tr`, `paste`, `join`, `split`
- [ ] Manipular `.csv` e `.json` com `jq`
- [ ] Gerar relatórios em terminal (com alinhamento e contagem)

---

## 🔶 Nível 7 – Segurança e Diagnóstico

- [ ] Ver logs do sistema: `journalctl`, `tail -f /var/log/*`
- [ ] Detectar falhas automaticamente (criar analisadores simples)
- [ ] Analisar conexões de rede: `netstat`, `ss`, `lsof`, `nmap`
- [ ] Bloquear IPs com `iptables`, `ufw`, `fail2ban`
- [ ] Verificar permissões de diretórios sensíveis
- [ ] Criptografar e descriptografar arquivos com `gpg`, `openssl`
- [ ] Detectar e registrar logins suspeitos

---

## ⚫ Nível 8 – Integrações e APIs com Bash

- [ ] Enviar mensagens para Telegram, Slack ou Discord via Bash
- [ ] Fazer requisições HTTP com `curl`
- [ ] Interpretar e processar JSON com `jq`
- [ ] Autenticação com token em APIs REST
- [ ] Usar APIs públicas e privadas (clima, moedas, GitHub etc.)
- [ ] Integrações com repositórios, serviços e bancos de dados

---

## 👑 Nível 9 – Terminal Supremo: Autonomia Total

- [ ] Segurança com `set -e`, `set -u`, `trap`, `pipefail`
- [ ] Scripts autorreparáveis (auto-healing)
- [ ] Debug profissional com `bash -x`, `strace`, `lsof`, `dmesg`
- [ ] Automatização de containers: `docker`, `podman`, `lxc`
- [ ] Scripts que geram outros scripts automaticamente
- [ ] Interfaces ricas em terminal com `dialog`, `whiptail`, `fzf`
- [ ] Automação de infraestrutura via Bash: AWS CLI, GCP, Terraform

---

## 📌 Como usar

Clone este repositório, estude com calma e marque `[x]` cada item conforme for concluindo.  
O plano é longo, mas te leva do zero ao topo do Bash como ferramenta de automação e gerenciamento de sistemas Linux! 💪🐧
