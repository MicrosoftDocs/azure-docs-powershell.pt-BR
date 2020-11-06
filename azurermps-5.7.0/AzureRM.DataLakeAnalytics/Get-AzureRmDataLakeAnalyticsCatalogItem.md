---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: A6899341-1E5E-4F8B-8D5D-5923B1223628
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/get-azurermdatalakeanalyticscatalogitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsCatalogItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsCatalogItem.md
ms.openlocfilehash: b7a608e4bed6e68f06660f10f2ef72effb6ad18b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602540"
---
# <span data-ttu-id="56e4c-101">Get-AzureRmDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="56e4c-101">Get-AzureRmDataLakeAnalyticsCatalogItem</span></span>

## <span data-ttu-id="56e4c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="56e4c-102">SYNOPSIS</span></span>
<span data-ttu-id="56e4c-103">Obtém um item de catálogo de análise de data Lake ou tipos de itens.</span><span class="sxs-lookup"><span data-stu-id="56e4c-103">Gets a Data Lake Analytics catalog item or types of items.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="56e4c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="56e4c-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeAnalyticsCatalogItem [-Account] <String> [-ItemType] <CatalogItemType>
 [[-Path] <CatalogPathInstance>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="56e4c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="56e4c-105">DESCRIPTION</span></span>
<span data-ttu-id="56e4c-106">**Get-AzureRmDataLakeAnalyticsCatalogItem** Obtém um item de catálogo especificado do Azure data Lake Analytics ou obtém itens de catálogo de um tipo especificado.</span><span class="sxs-lookup"><span data-stu-id="56e4c-106">The **Get-AzureRmDataLakeAnalyticsCatalogItem** gets a specified Azure Data Lake Analytics catalog item, or gets catalog items of a specified type.</span></span>

## <span data-ttu-id="56e4c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="56e4c-107">EXAMPLES</span></span>

### <span data-ttu-id="56e4c-108">Exemplo 1: obter um banco de dados especificado</span><span class="sxs-lookup"><span data-stu-id="56e4c-108">Example 1: Get a specified database</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsCatalogItem -Account "contosoadla" -ItemType Database -Path "databaseName"
```

<span data-ttu-id="56e4c-109">Este comando obtém o banco de dados especificado.</span><span class="sxs-lookup"><span data-stu-id="56e4c-109">This command gets the specified database.</span></span>

### <span data-ttu-id="56e4c-110">Exemplo 2: obter tabelas em um banco de dados e esquema especificado</span><span class="sxs-lookup"><span data-stu-id="56e4c-110">Example 2: Get tables in a specified database and schema</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsDataSource -AccountName "contosoadla" -ItemType Table -Path "databaseName.schemaName"
```

<span data-ttu-id="56e4c-111">Esse comando obtém uma lista de tabelas no banco de dados especificado.</span><span class="sxs-lookup"><span data-stu-id="56e4c-111">This command gets a list of tables in the specified database.</span></span>

## <span data-ttu-id="56e4c-112">OS</span><span class="sxs-lookup"><span data-stu-id="56e4c-112">PARAMETERS</span></span>

### <span data-ttu-id="56e4c-113">-Conta</span><span class="sxs-lookup"><span data-stu-id="56e4c-113">-Account</span></span>
<span data-ttu-id="56e4c-114">Especifica o nome da conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="56e4c-114">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56e4c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56e4c-115">-DefaultProfile</span></span>
<span data-ttu-id="56e4c-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="56e4c-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56e4c-117">-ItemType</span><span class="sxs-lookup"><span data-stu-id="56e4c-117">-ItemType</span></span>
<span data-ttu-id="56e4c-118">Especifica o tipo de item de catálogo do item que está sendo buscado ou listado.</span><span class="sxs-lookup"><span data-stu-id="56e4c-118">Specifies the catalog item type of the item(s) being fetched or listed.</span></span>
<span data-ttu-id="56e4c-119">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="56e4c-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="56e4c-120">Base</span><span class="sxs-lookup"><span data-stu-id="56e4c-120">Database</span></span>
- <span data-ttu-id="56e4c-121">Esquema</span><span class="sxs-lookup"><span data-stu-id="56e4c-121">Schema</span></span>
- <span data-ttu-id="56e4c-122">Assembly</span><span class="sxs-lookup"><span data-stu-id="56e4c-122">Assembly</span></span>
- <span data-ttu-id="56e4c-123">TableName</span><span class="sxs-lookup"><span data-stu-id="56e4c-123">Table</span></span>
- <span data-ttu-id="56e4c-124">TableValuedFunction</span><span class="sxs-lookup"><span data-stu-id="56e4c-124">TableValuedFunction</span></span>
- <span data-ttu-id="56e4c-125">TableStatistics</span><span class="sxs-lookup"><span data-stu-id="56e4c-125">TableStatistics</span></span>
- <span data-ttu-id="56e4c-126">ExternalDataSource</span><span class="sxs-lookup"><span data-stu-id="56e4c-126">ExternalDataSource</span></span>
- <span data-ttu-id="56e4c-127">Ver</span><span class="sxs-lookup"><span data-stu-id="56e4c-127">View</span></span>
- <span data-ttu-id="56e4c-128">Processo</span><span class="sxs-lookup"><span data-stu-id="56e4c-128">Procedure</span></span>
- <span data-ttu-id="56e4c-129">Metade</span><span class="sxs-lookup"><span data-stu-id="56e4c-129">Secret</span></span>
- <span data-ttu-id="56e4c-130">Provedores</span><span class="sxs-lookup"><span data-stu-id="56e4c-130">Credential</span></span>
- <span data-ttu-id="56e4c-131">Tipos</span><span class="sxs-lookup"><span data-stu-id="56e4c-131">Types</span></span>
- <span data-ttu-id="56e4c-132">TablePartition</span><span class="sxs-lookup"><span data-stu-id="56e4c-132">TablePartition</span></span>

```yaml
Type: CatalogItemType
Parameter Sets: (All)
Aliases: 
Accepted values: Database, Schema, Assembly, Table, TablePartition, TableValuedFunction, TableStatistics, ExternalDataSource, View, Procedure, Secret, Credential, Types, Package

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56e4c-133">-Caminho</span><span class="sxs-lookup"><span data-stu-id="56e4c-133">-Path</span></span>
<span data-ttu-id="56e4c-134">Especifica o caminho de várias partes para o item a ser recuperado ou para o item pai da lista de itens a serem listados.</span><span class="sxs-lookup"><span data-stu-id="56e4c-134">Specifies the multi-part path to the item to retrieve, or to the parent item of the items to list.</span></span>
<span data-ttu-id="56e4c-135">As partes do caminho devem ser separadas por um ponto (.).</span><span class="sxs-lookup"><span data-stu-id="56e4c-135">The parts of the path should be separated by a period (.).</span></span>

```yaml
Type: CatalogPathInstance
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56e4c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56e4c-136">CommonParameters</span></span>
<span data-ttu-id="56e4c-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56e4c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56e4c-138">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56e4c-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56e4c-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="56e4c-139">INPUTS</span></span>

### <span data-ttu-id="56e4c-140">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="56e4c-140">None</span></span>
<span data-ttu-id="56e4c-141">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="56e4c-141">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="56e4c-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="56e4c-142">OUTPUTS</span></span>

### <span data-ttu-id="56e4c-143">CatalogItem</span><span class="sxs-lookup"><span data-stu-id="56e4c-143">CatalogItem</span></span>
<span data-ttu-id="56e4c-144">O item de catálogo especificado.</span><span class="sxs-lookup"><span data-stu-id="56e4c-144">The specified catalog item.</span></span>

### <span data-ttu-id="56e4c-145">Programação<CatalogItem></span><span class="sxs-lookup"><span data-stu-id="56e4c-145">List<CatalogItem></span></span>
<span data-ttu-id="56e4c-146">A lista dos itens do catálogo especificado abaixo do contêiner correspondente.</span><span class="sxs-lookup"><span data-stu-id="56e4c-146">The list of the specified catalog items underneath their corresponding container.</span></span>

## <span data-ttu-id="56e4c-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="56e4c-147">NOTES</span></span>

## <span data-ttu-id="56e4c-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="56e4c-148">RELATED LINKS</span></span>

[<span data-ttu-id="56e4c-149">Test-AzureRmDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="56e4c-149">Test-AzureRmDataLakeAnalyticsCatalogItem</span></span>](./Test-AzureRmDataLakeAnalyticsCatalogItem.md)


