# Tests_dotnet

## Testes de unidade com xUnit 

Um teste de unidade é um teste que exercita componentes ou métodos de software individuais, também conhecidos como "unidade de trabalho". Testes de unidade devem testar apenas o código dentro do controle do desenvolvedor. Eles não testam questões de infraestrutura. Questões de infraestrutura incluem bancos de dados, sistemas de arquivos e recursos de rede.

xUnit é um framework de teste unitário para a plataforma .NET, amplamente adotado devido à sua simplicidade e capacidade de suportar testes parametrizados e teóricos de maneira robusta. Ele foi desenvolvido por membros da comunidade de código aberto e é uma evolução do popular framework NUnit. O xUnit é compatível com várias versões do .NET, incluindo .NET Framework, .NET Core e agora .NET 5, e integra-se perfeitamente com ferramentas de desenvolvimento, como o Visual Studio.

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



## Testes com Mock Objects

Mock Objects são uma ferramenta fundamental no desenvolvimento de software, especialmente em testes unitários, onde simulam o comportamento de objetos reais em um ambiente controlado. Esses objetos são particularmente úteis para simular dependências externas, permitindo que os desenvolvedores testem componentes de maneira isolada. Isso evita a necessidade de interações com bancos de dados, APIs externas ou qualquer outro serviço que possa variar, ser instável ou difícil de replicar em um ambiente de teste.

O principal objetivo dos Mock Objects é permitir que os desenvolvedores configurem expectativas, retornos e comportamentos esperados das dependências que não fazem parte do escopo do teste em si. Com mocks, é possível assegurar que o código em teste se comporta como esperado, independentemente das variações ou instabilidades das dependências externas.

### Testes com Moq

Moq é um framework dinâmico para .NET que permite aos desenvolvedores criar Mock Objects de maneira simples e declarativa. É particularmente poderoso por permitir a configuração detalhada do comportamento dos mocks, incluindo a definição de retornos específicos, a verificação de chamadas a métodos e a execução de ações quando métodos são invocados.
