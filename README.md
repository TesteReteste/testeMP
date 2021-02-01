# Menor Preço
Uma API (REST/JSON), usando ASP.NET Core 3.1, para consulta e recuperação de produtos.  

<h4 align="center"> 
  <a href="#sobre-o-projeto">Sobre o projeto</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#Tecnologias-e-ferramentas">Tecnologias e ferramentas</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp; 
  <a href="#Demonstração">Demonstração</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  </br>
  <a href="#Como-usar">Como usar</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#Licença">Licença</a>
</h4>

<br/>

<p align="center">
  <a href="https://opensource.org/licenses/MIT">
    <img src="https://img.shields.io/badge/License-MIT-blue.svg" alt="License MIT">
  </a>
</p>


# Sobre o projeto

Este é um projeto básico de uma API (REST/JSON) para consulta e recuperação de produtos, filtrada pelo código GTIN (EAN) e ordenada de forma crescente pelo preço.
A base de dados será importada através de uma rota (GET /v1/produtos) e preenchida no banco de dados de forma automática.                                            
*`OBS: Assim que importar o novo arquivo, pela rota, os dados que constam anteriormente nas tabelas do banco de dados serão substituídos pelo novo arquivo!`*

A consulta para obter os produtos contidos no banco de dados, passando como parâmetro um valor GTIN, será realizada através da rota (GET /v1/produtos/).
Esta rota terá o seguinte comportamento, caso não seja passado o parâmetro:                                                                             
- Retornará resposta 400 (Bad Request);                                                                                                    
- Caso o produto não exista, retornará 404 (Not Found).   


Neste projeto, serão importadas planilhas de forma dinâmica para o banco de dados. Dessa forma, é importante que a planilha siga o seguinte padrão, antes de enviá-la pela rota:

- Será enviado na seguinte ordem, como ilustrado abaixo.                                                                                                                                                                                                                                                                                                        *`Obs: Evite preencher os campos com símbolos de potência, pois este código não interpretará os símbolos.`*

![Template](https://github.com/TesteReteste/testeMP/blob/main/GG/TemplateCSV.png)
                                              
                                              
Resumidamente, foram seguindos os seguintes passos:

1 - Criação do modelo de dados utilizando o banco de dados sqlite.
A criação do modelo se deu pelo uso do EF (Entity Framework) Core, um mapeador relacional de objeto (O/RM).
Foram baixados os pacotes que fazem parte, via Nuget:
Instalar Microsoft.EntityFrameworkCore (3.1.0)
install Microsoft.EntityFrameworkCore.Relational (3.1.0)

Para a visualização dos relacionamentos das tabelas do banco de dados sqlite, foi utilizado o software DBeaver (versão 7.3.3):











E caso tenha mais afinidade, será deixado o script para geração do banco e tabelas no Microsoft SQL Server Management Studio) junto ao projeto, na pasta scripts:





                                              

# Tecnologias e ferramentas

O projeto foi desenvolvido com as seguintes tecnologias e ferramentas:

- [Visual Studio 2019](#Pré-requisitos)
- [.NET Core 3.1 LTS](#Pré-requisitos)
- [SQLite](#Pré-requisitos)


# Demonstração





![ScreenshotBD](https://github.com/renanegobbi/App/blob/master/github/BD.png)

![TelaApp](https://github.com/renanegobbi/App/blob/master/github/screenshot1.png)


# Como usar

Instalar a API chamada NewtonSoft, para trabalhar com JSON. A instalação da API pode ser via Nuget ou usando o comando via console:                 
*`Install-Package Newtonsoft.Json`*

Caso consuma outro JSON, alterar as propriedades na classe Data e substituir a constante URL_GET_DATA na classe ListagemViewModel:                       
*`const string URL_GET_DATA = "aqui_está_a_url_que_conterá_o_JSON"`*

# Licença
Este projeto está sob a licença do MIT. Consulte a [LICENÇA](https://github.com/TesteReteste/lim/blob/master/LICENSE) para obter mais informações.
