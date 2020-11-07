---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: ED17430D-4DAF-4B9E-937D-0F8A843DAB96
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/test-azdatalakeanalyticscatalogitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Test-AzDataLakeAnalyticsCatalogItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Test-AzDataLakeAnalyticsCatalogItem.md
ms.openlocfilehash: 2879923b38b6813213fe6819f84fa55a593f6930
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93940531"
---
# <span data-ttu-id="32a58-101">Test-AzDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="32a58-101">Test-AzDataLakeAnalyticsCatalogItem</span></span>

## <span data-ttu-id="32a58-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="32a58-102">SYNOPSIS</span></span>
<span data-ttu-id="32a58-103">Verifica a existência de um item de catálogo.</span><span class="sxs-lookup"><span data-stu-id="32a58-103">Checks for the existence of a catalog item.</span></span>

## <span data-ttu-id="32a58-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="32a58-104">SYNTAX</span></span>

```
Test-AzDataLakeAnalyticsCatalogItem [-Account] <String> [-ItemType] <CatalogItemType>
 [-Path] <CatalogPathInstance> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="32a58-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="32a58-105">DESCRIPTION</span></span>
<span data-ttu-id="32a58-106">O cmdlet **Test-AzDataLakeAnalyticsCatalogItem** verifica a existência de um item de catálogo do Azure data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="32a58-106">The **Test-AzDataLakeAnalyticsCatalogItem** cmdlet checks for the existence of an Azure Data Lake Analytics catalog item.</span></span>

## <span data-ttu-id="32a58-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="32a58-107">EXAMPLES</span></span>

### <span data-ttu-id="32a58-108">Exemplo 1: testar se existe um item de catálogo</span><span class="sxs-lookup"><span data-stu-id="32a58-108">Example 1: Test whether a catalog item exists</span></span>
```
PS C:\>Test-AzDataLakeAnalyticsCatalogItem -Account "ContosoAdlAccount" -ItemType Schema -Path "databaseName.schemaName"
```

<span data-ttu-id="32a58-109">Esse comando testa se existe um item de esquema especificado.</span><span class="sxs-lookup"><span data-stu-id="32a58-109">This command tests whether a specified Schema item exists.</span></span>

## <span data-ttu-id="32a58-110">OS</span><span class="sxs-lookup"><span data-stu-id="32a58-110">PARAMETERS</span></span>

### <span data-ttu-id="32a58-111">-Conta</span><span class="sxs-lookup"><span data-stu-id="32a58-111">-Account</span></span>
<span data-ttu-id="32a58-112">Especifica o nome da conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="32a58-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="32a58-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32a58-113">-DefaultProfile</span></span>
<span data-ttu-id="32a58-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="32a58-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="32a58-115">-ItemType</span><span class="sxs-lookup"><span data-stu-id="32a58-115">-ItemType</span></span>
<span data-ttu-id="32a58-116">Especifica o tipo de item de catálogo do item a ser verificado.</span><span class="sxs-lookup"><span data-stu-id="32a58-116">Specifies the catalog item type of the item to check.</span></span>
<span data-ttu-id="32a58-117">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="32a58-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="32a58-118">Base</span><span class="sxs-lookup"><span data-stu-id="32a58-118">Database</span></span>
- <span data-ttu-id="32a58-119">Esquema</span><span class="sxs-lookup"><span data-stu-id="32a58-119">Schema</span></span>
- <span data-ttu-id="32a58-120">Assembly</span><span class="sxs-lookup"><span data-stu-id="32a58-120">Assembly</span></span>
- <span data-ttu-id="32a58-121">TableName</span><span class="sxs-lookup"><span data-stu-id="32a58-121">Table</span></span>
- <span data-ttu-id="32a58-122">TablePartition</span><span class="sxs-lookup"><span data-stu-id="32a58-122">TablePartition</span></span>
- <span data-ttu-id="32a58-123">TableValuedFunction</span><span class="sxs-lookup"><span data-stu-id="32a58-123">TableValuedFunction</span></span>
- <span data-ttu-id="32a58-124">TableStatistics</span><span class="sxs-lookup"><span data-stu-id="32a58-124">TableStatistics</span></span>
- <span data-ttu-id="32a58-125">ExternalDataSource</span><span class="sxs-lookup"><span data-stu-id="32a58-125">ExternalDataSource</span></span>
- <span data-ttu-id="32a58-126">Ver</span><span class="sxs-lookup"><span data-stu-id="32a58-126">View</span></span>
- <span data-ttu-id="32a58-127">Processo</span><span class="sxs-lookup"><span data-stu-id="32a58-127">Procedure</span></span>
- <span data-ttu-id="32a58-128">Metade</span><span class="sxs-lookup"><span data-stu-id="32a58-128">Secret</span></span>
- <span data-ttu-id="32a58-129">Provedores</span><span class="sxs-lookup"><span data-stu-id="32a58-129">Credential</span></span>
- <span data-ttu-id="32a58-130">Tipos</span><span class="sxs-lookup"><span data-stu-id="32a58-130">Types</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+CatalogItemType
Parameter Sets: (All)
Aliases:
Accepted values: Database, Schema, Assembly, Table, TablePartition, TableValuedFunction, TableStatistics, ExternalDataSource, View, Procedure, Secret, Credential, Types, Package

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32a58-131">-Caminho</span><span class="sxs-lookup"><span data-stu-id="32a58-131">-Path</span></span>
<span data-ttu-id="32a58-132">Especifica o caminho para o item a ser buscado ou o caminho para o item pai da lista de itens a serem listados.</span><span class="sxs-lookup"><span data-stu-id="32a58-132">Specifies the path to the item to fetch, or the path to the parent item of the items to list.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32a58-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32a58-133">CommonParameters</span></span>
<span data-ttu-id="32a58-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32a58-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32a58-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32a58-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32a58-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="32a58-136">INPUTS</span></span>

### <span data-ttu-id="32a58-137">System. String</span><span class="sxs-lookup"><span data-stu-id="32a58-137">System.String</span></span>

### <span data-ttu-id="32a58-138">Microsoft. Azure. Commands. DataLakeAnalytics. Models. DataLakeAnalyticsEnums + CatalogItemType</span><span class="sxs-lookup"><span data-stu-id="32a58-138">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+CatalogItemType</span></span>

### <span data-ttu-id="32a58-139">Microsoft. Azure. Commands. DataLakeAnalytics. Models. CatalogPathInstance</span><span class="sxs-lookup"><span data-stu-id="32a58-139">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span></span>

## <span data-ttu-id="32a58-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="32a58-140">OUTPUTS</span></span>

### <span data-ttu-id="32a58-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="32a58-141">System.Boolean</span></span>

## <span data-ttu-id="32a58-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="32a58-142">NOTES</span></span>

## <span data-ttu-id="32a58-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="32a58-143">RELATED LINKS</span></span>

[<span data-ttu-id="32a58-144">Get-AzDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="32a58-144">Get-AzDataLakeAnalyticsCatalogItem</span></span>](./Get-AzDataLakeAnalyticsCatalogItem.md)


