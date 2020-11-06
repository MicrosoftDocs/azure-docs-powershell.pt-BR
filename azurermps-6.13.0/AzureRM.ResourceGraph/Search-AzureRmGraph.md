---
external help file: Microsoft.Azure.Commands.ResourceGraph.dll-Help.xml
Module Name: AzureRM.ResourceGraph
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resourcegraph/search-azurermgraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ResourceGraph/Commands.ResourceGraph/help/Search-AzureRmGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ResourceGraph/Commands.ResourceGraph/help/Search-AzureRmGraph.md
ms.openlocfilehash: 900722c15d1c7a6560ba1f498b9dd0d3981f899a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432271"
---
# <span data-ttu-id="316a7-101">Search-AzureRmGraph</span><span class="sxs-lookup"><span data-stu-id="316a7-101">Search-AzureRmGraph</span></span>

## <span data-ttu-id="316a7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="316a7-102">SYNOPSIS</span></span>
<span data-ttu-id="316a7-103">Consulta os recursos gerenciados pelo Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="316a7-103">Queries the resources managed by Azure Resource Manager.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="316a7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="316a7-104">SYNTAX</span></span>

```
Search-AzureRmGraph [-Query] <String> [-Subscription <String[]>] [-First <Int32>] [-Skip <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="316a7-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="316a7-105">DESCRIPTION</span></span>
<span data-ttu-id="316a7-106">Saiba mais sobre a sintaxe da consulta aqui: https://aka.ms/resource-graph/learntoquery</span><span class="sxs-lookup"><span data-stu-id="316a7-106">Learn more about the query syntax here: https://aka.ms/resource-graph/learntoquery</span></span>

## <span data-ttu-id="316a7-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="316a7-107">EXAMPLES</span></span>

### <span data-ttu-id="316a7-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="316a7-108">Example 1</span></span>
```powershell
PS C:\> Search-AzureRmGraph "project id, name, type, location, tags" -First 3


id         : /subscriptions/1ef51df4-f8a9-4b69-9919-1ef51df4eff6/resourceGroups/Service-INT-a/providers/Microsoft.Compute/virtualMachineScaleSets/nt
name       : nt
type       : microsoft.compute/virtualmachinescalesets
location   : eastus
tags       : @{resourceType=Service Fabric; clusterName=gov-art-int-nt-a}

id         : /subscriptions/1ef51df4-f8a9-4b69-9919-1ef51df4eff6/resourceGroups/Service-INT-a/providers/Microsoft.EventGrid/topics/egtopic-1
name       : egtopic-1
type       : microsoft.eventgrid/topics
location   : westus2
tags       :
```

<span data-ttu-id="316a7-109">Consulta de recursos simples solicitando um subconjunto de campos de recurso.</span><span class="sxs-lookup"><span data-stu-id="316a7-109">Simple resources query requesting a subset of resource fields.</span></span>

### <span data-ttu-id="316a7-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="316a7-110">Example 2</span></span>
```powershell
PS C:\> Search-AzureRmGraph "project id, name, type, location | where type =~ 'Microsoft.Compute/virtualMachines' | summarize count() by location | top 3 by count_"

location      count_
--------      ------
eastus            66
westcentralus     32
westus            26
```

<span data-ttu-id="316a7-111">Uma consulta complexa sobre recursos que apresentam seleção de campo, filtragem e resumo.</span><span class="sxs-lookup"><span data-stu-id="316a7-111">A complex query on resources featuring field selection, filtering and summarizing.</span></span>

## <span data-ttu-id="316a7-112">OS</span><span class="sxs-lookup"><span data-stu-id="316a7-112">PARAMETERS</span></span>

### <span data-ttu-id="316a7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="316a7-113">-DefaultProfile</span></span>
<span data-ttu-id="316a7-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="316a7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="316a7-115">-Consulta</span><span class="sxs-lookup"><span data-stu-id="316a7-115">-Query</span></span>
<span data-ttu-id="316a7-116">Consulta de gráfico de recursos.</span><span class="sxs-lookup"><span data-stu-id="316a7-116">Resource Graph query.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="316a7-117">-Assinatura</span><span class="sxs-lookup"><span data-stu-id="316a7-117">-Subscription</span></span>
<span data-ttu-id="316a7-118">Assinatura (s) para executar a consulta.</span><span class="sxs-lookup"><span data-stu-id="316a7-118">Subscription(s) to run query against.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="316a7-119">-Skip</span><span class="sxs-lookup"><span data-stu-id="316a7-119">-Skip</span></span>
<span data-ttu-id="316a7-120">Ignora os primeiros N objetos e, em seguida, obtém os objetos restantes.</span><span class="sxs-lookup"><span data-stu-id="316a7-120">Ignores the first N objects and then gets the remaining objects.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="316a7-121">-Primeiro</span><span class="sxs-lookup"><span data-stu-id="316a7-121">-First</span></span>
<span data-ttu-id="316a7-122">O número máximo de objetos a serem retornados.</span><span class="sxs-lookup"><span data-stu-id="316a7-122">The maximum number of objects to return.</span></span> <span data-ttu-id="316a7-123">Valores permitidos: 1-5000.</span><span class="sxs-lookup"><span data-stu-id="316a7-123">Allowed values: 1-5000.</span></span>
<span data-ttu-id="316a7-124">O valor padrão é 100.</span><span class="sxs-lookup"><span data-stu-id="316a7-124">Default value is 100.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="316a7-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="316a7-125">CommonParameters</span></span>
<span data-ttu-id="316a7-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="316a7-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="316a7-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="316a7-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="316a7-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="316a7-128">INPUTS</span></span>

### <span data-ttu-id="316a7-129">System. String</span><span class="sxs-lookup"><span data-stu-id="316a7-129">System.String</span></span>

## <span data-ttu-id="316a7-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="316a7-130">OUTPUTS</span></span>

### <span data-ttu-id="316a7-131">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="316a7-131">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="316a7-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="316a7-132">NOTES</span></span>

## <span data-ttu-id="316a7-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="316a7-133">RELATED LINKS</span></span>
