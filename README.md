# Sistema Simples de Satelites

Projeto Java em console criado para a GS. A ideia e simples: cadastrar satelites, registrar missoes, salvar leituras de sensores e gerar alertas quando algum valor estiver ruim.

## Estrutura

```text
sistema-satelites-java/
  src/
    presentation/     Menu e interacao com o usuario
    application/      Regras de aplicacao e integracao entre camadas
    domain/           Entidades do sistema
    infrastructure/   Repositorios em memoria usando ArrayList
  docs/
    diagrama-classes-domain.puml
```

## Como compilar e executar

No PowerShell, dentro da pasta `sistema-satelites-java`:

```powershell
$files = Get-ChildItem -Recurse src -Filter *.java | ForEach-Object { $_.FullName }
javac -d out $files
java -cp out presentation.Main
```

## Requisitos atendidos

- Pacotes: `presentation`, `application`, `domain`, `infrastructure`.
- Entidades com identificador unico, getters, setters, construtor padrao e construtor nao padrao.
- Heranca: `EntidadeBase` e a classe `Satelite` sao reutilizadas pelas outras classes.
- Override: `calcularPrioridadeOperacional()` e `exibirResumo()` em `SateliteComunicacao` e `SateliteObservacao`.
- Overload: exemplos em `mostrarSituacao`, `cadastrarMissao`, `buscarSatelite` e `registrarLeitura`.
- Armazenamento em memoria: todos os repositorios usam `ArrayList`.
- Usabilidade: menu de navegacao, validacao de texto vazio, numeros invalidos e satelite inexistente.

## Sugestao para o pitch

O sistema simula uma pequena central escolar de monitoramento de satelites. O usuario cadastra um satelite, cria uma missao, registra uma leitura como temperatura, bateria ou sinal, e o programa avisa quando algo esta em risco.
