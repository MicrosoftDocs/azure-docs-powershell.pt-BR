---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: A6899341-1E5E-4F8B-8D5D-5923B1223628
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticscatalogitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsCatalogItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsCatalogItem.md
ms.openlocfilehash: fb0e73d338c54b93626ee3a5ee78bbbe4adca884
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98264056"
---
# <span data-ttu-id="a674a-101">Get-AzDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="a674a-101">Get-AzDataLakeAnalyticsCatalogItem</span></span>

## <span data-ttu-id="a674a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a674a-102">SYNOPSIS</span></span>
<span data-ttu-id="a674a-103">Obtém um item de catálogo de análise de data Lake ou tipos de itens.</span><span class="sxs-lookup"><span data-stu-id="a674a-103">Gets a Data Lake Analytics catalog item or types of items.</span></span>

## <span data-ttu-id="a674a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a674a-104">SYNTAX</span></span>

```
Get-AzDataLakeAnalyticsCatalogItem [-Account] <String> [-ItemType] <CatalogItemType>
 [[-Path] <CatalogPathInstance>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a674a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a674a-105">DESCRIPTION</span></span>
<span data-ttu-id="a674a-106">**Get-AzDataLakeAnalyticsCatalogItem** Obtém um item de catálogo especificado do Azure data Lake Analytics ou obtém itens de catálogo de um tipo especificado.</span><span class="sxs-lookup"><span data-stu-id="a674a-106">The **Get-AzDataLakeAnalyticsCatalogItem** gets a specified Azure Data Lake Analytics catalog item, or gets catalog items of a specified type.</span></span>

## <span data-ttu-id="a674a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a674a-107">EXAMPLES</span></span>

### <span data-ttu-id="a674a-108">Exemplo 1: obter um banco de dados especificado</span><span class="sxs-lookup"><span data-stu-id="a674a-108">Example 1: Get a specified database</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsCatalogItem -Account "contosoadla" -ItemType Database -Path "databaseName"
```

<span data-ttu-id="a674a-109">Este comando obtém o banco de dados especificado.</span><span class="sxs-lookup"><span data-stu-id="a674a-109">This command gets the specified database.</span></span>

