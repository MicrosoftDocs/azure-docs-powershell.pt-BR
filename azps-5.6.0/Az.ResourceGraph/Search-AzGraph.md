---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.dll-Help.xml
Module Name: Az.ResourceGraph
online version: https://docs.microsoft.com/powershell/module/az.resourcegraph/search-azgraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Search-AzGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Search-AzGraph.md
ms.openlocfilehash: e96d4fa13dc1b479c37b56cb3887b6d519df24f1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891665"
---
# <span data-ttu-id="3ac5e-101">Search-AzGraph</span><span class="sxs-lookup"><span data-stu-id="3ac5e-101">Search-AzGraph</span></span>

## <span data-ttu-id="3ac5e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ac5e-102">SYNOPSIS</span></span>
<span data-ttu-id="3ac5e-103">Consulta os recursos gerenciados pelo Gerenciador de Recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="3ac5e-103">Queries the resources managed by Azure Resource Manager.</span></span>

## <span data-ttu-id="3ac5e-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="3ac5e-104">SYNTAX</span></span>

```
Search-AzGraph [-Query] <String> [-Subscription <String[]>] [-First <Int32>] [-Skip <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3ac5e-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="3ac5e-105">DESCRIPTION</span></span>
<span data-ttu-id="3ac5e-106">Saiba mais sobre a sintaxe de consulta aqui: https://aka.ms/resource-graph/learntoquery</span><span class="sxs-lookup"><span data-stu-id="3ac5e-106">Learn more about the query syntax here: https://aka.ms/resource-graph/learntoquery</span></span>

## <span data-ttu-id="3ac5e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3ac5e-107">EXAMPLES</span></span>

### <span data-ttu-id="3ac5e-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3ac5e-108">Example 1</span></span>
```powershell
PS C:\> Search-AzGraph "project id, name, type, location, tags" -First 3


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

<span data-ttu-id="3ac5e-109">Consulta de recursos simples solicitando um subconjunto de campos de recursos.</span><span class="sxs-lookup"><span data-stu-id="3ac5e-109">Simple resources query requesting a subset of resource fields.</span></span>

### <span data-ttu-id="3ac5e-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="3ac5e-110">Example 2</span></span>
```powershell
PS C:\> Search-AzGraph "project id, name, type, location | where type =~ 'Microsoft.Compute/virtualMachines' | summarize count() by location | top 3 by count_"

location      count_
--------      ------
eastus            66
westcentralus     32
westus            26
```

<span data-ttu-id="3ac5e-111">Uma consulta complexa sobre recursos com seleção de campo, filtragem e resumo.</span><span class="sxs-lookup"><span data-stu-id="3ac5e-111">A complex query on resources featuring field selection, filtering and summarizing.</span></span>

### <span data-ttu-id="3ac5e-112">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="3ac5e-112">Example 3</span></span>
```powershell
PS C:\> Search-AzGraph -Include DisplayName -Query 'where type =~ "Microsoft.Compute/virtualMachines"| where properties.storageProfile.osDisk.managedDisk == "" | project name, resourceGroup, subscriptionDisplayName'

name         resourceGroup      subscriptionDisplayName
----         -------------      -----------------------
ContosoVM    RG-Contoso         Contoso Production Subscription                                               

```
<span data-ttu-id="3ac5e-113">Uma consulta com todas as máquinas virtuais que não estão usando Discos Gerenciados e inclui nomes de exibição de assinatura.</span><span class="sxs-lookup"><span data-stu-id="3ac5e-113">A query featuring all virtual machines which are not using Managed Disks and includes subscription display names.</span></span>

### <span data-ttu-id="3ac5e-114">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="3ac5e-114">Example 4</span></span>
```powershell
PS C:\> Search-AzGraph -Include DisplayName -Query 'summarize count() by tenantDisplayName, subscriptionDisplayName'

tenantDisplayName   subscriptionDisplayName              count_
-----------------   -----------------------              ------
ContosoTenant       Contoso Production Subscription      118                                           
```
<span data-ttu-id="3ac5e-115">Uma consulta que exibe a contagem de recursos por locatários e nomes de exibição de assinatura.</span><span class="sxs-lookup"><span data-stu-id="3ac5e-115">A query displaying the count of resources by tenant and subscription display names.</span></span>

## <span data-ttu-id="3ac5e-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="3ac5e-116">PARAMETERS</span></span>

### <span data-ttu-id="3ac5e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ac5e-117">-DefaultProfile</span></span>
<span data-ttu-id="3ac5e-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3ac5e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ac5e-119">-Query</span><span class="sxs-lookup"><span data-stu-id="3ac5e-119">-Query</span></span>
<span data-ttu-id="3ac5e-120">Consulta resource Graph.</span><span class="sxs-lookup"><span data-stu-id="3ac5e-120">Resource Graph query.</span></span>

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

### <span data-ttu-id="3ac5e-121">-Subscription</span><span class="sxs-lookup"><span data-stu-id="3ac5e-121">-Subscription</span></span>
<span data-ttu-id="3ac5e-122">Subscription(s) to run query against.</span><span class="sxs-lookup"><span data-stu-id="3ac5e-122">Subscription(s) to run query against.</span></span>

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

### <span data-ttu-id="3ac5e-123">-Skip</span><span class="sxs-lookup"><span data-stu-id="3ac5e-123">-Skip</span></span>
<span data-ttu-id="3ac5e-124">Ignora os primeiros objetos N e obtém os objetos restantes.</span><span class="sxs-lookup"><span data-stu-id="3ac5e-124">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="3ac5e-125">-First</span><span class="sxs-lookup"><span data-stu-id="3ac5e-125">-First</span></span>
<span data-ttu-id="3ac5e-126">O número máximo de objetos a retornar.</span><span class="sxs-lookup"><span data-stu-id="3ac5e-126">The maximum number of objects to return.</span></span> <span data-ttu-id="3ac5e-127">Valores permitidos: 1-5000.</span><span class="sxs-lookup"><span data-stu-id="3ac5e-127">Allowed values: 1-5000.</span></span>
<span data-ttu-id="3ac5e-128">O valor padrão é 100.</span><span class="sxs-lookup"><span data-stu-id="3ac5e-128">Default value is 100.</span></span>

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

### <span data-ttu-id="3ac5e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ac5e-129">CommonParameters</span></span>
<span data-ttu-id="3ac5e-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ac5e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ac5e-131">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ac5e-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ac5e-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3ac5e-132">INPUTS</span></span>

### <span data-ttu-id="3ac5e-133">Nenhum</span><span class="sxs-lookup"><span data-stu-id="3ac5e-133">None</span></span>

## <span data-ttu-id="3ac5e-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="3ac5e-134">OUTPUTS</span></span>

### <span data-ttu-id="3ac5e-135">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="3ac5e-135">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="3ac5e-136">NOTES</span><span class="sxs-lookup"><span data-stu-id="3ac5e-136">NOTES</span></span>

## <span data-ttu-id="3ac5e-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3ac5e-137">RELATED LINKS</span></span>
