# Análise de dados do TCE-SP

## Contexto

O Tribunal de Contas do Estado de São Paulo disponibiliza APIs de consulta pública com informações detalhadas das receitas e despesas mensais dos Municípios jurisdicionados.

O programa consulta as despesas do período de um ano do Município selecionado pelo usuário. Reúne os dados num único dataframe e prossegue com as análises entendidas como relevantes.

## API

APIs (acrônimo de *Application Programming Interface*) são interfaces que facilitam a integração de programas. Possuem requisitos e protolocos que permitem a comunicação entre aplicações ou sistemas. Entre sistemas web, as APIs se comunicam, normalmente, nos padrões JSON (mais comum) e XML. 

Quando consumimos uma API como a do TCE, trazemos os dados para o nosso programa sem nos preocupar com a forma como tais informações são processadas na origem.

## Análises

Este Jupyter Notebook cria a requisição ao TCE com o nome do Município, ano e mês. Um loop repete a operação para os meses anteriores, até completar o período de um ano. Os arquivos JSON de resposta geram dataframes, que vão sendo concatenados para formar um dataframe único.

São identificados:

### Pessoas físicas:

* Os maiores pagamentos individuais realizados a PF
* Os maiores pagamentos acumulados feitos a PF
* As maiores quantidades de pagamentos realizados a cada PF
* Informações estatísticas sobre pagamentos feitos a PF

### Pessoas jurídicas:

* Os maiores pagamentos individuais realizados a PJ
* Os maiores pagamentos acumulados feitos a PJ
* As maiores quantidades de pagamentos realizados a cada PJ
* Informações estatísticas sobre pagamentos feitos a PJ


## Gravação de arquivo Excel

Ao final da análise, um arquivo Excel é gerado com os dados organizados.
