# Senac
## Curso Desenvolvedor Android

### Usando DART

**Variaveis**

Um valor armazenado na memoria ram do computador,
que perde seu valor sempre que o PC é desligado.
Seu valor pode ser modificado a qualquer momento.
Resumindo, a variavel é como uma caixa, onde eu guardo
um determinado valor, este valor podendo ser um numero,
um texto, um valor lógico (sim/nao), etc.

**Tipos de Variáveis**

- String - textos 
- int - números inteiros 
- double - números decimais
- bool - valor lógico

### Exemplo 1 - Tipos de Variáveis

```dart
void (){
  String nome = "Felipe";
  int idade = 28;
  double altura = 1.78;
  bool programador = true;
  }
 ```
 
### Exemplo 2 - Cálculo Simples

```dart
void main() {

double altura, peso , imc;

altura = 1.68;

peso = 83.0;

imc = peso / (altura * altura);

print ("SEU IMC É -> $imc");

}
```

## Condição Lógica IF

O IF serve para determinar se um bloco de instruções **deve** ou **não** ser executado, pode-se dizer que sempre que for necessário **testar** algum valor usaremos o *if*.

### Operadores Lógicos

- == *Igualdade*
- != *Diferente*
- \>= *Maior ou igual* 
- <= *Menor ou igual*
- \>  *Maior*
- <  *Menor*

### Sintaxe

```dart
if(teste_logico)
{
    //faz isso se o teste for verdadeiro
}
else
{
	//faz isso se o teste for falso
}
```

### Exemplo if :floppy_disk:
```dart
string curso = "programador android";

if(curso == "programador android")
{
    print("Parabéns, você faz ótimas escolhas.");
}
else
{
    print("Vacilão, aposto que você faz ADM.");
}
```
### Exemplo if 2

```dart
void main() {
	double nota1, nota2, media;
  	nota1 = 5;
  	nota2 = 2;
  	media = (nota1 + nota2) / 2;
	
  	if(media >= 5)
  	{
  		print("Aprovado com média $media");
  	}
  	else
  	{
    	print("Reprovado com média $media");
  	}
}
```

## Lógica com DART

Foi importada a *biblioteca* **dart:math** para podermos usar funções matemáticas como potência e raiz quadrada, no exemplo abaixo foi usada a função **math.sqrt()** para calcular a raiz de delta.

- Após a importação foi dado um "apelido" para chamar a função através da sintaxe **as** (dart:math as **math**)
- Foram usados 2 if, o 1º para dar acesso através da palavra mágica *shazam* e o 2º para fazer a equação.
- Cada **if** tem seu próprio **else** , daí a importância de *identar* , organizar o código com **TABS**

### Exemplos usando math

```dart
print(math.sqrt(9)); //exibe a raiz de 9
print(math.pi); //exibe o valor de pi
print(math.pow(2,7)); //exibe o resultado de 2 elevado a 7.
```

### Exemplo Usando If dentro de If (Login e Equação de 2º grau)

```dart
import 'dart:math' as math; 

void main() {

  String palavra_magica;
  palavra_magica = "mjolnir";
  if(palavra_magica == "mjolnir")
  {
    print("Exercício 1 - Bhaskara");
    double delta, a, b, c;
    a = 1;
    b = -10;
    c = 25;
    delta = (b * b) - 4 * a * c;
    print("O DELTA = $delta");  
    if(delta < 0)
    {
      print("Nenhuma raiz real pq o delta menor q zero."); 
    }
    else
    {
      double raiz_q, x1, x2;
      //Raiz Quadrada
      raiz_q = math.sqrt(delta);
      print("A RAIZ DE DELTA = $raiz_q");
      x1 = (-b + raiz_q) / (2 * a);
      x2 = (-b - raiz_q) / (2 * a);
      print("X1 = $x1");
      print("X2 = $x2");
    }
  }
  else
  {
    print("Acesso negado, você não é digno.");  
  }
}
```
## if aninhado ou if encadeado

Quando temos mais do que 2 testes possíveis, é necessário alterar a estrutura e acrescentar um **else if** após o primeiro if.

```dart
if(teste)
{
   //faz isso
}
else if(teste)
{
   //faz isso
}
else
{
   //nenhum dos anteriores
}
```
## Exemplo if else if

```dart
  void main() {
 
  String cidade_natal;
  
  cidade_natal = "rio de janeiro";
  
  if(cidade_natal.toLowerCase() == "são joão da boa vista")
  {
  	print("São Joanense");
  }
  else if(cidade_natal.toLowerCase() == "espírito santo do pinhal")
  {
    print("Pinhalense");
  }
  else if(cidade_natal.toLowerCase() == "rio de janeiro")
  {
    print("Carioca");
  }
  else if(cidade_natal.toLowerCase() == "aguaí")
  {
    print("Aguaiano");
  }
  else if(cidade_natal.toLowerCase() == "águas da prata")
  {
    print("Pratense");
  }
  else
  {
    print("Cidade Não Cadastrada.");
  }
  
}
```

## Operadores Lógicos

### Operador E (AND) &&

*"Somente será **VERDADE** se todas as expressões forem VERDADE".*

### Operador OU (OR) ||

*"Somente será **FALSO** se todas as expressões forem FALSAS".*

## Exemplo teste booleano
```dart
void main() {

  bool var_a, var_b;
  var_a = true;
  var_b = false;
  print((!var_a && var_a) ||  (var_b || !var_b));
  int numero = 10;
  if(var_a == var_b)
  {
    numero = 666;
  }
  else
  {
    numero = numero + 1;
  }
  print(numero);	
}
