# Cognitivo.ai teste

Teste de Engenheiro de Dados

## Iniciando

As instruções a baixo auxiliaram para conseguir rodar o projeto.

### Prerequisitos

Antes de tudo, você precisa instalar o python3 e o PIP para que seja possível rodar o sistema. 


### Instalando

Siga o passo a passo, é bem simples ;)

```
git clone https://bitbucket.org/fredericowu/django-cognitivo
cd django-cognitivo
./build_env.sh
```
Durante a execução do build_env.sh, será perguntado o usuário administrador da interface de administração web e seus dados.

Username, Email address, Password, Password (again)


### Carregando os dados
Ao clonar o git, os dados disponibilizados se encontram no diretório input_data.
Para carregá-los no banco de dados (sqlite), basta executar o comando:

```
./load_data.sh
```
Esse processo pode demorar um pouco.

### Testes

Para garantir o funcionamento do sistema com os dados fornecidos e modelo de dados criado, foi criado um exportador dos dados do sqlite para o formato CSV original, execute:

```
./run_tests.sh
```

Esse comando vai gerar os arquivos out_bill_of_materials.csv, out_comp_boss.csv e out_price_quote.csv dentro do diretório exports.
Depois, vai gerar o MD5 checksum dos arquivos de entrada e saída para comparar e garantir que são idênticos, após ordenar os dados.


### Administração Web

Para gerar um pouco de interatividade com os dados carregados e o modelo criado, foi disponibilizada uma interface web, própria do Django.
Para iniciar o webserver em modo de debug para experimentar a interface, faça:

```
./run_webserver.sh
```

Após iniciar o processo, vá até o navegador e utilize a URL:
http://127.0.0.1:8888/admin/

Disponibilizado para testes aqui:
http://fredericowu.com.br:8888/admin/

> user: admin
> password: cognitivo


### APIs REST
Para acessar as APIs, acesse a URL: http://127.0.0.1:8888/api/


### Modelo de Dados
Dentro do diretório docs estão os arquivos Diagrama EER.mwb (formato MySQL Workbench) e Diagrama EER.png (exportado em imagem).


### Power BI
Disponibilizado dentro do diretório docs/ o arquivo cognitivo.pbix, esse possui Data Sources que se comunicam com a API do sistema para realizar a extração dos dados e montar o dashboard.
O PBIX está configurado para acessar os dados em http://fredericowu.com.br:8888/api/


## Construído com

* [Django](https://www.djangoproject.com/) - O framework usado

## Autor

* **Frederico Wu** - *Trabalho inicial* - [fredericowu](https://bitbucket.com/fredericowu/cognitivo)





