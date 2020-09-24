<p align="center">
  <img width="400" src="https://alfameta-cdn.s3-sa-east-1.amazonaws.com/logotransparente.png">
</p>

# Padrões do setor WEB/Mobile 1.0

 
_Esse documento tem  como finalidade definir alguns padrões de desenvolvimento para o setor._

<h4>Regras gerais</h4>

* Use Nomes fáceis de se encontrar.
* Use nomes pronunciaveis.
* Evite siglas ou acrônimos.
* Não economize nas palavras.
* Revele a intenção do código.
* Evite palavras que podem ser variaveis ou palavras .reservadas em outras plataformas.
* Evite dar nomes como "doubleValorPromocional", o tipo não precisa estar no nome.
* Evite trocadilhos.
* Não misture idiomas.
* Não mescle nomes.
* Nome das classes devem ser substantivos e não devem conter verbos. Ex: **ClienteRepository**.
* Nome dos metodos devem conter verbos de preferencia no infinitivo. Ex: **AdicionarCliente**.
* Nome das classes e dos arquivos devem ser escritos em PascalCase.


<h4>Variaveis</h4>

* Variaveis privadas devem ser escritas em camelCase.
* Variaveis privadas devem ser escritas com _ (underline) antes do nome.
* Variaveis publicas (Gets e Sets) devem ser escritas em PascalCase.
* Variaveis constantes devem ser escritas com todas as letras em MAISCULO.
* Variaveis que forem iniciadas apenas no construtor devem receber o atributo "readonly".
* Não colocar o atributo "private" na frente de variaveis privadas (por padrão, todas as variaveis são privadas no C#).

<h4>Metodos</h4>

  * Extraia trechos em métodos privados.
  * Métodos devem fazer apenas uma coisa, fazê-la certa e somente fazê-la.
  * Evite muitos parâmetros.
  * Não deixe o metodo mentir dizendo que faz uma coisa e faz outras "escondidas".
  * Se o método tiver mais de uma responsabilidade extraia em dois ou mais.
  * Leia seu método de cima pra baixo como uma narrativa, ele deve fazer sentido.
  * Aplique uma boa indentação
  * Nome dos métodos devem ser escritos em PascalCase
  
<h4>Quando for usar Javascript</h4>

* Nome dos arquivos devem ser escritos em PascalCase
* Nome dos metodos devem ser escritos em camelCase
* Comparações devem utilizar 3 sinais de igual "==="
* Sempre que possivel, utilizar interpolação ao invés de concatenar string
