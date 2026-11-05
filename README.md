# CarbonTrack BR

Estudo de dados públicos de companhias abertas brasileiras, com interesse em sustentabilidade e análise ESG.

**Estado atual:** conjuntos de dados CSV publicados. O pipeline automatizado e o painel de risco de carbono são objetivos futuros.

## Conteúdo disponível

| Diretório | Arquivos |
| --- | --- |
| `data/raw/` | `cad_cia_aberta.csv` e `ise_carteira.csv` |
| `data/processed/` | `empresas_mg_esg.csv`, `ise_limpo.csv`, `ise_x_cvm.csv` e `ise_mg.csv` |

Os arquivos reúnem cadastro de companhias da CVM, carteira ISE B3 e recortes/processamentos exploratórios. A presença na carteira ISE não deve ser interpretada como certificação ESG ou medida de emissões.

## Como consultar

```bash
git clone https://github.com/raipbarboza/carbontrack-br.git
cd carbontrack-br
```

Abra os CSVs em um editor ou ferramenta de análise. Confira separador e codificação antes de importar: os arquivos brutos e processados podem ter formatos diferentes.

## Reprodução e limitações

Parte da exploração está registrada na [aula 05 de python-esg-studies](https://github.com/raipbarboza/python-esg-studies/blob/main/aula05/aula05.ipynb). O notebook utiliza caminhos locais que precisam ser adaptados e não constitui um pipeline automatizado deste repositório.

O cruzamento exploratório usa correspondência parcial entre nomes de empresas. Pode gerar falsos positivos e múltiplos registros por companhia; exige revisão e identificação consistente por CNPJ antes de apoiar conclusões. Quantidade de linhas, de ações e de empresas são medidas diferentes.

As datas de coleta, fontes por arquivo e regras de transformação ainda precisam ser consolidadas em um dicionário de dados. Os CSVs são recortes de estudo e não representam necessariamente as carteiras ou os cadastros atuais.

## Evolução planejada

- Documentar origem, data de referência e licença de cada conjunto de dados.
- Trazer os scripts de coleta e transformação para o repositório.
- Validar o relacionamento entre empresas e ações.
- Avaliar dados de emissões, IBAMA e relatórios de sustentabilidade.
- Implementar armazenamento, ambiente reproduzível e visualizações conforme a necessidade.

Python, Pandas, SQL/PostgreSQL e Docker são tecnologias consideradas para essa evolução; não há scripts, notebooks ou configuração Docker publicados aqui nesta etapa. O projeto ainda não calcula risco de carbono nem comprova conformidade regulatória.

## Autor

[Rai Barboza](https://www.linkedin.com/in/rai-barboza-01a90a262/)
