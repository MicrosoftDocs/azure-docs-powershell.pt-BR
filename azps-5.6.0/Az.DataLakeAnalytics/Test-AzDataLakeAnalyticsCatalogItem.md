---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: ED17430D-4DAF-4B9E-937D-0F8A843DAB96
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/test-azdatalakeanalyticscatalogitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Test-AzDataLakeAnalyticsCatalogItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Test-AzDataLakeAnalyticsCatalogItem.md
ms.openlocfilehash: 2642a310e2a318498b3d170b463ac7e366bf5818
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886053"
---
# <span data-ttu-id="ceea0-101">Test-AzDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="ceea0-101">Test-AzDataLakeAnalyticsCatalogItem</span></span>

## <span data-ttu-id="ceea0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ceea0-102">SYNOPSIS</span></span>
<span data-ttu-id="ceea0-103">Verifica a existência de um item de catálogo.</span><span class="sxs-lookup"><span data-stu-id="ceea0-103">Checks for the existence of a catalog item.</span></span>

## <span data-ttu-id="ceea0-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ceea0-104">SYNTAX</span></span>

```
Test-AzDataLakeAnalyticsCatalogItem [-Account] <String> [-ItemType] <CatalogItemType>
 [-Path] <CatalogPathInstance> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ceea0-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ceea0-105">DESCRIPTION</span></span>
<span data-ttu-id="ceea0-106">O cmdlet **Test-AzDataLakeAnalyticsCatalogItem** verifica a existência de um item de catálogo do Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="ceea0-106">The **Test-AzDataLakeAnalyticsCatalogItem** cmdlet checks for the existence of an Azure Data Lake Analytics catalog item.</span></span>

## <span data-ttu-id="ceea0-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ceea0-107">EXAMPLES</span></span>

### <span data-ttu-id="ceea0-108">Exemplo 1: Testar se existe um item de catálogo</span><span class="sxs-lookup"><span data-stu-id="ceea0-108">Example 1: Test whether a catalog item exists</span></span>
```
PS C:\>Test-AzDataLakeAnalyticsCatalogItem -Account "ContosoAdlAccount" -ItemType Schema -Path "databaseName.schemaName"
```

<span data-ttu-id="ceea0-109">Este comando testa se existe um item de Esquema especificado.</span><span class="sxs-lookup"><span data-stu-id="ceea0-109">This command tests whether a specified Schema item exists.</span></span>

## <span data-ttu-id="ceea0-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ceea0-110">PARAMETERS</span></span>

### <span data-ttu-id="ceea0-111">-Account</span><span class="sxs-lookup"><span data-stu-id="ceea0-111">-Account</span></span>
<span data-ttu-id="ceea0-112">Especifica o nome da conta do Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="ceea0-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="ceea0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ceea0-113">-DefaultProfile</span></span>
<span data-ttu-id="ceea0-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="ceea0-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ceea0-115">-ItemType</span><span class="sxs-lookup"><span data-stu-id="ceea0-115">-ItemType</span></span>
<span data-ttu-id="ceea0-116">Especifica o tipo de item de catálogo do item a ser consultado.</span><span class="sxs-lookup"><span data-stu-id="ceea0-116">Specifies the catalog item type of the item to check.</span></span>
<span data-ttu-id="ceea0-117">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="ceea0-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ceea0-118">Banco de Dados</span><span class="sxs-lookup"><span data-stu-id="ceea0-118">Database</span></span>
- <span data-ttu-id="ceea0-119">Esquema</span><span class="sxs-lookup"><span data-stu-id="ceea0-119">Schema</span></span>
- <span data-ttu-id="ceea0-120">Assembly</span><span class="sxs-lookup"><span data-stu-id="ceea0-120">Assembly</span></span>
- <span data-ttu-id="ceea0-121">Tabela</span><span class="sxs-lookup"><span data-stu-id="ceea0-121">Table</span></span>
- <span data-ttu-id="ceea0-122">TablePartition</span><span class="sxs-lookup"><span data-stu-id="ceea0-122">TablePartition</span></span>
- <span data-ttu-id="ceea0-123">TableValuedFunction</span><span class="sxs-lookup"><span data-stu-id="ceea0-123">TableValuedFunction</span></span>
- <span data-ttu-id="ceea0-124">TableStatistics</span><span class="sxs-lookup"><span data-stu-id="ceea0-124">TableStatistics</span></span>
- <span data-ttu-id="ceea0-125">ExternalDataSource</span><span class="sxs-lookup"><span data-stu-id="ceea0-125">ExternalDataSource</span></span>
- <span data-ttu-id="ceea0-126">Exibir</span><span class="sxs-lookup"><span data-stu-id="ceea0-126">View</span></span>
- <span data-ttu-id="ceea0-127">Procedimento</span><span class="sxs-lookup"><span data-stu-id="ceea0-127">Procedure</span></span>
- <span data-ttu-id="ceea0-128">Segredo</span><span class="sxs-lookup"><span data-stu-id="ceea0-128">Secret</span></span>
- <span data-ttu-id="ceea0-129">Credencial</span><span class="sxs-lookup"><span data-stu-id="ceea0-129">Credential</span></span>
- <span data-ttu-id="ceea0-130">Tipos</span><span class="sxs-lookup"><span data-stu-id="ceea0-130">Types</span></span>

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

### <span data-ttu-id="ceea0-131">-Path</span><span class="sxs-lookup"><span data-stu-id="ceea0-131">-Path</span></span>
<span data-ttu-id="ceea0-132">Especifica o caminho para o item a ser buscado ou o caminho para o item pai dos itens a listar.</span><span class="sxs-lookup"><span data-stu-id="ceea0-132">Specifies the path to the item to fetch, or the path to the parent item of the items to list.</span></span>

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

### <span data-ttu-id="ceea0-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ceea0-133">CommonParameters</span></span>
<span data-ttu-id="ceea0-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ceea0-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ceea0-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ceea0-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ceea0-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ceea0-136">INPUTS</span></span>

### <span data-ttu-id="ceea0-137">System.String</span><span class="sxs-lookup"><span data-stu-id="ceea0-137">System.String</span></span>

### <span data-ttu-id="ceea0-138">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+CatalogItemType</span><span class="sxs-lookup"><span data-stu-id="ceea0-138">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+CatalogItemType</span></span>

### <span data-ttu-id="ceea0-139">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span><span class="sxs-lookup"><span data-stu-id="ceea0-139">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span></span>

## <span data-ttu-id="ceea0-140">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ceea0-140">OUTPUTS</span></span>

### <span data-ttu-id="ceea0-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ceea0-141">System.Boolean</span></span>

## <span data-ttu-id="ceea0-142">NOTES</span><span class="sxs-lookup"><span data-stu-id="ceea0-142">NOTES</span></span>

## <span data-ttu-id="ceea0-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ceea0-143">RELATED LINKS</span></span>

[<span data-ttu-id="ceea0-144">Get-AzDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="ceea0-144">Get-AzDataLakeAnalyticsCatalogItem</span></span>](./Get-AzDataLakeAnalyticsCatalogItem.md)


