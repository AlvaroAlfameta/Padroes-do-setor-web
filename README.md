<p align="center">
  <img width="400" src="https://alfameta-cdn.s3-sa-east-1.amazonaws.com/logotransparente.png">
</p>

# Padrões do setor WEB/Mobile

## Versão 1.0

_Esse documento tem  como finalidade definir alguns padrões de desenvolvimento para o setor._

### 1 - Regras gerais para todas as linguagens

* Use Nomes fáceis de se encontrar.
* Use nomes pronunciáveis.
* Não economize nas palavras.
* Use nomes que descrevam a intenção do código.
* Evite palavras que podem ser variáveis ou palavras reservadas em outras plataformas.
* Evite nomes como "doubleValorPromocional", o tipo não precisa estar no nome.
* Evite trocadilhos.
* Não misture idiomas.
* Nome das classes devem ser substantivos e não devem conter verbos. Ex: **ClienteRepository**.
* Nome dos métodos devem conter verbos de preferência no infinitivo. Ex: **AdicionarCliente**.

* A linguagem padrão para escrita do código é o inglês (Exceção para jargões técnicos)*
* Se uma abreviação ou acrônimo possuir até 3 letras, deve ser escrito em maiúsculo. Ex:

```CSharp
  string ATR; // Correto, ATR tem apenas 3 letras.
  string CNPJ; // Errado, Cnpj possui mais do que 3 letras, o correto é Cnpj.
```

* Codifique somente o necessário e nada mais.
* Quando for codificar, faça corretamente para evitar codificar novamente.
* Evite implementar funcionalidades desnecessárias.
* Ao implementar uma nova funcionalidade, implemente-a corretamente.
* Evite gambiarras, gambiarras apenas empurram o problema pra frente e com um custo muito alto, alguém no futuro vai precisar entender a gambiarra que você fez, desfazê-la e então implementar a solução corretamente.
* Quando você arrumar um bug, primeiro escreva um teste que falhe, então corrija o bug e verifique se o teste passa.*
* Crie testes para novas funcionalidades.*
* Não commite códigos sem antes testar.
* Não commite códigos que não rodam.
* Resolva problemas reais resolvendo literalmente um problema real.
  Quando for possível, entre em contato com o cliente que deseja a funcionalidade que você esta desenvolvendo e com a ajuda dele, entenda o problema, valide e teste a solução. Apenas usando na vida real é que podemos ter certeza que que ele esta atendendo o cliente e esta pronto para uso.
* Aplique uma boa indentação

(*válido para todos os projetos criados a partir da publicação desse documento)
  
#### 1.1 - Comentários

* Evite documentação desnecessária
* Evite utilizar comentários desnecessários.
* Faça uso de comentários TODO
* Uma boa pratica do uso dos comentários e explicar o por que foi feito daquela maneira ou qual é a regra de negócio que foi implementada no método.
  


### 2 - Quando estiver usando CSharp (C#)

#### 2.1 Variáveis

* Variáveis privadas devem ser escritas em lowerCamelCase.
* Variáveis privadas devem ter _ (underline) antes do nome.
* Propriedades devem ser escritas em UpperCamelCase.
* Variáveis constantes devem ser escritas com todas as letras em MAIÚSCULO.
* Variáveis que forem iniciadas apenas no construtor devem receber o atributo "readonly".
* Não colocar o atributo "private" na frente de variáveis privadas.

#### 2.2 - Classes e Métodos

* Extraia trechos em métodos privados.
* Métodos devem fazer apenas uma coisa, fazê-la certa e somente fazê-la.
* Evite muitos parâmetros.
* Não deixe o método mentir dizendo que faz uma coisa e faz outras "escondidas".
* Se o método tiver mais de uma responsabilidade extraia em dois ou mais.
* Leia seu método de cima pra baixo como uma narrativa, ele deve fazer sentido.
* Nome dos métodos devem ser escritos em UppperCamelCase
* Nome das classes e dos arquivos devem ser escritos em UppperCamelCase.
* Não colocar o atributo "private" na frente de métodos privados.
* Evite acoplamento desnecessários.

#### 2.3 - Regras Gerais

* Evite linhas com mais de 100 caracteres
* As chaves devem iniciar sempre na linha de baixo. Ex:
* Sempre que possivel, use interpolação ao invés de concatenação.

  ```CSharp
    void Metodo()
    {
      // Faz alguma coisa
    }
  ```

* Comentários devem possuir um espaço após as barras de comentário. Ex:

  ```CSharp
    //Errado
    // Correto
  ```
  
### 3 - Quando estiver usando Javascript

* Nome dos arquivos devem ser escritos em lowercase.
* Nome dos métodos devem ser escritos em lowerCamelCase.
* Comparações devem utilizar 3 sinais de igual "===". Ex:

  ```javascript
  if(age === 18) {
    // Faz alguma coisa
  }
  ```

* Sempre que possível, utilizar interpolação ao invés de concatenar string. Ex:
  
  ```javascript
  let welcomeText = `Olá, seja bem vindo ${nome}`
  ```

* Evite linhas com mais de 80 caracteres.
* Use 1 linha em branco para separar um método do outro.
* Fazer sempre uso de linters para ajudar na padronização do código.
* Evite utilizar **var**, utilize **const** ou **let**.
* Sempre inicialize objetos com a sintaxe {}

```javascript
  const objeto = {} // Correto
  const objeto = new Object(); // Errado
```

### 4 - Quando estiver usando Vue.JS

* Nome dos arquivos devem ser escritos em UpperCamelCase.
* Nome dos métodos devem ser escritos em lowerCamelCase.
* Os estilos sempre devem ser do tipo 'Scoped'.

### 5 - Quando estiver usando Dart/Flutter

* Nome das classes deve ser escrito em UpperCamelCase.
* Nome dos arquivos devem ser escritos em snake_case.
* Nome das variáveis deve ser escrito com lowerCamelCase.
* Nome de variáveis constantes deve ser escrito lowerCamelCase.
* Não inicie com _ (underline) variáveis que não são privadas.
* Evite linhas com mais de 80 caracteres.
* Nome de variável constante global deve ser escrita com um k na frente. Ex:

  ```dart
    const kDefaultTextStyle = TextStyle();
  ```

### 6 - PostgresSQL

* Nome das tabelas e colunas devem ser escritos em snake_case.
* Não usar no nome das tabelas e colunas palavras reservadas do banco. Ex: **SELECT, WHERE**
* Todos os comandos e palavras reservadas devem ser escritos em letras MAIÚSCULAS. Ex:

```sql
  select * from usuario where id > 50; // Errado
  SELECT * FROM usuario WHERE id > 50; // Correto
```

* Tabelas devem possuir nome no plural. Ex;

```sql
  CREATE TABLE usuarios () // Correto
  CREATE TABLE usuario () // Errado
```

&nbsp;
&nbsp;
&nbsp;
&nbsp;
&nbsp;
&nbsp;

### 7 - Bibliografia

* [Style guide for Flutter repo](https://github.com/flutter/flutter/wiki/Style-guide-for-Flutter-repo)
* [Effective Dart](https://dart.dev/guides/language/effective-dart)
* [Seção CleanCode do curso de arquitetura de software](https://desenvolvedor.io/curso-online-fundamentos-de-arquitetura-de-software)
* [Google JavaScript Style Guide](https://google.github.io/styleguide/jsguide.html)
