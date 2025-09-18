Global Solution 2 (2024)
Este projeto foi desenvolvido para simular o consumo de energia de um dispositivo, armazenando dados em um banco de dados e fornecendo alertas sobre o consumo.

### Tecnologias Utilizadas

- **Pandas**: Utilizado para ler e processar o dataset que simula a coleta de dados de um dispositivo.
- **Flask**: Framework web simples para criar a API.
- **Bcrypt**: Usado para criptografar senhas de usuários.
- **Pytest**: Framework para testes automatizados.
- **SQLite**: Banco de dados leve e simples, utilizado para armazenar os dados de consumo e alertas.
- **SQLAlchemy**: ORM para interagir com o banco de dados de forma simples e eficiente.
- **AVL**: Estrutura de dados utilizada para garantir a ordem dos dispositivos no sistema.

### Funcionalidades

1. **Simulação de Consumo**: O sistema simula o consumo de energia baseado em um dataset.
2. **Alertas de Consumo**: São criados alertas sempre que o consumo de energia atinge determinados valores.
3. **Armazenamento de Dados**: Os dados de consumo são armazenados no banco de dados SQLite.

### Estrutura do Projeto

- **Dataset**: Contém dados de consumo simulados, lidos com a ajuda do Pandas.
- **API**: Desenvolvida com Flask para expor os dados de consumo e alertas.
- **Banco de Dados**: Usado para armazenar as informações de consumo e alertas. A interação com o banco é feita através do SQLAlchemy.
- **Testes**: Testes automatizados são realizados com o Pytest para garantir a funcionalidade do sistema.

### Requisitos

- **bcrypt==4.0.1**
- **pandas**
- **flask**
- **pytest**

Sistema Luz: Monitoramento de Dispositivos IoT e Consumo de Energia
 
###Descrição do Projeto
O Luz é uma solução desenvolvida para monitorar dispositivos IoT e gerenciar o consumo de energia em qualquer tipo de ambiente. 
Ele oferece ao usuário:
*Login e Cadastro*: Acesso seguro à plataforma.
*Dashboard*: Monitoramento em tempo real dos dispositivos cadastrados.
*Gestão de Dispositivos*: Cadastro, edição e acompanhamento de dispositivos IoT.
*Gráficos Analíticos*: Visualização detalhada do impacto energético para promover economia.
 
###Tecnologias
 
###FRONT-END
*React*: Base para desenvolvimento da interface.
*JavaScript*: Usado para estilização e funcionalidades.
*React Router DOM*: Gerenciamento de rotas na aplicação.
*Recharts*: Gráficos interativos e responsivos.
*React Helmet*: Gerenciamento do <head> da aplicação.
*React Hooks (useState, useNavigate)*: Gerenciamento de estados e navegação programática.
 
#Componentes Principais
* App: Ponto de entrada da aplicação.
* Dashboard:
	- Apresenta consumo em tempo real.
	- Navegação entre seções: Dashboard, Dispositivos e Consumo.
	- Exibição de gráficos e tabelas com Recharts.
 
* Dispositivos: Cadastro e edição de dispositivos IoT.
	- Funções principais: handleAddDevice, handleEditDevice, handleSaveEdit, handleCancelEdit.
 
* Consumo: Gráficos de consumo diário e mensal.
	- Tabelas detalhadas por dispositivo.
 
###BACK-END
*Flask*: Framework web para a API.
*Pandas*: Processamento de dados simulados.
*Bcrypt*: Criptografia de senhas.
*Pytest*: Testes automatizados.
*SQLite*: Banco de dados para armazenamento de informações.
*SQLAlchemy*: ORM para interação com o banco.
*AVL*: Estrutura de dados para ordenação eficiente.
 
# Funcionalidades
1. Simulação de Consumo: Com base em datasets.
2. Alertas de Consumo: Notificações para consumo elevado.
3. Armazenamento de Dados: Dados salvos e gerenciados via SQLite.
 
# Estrutura do Projeto
- *Dataset*: Contém dados de consumo simulados, lidos com a ajuda do Pandas.
- *API*: Desenvolvida com Flask para expor os dados de consumo e alertas.
- *Banco de Dados*: Usado para armazenar as informações de consumo e alertas. A interação com o banco é feita através do SQLAlchemy.
- *Testes*: Testes automatizados são realizados com o Pytest para garantir a funcionalidade do sistema.
 
 
# Como Rodar
1. Clone o repositório:
   bash
   git clone <url_do_repositório>

 
2. Instale as dependências:
   bash
   pip install -r requirements.txt

 
3. Execute o servidor Flask:
   bash
   flask run
 
 
# Requisitos
- *bcrypt==4.0.1*
- *pandas*
- *flask*
- *pytest*
 
 
###BANCO DE DADOS
 
##Entidades e Atributos
 
*Usuário (USUARIO)*
id_usuario: Identificador único.
nome_usuario: Nome do usuário.
email_usuario: Email do usuário.
senha: Senha criptografada.
data_criacao: Data de criação do cadastro.
 
*Dispositivo (DISPOSITIVO)*
id_dispositivo: Identificador único.
id_usuario: Relacionamento com o usuário.
nome_dispositivo: Nome do dispositivo.
localizacao_dispositivo: Local de instalação.
data_instalacao: Data de instalação.
status_dispositivo: Ativo ou inativo.
 
*Consumo de Energia (CONSUMO_ENERGIA)*
id_consumo: Identificador único.
id_dispositivo: Referência ao dispositivo.
datahora_consumo: Data e hora do registro.
consumo_energia: Quantidade de energia consumida.
tipo_energia: Tipo de energia consumida.
 
*Alerta de Consumo (ALERTA_CONSUMO)*
id_alerta: Identificador único.
id_usuario: Referência ao usuário.
id_dispositivo: Referência ao dispositivo.
limite_consumo: Limite para disparo do alerta.
mensagem_alerta: Mensagem do alerta.
 
*Eficiência de Consumo (EFICIENCIA_CONSUMO)*
id_eficiencia: Identificador único.
id_usuario: Referência ao usuário.
mensagem_eficiencia: Mensagem de orientação para economia.
 
#Relacionamentos.
Um Usuário pode ter vários Dispositivos.
Um Dispositivo pode ter vários registros de Consumo de Energia.
