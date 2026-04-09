# CarbonTrack BR

Pipeline de dados públicos para análise de risco de carbono e ESG 
de companhias abertas brasileiras.

## Objetivo

Coletar, limpar e analisar dados de emissões e sustentabilidade 
de empresas brasileiras a partir de fontes públicas — CVM, IBAMA, 
B3 ISE e relatórios GRI — gerando um painel de risco de carbono 
por setor alinhado ao SBCE (Sistema Brasileiro de Comércio de Emissões).

## Fontes de dados

| Fonte | Dados | Status |
|---|---|---|
| CVM | Cadastro de companhias abertas | ✓ Coletado |
| IBAMA | Licenças e autos de infração | Em breve |
| B3 ISE | Empresas do índice de sustentabilidade | Em breve |
| GRI / CDP | Relatórios públicos de sustentabilidade | Em breve |

## Stack

- **Python** — pandas, requests, pdfplumber, BeautifulSoup
- **SQL** — PostgreSQL para armazenamento e limpeza
- **Docker** — ambiente reproduzível
- **Jupyter** — exploração e análise

## Estrutura

carbontrack-br/
├── data/
│   ├── raw/          # dados brutos das fontes
│   └── processed/    # dados limpos para análise
├── notebooks/        # exploração e análise
└── src/              # scripts reutilizáveis

## Contexto

A Lei 15.042/2024 regulamenta o SBCE e o mercado regulado de 
carbono começa a operar em 2026. Empresas obrigadas a reportar 
emissões precisarão de dados verificáveis — esse projeto constrói 
a base de dados pública para esse fim.

## Autor

Raí Barboza — [LinkedIn](https://www.linkedin.com/in/rai-pereira-barboza-01a90a262)