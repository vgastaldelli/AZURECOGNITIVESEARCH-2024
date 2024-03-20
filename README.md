# MICROSOFT AZURE - AL SEARCH

Criando um serviço de pesquisa utilizando o AL Search do Microsoft Azure. Com o objetivo de entender o uso prático de uma ferramenta de extrema importância quando estamos falando de coleta de dadosdos clientes, buscando melhores caminhos para a intervenção em problemas cotidianos.

1. Como passo inicial, devemos criar um Search Service, acessando o [Microsoft Azure](https://azure.microsoft.com/pt-br/):

![Azure Search Tela Inicial](https://github.com/vgastaldelli/AZURECOGNITIVESEARCH-2024/assets/160192109/82a22ffb-fa28-4705-9aed-19946e6918b4)

![Create a serch servive right one](https://github.com/vgastaldelli/AZURECOGNITIVESEARCH-2024/assets/160192109/7b192d90-c989-4c09-87c6-49eaf1a8e20c)

**Na opção "Change Princing Tier" colocar "BASIC 2GB, max 3 replicas, max 1 partitions, max 3 seach units". Depois, "Review+Create"**

2. Depois de feito um Search Service, deverá ser criado um serviço de IA, um resource **Azure Al Services**.

![AI Resource creating resource](https://github.com/vgastaldelli/AZURECOGNITIVESEARCH-2024/assets/160192109/fbd56b9e-59fb-4640-99f8-9667f713cd92)

3. Terceiro passo, deverá criar uma conta de armazenamento no Storage Accounts:

![Create Storage Acconts](https://github.com/vgastaldelli/AZURECOGNITIVESEARCH-2024/assets/160192109/a8384535-1c25-4a68-89f4-2b108f157918)

Página de criação:

![New Storage Account creation](https://github.com/vgastaldelli/AZURECOGNITIVESEARCH-2024/assets/160192109/7ac616a2-a5a0-485b-9234-df800604a611)

**Na opção performance colocar "Standard: Recommended for most scenarios (general-purpose v2 account)" e na redundancy, escolher "Locally-redudant storage (LRS)".**

4. Depois de criado o Storage Account, teremos que alterar algumas configurações, no campo **Settings**, na aba **Configuration**:

![Allow blob](https://github.com/vgastaldelli/AZURECOGNITIVESEARCH-2024/assets/160192109/50d1cc03-beee-4b9e-a6b6-94277293bbd6)

**Na opção "Allow Blob anonymous access", estará como Disabled, colocar como Enabled. Depois, salvar**.

5. Em sequência, na aba Data Storage, acessar **containers**
