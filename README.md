# Sistema de Satelites Java

Sistema em Java para gerenciamento de satelites, missoes, leituras de sensores e alertas orbitais. O projeto roda pelo console e foi organizado em camadas para demonstrar conceitos de programacao orientada a objetos.

## Funcionalidades

- Cadastro de satelites de comunicacao.
- Cadastro de satelites de observacao.
- Listagem e busca de satelites.
- Cadastro e listagem de missoes.
- Registro de leituras de sensores.
- Geracao automatica de alertas para leituras em risco.
- Validacao de entradas no menu do console.

## Tecnologias

- Java
- Programacao orientada a objetos
- Repositorios em memoria com `ArrayList`
- Diagrama de classes em PlantUML

## Estrutura do projeto

```text
sistema-satelites-java/
  docs/
    diagrama-classes-domain.puml
  src/
    application/      Regras de aplicacao
    domain/           Entidades e regras de dominio
    infrastructure/   Repositorios em memoria
    presentation/     Menu e interacao com o usuario
```

## Como executar

Tenha o JDK instalado e execute os comandos abaixo no PowerShell, dentro da pasta do projeto:

```powershell
$files = Get-ChildItem -Recurse src -Filter *.java | ForEach-Object { $_.FullName }
javac -d out $files
java -cp out presentation.Main
```

## Menu principal

O sistema permite:

- Cadastrar satelite de comunicacao.
- Cadastrar satelite de observacao.
- Listar satelites.
- Registrar leitura de sensor.
- Gerar alerta orbital.
- Cadastrar missao.
- Listar missoes, leituras e alertas.
- Buscar satelite por nome.

## Conceitos aplicados

- Separacao em pacotes: `presentation`, `application`, `domain` e `infrastructure`.
- Encapsulamento com atributos privados, getters e setters.
- Construtor padrao e construtores com parametros.
- Heranca usando `EntidadeBase` e `Satelite`.
- Sobrescrita de metodos em `SateliteComunicacao` e `SateliteObservacao`.
- Sobrecarga de metodos em servicos e entidades.
- Persistencia em memoria com listas.

## Diagrama

O diagrama de classes do dominio esta em:

```text
docs/diagrama-classes-domain.puml
```

Ele pode ser aberto em extensoes PlantUML ou renderizado em ferramentas compativeis.
