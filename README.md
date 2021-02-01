# Menor Preço
Uma API (REST/JSON), usando ASP.NET Core 3.1, para consulta e recuperação de produtos.  

<h4 align="center"> 
  <a href="#sobre-o-projeto">Sobre o projeto</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#Tecnologias-e-ferramentas">Tecnologias e ferramentas</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp; 
  </br>
  <a href="#Demonstração">Demonstração</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
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
-> Retornará resposta 400 (Bad Request);                                                                                                    
-> Caso o produto não exista, retornará 404 (Not Found).                                                                           


aplicação utilizando o padrão *`MVC`*, criando uma WebAPI, usando o [asp.net core 3.1](https://dotnet.microsoft.com/download/dotnet-core/3.1).
É utilizado um padrão que define um conjunto de práticas para criar e consumir a Web APIs, conhecido como [OData](https://docs.microsoft.com/en-us/odata/) (Open Data Protocol). Por meio das conveções da URL do OData, pode-se expor uma API, tornando-a mais flexível e fácil para consultas específicas, requisitadas pelo cliente da API.                                              
A API fará conexão com um banco de dados, o [SQL Server](https://www.microsoft.com/pt-br/sql-server/), com sua estrutura criada e populada previamente.

# Tecnologias e ferramentas

O projeto foi desenvolvido com as seguintes tecnologias:

- [Visual Studio 2019](#Pré-requisitos)
- [.NET Core 3.1 LTS](#Pré-requisitos)
- [SQLite](#Pré-requisitos)


# Demonstração

![ScreenshotBD](https://github.com/renanegobbi/App/blob/master/github/BD.png)

![TelaApp](https://github.com/renanegobbi/App/blob/master/github/screenshot1.png)


# Como usar

[Em breve...]

# Licença
Este projeto está sob a licença do MIT. Consulte a [LICENÇA](https://github.com/TesteReteste/lim/blob/master/LICENSE) para obter mais informações.
