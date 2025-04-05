# Trabalho Introdutório

A ideia principal do trabalho é converter uma arquivo csv em um arquivo binário e, após isso, fazer operações para a leitura desse arquivo.


## Structs
Serão necessários dois tipos de structs: struct de cabeçalho e struct de dados.
  * Struct de cabeçalho: registro que guarda as principais informações do arquivo.
  * Struct de dados: registro que guarda os dados em si.

Structs em c:
```c
typedef struct cabecalho
{
    char status;
    long int topo;
    long int proxByteOffset;
    int nroRegArq;
    int nroRegMem;
    char descreveIdentificador[23];
    char descreveYear[27];
    char descreveFinancialLoss[28];
    char codDescreveCountry;
    char descreveCountry[26];
    char codDescreveType;
    char descreveType[38];
    char codDescreveTargetIndustry;
    char descreveTargetIndustry[38];
    char codDescreveDefense;
    char descreveDefense[67];
} head;

typedef struct dado
{
    char removido;
    int tamanhoRegistro;
    long int prox;
    int idAttack;
    int year;
    float financialLoss;
    char* country;
    char* attackType;
    char* targetIndustry;
    char* defenseMechanism;
} data;
```


