# Estagio Silvana
Este repositório é para envio das tarefas semanalmente.

## Semanas

* 19/09 a 25/09 - Concluída

* 25/09 a 02/10 - em andamento

 Git- Github - fundamentos Java
 Git-Github- fundamentos em Java
 
 
Conceito de Classes e objetos

A classe é um modelo, um planejamento, tal como o projeto de um carro. O objeto seria a classe materializada, ou seja, um objeto com os devidos atributos qualificados: um carro vermelho, teto solar, bancos de couro, fabricado em 2021, com valor atual de $ 200.000,00.

Instância de objeto
 A instanciação é um processo por meio do qual se realiza a cópia de um objeto (classe) existente. Uma classe, a qual tem a função de determinar um tipo de dado, deve ser instanciada para que possamos utilizá-la. Sendo assim, devemos criar sua instância, a qual definimos como sendo um objeto referente ao tipo de dado que foi definido pela classe. Ressaltamos, executando a classe abstract, qualquer outra classe pode ser instanciada como um tipo de dado de C#.

 Para que possamos entender melhor o processo de instanciação, vamos ver o exemplo abaixo, que usa a classe Pessoa:

public class Pessoa

        {

            public char sexo;

            public string nome;

            public int idade;

        }

 

public class Funcionario

        {

            static void Main()

            {

                //Faço a declaração da minha classe e a instancio, tudo na mesma linha

                Pessoa objPessoa = new Pessoa();

 

                //Defino o valor dos campos criados na classe Pessoa

                objPessoa.sexo = 'm';

                objPessoa.nome = "Wellington";

                objPessoa.idade = 21;

 

                //Leio o valor do campo nome

                Console.WriteLine(objPessoa.nome);

            }          

        }

 Importante ressaltar que se apenas declararmos a classe desta forma: Pessoa objPessoa, não significa que ela foi criada automaticamente. Assim, devemos usar o new nomeClasse(). Uma vez realizada a instanciação, usamos o nomeObjetoCriado.membro para que possamos nos referenciar aos membros do objeto criado (neste caso, às variáveis sexo, nome, idade).

 Portanto, para poupar tempo e código declaramos e instanciamos a classe em uma única linha apenas desta forma: Pessoa objPessoa = new Pessoa();.

 Inicialização dos atributos de uma classe – Podemos determinar os valores de inicialização a quaisquer atributos de uma classe. No entanto, caso os atributos de uma classe não possuam valores de inicialização, tais valores serão determinados conforme o tipo de classe no momento de sua instanciação.

 Vejam a seguir quais são os tipos de classes e os valores de inicialização determinados aos seus respectivos atributos:

 - Se for do tipo int, seu valor será 0;

 - Se for do tipo boolean, seu valor será false;

 - Se for do tipo String, seu valor será null.

 Caso os valores de inicialização sejam estabelecidos aos atributos de uma classe, estes serão os valores utilizados no processo de instanciação do objeto dessa mesma classe. Por exemplo:

public class Pessoa

        {

            public char sexo = 'f';

            public string nome = "Maria";

            public int idade = 25;

        }

 E no método Main, chamamos os membros da classe:

Pessoa objPessoa = new Pessoa();

 

            Console.WriteLine(objPessoa.sexo);

            Console.WriteLine(objPessoa.nome);

            Console.WriteLine(objPessoa.idade);

 

            Console.ReadKey();

 Veja o resultado:

f
Maria
25



Construtores
Também conhecidos pelo inglês constructors, os construtores são os responsáveis por criar o objeto em memória, ou seja, instanciar a classe que foi definida. Eles são obrigatórios e são declarados.

Nota:

Em Java apenas as Interfaces não possuem construtores.

exemplo: Declaração de Construtores

public class Carro{

/* CONSTRUTOR DA CLASSE Carro */
public Carro(){
//Faça o que desejar na construção do objeto
}

}
O construtor sempre tem a seguinte assinatura:
modificadores de acesso (public nesse caso) + nome da classe (Carro nesse caso) + parâmetros (nenhum definido
neste caso). O construtor pode ter níveis como: public, private ou protected.

Atributos e Metodos

