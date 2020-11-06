---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: ED17430D-4DAF-4B9E-937D-0F8A843DAB96
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/test-azurermdatalakeanalyticscatalogitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Test-AzureRmDataLakeAnalyticsCatalogItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Test-AzureRmDataLakeAnalyticsCatalogItem.md
ms.openlocfilehash: 1cada55b8db886d85f88d34254c8814cdfc44665
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431998"
---
# <span data-ttu-id="29f0c-101">Test-AzureRmDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="29f0c-101">Test-AzureRmDataLakeAnalyticsCatalogItem</span></span>

## <span data-ttu-id="29f0c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="29f0c-102">SYNOPSIS</span></span>
<span data-ttu-id="29f0c-103">Verifica a existência de um item de catálogo.</span><span class="sxs-lookup"><span data-stu-id="29f0c-103">Checks for the existence of a catalog item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="29f0c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="29f0c-104">SYNTAX</span></span>

```
Test-AzureRmDataLakeAnalyticsCatalogItem [-Account] <String> [-ItemType] <CatalogItemType>
 [-Path] <CatalogPathInstance> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="29f0c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="29f0c-105">DESCRIPTION</span></span>
<span data-ttu-id="29f0c-106">O cmdlet **Test-AzureRmDataLakeAnalyticsCatalogItem** verifica a existência de um item de catálogo do Azure data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="29f0c-106">The **Test-AzureRmDataLakeAnalyticsCatalogItem** cmdlet checks for the existence of an Azure Data Lake Analytics catalog item.</span></span>

## <span data-ttu-id="29f0c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="29f0c-107">EXAMPLES</span></span>

### <span data-ttu-id="29f0c-108">Exemplo 1: testar se existe um item de catálogo</span><span class="sxs-lookup"><span data-stu-id="29f0c-108">Example 1: Test whether a catalog item exists</span></span>
```
PS C:\>Test-AzureRmDataLakeAnalyticsCatalogItem -Account "ContosoAdlAccount" -ItemType Schema -Path "databaseName.schemaName"
```

<span data-ttu-id="29f0c-109">Esse comando testa se existe um item de esquema especificado.</span><span class="sxs-lookup"><span data-stu-id="29f0c-109">This command tests whether a specified Schema item exists.</span></span>

## <span data-ttu-id="29f0c-110">OS</span><span class="sxs-lookup"><span data-stu-id="29f0c-110">PARAMETERS</span></span>

### <span data-ttu-id="29f0c-111">-Conta</span><span class="sxs-lookup"><span data-stu-id="29f0c-111">-Account</span></span>
<span data-ttu-id="29f0c-112">Especifica o nome da conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="29f0c-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="29f0c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29f0c-113">-DefaultProfile</span></span>
<span data-ttu-id="29f0c-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="29f0c-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="29f0c-115">-ItemType</span><span class="sxs-lookup"><span data-stu-id="29f0c-115">-ItemType</span></span>
<span data-ttu-id="29f0c-116">Especifica o tipo de item de catálogo do item a ser verificado.</span><span class="sxs-lookup"><span data-stu-id="29f0c-116">Specifies the catalog item type of the item to check.</span></span>
<span data-ttu-id="29f0c-117">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="29f0c-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="29f0c-118">Base</span><span class="sxs-lookup"><span data-stu-id="29f0c-118">Database</span></span>
- <span data-ttu-id="29f0c-119">Esquema</span><span class="sxs-lookup"><span data-stu-id="29f0c-119">Schema</span></span>
- <span data-ttu-id="29f0c-120">Assembly</span><span class="sxs-lookup"><span data-stu-id="29f0c-120">Assembly</span></span>
- <span data-ttu-id="29f0c-121">TableName</span><span class="sxs-lookup"><span data-stu-id="29f0c-121">Table</span></span>
- <span data-ttu-id="29f0c-122">TablePartition</span><span class="sxs-lookup"><span data-stu-id="29f0c-122">TablePartition</span></span>
- <span data-ttu-id="29f0c-123">TableValuedFunction</span><span class="sxs-lookup"><span data-stu-id="29f0c-123">TableValuedFunction</span></span>
- <span data-ttu-id="29f0c-124">TableStatistics</span><span class="sxs-lookup"><span data-stu-id="29f0c-124">TableStatistics</span></span>
- <span data-ttu-id="29f0c-125">ExternalDataSource</span><span class="sxs-lookup"><span data-stu-id="29f0c-125">ExternalDataSource</span></span>
- <span data-ttu-id="29f0c-126">Ver</span><span class="sxs-lookup"><span data-stu-id="29f0c-126">View</span></span>
- <span data-ttu-id="29f0c-127">Processo</span><span class="sxs-lookup"><span data-stu-id="29f0c-127">Procedure</span></span>
- <span data-ttu-id="29f0c-128">Metade</span><span class="sxs-lookup"><span data-stu-id="29f0c-128">Secret</span></span>
- <span data-ttu-id="29f0c-129">Provedores</span><span class="sxs-lookup"><span data-stu-id="29f0c-129">Credential</span></span>
- <span data-ttu-id="29f0c-130">Tipos</span><span class="sxs-lookup"><span data-stu-id="29f0c-130">Types</span></span>

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

### <span data-ttu-id="29f0c-131">-Caminho</span><span class="sxs-lookup"><span data-stu-id="29f0c-131">-Path</span></span>
<span data-ttu-id="29f0c-132">Especifica o caminho para o item a ser buscado ou o caminho para o item pai da lista de itens a serem listados.</span><span class="sxs-lookup"><span data-stu-id="29f0c-132">Specifies the path to the item to fetch, or the path to the parent item of the items to list.</span></span>

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

### <span data-ttu-id="29f0c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29f0c-133">CommonParameters</span></span>
<span data-ttu-id="29f0c-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29f0c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29f0c-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29f0c-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29f0c-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="29f0c-136">INPUTS</span></span>

### <span data-ttu-id="29f0c-137">System. String</span><span class="sxs-lookup"><span data-stu-id="29f0c-137">System.String</span></span>

### <span data-ttu-id="29f0c-138">Microsoft. Azure. Commands. DataLakeAnalytics. Models. DataLakeAnalyticsEnums + CatalogItemType</span><span class="sxs-lookup"><span data-stu-id="29f0c-138">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+CatalogItemType</span></span>

### <span data-ttu-id="29f0c-139">Microsoft. Azure. Commands. DataLakeAnalytics. Models. CatalogPathInstance</span><span class="sxs-lookup"><span data-stu-id="29f0c-139">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span></span>

## <span data-ttu-id="29f0c-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="29f0c-140">OUTPUTS</span></span>

### <span data-ttu-id="29f0c-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="29f0c-141">System.Boolean</span></span>

## <span data-ttu-id="29f0c-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="29f0c-142">NOTES</span></span>

## <span data-ttu-id="29f0c-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="29f0c-143">RELATED LINKS</span></span>

[<span data-ttu-id="29f0c-144">Get-AzureRmDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="29f0c-144">Get-AzureRmDataLakeAnalyticsCatalogItem</span></span>](./Get-AzureRmDataLakeAnalyticsCatalogItem.md)


