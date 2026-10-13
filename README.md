# Consulta de CEP com Blazor

![.NET](https://img.shields.io/badge/.NET-10.0-512BD4?logo=dotnet&logoColor=white) ![Blazor](https://img.shields.io/badge/Blazor-WebAssembly-512BD4?logo=blazor&logoColor=white) ![C#](https://img.shields.io/badge/C%23-ASP.NET-239120)

Aplicação web desenvolvida como atividade acadêmica para consultar endereços brasileiros usando a **API ViaCEP**. O usuário informa um CEP e visualiza os dados do endereço em uma tabela.

## Funcionalidades

- Consulta de CEP pela API pública do [ViaCEP](https://viacep.com.br/).
- Aceita CEP com ou sem hífen, removendo caracteres não numéricos antes da consulta.
- Verifica se o CEP informado possui **8 dígitos**.
- Exibe CEP, logradouro, complemento, bairro, cidade, UF e DDD.
- Mostra mensagens para campos vazios, CEPs inválidos, consultas sem resultado e erros de comunicação.

## Tecnologias utilizadas

| Tecnologia | Utilização |
| --- | --- |
| C# / .NET 10 | Linguagem e plataforma |
| Blazor WebAssembly | Interface web executada no navegador |
| HttpClient | Requisições HTTP para o ViaCEP |
| System.Text.Json | Conversão dos dados JSON em objetos C# |
| Bootstrap | Estilização dos componentes |

## Como executar

**Requisito:** [.NET SDK 10](https://dotnet.microsoft.com/download/dotnet/10.0) instalado.

1. Clone o repositório:
   ```bash
   git clone https://github.com/lucaslimadmt/blazor-viacep-net.git
   ```
2. Entre na pasta:
   ```bash
   cd blazor-viacep-net
   ```
3. Restaure as dependências e inicie a aplicação:
   ```bash
   dotnet restore
   dotnet run
   ```
4. Acesse o endereço local informado no terminal.

## Exemplo de uso

Digite o CEP `01001-000` e clique em **Consultar**. A aplicação faz uma requisição ao endpoint:

```text
https://viacep.com.br/ws/01001000/json/
```

Se a consulta retornar um endereço, os dados aparecem em uma tabela na página.

## Estrutura do projeto

```text
blazor-viacep-net/
├── Layout/               # Layout e menu de navegação
├── Models/
│   └── Endereco.cs       # Modelo de resposta do ViaCEP
├── Pages/
│   └── Home.razor        # Formulário, consulta e resultado
├── wwwroot/              # Arquivos estáticos e estilos
├── Program.cs            # Configuração e inicialização
└── BlazorViaCep.csproj   # Dependências e configuração .NET
```

## Observações

- O projeto depende de acesso à internet e da disponibilidade da API ViaCEP.
- O tratamento de CEP inexistente é realizado pela verificação dos dados retornados.
- Este repositório contém a **Prática 08**, desenvolvida para fins de aprendizado de Blazor e consumo de APIs REST.

---

**Autor:** [Lucas Lima](https://github.com/lucaslimadmt)  
**Projeto acadêmico — Prática 08**