Atributos são as propriedades de um objeto. Métodos são as ações que um objeto pode realizar. Os objetos são características definidas pelas classes. Neles é permitido instanciar objetos da classe para inicializar os atributos e invocar os método;

        public class Cachorro{

            public String nome;

            public float peso;

            public float altura;

            public String cor;

 Métodos
             utilizando o exemplo dos cães, temos alguns exemplos: latir, correr, pular.


   pacotes de acesso e modificadores
           3 Modificadores de Visibilidade
Permitem controlar a manipulação de membros (atributos e métodos) por métodos considerando os escopos de classe, subclasse e pacote, de forma combinada.
Modificadores:
private
protected
package
public

4 Pacote (package) Organização lógica de classes em grupos
Corresponde à noção de módulo
Há pacotes disponibilizados em Java: java.io, java.lang, java.net, java.awt, ...
Usuários podem criar seus próprios pacotes: basta adicionar a cláusula package <nome> como primeira linha de comando em um arquivo

5 Modificador private
Um membro qualificado como private somente é acessível a partir de métodos da própria classe à qual pertence o membro.

6 Modificador public
Um membro qualificado como public é acessível a partir de qualquer método de qualquer classe, independentemente de subclasse e de pacote.

7 Modificadores public e private Exemplo 1
class Pessoa
{ private int idade; private int altura;
public Pessoa(int i, int a)
{ idade = i; altura = a; }
private void cresce( ) { idade++; altura++; }
private void decresce( ) { idade++; altura--; }
public void envelhece( )
{ if (idade < 22) cresce( ) else decresce( ); }
}
8 Modificadores public e private Exemplo 2
class Funcionario extends Pessoa
{ private int nivel; private int horas;
public Funcionario(int i, int a, int n, int h)
{ super(i, a); nivel = n; horas = h; }
public double salario( )
{ return ( nivel * 80 * horas) ; }
}
9 Modificador package
Um membro qualificado como package é acessível a partir de qualquer método de qualquer classe pertencente ao mesmo pacote que a classe à qual pertence o membro, independentemente de subclasse.

10 Modificador protected
Um membro qualificado como protected é acessível a partir de qualquer método de qualquer classe, exceto se a classe de acesso estiver em pacote distinto e não for subclasse da classe à qual pertence o membro.

11 Modificadores package e protected - Exemplo 1
class Veiculo { int ano; // package
protected int potencia; ... }
class Carro extends Veiculo
{ ... potencia++;
ano++; }
class Retificadora
{ ... Carro c = new Carro (...) ;
c.ano = 1980;
c.potencia = 100; ... }

12 Modificadores package e protected - Exemplo 2
package Basico; // arquivo 1
class Veiculo { int ano; // package
protected int potencia; ... }
package Extensao; // arquivo 2
class Carro extends Veiculo
{ ... potencia++; ... } // sem acesso a ano
class Retificadora
{ ... Carro c = new Carro (...) ; ... }
// sem acesso a ano e potencia

13 Resumo Visibilidade Public Protected Package Private Da mesma classe S
De qualquer classe do mesmo pacote
N
De qualquer classe fora do pacote
De uma subclasse no mesmo pacote
De uma subclasse fora do pacote

14 Pacotes (packages) - definição básica -
Maneira de organizar classes em grupos
Um pacote contém um número qualquer de classes relacionadas de acordo com:
propósito
escopo
herança

15 Pacotes - utilidades/razões -
Permitem organizar classes em unidades, de forma similiar à organização de arquivos em pastas, facilitando a sua manipulação.
Reduzem problemas de conflitos de nomes, pois classes podem ser "escondidas" em pacotes.

16 Pacotes - utilidades/razões -
Permitem proteger classes, atributos e métodos de forma mais abrangente que proteção baseada em classes (modificadores de visibilidade package e protected).
Podem ser usados para identificação de classes (um pacote de classes para um certo propósito pode conter o nome da organização e o nome do autor do pacote).

17 Pacotes - organização em hierarquia -
Um pacote pode conter outro pacote, definindo uma hierarquia de pacotes.
Exemplo: O pacote java, contém os pacotes io, net, util e awt. O pacote awt, por sua vez, contém o pacote image e outros. Assim o nome completo deste último pacote é java.awt.image.

18 Pacotes - utilização -
Classes do pacote java.lang (System, Date, String, Integer, ...) são automaticamente disponíveis.
Uma classe de outro pacote pode ser referenciada através de seu nome completo (por exemplo, java.awt.Font f = new java.awt.Font(); ).
Classes de outro pacote usadas com freqüência devem ser "importadas" (individual ou coletivamente), permitindo que sejam referenciadas somente por nome (por exemplo, Font).

19 Pacotes - comando import -
Usado para importar uma certa classe. Ex:
import java.util.Vector ;
...
Vector v = new Vector();
Usado para importar todas as classes públicas de um pacote. Ex: import java.awt.* ;
Não importa pacotes recursivamente. Por exemplo, import java.awt.* não importa as classes do pacote image.
Devem aparecer no início de um arquivo.

20 Pacotes - conflitos de nomes -
Duas classes com o mesmo nome (obviamente, pertencentes a dois pacotes distintos) só podem ser referenciadas através de seu nome completo.
Exemplo: Classe Table disponível nos pacotes Oracle e SQLServer.
import Oracle.* ;
import SQLServer.* ;
Oracle.Table t1 = new Oracle.Table( ... );
SQLServer.Table t2 = new SQLServer.Table( ... );

21 Pacotes - variável CLASSPATH -
Java combina duas coisas para encontrar classes: o nome do pacote e a lista de diretórios especificada na variável de ambiente CLASSPATH.
Para cada nome de pacote deve haver um diretório no sistema de arquivos, recursivamente (a hierarquia de diretórios espelha a hierarquia de pacotes). Por exemplo, para o pacote java.applet deve haver o diretório java e, dentro deste, o diretório applet, contendo as classes do pacote.

22 Pacotes - variável CLASSPATH - (cont.)
Cada diretório raiz (correspondente a um pacote raiz) deve estar contido em um dos diretórios listados na variável CLASSPATH.
Por exemplo, a variável CLASSPATH pode ser definida como
C:\java\lib; C:\netscape\lib; .
onde o ponto final significa o diretório corrente.

23 Pacotes - processo de criação -
Definir um nome. Por exemplo, pucpr.ccet.analise.
Criar a correspondente estrutura de diretórios. Por exemplo, criar o diretório pucpr dentro de um dos diretórios especificados em CLASSPATH, daí, dentro de pucpr, criar o diretório ccet, e dentro deste o diretório analise.

24 Pacotes - processo de criação - (cont.)
Usar o comando package para inserir classes em um pacote.
Deve ser único em um arquivo e deve ser o primeiro comando presente no arquivo.
Todas as classes definidas no arquivo passam a fazer parte do pacote especificado.
Quando não especificado, as classes são inseridas no pacote default de Java.
Pode ser especificado com o mesmo nome de pacote em diversos arquivos.

25 Pacotes - proteção de classes -
Uma classe só é visível fora de seu pacote se for qualificada como public.
Um arquivo pode conter diversas classes, mas somente uma delas pode ser qualificada como public (o nome do arquivo deve ser igual ao nome dessa classe).
Um comando import do tipo import p.* importa somente as classes públicas do pacote p.

26 Pacotes - proteção de classes - (cont.)
Exemplo:
package colecoes;
public class Lista { // arquivo Lista.java
private Nodo raiz;
public void insere(Object o) { ... }
...}
class Nodo { // visibilidade package
... }


Operadores this 

Praticamente a palavra-chave "this" é uma referência ao objeto atual (ele mesmo). isso pode ser usado dentro de algum método ou construtor. ... Esta é uma palavra-chave em Java. Que pode ser usado dentro do método ou construtor da classe.

Fork e Pull request
Ele faz a clonagem de um repositorio diretamente no seu github.
Ao fazer um fork você pode fazer qualquer tipo de alteração no projeto clonado sem interferir no projeto original. caso você queira fazer alguma alteração no projeto original, então você usa o pull request, sinalizando as alterações ao dono do projeto. quando o dono do projeto receber um pull request ele pode aceitar ou não as mudanças.O pull request e
é uma forma de você contribuir com os projetos da comunidade.

A diferença do comando clone
quando vc faz um fork, o repositorio fica apenas na git hub, na sua maquina virtual. para que ele passe para seu git na pasta do seu computador é preciso clonar.

.gitignore
são arquivos que você não deseja versionalizar
voce cria um arquivo com a denominação .gitignore e guarda as informações dos arquivos que voc~e quer ignorar .
exemplo = se eu salvar nesse arquivo uma doc. com a terminação .xcf
o editor ja vai entender e colocar nesse arquivo os documentos que tem essa terminação.

