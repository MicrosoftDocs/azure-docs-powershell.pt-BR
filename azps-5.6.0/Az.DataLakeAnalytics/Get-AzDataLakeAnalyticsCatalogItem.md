---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: A6899341-1E5E-4F8B-8D5D-5923B1223628
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticscatalogitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsCatalogItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsCatalogItem.md
ms.openlocfilehash: 738820c4c06fd32862def36ec76983968e99efb1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891437"
---
# <span data-ttu-id="839b1-101">Get-AzDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="839b1-101">Get-AzDataLakeAnalyticsCatalogItem</span></span>

## <span data-ttu-id="839b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="839b1-102">SYNOPSIS</span></span>
<span data-ttu-id="839b1-103">Obtém um item de catálogo do Data Lake Analytics ou tipos de itens.</span><span class="sxs-lookup"><span data-stu-id="839b1-103">Gets a Data Lake Analytics catalog item or types of items.</span></span>

## <span data-ttu-id="839b1-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="839b1-104">SYNTAX</span></span>

```
Get-AzDataLakeAnalyticsCatalogItem [-Account] <String> [-ItemType] <CatalogItemType>
 [[-Path] <CatalogPathInstance>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="839b1-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="839b1-105">DESCRIPTION</span></span>
<span data-ttu-id="839b1-106">**Get-AzDataLakeAnalyticsCatalogItem** obtém um item de catálogo do Azure Data Lake Analytics especificado ou obtém itens de catálogo de um tipo especificado.</span><span class="sxs-lookup"><span data-stu-id="839b1-106">The **Get-AzDataLakeAnalyticsCatalogItem** gets a specified Azure Data Lake Analytics catalog item, or gets catalog items of a specified type.</span></span>

## <span data-ttu-id="839b1-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="839b1-107">EXAMPLES</span></span>

### <span data-ttu-id="839b1-108">Exemplo 1: Obter um banco de dados especificado</span><span class="sxs-lookup"><span data-stu-id="839b1-108">Example 1: Get a specified database</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsCatalogItem -Account "contosoadla" -ItemType Database -Path "databaseName"
```

<span data-ttu-id="839b1-109">Este comando obtém o banco de dados especificado.</span><span class="sxs-lookup"><span data-stu-id="839b1-109">This command gets the specified database.</span></span>

