# Teste Prático

## Pré-requisitos

- Docker
- Docker Compose

## Passos para Configuração do Ambiente

1. Clone este repositório:

```bash
git clone https://git.nexxera.com/bi/teste-pratico.git
cd teste-pratico
```
2. Suba o container:

```bash
docker compose up --build
```

3.	Acesse o Jupyter Notebook:

	•	Abra o navegador e acesse http://localhost:8889.

	•	O diretório de trabalho é montado no container, então você verá o arquivo financial_data.csv na pasta work.

# Instruções para o Teste Prático de BI

O teste deve ser executado em um notebook no Jupyter respeitando o seguinte roteiro:

#### Bloco 1: 
    . Configure a sessão Spark com suporte ao Delta Lake.

#### Bloco 2: 
    . Carregue o arquivo financial_data.csv localizado na pasta work.

#### Bloco 3: 
    . Converta a coluna ‘valor’ para o tipo de dados double.

#### Bloco 4: 
    . Filtre as transações com valor acima de 1000.

#### Bloco 5:
    . Salve os dados filtrados em um Delta Lake, particionados pela data da transação, no diretório /home/jovyan/work/delta/financial_data.

#### Bloco 6:
    . Crie uma delta table chamada financial_data a partir dos dados salvos.

#### Bloco 7:
    . Realize uma consulta para selecionar todas as transações com valor acima de 2000.

#### Bloco 8:
    . Exiba o histórico de versões da delta table.

#### Bloco 9:
    . Adicione os seguintes novos dados à tabela Delta:

	- id_transacao: 11, data_transacao: '2024-07-08', valor: 3000.95, tipo_transacao: 'DEPOSITO', descricao: 'Bônus Anual'
	- id_transacao: 12, data_transacao: '2024-07-08', valor: -150.40, tipo_transacao: 'PAGAMENTO', descricao: 'Restaurante'
	- id_transacao: 13, data_transacao: '2024-07-09', valor: 800.75, tipo_transacao: 'TRANSFERENCIA', descricao: 'Transferência da Conta Corrente'
	- id_transacao: 14, data_transacao: '2024-07-09', valor: -200.22, tipo_transacao: 'PAGAMENTO', descricao: 'Cinema'

#### Bloco 10:
    . Realize uma consulta para selecionar todas as transações com valor acima de 1000.

#### Bloco 11:
    . Agrupe as transações por tipo e some os valores.

## Entrega

Salve o notebook completo e publique em um repositório git. 

Envie a URL para o e-mail: isabella.lacerda@nexxera.com

## Critérios de aceite

É imprescindível que o notebook execute sem erros. 

Boas práticas de desenvolvimento de software serão consideradas.
