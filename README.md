<p align="center">
  <img width="400" src="https://alfameta-cdn.s3-sa-east-1.amazonaws.com/logotransparente.png">
</p>

# Padrões do setor WEB/Mobile 1.0

 
_Esse documento tem  como finalidade definir alguns padrões de desenvolvimento para o setor._

<h3>Regras gerais para todas as linguagens</h3>

  * Use Nomes fáceis de se encontrar.
  * Use nomes pronunciaveis.
  * Não economize nas palavras.
  * Revele a intenção do código.
  * Evite palavras que podem ser variaveis ou palavras reservadas em outras plataformas.
  * Evite dar nomes como "doubleValorPromocional", o tipo não precisa estar no nome.
  * Evite trocadilhos.
  * Não misture idiomas.
  * Não mescle nomes.
  * Nome das classes devem ser substantivos e não devem conter verbos. Ex: **ClienteRepository**.
  * Nome dos metodos devem conter verbos de preferencia no infinitivo. Ex: **AdicionarCliente**.
  * Evite linhas com mais que 100 caracteres.
  * A linguagem padrão para escrita do código é em inglês* 
  * Se uma abreviação ou acronimo possuir até 3 letras, deve ser escrito em maisculo. Ex: 
  ```CSharp
    string ATR; // Correto, ATR tem apenas 3 letras.
    string CNPJ; // Errado, Cnpj possui mais do que 3 letras, o correto é Cnpj.
  ```
  * Codifique somente o necessário e nada mais, mas quando for codificar, faça corretamente para evitar codificar novamente.
  * Evite implementar funcionalidades desnecessarias.
  * Ao implementar uma nova funcionalidade, a implemente corretamente.
  * Evite gambiarras, gambiarras apenas empurram o problema pra frente e com um custo muito alto, alguém no futuro vai precisar entender a gambiarra que você fez, desfaze-la e então implementar a solução corretamente.
  * Quando você arrumar um bug, primeiro escreva um teste que falhe, então corrija o bug e verifique se o teste passa.*
  * Crie testes para novas funcionalidades.*
  * Não commite codigos sem antes testar.
  * Resolva problemas reais resolvendo literalmente um problema real.
    Quando for possivel, entre em contato com o cliente que deseja a funcionalidade que você esta    desenvolvendo e com a ajuda dele, entenda o problema, valide e teste a solução diretamente com ele. Apenas usando na vida real é que podemos ter certeza que que ele esta atendendo o cliente e esta pronto para uso.

<p style="font-size:12px">*válido para todos os projetos criados a partir da publicação desse documento</p>

<h3>1 - Quando estiver usando C#</h3>

<h5>1.1 Variaveis</h5>

* Variaveis privadas devem ser escritas em lowerCamelCase.
* Variaveis privadas devem ter _ (underline) antes do nome.
* Variaveis publicas (Gets e Sets) e estaticas devem ser escritas em UpperCamelCase.
* Variaveis constantes devem ser escritas com todas as letras em MAISCULO.
* Variaveis que forem iniciadas apenas no construtor devem receber o atributo "readonly".
* Não colocar o atributo "private" na frente de variaveis privadas.

<h5>1.2 - Classes e Metodos</h5>

  * Extraia trechos em métodos privados.
  * Métodos devem fazer apenas uma coisa, fazê-la certa e somente fazê-la.
  * Evite muitos parâmetros.
  * Não deixe o metodo mentir dizendo que faz uma coisa e faz outras "escondidas".
  * Se o método tiver mais de uma responsabilidade extraia em dois ou mais.
  * Leia seu método de cima pra baixo como uma narrativa, ele deve fazer sentido.
  * Aplique uma boa indentação
  * Nome dos métodos devem ser escritos em UppperCamelCase
  * Nome das classes e dos arquivos devem ser escritos em UppperCamelCase.

<h5>1.3 - Regras Gerais</h5>

  * As chaves devem iniciar sempre na linha de baixo. Ex:
  ```CSharp
    void Metodo()
    {
      // faz alguma coisa
    }
  ```

  * Comentarios devem possuir um espaço após as barras de comentario. Ex:
  ```CSharp
    //Errado
    // Correto
  ```
  
  * Evite utilizar comentarios desnecessários.
  * Uma boa pratica do uso dos comentaríos e explicar o por que foi feito daquela maneira ou qual é a regra de negócio do metodo.
<h3>2 - Quando estiver usando Javascript</h3>

* Nome dos arquivos devem ser escritos em lowerCamelCase.
* Nome dos metodos devem ser escritos em lowerCamelCase.
* Comparações devem utilizar 3 sinais de igual "===". Ex:
  ```javascript
  if(idade === 18) {
    ...
  }
  ```
* Sempre que possivel, utilizar interpolação ao invés de concatenar string. Ex:
  ```javascript
  var welcomeText = `Olá, seja bem vindo ${nome}`
  ```

<h3>3 - Quando estiver usando Vue.JS</h3>

* Nome dos arquivos devem ser escritos em UpperCamelCase.
* Nome dos metodos devem ser escritos em lowerCamelCase.


<h3>4 - Quando estiver usando Flutter</h3>

* Nome das classes deve ser escrito em UpperCamelCase.
* Nome dos arquivos devem ser escritos em lowerCase_with_underscore.
* Nome das variaveis deve ser escrito com lowerCamelCase.
* Nome de variaveis constantes deve ser escrito lowerCamelCase.
* Não use _ (underline) para variaveis que não são privadas
* Nome de variavel constante global deve ser escrita com um k na frente. Ex:
  ```dart
    const kDefaultTextStyle = TextStyle();
  ```