### <span data-ttu-id="839b1-110">Exemplo 2: Obter tabelas em um banco de dados e esquema especificados</span><span class="sxs-lookup"><span data-stu-id="839b1-110">Example 2: Get tables in a specified database and schema</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsDataSource -AccountName "contosoadla" -ItemType Table -Path "databaseName.schemaName"
```

<span data-ttu-id="839b1-111">Este comando obtém uma lista de tabelas no banco de dados especificado.</span><span class="sxs-lookup"><span data-stu-id="839b1-111">This command gets a list of tables in the specified database.</span></span>

## <span data-ttu-id="839b1-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="839b1-112">PARAMETERS</span></span>

### <span data-ttu-id="839b1-113">-Account</span><span class="sxs-lookup"><span data-stu-id="839b1-113">-Account</span></span>
<span data-ttu-id="839b1-114">Especifica o nome da conta do Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="839b1-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="839b1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="839b1-115">-DefaultProfile</span></span>
<span data-ttu-id="839b1-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="839b1-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="839b1-117">-ItemType</span><span class="sxs-lookup"><span data-stu-id="839b1-117">-ItemType</span></span>
<span data-ttu-id="839b1-118">Especifica o tipo de item de catálogo dos itens que estão sendo buscados ou listados.</span><span class="sxs-lookup"><span data-stu-id="839b1-118">Specifies the catalog item type of the item(s) being fetched or listed.</span></span>
<span data-ttu-id="839b1-119">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="839b1-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="839b1-120">Banco de Dados</span><span class="sxs-lookup"><span data-stu-id="839b1-120">Database</span></span>
- <span data-ttu-id="839b1-121">Esquema</span><span class="sxs-lookup"><span data-stu-id="839b1-121">Schema</span></span>
- <span data-ttu-id="839b1-122">Assembly</span><span class="sxs-lookup"><span data-stu-id="839b1-122">Assembly</span></span>
- <span data-ttu-id="839b1-123">Tabela</span><span class="sxs-lookup"><span data-stu-id="839b1-123">Table</span></span>
- <span data-ttu-id="839b1-124">TableValuedFunction</span><span class="sxs-lookup"><span data-stu-id="839b1-124">TableValuedFunction</span></span>
- <span data-ttu-id="839b1-125">TableStatistics</span><span class="sxs-lookup"><span data-stu-id="839b1-125">TableStatistics</span></span>
- <span data-ttu-id="839b1-126">ExternalDataSource</span><span class="sxs-lookup"><span data-stu-id="839b1-126">ExternalDataSource</span></span>
- <span data-ttu-id="839b1-127">Exibir</span><span class="sxs-lookup"><span data-stu-id="839b1-127">View</span></span>
- <span data-ttu-id="839b1-128">Procedimento</span><span class="sxs-lookup"><span data-stu-id="839b1-128">Procedure</span></span>
- <span data-ttu-id="839b1-129">Segredo</span><span class="sxs-lookup"><span data-stu-id="839b1-129">Secret</span></span>
- <span data-ttu-id="839b1-130">Credencial</span><span class="sxs-lookup"><span data-stu-id="839b1-130">Credential</span></span>
- <span data-ttu-id="839b1-131">Tipos</span><span class="sxs-lookup"><span data-stu-id="839b1-131">Types</span></span>
- <span data-ttu-id="839b1-132">TablePartition</span><span class="sxs-lookup"><span data-stu-id="839b1-132">TablePartition</span></span>

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

### <span data-ttu-id="839b1-133">-Path</span><span class="sxs-lookup"><span data-stu-id="839b1-133">-Path</span></span>
<span data-ttu-id="839b1-134">Especifica o caminho de várias partes para o item a ser recuperado ou para o item pai dos itens a listar.</span><span class="sxs-lookup"><span data-stu-id="839b1-134">Specifies the multi-part path to the item to retrieve, or to the parent item of the items to list.</span></span>
<span data-ttu-id="839b1-135">As partes do caminho devem ser separadas por um ponto (.).</span><span class="sxs-lookup"><span data-stu-id="839b1-135">The parts of the path should be separated by a period (.).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="839b1-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="839b1-136">CommonParameters</span></span>
<span data-ttu-id="839b1-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="839b1-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="839b1-138">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="839b1-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="839b1-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="839b1-139">INPUTS</span></span>

### <span data-ttu-id="839b1-140">System.String</span><span class="sxs-lookup"><span data-stu-id="839b1-140">System.String</span></span>

### <span data-ttu-id="839b1-141">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+CatalogItemType</span><span class="sxs-lookup"><span data-stu-id="839b1-141">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+CatalogItemType</span></span>

### <span data-ttu-id="839b1-142">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span><span class="sxs-lookup"><span data-stu-id="839b1-142">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span></span>

## <span data-ttu-id="839b1-143">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="839b1-143">OUTPUTS</span></span>

### <span data-ttu-id="839b1-144">Microsoft.Azure.Management.DataLake.Analytics.Models.CatalogItem</span><span class="sxs-lookup"><span data-stu-id="839b1-144">Microsoft.Azure.Management.DataLake.Analytics.Models.CatalogItem</span></span>

## <span data-ttu-id="839b1-145">NOTES</span><span class="sxs-lookup"><span data-stu-id="839b1-145">NOTES</span></span>

## <span data-ttu-id="839b1-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="839b1-146">RELATED LINKS</span></span>

[<span data-ttu-id="839b1-147">Test-AzDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="839b1-147">Test-AzDataLakeAnalyticsCatalogItem</span></span>](./Test-AzDataLakeAnalyticsCatalogItem.md)


