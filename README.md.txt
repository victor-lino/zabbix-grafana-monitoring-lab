# Zabbix + Grafana Monitoring Lab (VM Infrastructure Project)

## Visão geral

Este projeto consiste na implementação de um ambiente completo de monitoramento utilizando Zabbix e Grafana em máquinas virtuais Linux e Windows.

O objetivo foi simular um cenário próximo ao de produção, com foco em observabilidade, troubleshooting de rede, integração entre ferramentas e alertas automatizados.

---

## Arquitetura do ambiente

- Zabbix Server (Linux VM)
- Zabbix Frontend (Web UI)
- Linux Agent (com múltiplas interfaces de rede)
- Windows Agent
- Grafana (dashboard de visualização)
- Integração via Zabbix API
- Alertas por e-mail via Zabbix Media Types

---

## Objetivos do projeto

- Implementar monitoramento centralizado de infraestrutura
- Coletar métricas de máquinas Linux e Windows
- Criar dashboards separados por host no Grafana
- Configurar alertas automáticos por e-mail
- Simular um ambiente real de observabilidade
- Praticar troubleshooting de rede e serviços distribuídos

---

## Tecnologias utilizadas

- Zabbix Server / Zabbix Agent
- Grafana
- Linux (Debian/Ubuntu)
- Windows Server / Windows VM
- Networking com múltiplas sub-redes
- Zabbix API
- SMTP para envio de e-mails

---

## Prints do projeto

### Arquitetura do ambiente
![Arquitetura](images/architecture.png)

### Dashboard Grafana - Linux
![Grafana Linux](images/grafana-linux.png)

### Dashboard Grafana - Windows
![Grafana Windows](images/grafana-windows.png)

### Hosts no Zabbix
![Hosts Zabbix](images/zabbix-hosts.png)

### Dados em tempo real (Latest Data)
![Latest Data](images/latest-data.png)

### Alertas por e-mail
![Email Alerts](images/email-alerts.png)

### Teste de comunicação (zabbix_get)
![Terminal](images/terminal-zabbix-get.png)

---

## Problemas enfrentados e soluções

### 1. Integração Grafana + Zabbix
- Problema: falha de conexão via API
- Causa: endpoint e configuração incorreta
- Solução: ajuste de URL e autenticação da API

---

### 2. EMPTY RESPONSE no Zabbix Agent
- Problema: zabbix_get não retornava dados
- Causa: mismatch entre IP do host e interface configurada
- Solução: correção de Server e ServerActive no agent

---

### 3. Conflito de redes
- Problema: múltiplas interfaces (192.168.99.x e 192.168.244.x)
- Causa: confusão de roteamento entre sub-redes
- Solução: padronização do IP usado pelo Zabbix

---

### 4. Host mal configurado no Zabbix frontend
- Problema: agent não respondia corretamente
- Causa: interface IP incorreta no host
- Solução: ajuste do IP do host para o agente correto

---

### 5. Validação de comunicação
Ferramentas utilizadas para diagnóstico:

- zabbix_get
- nc (netcat)
- curl
- ss

---

## Resultados finais

- Ambiente de monitoramento totalmente funcional
- Coleta de métricas em tempo real
- Dashboards separados por máquina no Grafana
- Alertas por e-mail operando corretamente
- Visibilidade completa da infraestrutura virtual

---

## Aprendizados

Este projeto reforçou conceitos essenciais de infraestrutura e observabilidade:

- Monitoramento depende da comunicação correta entre componentes
- Pequenos erros de rede podem quebrar toda a cadeia de observabilidade
- Troubleshooting com ferramentas de linha de comando é essencial
- Entendimento de redes e interfaces é crítico em ambientes distribuídos
- Integração entre sistemas exige precisão e validação constante

---

## Conclusão

Este projeto consolidou minha experiência prática com infraestrutura, monitoramento e troubleshooting em ambientes distribuídos.

Foi fundamental para desenvolver uma visão mais realista de ambientes de produção e fortalecer habilidades em Linux, redes e observabilidade.

---

## Status

Projeto funcional  
Ambiente estável  
Monitoramento ativo