### <span data-ttu-id="a674a-110">Exemplo 2: obter tabelas em um banco de dados e esquema especificado</span><span class="sxs-lookup"><span data-stu-id="a674a-110">Example 2: Get tables in a specified database and schema</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsDataSource -AccountName "contosoadla" -ItemType Table -Path "databaseName.schemaName"
```

<span data-ttu-id="a674a-111">Esse comando obtém uma lista de tabelas no banco de dados especificado.</span><span class="sxs-lookup"><span data-stu-id="a674a-111">This command gets a list of tables in the specified database.</span></span>

## <span data-ttu-id="a674a-112">OS</span><span class="sxs-lookup"><span data-stu-id="a674a-112">PARAMETERS</span></span>

### <span data-ttu-id="a674a-113">-Conta</span><span class="sxs-lookup"><span data-stu-id="a674a-113">-Account</span></span>
<span data-ttu-id="a674a-114">Especifica o nome da conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="a674a-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="a674a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a674a-115">-DefaultProfile</span></span>
<span data-ttu-id="a674a-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="a674a-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a674a-117">-ItemType</span><span class="sxs-lookup"><span data-stu-id="a674a-117">-ItemType</span></span>
<span data-ttu-id="a674a-118">Especifica o tipo de item de catálogo do item que está sendo buscado ou listado.</span><span class="sxs-lookup"><span data-stu-id="a674a-118">Specifies the catalog item type of the item(s) being fetched or listed.</span></span>
<span data-ttu-id="a674a-119">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="a674a-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a674a-120">Base</span><span class="sxs-lookup"><span data-stu-id="a674a-120">Database</span></span>
- <span data-ttu-id="a674a-121">Esquema</span><span class="sxs-lookup"><span data-stu-id="a674a-121">Schema</span></span>
- <span data-ttu-id="a674a-122">Assembly</span><span class="sxs-lookup"><span data-stu-id="a674a-122">Assembly</span></span>
- <span data-ttu-id="a674a-123">TableName</span><span class="sxs-lookup"><span data-stu-id="a674a-123">Table</span></span>
- <span data-ttu-id="a674a-124">TableValuedFunction</span><span class="sxs-lookup"><span data-stu-id="a674a-124">TableValuedFunction</span></span>
- <span data-ttu-id="a674a-125">TableStatistics</span><span class="sxs-lookup"><span data-stu-id="a674a-125">TableStatistics</span></span>
- <span data-ttu-id="a674a-126">ExternalDataSource</span><span class="sxs-lookup"><span data-stu-id="a674a-126">ExternalDataSource</span></span>
- <span data-ttu-id="a674a-127">Ver</span><span class="sxs-lookup"><span data-stu-id="a674a-127">View</span></span>
- <span data-ttu-id="a674a-128">Processo</span><span class="sxs-lookup"><span data-stu-id="a674a-128">Procedure</span></span>
- <span data-ttu-id="a674a-129">Metade</span><span class="sxs-lookup"><span data-stu-id="a674a-129">Secret</span></span>
- <span data-ttu-id="a674a-130">Provedores</span><span class="sxs-lookup"><span data-stu-id="a674a-130">Credential</span></span>
- <span data-ttu-id="a674a-131">Tipos</span><span class="sxs-lookup"><span data-stu-id="a674a-131">Types</span></span>
- <span data-ttu-id="a674a-132">TablePartition</span><span class="sxs-lookup"><span data-stu-id="a674a-132">TablePartition</span></span>

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

### <span data-ttu-id="a674a-133">-Caminho</span><span class="sxs-lookup"><span data-stu-id="a674a-133">-Path</span></span>
<span data-ttu-id="a674a-134">Especifica o caminho de várias partes para o item a ser recuperado ou para o item pai da lista de itens a serem listados.</span><span class="sxs-lookup"><span data-stu-id="a674a-134">Specifies the multi-part path to the item to retrieve, or to the parent item of the items to list.</span></span>
<span data-ttu-id="a674a-135">As partes do caminho devem ser separadas por um ponto (.).</span><span class="sxs-lookup"><span data-stu-id="a674a-135">The parts of the path should be separated by a period (.).</span></span>

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

### <span data-ttu-id="a674a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a674a-136">CommonParameters</span></span>
<span data-ttu-id="a674a-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a674a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a674a-138">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a674a-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a674a-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a674a-139">INPUTS</span></span>

### <span data-ttu-id="a674a-140">System. String</span><span class="sxs-lookup"><span data-stu-id="a674a-140">System.String</span></span>

### <span data-ttu-id="a674a-141">Microsoft. Azure. Commands. DataLakeAnalytics. Models. DataLakeAnalyticsEnums + CatalogItemType</span><span class="sxs-lookup"><span data-stu-id="a674a-141">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+CatalogItemType</span></span>

### <span data-ttu-id="a674a-142">Microsoft. Azure. Commands. DataLakeAnalytics. Models. CatalogPathInstance</span><span class="sxs-lookup"><span data-stu-id="a674a-142">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span></span>

## <span data-ttu-id="a674a-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a674a-143">OUTPUTS</span></span>

### <span data-ttu-id="a674a-144">Microsoft. Azure. Management. datalake. Analytics. Models. CatalogItem</span><span class="sxs-lookup"><span data-stu-id="a674a-144">Microsoft.Azure.Management.DataLake.Analytics.Models.CatalogItem</span></span>

## <span data-ttu-id="a674a-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a674a-145">NOTES</span></span>

## <span data-ttu-id="a674a-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a674a-146">RELATED LINKS</span></span>

[<span data-ttu-id="a674a-147">Test-AzDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="a674a-147">Test-AzDataLakeAnalyticsCatalogItem</span></span>](./Test-AzDataLakeAnalyticsCatalogItem.md)


