---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: ED17430D-4DAF-4B9E-937D-0F8A843DAB96
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/test-azurermdatalakeanalyticscatalogitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Test-AzureRmDataLakeAnalyticsCatalogItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Test-AzureRmDataLakeAnalyticsCatalogItem.md
ms.openlocfilehash: deb93fb17c2c739dcf377665f8b2f604a2fb4847
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429811"
---
# <span data-ttu-id="e82f9-101">Test-AzureRmDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="e82f9-101">Test-AzureRmDataLakeAnalyticsCatalogItem</span></span>

## <span data-ttu-id="e82f9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e82f9-102">SYNOPSIS</span></span>
<span data-ttu-id="e82f9-103">Verifica a existência de um item de catálogo.</span><span class="sxs-lookup"><span data-stu-id="e82f9-103">Checks for the existence of a catalog item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e82f9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e82f9-104">SYNTAX</span></span>

```
Test-AzureRmDataLakeAnalyticsCatalogItem [-Account] <String> [-ItemType] <CatalogItemType>
 [-Path] <CatalogPathInstance> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e82f9-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e82f9-105">DESCRIPTION</span></span>
<span data-ttu-id="e82f9-106">O cmdlet **Test-AzureRmDataLakeAnalyticsCatalogItem** verifica a existência de um item de catálogo do Azure data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="e82f9-106">The **Test-AzureRmDataLakeAnalyticsCatalogItem** cmdlet checks for the existence of an Azure Data Lake Analytics catalog item.</span></span>

## <span data-ttu-id="e82f9-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e82f9-107">EXAMPLES</span></span>

### <span data-ttu-id="e82f9-108">Exemplo 1: testar se existe um item de catálogo</span><span class="sxs-lookup"><span data-stu-id="e82f9-108">Example 1: Test whether a catalog item exists</span></span>
```
PS C:\>Test-AzureRmDataLakeAnalyticsCatalogItem -Account "ContosoAdlAccount" -ItemType Schema -Path "databaseName.schemaName"
```

<span data-ttu-id="e82f9-109">Esse comando testa se existe um item de esquema especificado.</span><span class="sxs-lookup"><span data-stu-id="e82f9-109">This command tests whether a specified Schema item exists.</span></span>

## <span data-ttu-id="e82f9-110">OS</span><span class="sxs-lookup"><span data-stu-id="e82f9-110">PARAMETERS</span></span>

### <span data-ttu-id="e82f9-111">-Conta</span><span class="sxs-lookup"><span data-stu-id="e82f9-111">-Account</span></span>
<span data-ttu-id="e82f9-112">Especifica o nome da conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="e82f9-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="e82f9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e82f9-113">-DefaultProfile</span></span>
<span data-ttu-id="e82f9-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="e82f9-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e82f9-115">-ItemType</span><span class="sxs-lookup"><span data-stu-id="e82f9-115">-ItemType</span></span>
<span data-ttu-id="e82f9-116">Especifica o tipo de item de catálogo do item a ser verificado.</span><span class="sxs-lookup"><span data-stu-id="e82f9-116">Specifies the catalog item type of the item to check.</span></span>
<span data-ttu-id="e82f9-117">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="e82f9-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e82f9-118">Base</span><span class="sxs-lookup"><span data-stu-id="e82f9-118">Database</span></span>
- <span data-ttu-id="e82f9-119">Esquema</span><span class="sxs-lookup"><span data-stu-id="e82f9-119">Schema</span></span>
- <span data-ttu-id="e82f9-120">Assembly</span><span class="sxs-lookup"><span data-stu-id="e82f9-120">Assembly</span></span>
- <span data-ttu-id="e82f9-121">TableName</span><span class="sxs-lookup"><span data-stu-id="e82f9-121">Table</span></span>
- <span data-ttu-id="e82f9-122">TablePartition</span><span class="sxs-lookup"><span data-stu-id="e82f9-122">TablePartition</span></span>
- <span data-ttu-id="e82f9-123">TableValuedFunction</span><span class="sxs-lookup"><span data-stu-id="e82f9-123">TableValuedFunction</span></span>
- <span data-ttu-id="e82f9-124">TableStatistics</span><span class="sxs-lookup"><span data-stu-id="e82f9-124">TableStatistics</span></span>
- <span data-ttu-id="e82f9-125">ExternalDataSource</span><span class="sxs-lookup"><span data-stu-id="e82f9-125">ExternalDataSource</span></span>
- <span data-ttu-id="e82f9-126">Ver</span><span class="sxs-lookup"><span data-stu-id="e82f9-126">View</span></span>
- <span data-ttu-id="e82f9-127">Processo</span><span class="sxs-lookup"><span data-stu-id="e82f9-127">Procedure</span></span>
- <span data-ttu-id="e82f9-128">Metade</span><span class="sxs-lookup"><span data-stu-id="e82f9-128">Secret</span></span>
- <span data-ttu-id="e82f9-129">Provedores</span><span class="sxs-lookup"><span data-stu-id="e82f9-129">Credential</span></span>
- <span data-ttu-id="e82f9-130">Tipos</span><span class="sxs-lookup"><span data-stu-id="e82f9-130">Types</span></span>

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

### <span data-ttu-id="e82f9-131">-Caminho</span><span class="sxs-lookup"><span data-stu-id="e82f9-131">-Path</span></span>
<span data-ttu-id="e82f9-132">Especifica o caminho para o item a ser buscado ou o caminho para o item pai da lista de itens a serem listados.</span><span class="sxs-lookup"><span data-stu-id="e82f9-132">Specifies the path to the item to fetch, or the path to the parent item of the items to list.</span></span>

```yaml
Type: CatalogPathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e82f9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e82f9-133">CommonParameters</span></span>
<span data-ttu-id="e82f9-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e82f9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e82f9-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e82f9-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e82f9-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e82f9-136">INPUTS</span></span>

### <span data-ttu-id="e82f9-137">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="e82f9-137">None</span></span>
<span data-ttu-id="e82f9-138">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="e82f9-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e82f9-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e82f9-139">OUTPUTS</span></span>

### <span data-ttu-id="e82f9-140">bool</span><span class="sxs-lookup"><span data-stu-id="e82f9-140">bool</span></span>
<span data-ttu-id="e82f9-141">True ou false que indica se o item de catálogo especificado existe ou não.</span><span class="sxs-lookup"><span data-stu-id="e82f9-141">True or false indicating if the specified catalog item exists or not.</span></span>

## <span data-ttu-id="e82f9-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e82f9-142">NOTES</span></span>

## <span data-ttu-id="e82f9-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e82f9-143">RELATED LINKS</span></span>

[<span data-ttu-id="e82f9-144">Get-AzureRmDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="e82f9-144">Get-AzureRmDataLakeAnalyticsCatalogItem</span></span>](./Get-AzureRmDataLakeAnalyticsCatalogItem.md)


