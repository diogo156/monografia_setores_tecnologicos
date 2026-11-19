# Setores intensivos em tecnologia na economia brasileira (2018)

Códigos em R Markdown utilizados na monografia **"Análise da potencialidade dos setores intensivos em tecnologia na economia brasileira: uma abordagem de insumo-produto"**, apresentada ao Departamento de Economia da Universidade de Brasília (UnB).

- **Autor:** Diogo Araujo Nogueira
- **Orientadora:** Profa. Milene Takasago
- **Coorientador:** Prof. Carlos Alberto Ramos

## Conteúdo

| Arquivo | O que faz |
|---|---|
| `monografia.Rmd` | **Parte 1.** Leitura e conferência das bases e estimação da P&D direta e incorporada (insumos nacionais e importados e bens de investimento) dos 68 setores em 2018, com base em Morceiro (2018) e Morceiro, Tessarin e Guilhoto (2022). Calcula o índice de esforço tecnológico (IE) e identifica os setores intensivos em tecnologia (IE > 1). |
| `Analise_dos_indicadores.Rmd` | **Parte 2.** Indicadores de insumo-produto dos setores intensivos e não intensivos: índices de ligação de Hirschman-Rasmussen, índices puros de ligação (Guilhoto, Sonis e Hewings, 1996), campo de influência (Sonis e Hewings), rede de coeficientes técnicos e mapa de calor, além da exportação de tabelas e figuras. |

Os arquivos devem ser executados nessa ordem e na mesma sessão do R: a Parte 2 utiliza objetos criados pela Parte 1 no Environment (`mZ`, `mA`, `mLeontief`, `vX`, `nSetores`, `lCodigoSetores`, `dReferencia` e `dEsforco_C2`). Os resultados são gravados na pasta `Outputs/`, criada automaticamente.

## Dados

As bases não estão incluídas no repositório. Elas devem ser obtidas nas fontes originais e importadas no RStudio (*Import Dataset > From Excel*) com os nomes de objeto que cada parte verifica no início:

- Matriz de insumo-produto do Brasil de 2018 (68 setores), estimada pelo NEREUS/USP: abas de usos setor × setor e produto × setor, produção, importações, coeficientes técnicos e matriz de Leontief.
- Tabelas de Recursos e Usos de 2018 do Sistema de Contas Nacionais (IBGE): produção e oferta.
- Matriz de Absorção de Investimento (MAI) de 2018, do IPEA.
- Parâmetros de Morceiro (2018): Apêndice H (P&D dos 68 setores em 2013) e Tabela K (fronteira tecnológica).

## Requisitos

R (versão 4.4 ou superior recomendada) e os pacotes `openxlsx`, `readxl`, `dplyr`, `ggplot2`, `httr`, `fs`, `htmltools`, `htmlTable`, `matrixStats`, `ggrepel`, `igraph` e `kableExtra`. Os pacotes `flextable` e `officer` são opcionais e só são usados para gerar as tabelas e figuras em Word.

## Referências principais

- GUILHOTO, J. J. M.; SONIS, M.; HEWINGS, G. J. D. *Linkages and multipliers in a multiregional framework*: integrations of alternative approaches. Urbana: University of Illinois, 1996.
- MORCEIRO, P. C. *A indústria brasileira no limiar do século XXI*: uma análise da sua evolução estrutural, comercial e tecnológica. Tese (Doutorado em Economia) – FEA/USP, São Paulo, 2018.
- MORCEIRO, P. C.; TESSARIN, M. S.; GUILHOTO, J. J. M. Produção e uso setorial de tecnologia no Brasil. *Economia Aplicada*, v. 26, n. 4, p. 517-550, 2022.
- VALE, V. A.; PEROBELLI, F. S. *Análise de insumo-produto*: teoria e aplicações no R. Curitiba: Edição Independente, 2020.
