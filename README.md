# Tests_dotnet

## Testes de unidade com xUnit 

Um teste de unidade é um teste que exercita componentes ou métodos de software individuais, também conhecidos como "unidade de trabalho". Testes de unidade devem testar apenas o código dentro do controle do desenvolvedor. Eles não testam questões de infraestrutura. Questões de infraestrutura incluem bancos de dados, sistemas de arquivos e recursos de rede.

xUnit é um framework de teste unitário para .NET, muito utilizado por ser simples e ter capacidade de suportar testes parametrizados e teóricos de maneira robusta. O xUnit é compatível com várias versões do .NET, incluindo .NET Framework, .NET Core e .NET 5 queé o utilizado, e integra-se com ferramentas de desenvolvimento, como o Visual Studio.

Para criar testes unitários com xUnit, é necessário primeiro configurar o ambiente de teste no projeto .NET. Isso inclui a instalação do pacote NuGet xUnit, além do xUnit runner que é necessário para a execução dos testes no Visual Studio

Os testes são estruturados utilizando os atributos **Theory** e **InlineData**, que permitem a execução de testes parametrizados. Isso significa que podemos fornecer vários conjuntos de entradas e saídas esperadas para o mesmo teste, aumentando a cobertura de testes sem a necessidade de escrever métodos de teste separados para cada cenário.

O atributo Theory indica que este é um teste parametrizado, enquanto cada InlineData representa um conjunto de entrada e a saída esperada. O método Assert.Equal é usado para verificar se o resultado da conversão corresponde ao valor esperado, considerando uma precisão de 1 ponto decimal.

### Testes realizados 
Existiam dois cenários de testes, um com sucesso e outro com o intuito de falha, a seguir o código com os dois tipos e depois as duas imagens com os dois testes sendo executados

```
public static class ConversorTemperatura
{
    public static double FahrenheitParaCelsius(double temperatura)
        => (temperatura - 32) / 1.8; // Simulação de falha
        //=> Math.Round((temperatura - 32) / 1.8, 2);
}
```


### Teste executado com sucesso 
![image](https://github.com/mariana2903/Tests_dotnet/assets/99264876/4fe92248-aece-4ffe-b711-d92d9a083266)


### Teste executado com falha 
![image](https://github.com/mariana2903/Tests_dotnet/assets/99264876/3547538e-6537-426c-b5b4-62d7f057e479)


## Testes com MStest

MSTest é o framework de testes unitários que permite aos desenvolvedores verificar o comportamento do código de maneira isolada e automatizada. Ele suporta uma variedade de testes, incluindo testes de unidade básicos, testes parametrizados e testes dirigidos por dados.

Uma das características mais poderosas do MSTest é a sua capacidade de realizar testes parametrizados. Isso é possível através dos atributos **DataTestMethod** e **DataRow**, que permitem executar um único método de teste várias vezes com diferentes conjuntos de dados. Esse recurso é extremamente útil quando você deseja testar a mesma função com vários valores de entrada, garantindo a robustez e a corretude do código em diversos cenários.

### Teste executado com sucesso 
![image](https://github.com/mariana2903/Tests_dotnet/assets/99264876/de791efc-999a-40b5-a527-608edd5d4403)

### Teste executado com falha 
![image](https://github.com/mariana2903/Tests_dotnet/assets/99264876/19d4bfe8-8f30-4af8-97ce-d757b6e5256e)


## Testes com Mock Objects

Mock Objects são uma ferramenta fundamental no desenvolvimento de software, e na construção de testes unitários, onde simulam o comportamento de objetos reais em um ambiente controlado. Esses objetos muito úteis para simular as dependências externas, o que permite o teste dos componentes de maneira isolada. Isso evita a necessidade de interações com bancos de dados, APIs externas ou qualquer outro serviço que possa variar, ser instável ou difícil de replicar em um ambiente de teste.

O principal objetivo dos Mock Objects é permitir que sejam configuradas expectativas, retornos e comportamentos esperados das dependências que não fazem parte do teste em si. Com mocks, é possível assegurar que o código em teste se comporta como esperado, independentemente das variações ou instabilidades de outras dependências externas.

### Testes com Moq

Moq é um framework dinâmico para .NET que permite a criação de Mock Objects de maneira simples e declarativa. É importante e poderosa por permitir a configuração detalhada do comportamento dos mocks, incluindo a definição de retornos específicos, a verificação de chamadas a métodos e a execução de ações quando métodos são chamados.

### Testes executados com sucesso 
![image](https://github.com/mariana2903/Tests_dotnet/assets/99264876/7ef79788-6fe6-42d2-9f04-2aa4219d6148)

