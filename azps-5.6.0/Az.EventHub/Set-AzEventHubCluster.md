---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/set-azeventhubcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubCluster.md
ms.openlocfilehash: 3fb0030d6475ab3fb41f78ab1dc1a54870ed2f8f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891426"
---
# <span data-ttu-id="51808-101">Set-AzEventHubCluster</span><span class="sxs-lookup"><span data-stu-id="51808-101">Set-AzEventHubCluster</span></span>

## <span data-ttu-id="51808-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="51808-102">SYNOPSIS</span></span>
<span data-ttu-id="51808-103">Atualiza a marca para o cluster determinado</span><span class="sxs-lookup"><span data-stu-id="51808-103">Updates the Tag for the given Cluster</span></span>

## <span data-ttu-id="51808-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="51808-104">SYNTAX</span></span>

### <span data-ttu-id="51808-105">ClusterPropertiesSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="51808-105">ClusterPropertiesSet (Default)</span></span>
```
Set-AzEventHubCluster [-ResourceGroupName] <String> [-Name] <String> [-Location <String>] [-Capacity <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51808-106">ClusterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="51808-106">ClusterResourceIdParameterSet</span></span>
```
Set-AzEventHubCluster [-Name] <String> [-ResourceId] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51808-107">ClusterInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="51808-107">ClusterInputObjectSet</span></span>
```
Set-AzEventHubCluster [-InputObject] <PSEventHubClusterAttributes> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51808-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="51808-108">DESCRIPTION</span></span>
<span data-ttu-id="51808-109">O Set-AzEventHubCluster cmdlet atualiza marcas do cluster determinado</span><span class="sxs-lookup"><span data-stu-id="51808-109">The Set-AzEventHubCluster cmdlet updates tags of the given cluster</span></span>

## <span data-ttu-id="51808-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="51808-110">EXAMPLES</span></span>

### <span data-ttu-id="51808-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="51808-111">Example 1</span></span>
```powershell
PS C:\> Set-AzEventHubCluster -ResourceGroupName RSG-Cluster27651 -Name Eventhub-Cluster-5557 -Tag @{"ClusterTag3" = "Tag3"; "ClusterTag4" = "Tag4";}

Id        : /subscriptions/{SubID}/resourceGroups/RSG-Cluster27651/providers/Microsoft.EventHub/clusters/Eventhub-Cluster-5557
Name      : Eventhub-Cluster-5557
Location  : southcentralus
CreatedAt : 09/10/2020 22:09:57
UpdatedAt : 09/11/2020 01:31:18
MetricId  :
Status    :
Sku       : Microsoft.Azure.Commands.EventHub.Models.PSEventHubsClusterSkuAttributes
Tags      : {[ClusterTag3, Tag3], [ClusterTag4, Tag4]}
```

<span data-ttu-id="51808-112">Atualiza marcas do cluster determinado.</span><span class="sxs-lookup"><span data-stu-id="51808-112">Updates tags of the given cluster.</span></span> 

## <span data-ttu-id="51808-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="51808-113">PARAMETERS</span></span>

### <span data-ttu-id="51808-114">-Capacity</span><span class="sxs-lookup"><span data-stu-id="51808-114">-Capacity</span></span>
<span data-ttu-id="51808-115">Capacidade do Cluster (CU), curantrly, valor permitido = 1</span><span class="sxs-lookup"><span data-stu-id="51808-115">Cluster Capacity (CU), curerntrly, allowed value = 1</span></span>

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

### <span data-ttu-id="51808-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51808-116">-DefaultProfile</span></span>
<span data-ttu-id="51808-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="51808-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="51808-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="51808-118">-InputObject</span></span>
<span data-ttu-id="51808-119">Nome do cluster</span><span class="sxs-lookup"><span data-stu-id="51808-119">Cluster Name</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSEventHubClusterAttributes
Parameter Sets: ClusterInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51808-120">-Location</span><span class="sxs-lookup"><span data-stu-id="51808-120">-Location</span></span>
<span data-ttu-id="51808-121">Local do Cluster</span><span class="sxs-lookup"><span data-stu-id="51808-121">Location of Cluster</span></span>

```yaml
Type: System.String
Parameter Sets: ClusterPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51808-122">-Name</span><span class="sxs-lookup"><span data-stu-id="51808-122">-Name</span></span>
<span data-ttu-id="51808-123">Nome do cluster</span><span class="sxs-lookup"><span data-stu-id="51808-123">Cluster Name</span></span>

```yaml
Type: System.String
Parameter Sets: ClusterPropertiesSet, ClusterResourceIdParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51808-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51808-124">-ResourceGroupName</span></span>
<span data-ttu-id="51808-125">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="51808-125">Resource Group Name</span></span>

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

### <span data-ttu-id="51808-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="51808-126">-ResourceId</span></span>
<span data-ttu-id="51808-127">ID de Recurso do Cluster</span><span class="sxs-lookup"><span data-stu-id="51808-127">Resource ID of Cluster</span></span>

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

### <span data-ttu-id="51808-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="51808-128">-Tag</span></span>
<span data-ttu-id="51808-129">Hashtables que representa a marca de recurso para clusters</span><span class="sxs-lookup"><span data-stu-id="51808-129">Hashtables which represents resource Tag for Clusters</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ClusterPropertiesSet, ClusterResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51808-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="51808-130">-Confirm</span></span>
<span data-ttu-id="51808-131">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="51808-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51808-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51808-132">-WhatIf</span></span>
<span data-ttu-id="51808-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="51808-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51808-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="51808-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51808-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51808-135">CommonParameters</span></span>
<span data-ttu-id="51808-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51808-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51808-137">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="51808-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51808-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="51808-138">INPUTS</span></span>

### <span data-ttu-id="51808-139">System.String</span><span class="sxs-lookup"><span data-stu-id="51808-139">System.String</span></span>

### <span data-ttu-id="51808-140">System.Nullable'1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="51808-140">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="51808-141">Microsoft.Azure.Commands.EventHub.Models.PSEventHubClusterAttributes</span><span class="sxs-lookup"><span data-stu-id="51808-141">Microsoft.Azure.Commands.EventHub.Models.PSEventHubClusterAttributes</span></span>

### <span data-ttu-id="51808-142">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="51808-142">System.Collections.Hashtable</span></span>

## <span data-ttu-id="51808-143">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="51808-143">OUTPUTS</span></span>

### <span data-ttu-id="51808-144">Microsoft.Azure.Commands.EventHub.Models.PSEventHubClusterAttributes</span><span class="sxs-lookup"><span data-stu-id="51808-144">Microsoft.Azure.Commands.EventHub.Models.PSEventHubClusterAttributes</span></span>

## <span data-ttu-id="51808-145">NOTES</span><span class="sxs-lookup"><span data-stu-id="51808-145">NOTES</span></span>

## <span data-ttu-id="51808-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="51808-146">RELATED LINKS</span></span>
