---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: BF0A5D64-AC93-48F5-AED2-C21CC8829053
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoredeleteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreDeletedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreDeletedItem.md
ms.openlocfilehash: cfcdf8accb5de467c5b243df2c973074fe9ae31a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117726"
---
# <span data-ttu-id="a9bde-101">Get-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="a9bde-101">Get-AzDataLakeStoreDeletedItem</span></span>

## <span data-ttu-id="a9bde-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a9bde-102">SYNOPSIS</span></span>
<span data-ttu-id="a9bde-103">Procura entradas excluídas na lixeira que corresponderem ao filtro.</span><span class="sxs-lookup"><span data-stu-id="a9bde-103">Searches for deleted entries in trash which match the filter.</span></span>

## <span data-ttu-id="a9bde-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a9bde-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreDeletedItem [-Account] <String> [-Filter] <String> [-Count <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a9bde-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="a9bde-105">DESCRIPTION</span></span>
<span data-ttu-id="a9bde-106">O cmdlet **Get-AzDataLakeStoreDeletedItem** pesquisa os arquivos ou pastas excluídos no Data Lake Store que corresponderem ao filtro determinado.</span><span class="sxs-lookup"><span data-stu-id="a9bde-106">The **Get-AzDataLakeStoreDeletedItem** cmdlet searches the deleted files or folders in Data Lake Store which match the given filter.</span></span>
<span data-ttu-id="a9bde-107">Ele exibe os seguintes atributos dos itens excluídos – OriginalPath, TrashDirPath, Type, CreationTime.</span><span class="sxs-lookup"><span data-stu-id="a9bde-107">It displays the following attributes of the deleted items - OriginalPath, TrashDirPath, Type, CreationTime.</span></span>
<span data-ttu-id="a9bde-108">Isso pode ser uma operação longa, pois pode ser preciso pesquisar milhões de arquivos na lixeira e pode ser executado como um trabalho.</span><span class="sxs-lookup"><span data-stu-id="a9bde-108">This could be a long running operation as it may have to search through millions of files in trash and could be run as a job.</span></span>
<span data-ttu-id="a9bde-109">Cuidado: a reseleção de arquivos é uma operação de melhor esforço.</span><span class="sxs-lookup"><span data-stu-id="a9bde-109">Caution: Undeleting files is a best effort operation.</span></span> <span data-ttu-id="a9bde-110">Não há garantias de que um arquivo possa ser restaurado depois de excluído.</span><span class="sxs-lookup"><span data-stu-id="a9bde-110">There are no guarantees that a file can be restored once it is deleted.</span></span> <span data-ttu-id="a9bde-111">O uso dessa API está habilitado por meio da lista de contatos.</span><span class="sxs-lookup"><span data-stu-id="a9bde-111">The use of this API is enabled via whitelisting.</span></span> <span data-ttu-id="a9bde-112">Se sua conta do ADL não estiver listada em branco, o uso dessa api lançará exceção não implementada.</span><span class="sxs-lookup"><span data-stu-id="a9bde-112">If your ADL account is not whitelisted, then using this api will throw Not implemented exception.</span></span> <span data-ttu-id="a9bde-113">Para obter mais informações e assistência, entre em contato com o suporte da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a9bde-113">For further information and assistance please contact Microsoft support.</span></span>

## <span data-ttu-id="a9bde-114">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a9bde-114">EXAMPLES</span></span>

### <span data-ttu-id="a9bde-115">Exemplo: Obter detalhes de um arquivo do Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="a9bde-115">Example: Get details of a file from the Data Lake Store</span></span>
```
PS> Get-AzDataLakeStoreDeletedItem -Account ml1ptrashtest -Filter test0/file_123

TrashDirPath                         OriginalPath                                          Type CreationTime
------------                         ------------                                          ---- ------------
cd6ad5ce-792b-4812-8a33-8f9ed19eb532 adl://ml1ptrashtest.azuredatalake.com/test0/file_1230 FILE 2/8/2019 8:12:18 AM
356cfd42-39c7-451e-96cb-9f47883d91e2 adl://ml1ptrashtest.azuredatalake.com/test0/file_1232 FILE 2/8/2019 8:12:18 AM
e7b30ac8-2dbc-43a3-8ca6-2d420ac0c488 adl://ml1ptrashtest.azuredatalake.com/test0/file_1237 FILE 2/8/2019 8:12:18 AM
```

## <span data-ttu-id="a9bde-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a9bde-116">PARAMETERS</span></span>

### <span data-ttu-id="a9bde-117">-Conta</span><span class="sxs-lookup"><span data-stu-id="a9bde-117">-Account</span></span>
<span data-ttu-id="a9bde-118">Especifica o nome da conta do Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="a9bde-118">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="a9bde-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a9bde-119">-AsJob</span></span>
<span data-ttu-id="a9bde-120">Executar cmdlet em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="a9bde-120">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="a9bde-121">-Contagem</span><span class="sxs-lookup"><span data-stu-id="a9bde-121">-Count</span></span>
<span data-ttu-id="a9bde-122">Especifica o número de resultados que o usuário deseja encontrar.</span><span class="sxs-lookup"><span data-stu-id="a9bde-122">Specifies the number of results the user wants to find.</span></span> <span data-ttu-id="a9bde-123">A consulta é executado até encontrar os resultados da Contagem ou pesquisa toda a lixeira, o que acontecer primeiro.</span><span class="sxs-lookup"><span data-stu-id="a9bde-123">The query runs until it finds Count results or it searches through entire trash, whichever happens first.</span></span>

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

### <span data-ttu-id="a9bde-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9bde-124">-DefaultProfile</span></span>
<span data-ttu-id="a9bde-125">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a9bde-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9bde-126">-Filtro</span><span class="sxs-lookup"><span data-stu-id="a9bde-126">-Filter</span></span>
<span data-ttu-id="a9bde-127">Especifica a consulta de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="a9bde-127">Specifies the search query.</span></span> <span data-ttu-id="a9bde-128">Um valor mais específico fornece resultados mais relevantes.</span><span class="sxs-lookup"><span data-stu-id="a9bde-128">A more specific value gives more relevant results.</span></span>

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

### <span data-ttu-id="a9bde-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9bde-129">CommonParameters</span></span>
<span data-ttu-id="a9bde-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9bde-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9bde-131">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9bde-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9bde-132">Entradas</span><span class="sxs-lookup"><span data-stu-id="a9bde-132">INPUTS</span></span>

### <span data-ttu-id="a9bde-133">System.String</span><span class="sxs-lookup"><span data-stu-id="a9bde-133">System.String</span></span>

## <span data-ttu-id="a9bde-134">Saídas</span><span class="sxs-lookup"><span data-stu-id="a9bde-134">OUTPUTS</span></span>

### <span data-ttu-id="a9bde-135">System.Collections.Generic.List<Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreDeletedItem></span><span class="sxs-lookup"><span data-stu-id="a9bde-135">System.Collections.Generic.List<Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreDeletedItem></span></span>

## <span data-ttu-id="a9bde-136">Notas</span><span class="sxs-lookup"><span data-stu-id="a9bde-136">NOTES</span></span>

## <span data-ttu-id="a9bde-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a9bde-137">RELATED LINKS</span></span>

[<span data-ttu-id="a9bde-138">Restore-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="a9bde-138">Restore-AzDataLakeStoreDeletedItem</span></span>](./Restore-AzDataLakeStoreDeletedItem.md)