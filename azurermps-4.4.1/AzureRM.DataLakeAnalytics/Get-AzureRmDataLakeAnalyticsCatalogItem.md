---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: A6899341-1E5E-4F8B-8D5D-5923B1223628
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsCatalogItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsCatalogItem.md
ms.openlocfilehash: b12b09c686a2e0a5fcd85854551608b16cb43d3f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440676"
---
# <span data-ttu-id="c3164-101">Get-AzureRmDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="c3164-101">Get-AzureRmDataLakeAnalyticsCatalogItem</span></span>

## <span data-ttu-id="c3164-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c3164-102">SYNOPSIS</span></span>
<span data-ttu-id="c3164-103">Obtém um item de catálogo de análise de data Lake ou tipos de itens.</span><span class="sxs-lookup"><span data-stu-id="c3164-103">Gets a Data Lake Analytics catalog item or types of items.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c3164-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c3164-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeAnalyticsCatalogItem [-Account] <String> [-ItemType] <CatalogItemType>
 [[-Path] <CatalogPathInstance>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c3164-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c3164-105">DESCRIPTION</span></span>
<span data-ttu-id="c3164-106">**Get-AzureRmDataLakeAnalyticsCatalogItem** Obtém um item de catálogo especificado do Azure data Lake Analytics ou obtém itens de catálogo de um tipo especificado.</span><span class="sxs-lookup"><span data-stu-id="c3164-106">The **Get-AzureRmDataLakeAnalyticsCatalogItem** gets a specified Azure Data Lake Analytics catalog item, or gets catalog items of a specified type.</span></span>

## <span data-ttu-id="c3164-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c3164-107">EXAMPLES</span></span>

### <span data-ttu-id="c3164-108">Exemplo 1: obter um banco de dados especificado</span><span class="sxs-lookup"><span data-stu-id="c3164-108">Example 1: Get a specified database</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsCatalogItem -Account "contosoadla" -ItemType Database -Path "databaseName"
```

<span data-ttu-id="c3164-109">Este comando obtém o banco de dados especificado.</span><span class="sxs-lookup"><span data-stu-id="c3164-109">This command gets the specified database.</span></span>

### <span data-ttu-id="c3164-110">Exemplo 2: obter tabelas em um banco de dados e esquema especificado</span><span class="sxs-lookup"><span data-stu-id="c3164-110">Example 2: Get tables in a specified database and schema</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsDataSource -AccountName "contosoadla" -ItemType Table -Path "databaseName.schemaName"
```

<span data-ttu-id="c3164-111">Esse comando obtém uma lista de tabelas no banco de dados especificado.</span><span class="sxs-lookup"><span data-stu-id="c3164-111">This command gets a list of tables in the specified database.</span></span>

## <span data-ttu-id="c3164-112">OS</span><span class="sxs-lookup"><span data-stu-id="c3164-112">PARAMETERS</span></span>

### <span data-ttu-id="c3164-113">-Conta</span><span class="sxs-lookup"><span data-stu-id="c3164-113">-Account</span></span>
<span data-ttu-id="c3164-114">Especifica o nome da conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="c3164-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="c3164-115">-ItemType</span><span class="sxs-lookup"><span data-stu-id="c3164-115">-ItemType</span></span>
<span data-ttu-id="c3164-116">Especifica o tipo de item de catálogo do item que está sendo buscado ou listado.</span><span class="sxs-lookup"><span data-stu-id="c3164-116">Specifies the catalog item type of the item(s) being fetched or listed.</span></span>
<span data-ttu-id="c3164-117">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="c3164-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c3164-118">Base</span><span class="sxs-lookup"><span data-stu-id="c3164-118">Database</span></span>
- <span data-ttu-id="c3164-119">Esquema</span><span class="sxs-lookup"><span data-stu-id="c3164-119">Schema</span></span>
- <span data-ttu-id="c3164-120">Assembly</span><span class="sxs-lookup"><span data-stu-id="c3164-120">Assembly</span></span>
- <span data-ttu-id="c3164-121">TableName</span><span class="sxs-lookup"><span data-stu-id="c3164-121">Table</span></span>
- <span data-ttu-id="c3164-122">TableValuedFunction</span><span class="sxs-lookup"><span data-stu-id="c3164-122">TableValuedFunction</span></span>
- <span data-ttu-id="c3164-123">TableStatistics</span><span class="sxs-lookup"><span data-stu-id="c3164-123">TableStatistics</span></span>
- <span data-ttu-id="c3164-124">ExternalDataSource</span><span class="sxs-lookup"><span data-stu-id="c3164-124">ExternalDataSource</span></span>
- <span data-ttu-id="c3164-125">Ver</span><span class="sxs-lookup"><span data-stu-id="c3164-125">View</span></span>
- <span data-ttu-id="c3164-126">Processo</span><span class="sxs-lookup"><span data-stu-id="c3164-126">Procedure</span></span>
- <span data-ttu-id="c3164-127">Metade</span><span class="sxs-lookup"><span data-stu-id="c3164-127">Secret</span></span>
- <span data-ttu-id="c3164-128">Provedores</span><span class="sxs-lookup"><span data-stu-id="c3164-128">Credential</span></span>
- <span data-ttu-id="c3164-129">Tipos</span><span class="sxs-lookup"><span data-stu-id="c3164-129">Types</span></span>
- <span data-ttu-id="c3164-130">TablePartition</span><span class="sxs-lookup"><span data-stu-id="c3164-130">TablePartition</span></span>

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

### <span data-ttu-id="c3164-131">-Caminho</span><span class="sxs-lookup"><span data-stu-id="c3164-131">-Path</span></span>
<span data-ttu-id="c3164-132">Especifica o caminho de várias partes para o item a ser recuperado ou para o item pai da lista de itens a serem listados.</span><span class="sxs-lookup"><span data-stu-id="c3164-132">Specifies the multi-part path to the item to retrieve, or to the parent item of the items to list.</span></span>
<span data-ttu-id="c3164-133">As partes do caminho devem ser separadas por um ponto (.).</span><span class="sxs-lookup"><span data-stu-id="c3164-133">The parts of the path should be separated by a period (.).</span></span>

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

### <span data-ttu-id="c3164-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3164-134">-DefaultProfile</span></span>
<span data-ttu-id="c3164-135">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c3164-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3164-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3164-136">CommonParameters</span></span>
<span data-ttu-id="c3164-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3164-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3164-138">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3164-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3164-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c3164-139">INPUTS</span></span>

## <span data-ttu-id="c3164-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c3164-140">OUTPUTS</span></span>

### <span data-ttu-id="c3164-141">CatalogItem</span><span class="sxs-lookup"><span data-stu-id="c3164-141">CatalogItem</span></span>
<span data-ttu-id="c3164-142">O item de catálogo especificado.</span><span class="sxs-lookup"><span data-stu-id="c3164-142">The specified catalog item.</span></span>

### <span data-ttu-id="c3164-143">Programação<CatalogItem></span><span class="sxs-lookup"><span data-stu-id="c3164-143">List<CatalogItem></span></span>
<span data-ttu-id="c3164-144">A lista dos itens do catálogo especificado abaixo do contêiner correspondente.</span><span class="sxs-lookup"><span data-stu-id="c3164-144">The list of the specified catalog items underneath their corresponding container.</span></span>

## <span data-ttu-id="c3164-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c3164-145">NOTES</span></span>

## <span data-ttu-id="c3164-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c3164-146">RELATED LINKS</span></span>

[<span data-ttu-id="c3164-147">Test-AzureRmDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="c3164-147">Test-AzureRmDataLakeAnalyticsCatalogItem</span></span>](./Test-AzureRmDataLakeAnalyticsCatalogItem.md)


