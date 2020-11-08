---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubCluster.md
ms.openlocfilehash: 3e78e302aafb3e59293f04ade7035e5b4ebbd84c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94125011"
---
# <span data-ttu-id="d450e-101">Set-AzEventHubCluster</span><span class="sxs-lookup"><span data-stu-id="d450e-101">Set-AzEventHubCluster</span></span>

## <span data-ttu-id="d450e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d450e-102">SYNOPSIS</span></span>
<span data-ttu-id="d450e-103">Atualiza a marca do cluster fornecido</span><span class="sxs-lookup"><span data-stu-id="d450e-103">Updates the Tag for the given Cluster</span></span>

## <span data-ttu-id="d450e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d450e-104">SYNTAX</span></span>

### <span data-ttu-id="d450e-105">ClusterPropertiesSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="d450e-105">ClusterPropertiesSet (Default)</span></span>
```
Set-AzEventHubCluster [-ResourceGroupName] <String> [-Name] <String> [-Location <String>] [-Capacity <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d450e-106">ClusterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d450e-106">ClusterResourceIdParameterSet</span></span>
```
Set-AzEventHubCluster [-Name] <String> [-ResourceId] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d450e-107">ClusterInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d450e-107">ClusterInputObjectSet</span></span>
```
Set-AzEventHubCluster [-InputObject] <PSEventHubClusterAttributes> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d450e-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d450e-108">DESCRIPTION</span></span>
<span data-ttu-id="d450e-109">O cmdlet Set-AzEventHubCluster atualiza as marcas do cluster fornecido</span><span class="sxs-lookup"><span data-stu-id="d450e-109">The Set-AzEventHubCluster cmdlet updates tags of the given cluster</span></span>

## <span data-ttu-id="d450e-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d450e-110">EXAMPLES</span></span>

### <span data-ttu-id="d450e-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d450e-111">Example 1</span></span>
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

<span data-ttu-id="d450e-112">Atualiza as marcas do cluster fornecido.</span><span class="sxs-lookup"><span data-stu-id="d450e-112">Updates tags of the given cluster.</span></span> 

## <span data-ttu-id="d450e-113">OS</span><span class="sxs-lookup"><span data-stu-id="d450e-113">PARAMETERS</span></span>

### <span data-ttu-id="d450e-114">-Capacidade</span><span class="sxs-lookup"><span data-stu-id="d450e-114">-Capacity</span></span>
<span data-ttu-id="d450e-115">Capacidade do cluster (RECOR), curerntrly, valor permitido = 1</span><span class="sxs-lookup"><span data-stu-id="d450e-115">Cluster Capacity (CU), curerntrly, allowed value = 1</span></span>

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

### <span data-ttu-id="d450e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d450e-116">-DefaultProfile</span></span>
<span data-ttu-id="d450e-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d450e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d450e-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d450e-118">-InputObject</span></span>
<span data-ttu-id="d450e-119">Nome do cluster</span><span class="sxs-lookup"><span data-stu-id="d450e-119">Cluster Name</span></span>

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

### <span data-ttu-id="d450e-120">-Local</span><span class="sxs-lookup"><span data-stu-id="d450e-120">-Location</span></span>
<span data-ttu-id="d450e-121">Local do cluster</span><span class="sxs-lookup"><span data-stu-id="d450e-121">Location of Cluster</span></span>

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

### <span data-ttu-id="d450e-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="d450e-122">-Name</span></span>
<span data-ttu-id="d450e-123">Nome do cluster</span><span class="sxs-lookup"><span data-stu-id="d450e-123">Cluster Name</span></span>

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

### <span data-ttu-id="d450e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d450e-124">-ResourceGroupName</span></span>
<span data-ttu-id="d450e-125">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="d450e-125">Resource Group Name</span></span>

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

### <span data-ttu-id="d450e-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d450e-126">-ResourceId</span></span>
<span data-ttu-id="d450e-127">ID do recurso do cluster</span><span class="sxs-lookup"><span data-stu-id="d450e-127">Resource ID of Cluster</span></span>

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

### <span data-ttu-id="d450e-128">-Marca</span><span class="sxs-lookup"><span data-stu-id="d450e-128">-Tag</span></span>
<span data-ttu-id="d450e-129">Hashtables que representam a marca de recursos para clusters</span><span class="sxs-lookup"><span data-stu-id="d450e-129">Hashtables which represents resource Tag for Clusters</span></span>

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

### <span data-ttu-id="d450e-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d450e-130">-Confirm</span></span>
<span data-ttu-id="d450e-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d450e-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d450e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d450e-132">-WhatIf</span></span>
<span data-ttu-id="d450e-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d450e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d450e-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d450e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d450e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d450e-135">CommonParameters</span></span>
<span data-ttu-id="d450e-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d450e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d450e-137">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d450e-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d450e-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d450e-138">INPUTS</span></span>

### <span data-ttu-id="d450e-139">System. String</span><span class="sxs-lookup"><span data-stu-id="d450e-139">System.String</span></span>

### <span data-ttu-id="d450e-140">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="d450e-140">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="d450e-141">Microsoft. Azure. Commands. EventHub. Models. PSEventHubClusterAttributes</span><span class="sxs-lookup"><span data-stu-id="d450e-141">Microsoft.Azure.Commands.EventHub.Models.PSEventHubClusterAttributes</span></span>

### <span data-ttu-id="d450e-142">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="d450e-142">System.Collections.Hashtable</span></span>

## <span data-ttu-id="d450e-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d450e-143">OUTPUTS</span></span>

### <span data-ttu-id="d450e-144">Microsoft. Azure. Commands. EventHub. Models. PSEventHubClusterAttributes</span><span class="sxs-lookup"><span data-stu-id="d450e-144">Microsoft.Azure.Commands.EventHub.Models.PSEventHubClusterAttributes</span></span>

## <span data-ttu-id="d450e-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d450e-145">NOTES</span></span>

## <span data-ttu-id="d450e-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d450e-146">RELATED LINKS</span></span>
