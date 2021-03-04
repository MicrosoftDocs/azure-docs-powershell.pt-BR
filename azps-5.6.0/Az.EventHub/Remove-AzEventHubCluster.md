---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/remove-azeventhubcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubCluster.md
ms.openlocfilehash: 7ba6a5f95c1cc37f7cdef7d8ead7a2514927e089
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890626"
---
# <span data-ttu-id="aa9ac-101">Remove-AzEventHubCluster</span><span class="sxs-lookup"><span data-stu-id="aa9ac-101">Remove-AzEventHubCluster</span></span>

## <span data-ttu-id="aa9ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aa9ac-102">SYNOPSIS</span></span>
<span data-ttu-id="aa9ac-103">Exclui o Cluster Eventhub Dedicado especificado do ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="aa9ac-103">Deletes the specified Dedicated Eventhub Cluster from the ResourceGroup</span></span>

## <span data-ttu-id="aa9ac-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="aa9ac-104">SYNTAX</span></span>

### <span data-ttu-id="aa9ac-105">ClusterPropertiesSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="aa9ac-105">ClusterPropertiesSet (Default)</span></span>
```
Remove-AzEventHubCluster [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa9ac-106">ClusterInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="aa9ac-106">ClusterInputObjectSet</span></span>
```
Remove-AzEventHubCluster [-InputObject] <PSEventHubAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa9ac-107">ClusterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="aa9ac-107">ClusterResourceIdParameterSet</span></span>
```
Remove-AzEventHubCluster [-ResourceId] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa9ac-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="aa9ac-108">DESCRIPTION</span></span>
<span data-ttu-id="aa9ac-109">O Remove-AzEventHubCluster cmdlet exclui o nome de Cluster eventhub dedicado do determinado grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="aa9ac-109">The Remove-AzEventHubCluster cmdlet deletes the given dedicated eventhub Cluster name from the given resourcegroup</span></span>

## <span data-ttu-id="aa9ac-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="aa9ac-110">EXAMPLES</span></span>

### <span data-ttu-id="aa9ac-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="aa9ac-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubCluster -ResourceGroupName RSG-Cluster27651 -Name Eventhub-Cluster-5557
```

<span data-ttu-id="aa9ac-112">Exclui o Cluster Eventhub-Cluster-5557 do RSG-Cluster27651 resourcegroup</span><span class="sxs-lookup"><span data-stu-id="aa9ac-112">Deletes Eventhub-Cluster-5557 Cluster from RSG-Cluster27651 resourcegroup</span></span>

## <span data-ttu-id="aa9ac-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="aa9ac-113">PARAMETERS</span></span>

### <span data-ttu-id="aa9ac-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="aa9ac-114">-AsJob</span></span>
<span data-ttu-id="aa9ac-115">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="aa9ac-115">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa9ac-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa9ac-116">-DefaultProfile</span></span>
<span data-ttu-id="aa9ac-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="aa9ac-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa9ac-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aa9ac-118">-InputObject</span></span>
<span data-ttu-id="aa9ac-119">Objeto Cluster</span><span class="sxs-lookup"><span data-stu-id="aa9ac-119">Cluster Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes
Parameter Sets: ClusterInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aa9ac-120">-Name</span><span class="sxs-lookup"><span data-stu-id="aa9ac-120">-Name</span></span>
<span data-ttu-id="aa9ac-121">Nome do cluster</span><span class="sxs-lookup"><span data-stu-id="aa9ac-121">Cluster Name</span></span>

```yaml
Type: System.String
Parameter Sets: ClusterPropertiesSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa9ac-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="aa9ac-122">-PassThru</span></span>
<span data-ttu-id="aa9ac-123">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="aa9ac-123">{{ Fill PassThru Description }}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa9ac-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa9ac-124">-ResourceGroupName</span></span>
<span data-ttu-id="aa9ac-125">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="aa9ac-125">Resource Group Name</span></span>

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

### <span data-ttu-id="aa9ac-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aa9ac-126">-ResourceId</span></span>
<span data-ttu-id="aa9ac-127">ID do Recurso de Cluster</span><span class="sxs-lookup"><span data-stu-id="aa9ac-127">Cluster Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ClusterResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa9ac-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aa9ac-128">-Confirm</span></span>
<span data-ttu-id="aa9ac-129">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aa9ac-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa9ac-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa9ac-130">-WhatIf</span></span>
<span data-ttu-id="aa9ac-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="aa9ac-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa9ac-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="aa9ac-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa9ac-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa9ac-133">CommonParameters</span></span>
<span data-ttu-id="aa9ac-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa9ac-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa9ac-135">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aa9ac-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa9ac-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="aa9ac-136">INPUTS</span></span>

### <span data-ttu-id="aa9ac-137">System.String</span><span class="sxs-lookup"><span data-stu-id="aa9ac-137">System.String</span></span>

### <span data-ttu-id="aa9ac-138">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="aa9ac-138">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="aa9ac-139">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="aa9ac-139">OUTPUTS</span></span>

### <span data-ttu-id="aa9ac-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="aa9ac-140">System.Boolean</span></span>

## <span data-ttu-id="aa9ac-141">NOTES</span><span class="sxs-lookup"><span data-stu-id="aa9ac-141">NOTES</span></span>

## <span data-ttu-id="aa9ac-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="aa9ac-142">RELATED LINKS</span></span>
