---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: BF0A5D64-AC93-48F5-AED2-C21CC8829053
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/get-azdatalakestoredeleteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreDeletedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreDeletedItem.md
ms.openlocfilehash: 92ad3143a52f0d9a81505375ff5abd221784fb2d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889683"
---
# <span data-ttu-id="9565e-101">Get-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="9565e-101">Get-AzDataLakeStoreDeletedItem</span></span>

## <span data-ttu-id="9565e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9565e-102">SYNOPSIS</span></span>
<span data-ttu-id="9565e-103">Pesquisa entradas excluídas no lixo que combinam com o filtro.</span><span class="sxs-lookup"><span data-stu-id="9565e-103">Searches for deleted entries in trash which match the filter.</span></span>

## <span data-ttu-id="9565e-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="9565e-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreDeletedItem [-Account] <String> [-Filter] <String> [-Count <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9565e-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="9565e-105">DESCRIPTION</span></span>
<span data-ttu-id="9565e-106">O cmdlet **Get-AzDataLakeStoreDeletedItem** pesquisa os arquivos ou pastas excluídos no Data Lake Store que corresponderão ao filtro determinado.</span><span class="sxs-lookup"><span data-stu-id="9565e-106">The **Get-AzDataLakeStoreDeletedItem** cmdlet searches the deleted files or folders in Data Lake Store which match the given filter.</span></span>
<span data-ttu-id="9565e-107">Ele exibe os seguintes atributos dos itens excluídos - OriginalPath, TrashDirPath, Type, CreationTime.</span><span class="sxs-lookup"><span data-stu-id="9565e-107">It displays the following attributes of the deleted items - OriginalPath, TrashDirPath, Type, CreationTime.</span></span>
<span data-ttu-id="9565e-108">Essa operação pode ser longa, pois pode ter que pesquisar milhões de arquivos no lixo e pode ser executado como um trabalho.</span><span class="sxs-lookup"><span data-stu-id="9565e-108">This could be a long running operation as it may have to search through millions of files in trash and could be run as a job.</span></span>
<span data-ttu-id="9565e-109">Cuidado: a deseleção de arquivos é uma operação de melhor esforço.</span><span class="sxs-lookup"><span data-stu-id="9565e-109">Caution: Undeleting files is a best effort operation.</span></span> <span data-ttu-id="9565e-110">Não há garantias de que um arquivo possa ser restaurado depois que ele for excluído.</span><span class="sxs-lookup"><span data-stu-id="9565e-110">There are no guarantees that a file can be restored once it is deleted.</span></span> <span data-ttu-id="9565e-111">O uso dessa API é habilitado por meio da lista branca.</span><span class="sxs-lookup"><span data-stu-id="9565e-111">The use of this API is enabled via whitelisting.</span></span> <span data-ttu-id="9565e-112">Se sua conta do ADL não estiver na lista branca, o uso dessa api lançará exceção não implementada.</span><span class="sxs-lookup"><span data-stu-id="9565e-112">If your ADL account is not whitelisted, then using this api will throw Not implemented exception.</span></span> <span data-ttu-id="9565e-113">Para obter mais informações e assistência, entre em contato com o suporte da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="9565e-113">For further information and assistance please contact Microsoft support.</span></span>

## <span data-ttu-id="9565e-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9565e-114">EXAMPLES</span></span>

### <span data-ttu-id="9565e-115">Exemplo: obter detalhes de um arquivo do Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="9565e-115">Example: Get details of a file from the Data Lake Store</span></span>
```
PS> Get-AzDataLakeStoreDeletedItem -Account ml1ptrashtest -Filter test0/file_123

TrashDirPath                         OriginalPath                                          Type CreationTime
------------                         ------------                                          ---- ------------
cd6ad5ce-792b-4812-8a33-8f9ed19eb532 adl://ml1ptrashtest.azuredatalake.com/test0/file_1230 FILE 2/8/2019 8:12:18 AM
356cfd42-39c7-451e-96cb-9f47883d91e2 adl://ml1ptrashtest.azuredatalake.com/test0/file_1232 FILE 2/8/2019 8:12:18 AM
e7b30ac8-2dbc-43a3-8ca6-2d420ac0c488 adl://ml1ptrashtest.azuredatalake.com/test0/file_1237 FILE 2/8/2019 8:12:18 AM
```

## <span data-ttu-id="9565e-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="9565e-116">PARAMETERS</span></span>

### <span data-ttu-id="9565e-117">-Account</span><span class="sxs-lookup"><span data-stu-id="9565e-117">-Account</span></span>
<span data-ttu-id="9565e-118">Especifica o nome da conta do Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="9565e-118">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="9565e-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9565e-119">-AsJob</span></span>
<span data-ttu-id="9565e-120">Execute o cmdlet em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="9565e-120">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="9565e-121">-Count</span><span class="sxs-lookup"><span data-stu-id="9565e-121">-Count</span></span>
<span data-ttu-id="9565e-122">Especifica o número de resultados que o usuário deseja encontrar.</span><span class="sxs-lookup"><span data-stu-id="9565e-122">Specifies the number of results the user wants to find.</span></span> <span data-ttu-id="9565e-123">A consulta é executado até encontrar os resultados de Contagem ou pesquisa todo o lixo, o que acontecer primeiro.</span><span class="sxs-lookup"><span data-stu-id="9565e-123">The query runs until it finds Count results or it searches through entire trash, whichever happens first.</span></span>

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

### <span data-ttu-id="9565e-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9565e-124">-DefaultProfile</span></span>
<span data-ttu-id="9565e-125">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9565e-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9565e-126">-Filter</span><span class="sxs-lookup"><span data-stu-id="9565e-126">-Filter</span></span>
<span data-ttu-id="9565e-127">Especifica a consulta de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="9565e-127">Specifies the search query.</span></span> <span data-ttu-id="9565e-128">Um valor mais específico fornece resultados mais relevantes.</span><span class="sxs-lookup"><span data-stu-id="9565e-128">A more specific value gives more relevant results.</span></span>

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

### <span data-ttu-id="9565e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9565e-129">CommonParameters</span></span>
<span data-ttu-id="9565e-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9565e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9565e-131">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9565e-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9565e-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9565e-132">INPUTS</span></span>

### <span data-ttu-id="9565e-133">System.String</span><span class="sxs-lookup"><span data-stu-id="9565e-133">System.String</span></span>

## <span data-ttu-id="9565e-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="9565e-134">OUTPUTS</span></span>

### <span data-ttu-id="9565e-135">System.Collections.Generic.List<Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreDeletedItem></span><span class="sxs-lookup"><span data-stu-id="9565e-135">System.Collections.Generic.List<Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreDeletedItem></span></span>

## <span data-ttu-id="9565e-136">NOTES</span><span class="sxs-lookup"><span data-stu-id="9565e-136">NOTES</span></span>

## <span data-ttu-id="9565e-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9565e-137">RELATED LINKS</span></span>

[<span data-ttu-id="9565e-138">Restore-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="9565e-138">Restore-AzDataLakeStoreDeletedItem</span></span>](./Restore-AzDataLakeStoreDeletedItem.md)