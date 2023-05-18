# restaurante
Cardápio de Restaurante criado no C#

System.Console.WriteLine("Cardápio Restaurante");
//constante
const int row = 5;
const int col = 7;
//declarando a matriz linha x coluna
string [,] cardapio = new string[row,col]
// 3ª forma de preenchimento da matriz 
{
   {"2ª feira","3ª feira","4ª feira","5ª feira","6ª feira","sábado    ","domingo"},
   {"Comercial","Macarronada","Virado   ","Peixe   ","Feijoada","Churrasco   ","Filé"},
   {"R$30,00  ","R$32,00  ","R$35,00  ","R$38,00  ","R$42,00  ","R$50,00    ","R$52,00  "},
   {"Suco de Uva","Suco de Banana", "Suco de Abacaxi","Suco de Limão","Suco de Laranja","Suco Graviola","Suco de Cupuaçu"},
   {"R$15,00  ","R$12,00  ","R$15,00  ","R$12,00  ","R$12,00  ","R$18,00      ","R$12,00  "}
};

//imprimindo a matriz // 3ª forma de impressão
for (int i = 0; i < row; i++)
{
    for (int j = 0; j < col; j++)
    {
        System.Console.Write($"{cardapio[i,j]}\t");
    }
    System.Console.WriteLine();
}
//mensagem
string msg = "Opção inválida !!";
_etq:
//enunciado de opções
System.Console.WriteLine("Escolha sua refeição: \n (1) - Comercial\n (2) - Macarronada\n (3) - Virado\n (4) - Peixe\n (5) - Feijoada\n (6) - Churrasco\n (7) - Filé\n  ");
int opcao = int.Parse(Console.ReadLine());
switch (opcao)
{
    case 1:
    System.Console.WriteLine($"A refeição escolhida foi {cardapio[1,0]} por {cardapio[2,0]}");
    break;
     case 2:
    System.Console.WriteLine($"A refeição escolhida foi {cardapio[1,1]} por {cardapio[2,1]}");
    break;
     case 3:
    System.Console.WriteLine($"A refeição escolhida foi {cardapio[1,2]} por {cardapio[2,2]}");
    break;
     case 4:
    System.Console.WriteLine($"A refeição escolhida foi {cardapio[1,3]} por {cardapio[2,3]}");
    break;
     case 5:
    System.Console.WriteLine($"A refeição escolhida foi {cardapio[1,4]} por {cardapio[2,4]}");
    break;
    case 6:
    System.Console.WriteLine($"A refeição escolhida foi {cardapio[1,5]} por {cardapio[2,5]}");
    break;
    case 7:
    System.Console.WriteLine($"A refeição escolhida foi {cardapio[1,6]} por {cardapio[2,6]}");
    break;
    default:
        System.Console.WriteLine(msg);
       goto _etq;
}
_etq1:
System.Console.WriteLine("Gostaria de Adicionar Suco do dia?\n (1) SIM \n (2) NÃO");
int bebida0 = int.Parse(Console.ReadLine());
if (bebida0 == 1)
{
    if (opcao == 1)
    {
        System.Console.WriteLine($"A comida escolhida foi {cardapio[1,0]} por {cardapio[2,0]} e a bebida foi {cardapio[3,0]} por {cardapio[4,0]} totalizando R$45,00");
    }
    if (opcao == 2)
    {
        System.Console.WriteLine($"A comida escolhida foi {cardapio[1,1]} por {cardapio[2,1]} e a bebida foi {cardapio[3,1]} por {cardapio[4,1]} totalizando R$44,00");
    }
    if (opcao == 3)
    {
        System.Console.WriteLine($"A comida escolhida foi {cardapio[1,2]} por {cardapio[2,2]} e a bebida foi {cardapio[3,2]} por {cardapio[4,2]} totalizando R$50,00");
    }
    if (opcao == 4)
    {
        System.Console.WriteLine($"A comida escolhida foi {cardapio[1,3]} por {cardapio[2,3]} e a bebida foi {cardapio[3,3]} por {cardapio[4,3]} totalizando R$50,00");
    }
    if (opcao == 5)
    {
        System.Console.WriteLine($"A comida escolhida foi {cardapio[1,4]} por {cardapio[2,4]} e a bebida foi {cardapio[3,4]} por {cardapio[4,4]} totalizando R$44,00");
    }
    if (opcao == 6)
    {
        System.Console.WriteLine($"A comida escolhida foi {cardapio[1,5]} por {cardapio[2,5]} e a bebida foi {cardapio[3,5]} por {cardapio[4,5]} totalizando R$68,00");
    }
    if (opcao == 7)
    {
        System.Console.WriteLine($"A comida escolhida foi {cardapio[1,6]} por {cardapio[2,6]} e a bebida foi {cardapio[3,6]} por {cardapio[4,6]} totalizando R$64,00");
    }
}
else if (bebida0 == 0)
    {
     if (opcao == 1)
    {
        System.Console.WriteLine($"A refeição escolhida foi {cardapio[1,0]} por {cardapio[2,0]}");
    }
    if (opcao == 2)
    {
       System.Console.WriteLine($"A refeição escolhida foi {cardapio[1,1]} por {cardapio[2,1]}");
    }
    if (opcao == 3)
    {
        System.Console.WriteLine($"A refeição escolhida foi {cardapio[1,2]} por {cardapio[2,2]}");
    }
    if (opcao == 4)
    {
        System.Console.WriteLine($"A refeição escolhida foi {cardapio[1,3]} por {cardapio[2,3]}");
    }
    if (opcao == 5)
    {
        System.Console.WriteLine($"A refeição escolhida foi {cardapio[1,4]} por {cardapio[2,4]}");
    }
    if (opcao == 6)
    {
        System.Console.WriteLine($"A refeição escolhida foi {cardapio[1,5]} por {cardapio[2,5]}");
    }
    if (opcao == 7)
    {
        System.Console.WriteLine($"A refeição escolhida foi {cardapio[1,6]} por {cardapio[2,6]}");
    }
    }
     else //(opcao != 0 || opcao !=1)
    {
        System.Console.WriteLine(msg);
       goto _etq1;
    }
Console.ReadKey();
