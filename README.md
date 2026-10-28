# 🛡️ Incident Response ZFS

**Diagnóstico forense de pools ZFS em modo somente leitura.**

![Status](https://img.shields.io/badge/status-em%20constru%C3%A7%C3%A3o-yellow)
![Foco](https://img.shields.io/badge/foco-DFIR-blue)
![Shell](https://img.shields.io/badge/shell-Bash-4EAA25)
![ZFS](https://img.shields.io/badge/ZFS-OpenZFS-2E3192)

> Projeto criado a partir de um atendimento real de ransomware, com o objetivo de coletar evidências de um pool ZFS **sem alterar o seu estado**.

## 🚧 Status

Em construção — a primeira versão pública ainda não foi lançada.

## 🎯 Objetivo

Permitir que um analista colete metadados e evidências de um pool ZFS (Linux, TrueNAS ou Proxmox) preservando a integridade dos dados, com foco em:

- Levantamento da configuração do pool e dos datasets
- Histórico de operações (`zpool history`)
- Snapshots disponíveis e janela de recuperação
- Geração de relatório para o laudo

## 🧭 Princípios

| Princípio | Como é aplicado |
| :--- | :--- |
| **Somente leitura** | Nenhum comando que altere o pool é executado |
| **Rastreabilidade** | Toda coleta é registrada com data/hora e origem |
| **Reprodutibilidade** | A saída é padronizada e versionável |

## 🛠️ Requisitos

- Linux com OpenZFS 2.x
- Bash 4+
- Execução como `root` ou usuário com permissão de leitura nos devices

## 📦 Uso (previsto)

```bash
git clone https://github.com/felipe-xavier-cyber/incident-response-zfs.git
cd incident-response-zfs
sudo ./zfs-ir.sh --pool tank --out ./evidencias
```

## ⚠️ Aviso

Este projeto **não substitui** perícia oficial e não garante recuperação de dados. Sempre que possível, trabalhe sobre cópia ou imagem do dispositivo, e valide os procedimentos em laboratório antes de aplicar em produção.

## 📬 Contato

- LinkedIn: [felipe-vieira-0338b329a](https://www.linkedin.com/in/felipe-vieira-0338b329a/)
- GitHub: [@felipe-xavier-cyber](https://github.com/felipe-xavier-cyber)
