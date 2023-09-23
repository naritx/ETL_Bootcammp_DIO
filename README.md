# ETL_Bootcammp_DIO
# O desafio é criar o próprio ETL

## Criar um contexto diferente para um pipeline de ETL

## Planejamento:

Tema: Base de dados de clientes de uma loja

Ordenar os clientes por valor de compra

Para os 3 clientes com maior valor, enviar mensagem convidando para um sorteio

Para os 3 com menor valor, enviar descontos

### Geração de dados

Usando Chat GPT 3.5, criei uma base aleatória de 20 linhas

![Untitled](O%20desafio%20e%CC%81%20criar%20o%20pro%CC%81prio%20ETL%203b0da01cfe23408fb3adbdaebe15c9c7/Untitled.png)

Então transformei-a em formato csv

copiei o arquivo em bloco de notas:

![Untitled](O%20desafio%20e%CC%81%20criar%20o%20pro%CC%81prio%20ETL%203b0da01cfe23408fb3adbdaebe15c9c7/Untitled%201.png)

Salvei na pasta do bootcamp

[Base_ficticia_loja.csv](O%20desafio%20e%CC%81%20criar%20o%20pro%CC%81prio%20ETL%203b0da01cfe23408fb3adbdaebe15c9c7/Base_ficticia_loja.csv)

### Extract

Importar uma base de dados online 

[Base_ficticia_loja.csv](O%20desafio%20e%CC%81%20criar%20o%20pro%CC%81prio%20ETL%203b0da01cfe23408fb3adbdaebe15c9c7/Base_ficticia_loja.csv)

- Usar o collab para extrair esses dados
    - Importar a pasta para o collab
    
    ![Untitled](O%20desafio%20e%CC%81%20criar%20o%20pro%CC%81prio%20ETL%203b0da01cfe23408fb3adbdaebe15c9c7/Untitled%202.png)
    

### Transform

- Limpar e Organizar a base
    - [x]  Transformar as colunas primeiro nome e segundo nome em uma só, de nome completo Tentar fazer isso em uma única linha (Não aparenta ser possível)
    - [x]  Ordenar pelo valor das vendas
    
    ![Untitled](O%20desafio%20e%CC%81%20criar%20o%20pro%CC%81prio%20ETL%203b0da01cfe23408fb3adbdaebe15c9c7/Untitled%203.png)
    
    Para melhor visualização do código, comentei e coloquei na mesma célula
    
    ![Untitled](O%20desafio%20e%CC%81%20criar%20o%20pro%CC%81prio%20ETL%203b0da01cfe23408fb3adbdaebe15c9c7/Untitled%204.png)
    
    - [x]  Definir os parâmetros da mensagem:
        
        ![Untitled](O%20desafio%20e%CC%81%20criar%20o%20pro%CC%81prio%20ETL%203b0da01cfe23408fb3adbdaebe15c9c7/Untitled%205.png)
        
        Valores armazenados nas variáveis head3 e tail3
        
        Top3 maiores valores: Enviar mensagem de convite para um cartão fidelidade
        
        Top3 menores valores: Enviar mensagem com cupom de desconto
        
    - [x]  Desenvolver as mensagens
        
        ![Untitled](O%20desafio%20e%CC%81%20criar%20o%20pro%CC%81prio%20ETL%203b0da01cfe23408fb3adbdaebe15c9c7/Untitled%206.png)
        
    
    Expansão da lista para 40 itens
    

### Load

Uso da biblioteca CSV

importar os textos para uma base a qual será dividida em formato .csv

df.to_csv(’nome do arquivo’) - >Funciona apenas para df

Criação de arquivos em CSV e utilizando o índice da lista retornada das funções de texto para criar novas linhas

![Untitled](O%20desafio%20e%CC%81%20criar%20o%20pro%CC%81prio%20ETL%203b0da01cfe23408fb3adbdaebe15c9c7/Untitled%207.png)
