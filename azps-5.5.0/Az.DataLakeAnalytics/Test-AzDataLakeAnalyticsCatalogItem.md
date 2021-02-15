---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: ED17430D-4DAF-4B9E-937D-0F8A843DAB96
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/test-azdatalakeanalyticscatalogitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Test-AzDataLakeAnalyticsCatalogItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Test-AzDataLakeAnalyticsCatalogItem.md
ms.openlocfilehash: 2879923b38b6813213fe6819f84fa55a593f6930
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115396"
---
# <span data-ttu-id="4eb47-101">Test-AzDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="4eb47-101">Test-AzDataLakeAnalyticsCatalogItem</span></span>

## <span data-ttu-id="4eb47-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4eb47-102">SYNOPSIS</span></span>
<span data-ttu-id="4eb47-103">Verifica a existência de um item de catálogo.</span><span class="sxs-lookup"><span data-stu-id="4eb47-103">Checks for the existence of a catalog item.</span></span>

## <span data-ttu-id="4eb47-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4eb47-104">SYNTAX</span></span>

```
Test-AzDataLakeAnalyticsCatalogItem [-Account] <String> [-ItemType] <CatalogItemType>
 [-Path] <CatalogPathInstance> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4eb47-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="4eb47-105">DESCRIPTION</span></span>
<span data-ttu-id="4eb47-106">O cmdlet **Test-AzDataLakeAnalyticsCatalogItem** verifica a existência de um item de catálogo do Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="4eb47-106">The **Test-AzDataLakeAnalyticsCatalogItem** cmdlet checks for the existence of an Azure Data Lake Analytics catalog item.</span></span>

## <span data-ttu-id="4eb47-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4eb47-107">EXAMPLES</span></span>

### <span data-ttu-id="4eb47-108">Exemplo 1: Testar se um item de catálogo existe</span><span class="sxs-lookup"><span data-stu-id="4eb47-108">Example 1: Test whether a catalog item exists</span></span>
```
PS C:\>Test-AzDataLakeAnalyticsCatalogItem -Account "ContosoAdlAccount" -ItemType Schema -Path "databaseName.schemaName"
```

<span data-ttu-id="4eb47-109">Esse comando testa se existe um item de Esquema especificado.</span><span class="sxs-lookup"><span data-stu-id="4eb47-109">This command tests whether a specified Schema item exists.</span></span>

## <span data-ttu-id="4eb47-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4eb47-110">PARAMETERS</span></span>

### <span data-ttu-id="4eb47-111">-Conta</span><span class="sxs-lookup"><span data-stu-id="4eb47-111">-Account</span></span>
<span data-ttu-id="4eb47-112">Especifica o nome da conta do Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="4eb47-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="4eb47-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4eb47-113">-DefaultProfile</span></span>
<span data-ttu-id="4eb47-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="4eb47-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4eb47-115">-ItemType</span><span class="sxs-lookup"><span data-stu-id="4eb47-115">-ItemType</span></span>
<span data-ttu-id="4eb47-116">Especifica o tipo de item de catálogo do item a ser consultado.</span><span class="sxs-lookup"><span data-stu-id="4eb47-116">Specifies the catalog item type of the item to check.</span></span>
<span data-ttu-id="4eb47-117">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="4eb47-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4eb47-118">Database</span><span class="sxs-lookup"><span data-stu-id="4eb47-118">Database</span></span>
- <span data-ttu-id="4eb47-119">Esquema</span><span class="sxs-lookup"><span data-stu-id="4eb47-119">Schema</span></span>
- <span data-ttu-id="4eb47-120">Assembly</span><span class="sxs-lookup"><span data-stu-id="4eb47-120">Assembly</span></span>
- <span data-ttu-id="4eb47-121">Tabela</span><span class="sxs-lookup"><span data-stu-id="4eb47-121">Table</span></span>
- <span data-ttu-id="4eb47-122">TablePartition</span><span class="sxs-lookup"><span data-stu-id="4eb47-122">TablePartition</span></span>
- <span data-ttu-id="4eb47-123">TableValuedFunction</span><span class="sxs-lookup"><span data-stu-id="4eb47-123">TableValuedFunction</span></span>
- <span data-ttu-id="4eb47-124">TableStatistics</span><span class="sxs-lookup"><span data-stu-id="4eb47-124">TableStatistics</span></span>
- <span data-ttu-id="4eb47-125">ExternalDataSource</span><span class="sxs-lookup"><span data-stu-id="4eb47-125">ExternalDataSource</span></span>
- <span data-ttu-id="4eb47-126">Ver</span><span class="sxs-lookup"><span data-stu-id="4eb47-126">View</span></span>
- <span data-ttu-id="4eb47-127">Procedimento</span><span class="sxs-lookup"><span data-stu-id="4eb47-127">Procedure</span></span>
- <span data-ttu-id="4eb47-128">Segredo</span><span class="sxs-lookup"><span data-stu-id="4eb47-128">Secret</span></span>
- <span data-ttu-id="4eb47-129">Credencial</span><span class="sxs-lookup"><span data-stu-id="4eb47-129">Credential</span></span>
- <span data-ttu-id="4eb47-130">Tipos</span><span class="sxs-lookup"><span data-stu-id="4eb47-130">Types</span></span>

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

### <span data-ttu-id="4eb47-131">-Caminho</span><span class="sxs-lookup"><span data-stu-id="4eb47-131">-Path</span></span>
<span data-ttu-id="4eb47-132">Especifica o caminho para o item a ser buscado ou o caminho para o item pai dos itens a lista.</span><span class="sxs-lookup"><span data-stu-id="4eb47-132">Specifies the path to the item to fetch, or the path to the parent item of the items to list.</span></span>

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

### <span data-ttu-id="4eb47-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4eb47-133">CommonParameters</span></span>
<span data-ttu-id="4eb47-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4eb47-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4eb47-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4eb47-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4eb47-136">Entradas</span><span class="sxs-lookup"><span data-stu-id="4eb47-136">INPUTS</span></span>

### <span data-ttu-id="4eb47-137">System.String</span><span class="sxs-lookup"><span data-stu-id="4eb47-137">System.String</span></span>

### <span data-ttu-id="4eb47-138">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+CatalogItemType</span><span class="sxs-lookup"><span data-stu-id="4eb47-138">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+CatalogItemType</span></span>

### <span data-ttu-id="4eb47-139">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span><span class="sxs-lookup"><span data-stu-id="4eb47-139">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span></span>

## <span data-ttu-id="4eb47-140">Saídas</span><span class="sxs-lookup"><span data-stu-id="4eb47-140">OUTPUTS</span></span>

### <span data-ttu-id="4eb47-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4eb47-141">System.Boolean</span></span>

## <span data-ttu-id="4eb47-142">Notas</span><span class="sxs-lookup"><span data-stu-id="4eb47-142">NOTES</span></span>

## <span data-ttu-id="4eb47-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4eb47-143">RELATED LINKS</span></span>

[<span data-ttu-id="4eb47-144">Get-AzDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="4eb47-144">Get-AzDataLakeAnalyticsCatalogItem</span></span>](./Get-AzDataLakeAnalyticsCatalogItem.md)


