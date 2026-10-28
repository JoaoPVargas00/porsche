# Porsche Sales Intelligence

Dashboard interativa em HTML criada a partir da planilha sanitizada do desafio DIO.

## Objetivo

Transformar 100 registros de vendas Porsche em uma análise executiva, com filtros e perguntas de negócio claras, publicável no GitHub Pages sem depender do Excel.

## Perguntas de negócio escolhidas

1. Quais modelos Porsche geram mais receita?
   - Ajuda a identificar quais veículos têm maior peso financeiro no portfólio.

2. Quais estados concentram mais receita?
   - Mostra onde a operação comercial tem maior valor e ajuda a enxergar concentração geográfica.

3. Quais métodos de pagamento apresentam maior ticket médio?
   - Permite analisar se determinadas formas de pagamento estão associadas a compras de maior valor.

A dashboard também apresenta uma visão de apoio sobre status de entrega.

## Indicadores de topo

- Vendas filtradas
- Receita registrada
- Ticket médio
- Taxa de entregas concluídas
- Modelo líder em receita

## Filtros

- Modelo
- Estado
- Ano do modelo
- Método de pagamento
- Status de entrega

Todos os gráficos, indicadores e a tabela detalhada respondem aos filtros.

## Tratamento da base

Foi utilizada somente a versão sanitizada dos campos:

- `SaleDateSanitized`
- `PorscheModelSanitized`
- `ModelYearSanitized`
- `SalesPriceSanitized`
- `VehicleMileageSanitized`
- `PayMethodSanitized`
- `CitySanitized`
- `StateSanitized`
- `DeliveryStatusSanitized`

Conversões aplicadas:

- Ano convertido para número inteiro.
- Preço convertido para número decimal.
- Quilometragem convertida para número inteiro.
- Datas válidas mantidas no formato ISO.
- Registros com `SaleDateSanitized = INVALID` foram mantidos nas análises não temporais. A base possui 24 datas inválidas entre os 100 registros.

Nenhum campo cru foi utilizado na lógica da dashboard.

## Prompt utilizado

> Crie uma dashboard Porsche em HTML, arquivo único e responsivo, usando somente os campos sanitizados da base. O visual deve ser premium, escuro e inspirado na identidade esportiva da marca, com preto, off-white, vermelho e dourado discreto. Inclua filtros por modelo, estado, ano, método de pagamento e status de entrega. No topo, mostre total de vendas, receita, ticket médio, taxa de entregas e modelo líder. Responda três perguntas: quais modelos geram mais receita, quais estados concentram mais receita e quais métodos de pagamento têm maior ticket médio. Os filtros devem atualizar todos os indicadores e gráficos. Não use bibliotecas externas: o arquivo precisa funcionar sozinho no GitHub Pages.

## Refinamentos realizados

- Substituição de uma coleção de gráficos genéricos por três perguntas de negócio explícitas.
- Uso de barras horizontais para facilitar a leitura de modelos e estados com nomes longos.
- Inclusão de taxa de entrega como indicador operacional.
- Inclusão de tabela detalhada para conferir o efeito dos filtros.
- Remoção de dependências externas para que `index.html` funcione sozinho.
- Tratamento específico dos 24 registros com data sanitizada inválida.

## Ferramenta utilizada

ChatGPT para análise da base, definição das perguntas e geração/refino do HTML.

## Estrutura do repositório

```text
index.html
README.md
base_sanitizada.csv
```

## Como executar localmente

Basta abrir o arquivo `index.html` em um navegador moderno.

## Como publicar no GitHub Pages

1. Crie um repositório público, por exemplo `porsche-sales-dashboard`.
2. Envie `index.html`, `README.md` e `base_sanitizada.csv`.
3. Entre em `Settings`.
4. Acesse `Pages`.
5. Em `Build and deployment`, selecione `Deploy from a branch`.
6. Escolha a branch `main` e a pasta `/root`.
7. Salve.
8. Aguarde o GitHub gerar o endereço público.

## Dashboard publicada

Adicionar aqui depois da publicação:

`https://SEU-USUARIO.github.io/porsche-sales-dashboard/`

## Observação

Projeto acadêmico. A base utilizada é a versão sanitizada disponibilizada para o desafio da DIO.
