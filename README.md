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
- Retornará resposta 400 (Bad Request);                                                                                                    
- Caso o produto não exista, retornará 404 (Not Found).                                                                           
                                              

# Tecnologias e ferramentas

O projeto foi desenvolvido com as seguintes tecnologias e ferramentas:

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
