---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/new-azeventhubcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubCluster.md
ms.openlocfilehash: 4a76d54e4c8a3abda87fb9fd6de1d4439b051112
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886027"
---
# <span data-ttu-id="cf9c7-101">New-AzEventHubCluster</span><span class="sxs-lookup"><span data-stu-id="cf9c7-101">New-AzEventHubCluster</span></span>

## <span data-ttu-id="cf9c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf9c7-102">SYNOPSIS</span></span>
<span data-ttu-id="cf9c7-103">Cria um novo cluster eventhub dedicado</span><span class="sxs-lookup"><span data-stu-id="cf9c7-103">Creates a new dedicated eventhub cluster</span></span>

## <span data-ttu-id="cf9c7-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="cf9c7-104">SYNTAX</span></span>

### <span data-ttu-id="cf9c7-105">ClusterPropertiesSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="cf9c7-105">ClusterPropertiesSet (Default)</span></span>
```
New-AzEventHubCluster [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Capacity <Int32>]
 [-Tag <Hashtable>] [[-ResourceId] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cf9c7-106">ClusterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cf9c7-106">ClusterResourceIdParameterSet</span></span>
```
New-AzEventHubCluster [-Name] <String> [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf9c7-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="cf9c7-107">DESCRIPTION</span></span>
<span data-ttu-id="cf9c7-108">O New-AzEventHubCluster cmdlet cria o cluster eventhub dedicado no determinado grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="cf9c7-108">The New-AzEventHubCluster cmdlet creates the dedicated eventhub cluster in the given resource group</span></span>

## <span data-ttu-id="cf9c7-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cf9c7-109">EXAMPLES</span></span>

### <span data-ttu-id="cf9c7-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="cf9c7-110">Example 1</span></span>
```powershell
PS C:\>  New-AzEventHubCluster -ResourceGroupName RSG-Cluster27651 -Name Eventhub-Cluster-5557 -Location southcentralus -Capacity 1

Id        : /subscriptions/SubId/resourceGroups/RSG-Cluster27651/providers/Microsoft.EventHub/clusters/Eventhub-Cluster-5557
Name      : Eventhub-Cluster-5557
Location  : southcentralus
CreatedAt : 09/10/2020 22:09:57
UpdatedAt : 09/11/2020 01:31:18
MetricId  :
Status    :
Sku       : Microsoft.Azure.Commands.EventHub.Models.PSEventHubsClusterSkuAttributes
Tags      : {[ClusterTag1, Tag1], [ClusterTag2, Tag2]}

```

<span data-ttu-id="cf9c7-111">Cria cluster dedicado 'Eventhub-Cluster-5557' no grupo de recursos 'RSG-Cluster27651' com Localização southcentralus e Capacidade como 1</span><span class="sxs-lookup"><span data-stu-id="cf9c7-111">Creates 'Eventhub-Cluster-5557' dedicated cluster in resourcegroup 'RSG-Cluster27651' with Location southcentralus and Capacity as 1</span></span>

## <span data-ttu-id="cf9c7-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="cf9c7-112">PARAMETERS</span></span>

### <span data-ttu-id="cf9c7-113">-Capacity</span><span class="sxs-lookup"><span data-stu-id="cf9c7-113">-Capacity</span></span>
<span data-ttu-id="cf9c7-114">Capacidade do Cluster (CU), curantrly, valor permitido = 1</span><span class="sxs-lookup"><span data-stu-id="cf9c7-114">Cluster Capacity (CU), curerntrly, allowed value = 1</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ClusterPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf9c7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf9c7-115">-DefaultProfile</span></span>
<span data-ttu-id="cf9c7-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cf9c7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf9c7-117">-Location</span><span class="sxs-lookup"><span data-stu-id="cf9c7-117">-Location</span></span>
<span data-ttu-id="cf9c7-118">Local do Cluster</span><span class="sxs-lookup"><span data-stu-id="cf9c7-118">Location of Cluster</span></span>

```yaml
Type: System.String
Parameter Sets: ClusterPropertiesSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf9c7-119">-Name</span><span class="sxs-lookup"><span data-stu-id="cf9c7-119">-Name</span></span>
<span data-ttu-id="cf9c7-120">Nome do cluster</span><span class="sxs-lookup"><span data-stu-id="cf9c7-120">Cluster Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf9c7-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf9c7-121">-ResourceGroupName</span></span>
<span data-ttu-id="cf9c7-122">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="cf9c7-122">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ClusterPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf9c7-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cf9c7-123">-ResourceId</span></span>
<span data-ttu-id="cf9c7-124">ID de Recurso do Cluster</span><span class="sxs-lookup"><span data-stu-id="cf9c7-124">Resource ID of Cluster</span></span>

```yaml
Type: System.String
Parameter Sets: ClusterPropertiesSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ClusterResourceIdParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf9c7-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="cf9c7-125">-Tag</span></span>
<span data-ttu-id="cf9c7-126">Hashtables que representa marcas de recurso para clusters</span><span class="sxs-lookup"><span data-stu-id="cf9c7-126">Hashtables which represents resource Tags for Clusters</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ClusterPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf9c7-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cf9c7-127">-Confirm</span></span>
<span data-ttu-id="cf9c7-128">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cf9c7-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf9c7-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf9c7-129">-WhatIf</span></span>
<span data-ttu-id="cf9c7-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="cf9c7-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf9c7-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cf9c7-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf9c7-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf9c7-132">CommonParameters</span></span>
<span data-ttu-id="cf9c7-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf9c7-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf9c7-134">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cf9c7-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf9c7-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cf9c7-135">INPUTS</span></span>

### <span data-ttu-id="cf9c7-136">System.String</span><span class="sxs-lookup"><span data-stu-id="cf9c7-136">System.String</span></span>

### <span data-ttu-id="cf9c7-137">System.Nullable'1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="cf9c7-137">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="cf9c7-138">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="cf9c7-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="cf9c7-139">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="cf9c7-139">OUTPUTS</span></span>

### <span data-ttu-id="cf9c7-140">Microsoft.Azure.Commands.EventHub.Models.PSEventHubClusterAttributes</span><span class="sxs-lookup"><span data-stu-id="cf9c7-140">Microsoft.Azure.Commands.EventHub.Models.PSEventHubClusterAttributes</span></span>

## <span data-ttu-id="cf9c7-141">NOTES</span><span class="sxs-lookup"><span data-stu-id="cf9c7-141">NOTES</span></span>

## <span data-ttu-id="cf9c7-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cf9c7-142">RELATED LINKS</span></span>
