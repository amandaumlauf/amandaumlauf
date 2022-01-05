/*Biblioteca Pessoal
Função: O programa servirá como uma forma do usuário controlar seu acervo pessoal de livros. 
A partir do menu, o usuário conseguirá cadastrar novos livros, editar, consultar os livros que já possui e ver a quantidade.
Autores: Amanda Umlauf e João Victor Campregher
Data: 20/12/2021*/


#include <stdio.h>
#include <stdlib.h>
#include <string.h>

struct biblioteca {
    char nome_livro[30], autor[30], livro_lido[30];
    int pags, num_livro; 
};

FILE *pArq; 

void abrir_arq(){
    pArq = fopen("biblioteca.txt", "a");
    if(pArq == NULL){
        printf("Erro na abertura do arquivo!");
    return 1; 
}

void menu() 
{
    
    struct biblioteca lib[100];
    char nome_autor[30];
    int i, opcao, cont;
  
    i = opcao = cont = 0;
  
     while (opcao != 6) {
  
        printf("\n\n--------------"
               " BEM-VINDO A SUA BIBLIOTECA "
               "----------------\n");
        printf("\n\n *Utilize os números para navegar no menu* \n");
        printf("\n\n-------------------------\n");
        printf("\n\n1. ADICIONAR UM LIVRO NOVO "
               "\n2. MOSTRAR LIVROS CADASTRADOS\n");
        printf("4. REALIZAR BUSCA NOS LIVROS POR AUTOR\n");
        printf("5. VERIFICAR QUANTOS LIVROS TEM NA BIBLIOTECA\n");
        printf("6. SAIR");
  

        printf("\n\nESCOLHA UMA DAS OPCOES ACIMA: ");
        scanf("%d", &opcao);
  
        
        switch (opcao) {
  
         
        case 1:
  
            cadastrar();
            system ("pause");
            break;
        
        case 2:
            printf("LIVROS CADASTRADOS:\n");
            for (i = 0; i < cont; i++) {

                printf("\t LIVRO NÚMERO = %d", lib[i].num_livro);
  
                printf("\t NOME DO LIVRO = %s", lib[i].nome_livro);
  
                printf("\t NOME DO AUTOR = %s", lib[i].autor);
  
                printf("\t  QUANTIDADE DE PAGINAS = %d", lib[i].pags);
  
                printf("\t  STATUS DE LEITURA = %s \n", lib[i].livro_lido);
                }
    
            system ("pause");
            break;

        case 4:
            printf("INSIRA O NOME DO AUTOR: ");
            scanf("%s", nome_autor);
            for (i = 0; i < cont; i++) {
  
                if (strcmp(nome_autor, lib[i].autor) == 0)
                    printf("NOME DO LIVRO: %s  AUTOR: %s  %d páginas  STATUS: %s",
                           lib[i].nome_livro,
                           lib[i].autor,
                           lib[i].pags,
                           lib[i].livro_lido);
            }
            break;
  
        case 5:
            printf("\n QUANTIDADE DE LIVROS NA BIBLIOTECA: %d", cont);
            system ("pause");
            break;

        case 6:
            exit(0);
        }
    }

void cadastrar(){

    printf("INSIRA O NÚMERO DO LIVRO: ");
    scanf("%d", &lib[i].num_livro);
           
    printf("INSIRA O NOME DO LIVRO: ");
    scanf("%s", &lib[i].nome_livro);
  
    printf("INSIRA O NOME DO AUTOR: ");
    scanf("%s", &lib[i].autor);
  
    printf("INSIRA O NÚMERO DE PÁGINAS: ");
    scanf("%d", &lib[i].pags);
  
    printf("VOCÊ JÁ LEU ESSE LIVRO? (INSIRA NO FORMATO: LIDO/LEITURA PENDENTE) ");
    scanf("%s", &lib[i].livro_lido);

    cont++;
            
    printf("LIVROS JÁ CADASTRADOS:\n");
    for ( i = 0; i < cont; i++) {

    printf("\t LIVRO NÚMERO = %d", lib[i].num_livro);
  
    printf("\t NOME DO LIVRO = %s", lib[i].nome_livro);
  
    printf("\t NOME DO AUTOR = %s", lib[i].autor);
  
    printf("\t  QUANTIDADE DE PAGINAS = %d", lib[i].pags);
  
    printf("\t  STATUS DE LEITURA = %s \n", lib[i].livro_lido);
    }
}
        
int main()
{
  pArq = fopen("biblioteca.txt", "a");
  if(pArq == NULL){
   printf("Erro na abertura do arquivo!");
   return 1;  
}
  
  while (opcao != 6) {
      menu();
  }
return 0
}
    

