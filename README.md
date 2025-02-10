BLG language 2 é uma versão do BLG-compiler, é um compilador desenvolvido em C# usando a ferramenta ANTLR4 e o padrão de projeto Observer. É um compilador capaz de compilar uma linguagem de programação customizada chamada BLG Language

#Funcionalidades
Estruturas de controles:
1. Declaração de Funções
2. Comandos de Entrada e Saída (write,read)
3. Laço FOR
4. Laço WHILE
5. Laço DO-WHILE
6. Estrutura de Decisão IF-ELSE

#Exemplo de Programa:

function multiplicacao(num1, num2, num3) {
    write num1 * num2 / num3;
}

write "Digite o primeiro número:";
read num1;
write "Digite o segundo número:";
read num2;
write "Digite o terceiro número:";
read num3;

write "Chamando a função multiplicacao";
multiplicacao(num1, num2, num3);

function CalcFatorial(fatorial, n) {
    for (numero i = 1; i <= n; numero i = (i + 1)) {
        numero fatorial = fatorial * i;
    }
    write fatorial;
}

numero fatorial = 1;
write "fatorial de quanto?";
numero read n;

write "chamando a função CalcFatorial...";
CalcFatorial(fatorial, n);

write "informe um número:";
numero read x;
write "informe outro número:";
numero read y;

write "começo do FOR";
for (numero i; i < 10; numero i = i + 1) {
    numero x = (x + 1);
    write x;
}

write "informe um número:";
numero read x;
write "informe outro número:";
numero read y;

write "começo do WHILE";
while (i < 10) {
    numero x = (x + 1);
    write x;
}

write "informe um número:";
numero read x;
write "informe outro número:";
numero read y;

write "Começo DoWhile";
do {
    numero x = x + 1;
    write x;
} while (i < 10);

write "informe um número:";
numero read x;
write "informe outro número:";
numero read y;
if (x > y) {
    write "X é maior que Y";
} else {
    if (x < y) {
        write "Y é maior que X";
    } else {
        write "Y e X são iguais";
    }
}

#Para Compilar: 
utilize o seguinte comando:

antlr4 -package Grammar -visitor -Dlanguage=CSharp -o Grammar/ Lang.g4

Este comando gera a pasta GRAMMAR contendo os arquivos LangLexer.cs, LangParser.cs e LangVisitor.cs

