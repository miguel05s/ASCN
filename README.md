# ASCN — Warracker na Google Cloud

Trabalho prático de **Aplicações e Serviços de Computação em Nuvem** (Mestrado em Engenharia Informática, Universidade do Minho, 2026/27).

> 🚧 Projeto em desenvolvimento. Os playbooks e manifestos serão adicionados quando estiverem concluídos.

## Objetivo

Automatizar a instalação, configuração, monitorização e avaliação do [Warracker](https://github.com/sassanix/warracker), uma aplicação web de gestão de garantias de produtos, no **Google Kubernetes Engine (GKE)** com **Ansible**.

## A aplicação

- **`warracker`:** nginx (frontend estático e proxy de `/api/`) e gunicorn com o backend Flask (API REST com JWT e agendador de alertas), geridos pelo supervisord
- **`warrackerdb`:** PostgreSQL 15
- **Volumes:** `postgres_data` (base de dados) e `warracker_uploads` (anexos)

## Tarefas

1. **Instalação automática:** playbooks Ansible que criam o cluster GKE e instalam a aplicação (Deployments, Services, PVCs), com os componentes em pods distintos e dados persistentes entre paragens.
2. **Exploração e otimização:** identificar gargalos e pontos únicos de falha, replicar o servidor aplicacional com balanceamento de carga e autoscaling, monitorizar com o Google Cloud Monitoring e medir o impacto com testes de carga (Locust ou k6).

## Entregas

| Fase | Prazo | Estado |
|---|---|---|
| Checkpoint 1: relatório inicial | 08/11/2026 | ✅ [Relatório](checkpoint1-relatorio-inicial.pdf) |
| Checkpoint 2: aplicação no GKE acessível do exterior | 06/12/2026 | ⏳ |
| Entrega final: código e relatório | 30/12/2026 | ⏳ |

## Tecnologias

Ansible · Google Kubernetes Engine · Kubernetes · Docker · PostgreSQL · Google Cloud Monitoring
