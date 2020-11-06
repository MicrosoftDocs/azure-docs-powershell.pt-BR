---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: BF0A5D64-AC93-48F5-AED2-C21CC8829053
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoredeleteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreDeletedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreDeletedItem.md
ms.openlocfilehash: 750203e954ef96619e32b63ffd6eae333bb852f2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93596855"
---
# <span data-ttu-id="a9832-101">Get-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="a9832-101">Get-AzDataLakeStoreDeletedItem</span></span>

## <span data-ttu-id="a9832-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a9832-102">SYNOPSIS</span></span>
<span data-ttu-id="a9832-103">Procura por entradas excluídas no lixo que correspondam ao filtro.</span><span class="sxs-lookup"><span data-stu-id="a9832-103">Searches for deleted entries in trash which match the filter.</span></span>

## <span data-ttu-id="a9832-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a9832-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreDeletedItem [-Account] <String> [-Filter] <String> [-Count <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a9832-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a9832-105">DESCRIPTION</span></span>
<span data-ttu-id="a9832-106">O cmdlet **Get-AzDataLakeStoreDeletedItem** pesquisa os arquivos ou pastas excluídos no data Lake Store que correspondem ao filtro fornecido.</span><span class="sxs-lookup"><span data-stu-id="a9832-106">The **Get-AzDataLakeStoreDeletedItem** cmdlet searches the deleted files or folders in Data Lake Store which match the given filter.</span></span>
<span data-ttu-id="a9832-107">Ele exibe os seguintes atributos dos itens excluídos: OriginalPath, TrashDirPath, Type, CreationTime.</span><span class="sxs-lookup"><span data-stu-id="a9832-107">It displays the following attributes of the deleted items - OriginalPath, TrashDirPath, Type, CreationTime.</span></span>
<span data-ttu-id="a9832-108">Isso pode ser uma operação de longa duração, pois pode ser necessário pesquisar milhões de arquivos no lixo e executar como um trabalho.</span><span class="sxs-lookup"><span data-stu-id="a9832-108">This could be a long running operation as it may have to search through millions of files in trash and could be run as a job.</span></span>

## <span data-ttu-id="a9832-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a9832-109">EXAMPLES</span></span>

### <span data-ttu-id="a9832-110">Exemplo: obter detalhes de um arquivo do repositório data Lake</span><span class="sxs-lookup"><span data-stu-id="a9832-110">Example: Get details of a file from the Data Lake Store</span></span>
```
PS> Get-AzDataLakeStoreDeletedItem -Account ml1ptrashtest -Filter test0/file_123

TrashDirPath                         OriginalPath                                          Type CreationTime
------------                         ------------                                          ---- ------------
cd6ad5ce-792b-4812-8a33-8f9ed19eb532 adl://ml1ptrashtest.azuredatalake.com/test0/file_1230 FILE 2/8/2019 8:12:18 AM
356cfd42-39c7-451e-96cb-9f47883d91e2 adl://ml1ptrashtest.azuredatalake.com/test0/file_1232 FILE 2/8/2019 8:12:18 AM
e7b30ac8-2dbc-43a3-8ca6-2d420ac0c488 adl://ml1ptrashtest.azuredatalake.com/test0/file_1237 FILE 2/8/2019 8:12:18 AM
```

## <span data-ttu-id="a9832-111">OS</span><span class="sxs-lookup"><span data-stu-id="a9832-111">PARAMETERS</span></span>

### <span data-ttu-id="a9832-112">-Conta</span><span class="sxs-lookup"><span data-stu-id="a9832-112">-Account</span></span>
<span data-ttu-id="a9832-113">Especifica o nome da conta do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="a9832-113">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9832-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a9832-114">-AsJob</span></span>
<span data-ttu-id="a9832-115">Execute o cmdlet em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="a9832-115">Run cmdlet in the background.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9832-116">-Contagem</span><span class="sxs-lookup"><span data-stu-id="a9832-116">-Count</span></span>
<span data-ttu-id="a9832-117">Especifica o número de resultados que o usuário quer encontrar.</span><span class="sxs-lookup"><span data-stu-id="a9832-117">Specifies the number of results the user wants to find.</span></span> <span data-ttu-id="a9832-118">A consulta é executada até encontrar os resultados da contagem ou pesquisa por toda a lixeira, o que ocorrer primeiro.</span><span class="sxs-lookup"><span data-stu-id="a9832-118">The query runs until it finds Count results or it searches through entire trash, whichever happens first.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 1
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9832-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9832-119">-DefaultProfile</span></span>
<span data-ttu-id="a9832-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a9832-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9832-121">-Filtro</span><span class="sxs-lookup"><span data-stu-id="a9832-121">-Filter</span></span>
<span data-ttu-id="a9832-122">Especifica a consulta de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="a9832-122">Specifies the search query.</span></span> <span data-ttu-id="a9832-123">Um valor mais específico fornece resultados mais relevantes.</span><span class="sxs-lookup"><span data-stu-id="a9832-123">A more specific value gives more relevant results.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9832-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9832-124">CommonParameters</span></span>
<span data-ttu-id="a9832-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9832-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9832-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9832-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9832-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a9832-127">INPUTS</span></span>

### <span data-ttu-id="a9832-128">System. String</span><span class="sxs-lookup"><span data-stu-id="a9832-128">System.String</span></span>

## <span data-ttu-id="a9832-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a9832-129">OUTPUTS</span></span>

### <span data-ttu-id="a9832-130">System. Collections. Generic. List<Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreDeletedItem></span><span class="sxs-lookup"><span data-stu-id="a9832-130">System.Collections.Generic.List<Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreDeletedItem></span></span>

## <span data-ttu-id="a9832-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a9832-131">NOTES</span></span>

## <span data-ttu-id="a9832-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a9832-132">RELATED LINKS</span></span>

[<span data-ttu-id="a9832-133">Restore-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="a9832-133">Restore-AzDataLakeStoreDeletedItem</span></span>](./Restore-AzDataLakeStoreDeletedItem.md)