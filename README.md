# Global Finance

App fintech multi-moeda voltado para brasileiros, com foco inicial no mercado brasileiro e expansão futura para o exterior.

## Sobre o projeto

O Global Finance resolve dois problemas ao mesmo tempo: gestão de contas em múltiplos países e falta de clareza financeira. O diferencial é a camada de insights com IA — categorização automática de gastos (alimentação, transporte, contas fixas, lazer etc.) e recomendações personalizadas de economia, com uma experiência mais robusta.

Como o app lida com dados financeiros reais, a prioridade é robustez antes de expansão de funcionalidades.

## Stack técnica

**Backend**
- NestJS + Prisma ORM + PostgreSQL
- Docker Compose (ambiente local)
- Autenticação JWT + bcrypt

**Frontend**
- React Native + Expo

**Infra**
- Hospedagem: a definir
- Versionamento: GitHub

## Estrutura do repositório

```
global-finance/
├── backend/    # API NestJS
└── frontend/   # App React Native (Expo)
```

## Status atual

> **Desafio atual:** o bloqueio principal agora está no frontend — a conexão via QR code do Expo no iPhone não está funcionando (aparenta ser problema de rede). Isso está travando o teste do app em dispositivo real.

- [x] Backend com 4 módulos: Auth, Users, Exchange, Transactions
- [x] Autenticação funcionando (registro retornando JWT com sucesso)
- [x] Docker Compose configurado para PostgreSQL local
- [x] Frontend inicializado e rodando no navegador
- [x] Camada de serviços do frontend (API + Auth) criada
- [x] Repositórios unificados em monorepo
- [ ] Conexão via QR code no iPhone com problema de rede (bloqueio atual)
- [ ] Ajustes pendentes de geração do Prisma Client

## O que falta para o MVP

- [ ] Resolver a conexão do frontend via QR code no iPhone (bloqueio atual)
- [ ] Resolver a geração do Prisma Client no backend
- [ ] Implementar as 4 telas principais do app: Overview, Contas, Transações e Conversor de moedas
- [ ] Implementar a importação manual de extratos (CSV/PDF)
- [ ] Implementar a categorização automática de transações via IA
- [ ] Definir hospedagem definitiva

## Escopo do MVP

4 telas principais:
- Overview (Dashboard)
- Contas
- Transações
- Conversor de moedas

> O módulo de **Metas** foi propositalmente deixado para depois, dependendo do feedback do beta.

## Estratégia de dados bancários

Na fase de beta fechado, o app usa **importação manual de extratos (CSV/PDF)**, com a IA categorizando as transações. Isso valida a lógica de categorização com dados reais antes de lidar com a complexidade regulatória e técnica de integrações bancárias ao vivo.

**Depois do beta:**
- 🇧🇷 Open Finance via Pluggy ou Belvo
- 🇬🇧 Open Banking via a definir

## Roadmap

| Fase | Status |
|---|---|
| Build do MVP | Em andamento |
| Beta fechado | Previsto ainda para 2026 |
| Feedback e ajustes | — |
| Divulgação pública / site de apresentação | Somente após validação do beta |
| Lançamento comercial | Previsto para 2027 |
