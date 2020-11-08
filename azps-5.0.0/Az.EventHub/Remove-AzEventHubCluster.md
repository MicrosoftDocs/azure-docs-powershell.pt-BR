---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubCluster.md
ms.openlocfilehash: e67d70f91e523cd46755035abe951682b1764cbc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94115458"
---
# <span data-ttu-id="b196c-101">Remove-AzEventHubCluster</span><span class="sxs-lookup"><span data-stu-id="b196c-101">Remove-AzEventHubCluster</span></span>

## <span data-ttu-id="b196c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b196c-102">SYNOPSIS</span></span>
<span data-ttu-id="b196c-103">Exclui o cluster do Eventhub dedicado especificado do grupo de Resource</span><span class="sxs-lookup"><span data-stu-id="b196c-103">Deletes the specified Dedicated Eventhub Cluster from the ResourceGroup</span></span>

## <span data-ttu-id="b196c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b196c-104">SYNTAX</span></span>

### <span data-ttu-id="b196c-105">ClusterPropertiesSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="b196c-105">ClusterPropertiesSet (Default)</span></span>
```
Remove-AzEventHubCluster [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b196c-106">ClusterInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b196c-106">ClusterInputObjectSet</span></span>
```
Remove-AzEventHubCluster [-InputObject] <PSEventHubAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b196c-107">ClusterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b196c-107">ClusterResourceIdParameterSet</span></span>
```
Remove-AzEventHubCluster [-ResourceId] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b196c-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b196c-108">DESCRIPTION</span></span>
<span data-ttu-id="b196c-109">O cmdlet Remove-AzEventHubCluster exclui o nome de cluster do eventhub dedicado específico do grupo de Resources especificado</span><span class="sxs-lookup"><span data-stu-id="b196c-109">The Remove-AzEventHubCluster cmdlet deletes the given dedicated eventhub Cluster name from the given resourcegroup</span></span>

## <span data-ttu-id="b196c-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b196c-110">EXAMPLES</span></span>

### <span data-ttu-id="b196c-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b196c-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubCluster -ResourceGroupName RSG-Cluster27651 -Name Eventhub-Cluster-5557
```

<span data-ttu-id="b196c-112">Exclui o cluster do Eventhub-cluster-5557 de RSG-Cluster27651 grupo de Resources</span><span class="sxs-lookup"><span data-stu-id="b196c-112">Deletes Eventhub-Cluster-5557 Cluster from RSG-Cluster27651 resourcegroup</span></span>

## <span data-ttu-id="b196c-113">OS</span><span class="sxs-lookup"><span data-stu-id="b196c-113">PARAMETERS</span></span>

### <span data-ttu-id="b196c-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b196c-114">-AsJob</span></span>
<span data-ttu-id="b196c-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="b196c-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b196c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b196c-116">-DefaultProfile</span></span>
<span data-ttu-id="b196c-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b196c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b196c-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b196c-118">-InputObject</span></span>
<span data-ttu-id="b196c-119">Objeto de cluster</span><span class="sxs-lookup"><span data-stu-id="b196c-119">Cluster Object</span></span>

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

### <span data-ttu-id="b196c-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="b196c-120">-Name</span></span>
<span data-ttu-id="b196c-121">Nome do cluster</span><span class="sxs-lookup"><span data-stu-id="b196c-121">Cluster Name</span></span>

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

### <span data-ttu-id="b196c-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b196c-122">-PassThru</span></span>
<span data-ttu-id="b196c-123">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="b196c-123">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="b196c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b196c-124">-ResourceGroupName</span></span>
<span data-ttu-id="b196c-125">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="b196c-125">Resource Group Name</span></span>

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

### <span data-ttu-id="b196c-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b196c-126">-ResourceId</span></span>
<span data-ttu-id="b196c-127">ID do recurso de cluster</span><span class="sxs-lookup"><span data-stu-id="b196c-127">Cluster Resource Id</span></span>

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

### <span data-ttu-id="b196c-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b196c-128">-Confirm</span></span>
<span data-ttu-id="b196c-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b196c-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b196c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b196c-130">-WhatIf</span></span>
<span data-ttu-id="b196c-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b196c-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b196c-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b196c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b196c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b196c-133">CommonParameters</span></span>
<span data-ttu-id="b196c-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b196c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b196c-135">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b196c-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b196c-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b196c-136">INPUTS</span></span>

### <span data-ttu-id="b196c-137">System. String</span><span class="sxs-lookup"><span data-stu-id="b196c-137">System.String</span></span>

### <span data-ttu-id="b196c-138">Microsoft. Azure. Commands. EventHub. Models. PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="b196c-138">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="b196c-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b196c-139">OUTPUTS</span></span>

### <span data-ttu-id="b196c-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b196c-140">System.Boolean</span></span>

## <span data-ttu-id="b196c-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b196c-141">NOTES</span></span>

## <span data-ttu-id="b196c-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b196c-142">RELATED LINKS</span></span>
