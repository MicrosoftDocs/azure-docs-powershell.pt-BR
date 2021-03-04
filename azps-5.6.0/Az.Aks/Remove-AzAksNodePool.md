---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/powershell/module/az.aks/remove-azaksnodepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Remove-AzAksNodePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Remove-AzAksNodePool.md
ms.openlocfilehash: 27de96fccf2c420bd15e4a7522fecc16fd3032fe
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890680"
---
# <span data-ttu-id="9e541-101">Remove-AzAksNodePool</span><span class="sxs-lookup"><span data-stu-id="9e541-101">Remove-AzAksNodePool</span></span>

## <span data-ttu-id="9e541-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e541-102">SYNOPSIS</span></span>
<span data-ttu-id="9e541-103">Excluir pool de nós do cluster gerenciado.</span><span class="sxs-lookup"><span data-stu-id="9e541-103">Delete node pool from managed cluster.</span></span>

## <span data-ttu-id="9e541-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="9e541-104">SYNTAX</span></span>

### <span data-ttu-id="9e541-105">GroupNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="9e541-105">GroupNameParameterSet (Default)</span></span>
```
Remove-AzAksNodePool [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String> [-PassThru]
 [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e541-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e541-106">InputObjectParameterSet</span></span>
```
Remove-AzAksNodePool -InputObject <PSNodePool> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e541-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e541-107">IdParameterSet</span></span>
```
Remove-AzAksNodePool [-Id] <String> [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e541-108">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e541-108">ParentObjectParameterSet</span></span>
```
Remove-AzAksNodePool [-Name] <String> -ClusterObject <PSKubernetesCluster> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9e541-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="9e541-109">DESCRIPTION</span></span>
<span data-ttu-id="9e541-110">Excluir pool de nós do cluster gerenciado.</span><span class="sxs-lookup"><span data-stu-id="9e541-110">Delete node pool from managed cluster.</span></span>

## <span data-ttu-id="9e541-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9e541-111">EXAMPLES</span></span>

### <span data-ttu-id="9e541-112">Excluir pool de nós especificado</span><span class="sxs-lookup"><span data-stu-id="9e541-112">Delete specified node pool</span></span>
```powershell
PS C:\> Remove-AzAksNodePool -ResourceGroupName myResourceGroup -CulsterName myCluster -Name winpool
```

## <span data-ttu-id="9e541-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="9e541-113">PARAMETERS</span></span>

### <span data-ttu-id="9e541-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9e541-114">-AsJob</span></span>
<span data-ttu-id="9e541-115">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="9e541-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9e541-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="9e541-116">-ClusterName</span></span>
<span data-ttu-id="9e541-117">Nome do cluster kubernetes gerenciado</span><span class="sxs-lookup"><span data-stu-id="9e541-117">Name of your managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: GroupNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e541-118">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="9e541-118">-ClusterObject</span></span>
<span data-ttu-id="9e541-119">O objeto cluster.</span><span class="sxs-lookup"><span data-stu-id="9e541-119">The cluster object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster
Parameter Sets: ParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e541-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e541-120">-DefaultProfile</span></span>
<span data-ttu-id="9e541-121">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9e541-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e541-122">-Force</span><span class="sxs-lookup"><span data-stu-id="9e541-122">-Force</span></span>
<span data-ttu-id="9e541-123">Remover pool de nós sem prompt</span><span class="sxs-lookup"><span data-stu-id="9e541-123">Remove node pool without prompt</span></span>

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

### <span data-ttu-id="9e541-124">-Id</span><span class="sxs-lookup"><span data-stu-id="9e541-124">-Id</span></span>
<span data-ttu-id="9e541-125">ID de um pool de nós no cluster kubernetes gerenciado</span><span class="sxs-lookup"><span data-stu-id="9e541-125">Id of an node pool in managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e541-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9e541-126">-InputObject</span></span>
<span data-ttu-id="9e541-127">Um objeto PSAgentPool, normalmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="9e541-127">A PSAgentPool object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Aks.Models.PSNodePool
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9e541-128">-Name</span><span class="sxs-lookup"><span data-stu-id="9e541-128">-Name</span></span>
<span data-ttu-id="9e541-129">Nome do pool de nós</span><span class="sxs-lookup"><span data-stu-id="9e541-129">Name of your node pool</span></span>

```yaml
Type: System.String
Parameter Sets: GroupNameParameterSet, ParentObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e541-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9e541-130">-PassThru</span></span>
<span data-ttu-id="9e541-131">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="9e541-131">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="9e541-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e541-132">-ResourceGroupName</span></span>
<span data-ttu-id="9e541-133">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="9e541-133">Resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: GroupNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e541-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9e541-134">-Confirm</span></span>
<span data-ttu-id="9e541-135">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e541-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e541-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e541-136">-WhatIf</span></span>
<span data-ttu-id="9e541-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9e541-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e541-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9e541-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e541-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e541-139">CommonParameters</span></span>
<span data-ttu-id="9e541-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e541-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e541-141">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9e541-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e541-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9e541-142">INPUTS</span></span>

### <span data-ttu-id="9e541-143">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span><span class="sxs-lookup"><span data-stu-id="9e541-143">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

### <span data-ttu-id="9e541-144">System.String</span><span class="sxs-lookup"><span data-stu-id="9e541-144">System.String</span></span>

## <span data-ttu-id="9e541-145">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="9e541-145">OUTPUTS</span></span>

### <span data-ttu-id="9e541-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9e541-146">System.Boolean</span></span>

## <span data-ttu-id="9e541-147">NOTES</span><span class="sxs-lookup"><span data-stu-id="9e541-147">NOTES</span></span>

## <span data-ttu-id="9e541-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9e541-148">RELATED LINKS</span></span>
