# MICROSOFT AZURE - AI SEARCH🔍🔎

Criando um serviço de pesquisa utilizando o Microsoft Azure AI Search, visando compreender as suas funcionalidades e o uso prático de uma ferramenta de extrema importância, principalmente quando estamos falando de coleta de dados dos clientes, buscando melhores caminhos para a intervenção nos problemas cotidianos de uma empresa.

_Documentação base_:

[Explore an Azure AI Search index (UI)](https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/11-ai-search.html)


1. Como passo inicial, devemos criar um Search Service, acessando o [Microsoft Azure](https://azure.microsoft.com/pt-br/):

![Azure Search Tela Inicial](https://github.com/vgastaldelli/AZURECOGNITIVESEARCH-2024/assets/160192109/82a22ffb-fa28-4705-9aed-19946e6918b4)

![Create a serch servive right one](https://github.com/vgastaldelli/AZURECOGNITIVESEARCH-2024/assets/160192109/7b192d90-c989-4c09-87c6-49eaf1a8e20c)

**Na opção "Change Princing Tier" colocar "BASIC 2GB, max 3 replicas, max 1 partitions, max 3 seach units". Depois, "Review+Create".**

2. Depois de feito um Search Service, deverá ser criado um serviço de IA, um resource **Azure AI Services**.

![AI Resource creating resource](https://github.com/vgastaldelli/AZURECOGNITIVESEARCH-2024/assets/160192109/fbd56b9e-59fb-4640-99f8-9667f713cd92)

3. Terceiro passo, deverá criar uma conta de armazenamento no Storage Accounts:

![Create Storage Acconts](https://github.com/vgastaldelli/AZURECOGNITIVESEARCH-2024/assets/160192109/a8384535-1c25-4a68-89f4-2b108f157918)

Página de criação:

![New Storage Account creation](https://github.com/vgastaldelli/AZURECOGNITIVESEARCH-2024/assets/160192109/7ac616a2-a5a0-485b-9234-df800604a611)

**Na opção performance colocar "Standard: Recommended for most scenarios (general-purpose v2 account)" e na redundancy, escolher "Locally-redudant storage (LRS)".**

4. Depois de criado o Storage Account, teremos que alterar algumas configurações, no campo **Settings**, na aba **Configuration**:

![Allow blob](https://github.com/vgastaldelli/AZURECOGNITIVESEARCH-2024/assets/160192109/50d1cc03-beee-4b9e-a6b6-94277293bbd6)

**Na opção "Allow Blob anonymous access", estará como Disabled, colocar como Enabled. Depois, salvar**.

5. Em sequência, na aba **Data Storage**, acessar **Containers** e criar um novo. Abrirá uma aba à direita: "New container".

![Containers](https://github.com/vgastaldelli/AZURECOGNITIVESEARCH-2024/assets/160192109/6eaad8b9-876c-4099-a807-732d4c7b286a)

![New container](https://github.com/vgastaldelli/AZURECOGNITIVESEARCH-2024/assets/160192109/13643b4c-80e0-4d9c-ac68-f687823cc76e)

**No campo "Anonymous access level" selecionar a opção "Container (anonymous read access for containers and blobs). E, ademais, um nome. Aqui seguimos a documentação apresentada inicialmente como base. Assim, criar.**

_**Outro passo imprescindível é fazer o upload, no container criado, de toda a documentação a ser utilizada. Como pode ser verificado abaixo:**_

![documents upload](https://github.com/vgastaldelli/AZURECOGNITIVESEARCH-2024/assets/160192109/3f6e2f10-c308-48f8-8e80-e962acc6a294)

_**Como vemos até aqui: criamos um mecanismo de busca; um recurso de inteligência artificial; e um storage account.**_

6. Agora voltamos ao AI Search para importar dados. Segue as configurações abaixo:

![image](https://github.com/vgastaldelli/AZURECOGNITIVESEARCH-2024/assets/160192109/cdad063f-9633-4e5e-b31a-eed8189f453f)

**No campo "Connection string", selecionar "Choose an existing connection". Devendo, depois, selecionar seu Storage Account e o container a ser utilizado. Segue abaixo:**

![image](https://github.com/vgastaldelli/AZURECOGNITIVESEARCH-2024/assets/160192109/5c5fa73b-f7bf-42da-9a10-e8b901e8e66f)

7. Logo após, pressionar "Next: Add cognitive skills". No campo **Attach Al Services** deverá selecionar seu recurso:

![Azure Attach Resource](https://github.com/vgastaldelli/AZURECOGNITIVESEARCH-2024/assets/160192109/f222732c-c382-4083-9811-2541b7f75ad7)

No **Add enrichments** as configurações abaixo:

![Add enrichments](https://github.com/vgastaldelli/AZURECOGNITIVESEARCH-2024/assets/160192109/4a348a2a-8d65-44d6-9477-aa222d7e2c80)

![add enrichments 2](https://github.com/vgastaldelli/AZURECOGNITIVESEARCH-2024/assets/160192109/b497d132-1800-4eee-b8b7-be79a707a298)

Além disso, no campo **Save enrichments to a knowledge store**, seleciona-se as opções abaixo:

![save enrichment](https://github.com/vgastaldelli/AZURECOGNITIVESEARCH-2024/assets/160192109/9d29fd62-3f51-4fbb-b428-169f20553708)

Em seguida, costumizar **target index**:

![target index](https://github.com/vgastaldelli/AZURECOGNITIVESEARCH-2024/assets/160192109/588c9448-c849-4fe8-a5d4-71041477b3d1)

Finalmente, **Next: Create an indexer**:

![criando um indexer](https://github.com/vgastaldelli/AZURECOGNITIVESEARCH-2024/assets/160192109/9bc23a2f-9ae1-4273-9922-96f77e77504a)

Selecionar, ao final, **Submit**.

8. Retornando ao AI Search, acessando seu recurso, no campo **Search Management**, acesse **Indexes**, lá estará presente todos os dados importados:

![image](https://github.com/vgastaldelli/AZURECOGNITIVESEARCH-2024/assets/160192109/366925b1-5fba-4743-9a5f-0b44c54c70c5)

9. Logo, poderá acessar o **Search explorer**, para analisar os dados. Segue exemplo abaixo:

![Search explorer](https://github.com/vgastaldelli/AZURECOGNITIVESEARCH-2024/assets/160192109/63d590a3-1435-4f73-a51e-c588463f0848)

_**O mais essencial aprendizado, de todo esse processo até a finalização, é que nos tempos atuais, devido ao grande volume de dados produzidos cotidianamente, uma ferramenta desse porte oferece inúmeros caminhos para otimizar processos e garantir a rapidez na verificação de informações fornecidas por grandes grupos de clientes, distribuídos em diversas regiões geográficas. Assim, oferecendo mais ampla margem de ação para as empresas e aprimoramento de seus serviços no mercado.**_
