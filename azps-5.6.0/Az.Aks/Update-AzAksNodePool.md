---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/powershell/module/az.aks/update-azaksnodepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Update-AzAksNodePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Update-AzAksNodePool.md
ms.openlocfilehash: 6f16664eac63ab2bb543b2d032679d979f3c2122
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892909"
---
# <span data-ttu-id="32a43-101">Update-AzAksNodePool</span><span class="sxs-lookup"><span data-stu-id="32a43-101">Update-AzAksNodePool</span></span>

## <span data-ttu-id="32a43-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32a43-102">SYNOPSIS</span></span>
<span data-ttu-id="32a43-103">Atualizar pool de nós em um cluster gerenciado.</span><span class="sxs-lookup"><span data-stu-id="32a43-103">Update node pool in a managed cluster.</span></span>

## <span data-ttu-id="32a43-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="32a43-104">SYNTAX</span></span>

### <span data-ttu-id="32a43-105">defaultParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="32a43-105">defaultParameterSet (Default)</span></span>
```
Update-AzAksNodePool -ResourceGroupName <String> -ClusterName <String> -Name <String> [-AsJob] [-Force]
 [-KubernetesVersion <String>] [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32a43-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="32a43-106">ParentObjectParameterSet</span></span>
```
Update-AzAksNodePool -Name <String> -ClusterObject <PSKubernetesCluster> [-AsJob] [-Force]
 [-KubernetesVersion <String>] [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32a43-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="32a43-107">InputObjectParameterSet</span></span>
```
Update-AzAksNodePool -InputObject <PSNodePool> [-AsJob] [-Force] [-KubernetesVersion <String>]
 [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32a43-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="32a43-108">IdParameterSet</span></span>
```
Update-AzAksNodePool -Id <String> [-AsJob] [-Force] [-KubernetesVersion <String>] [-MinCount <Int32>]
 [-MaxCount <Int32>] [-EnableAutoScaling] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="32a43-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="32a43-109">DESCRIPTION</span></span>
<span data-ttu-id="32a43-110">Atualizar pool de nós em um cluster gerenciado.</span><span class="sxs-lookup"><span data-stu-id="32a43-110">Update node pool in a managed cluster.</span></span>

## <span data-ttu-id="32a43-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="32a43-111">EXAMPLES</span></span>

### <span data-ttu-id="32a43-112">Alterar a contagem de minimuns para 5 para pool de nós especificado</span><span class="sxs-lookup"><span data-stu-id="32a43-112">Change minimun count to 5 for specified node pool</span></span>
```powershell
PS C:\> Update-AzAksNodePool -ResourceGroupName myResourceGroup -ClusterName myCluster -Name linuxpool -MinCount 5
```

## <span data-ttu-id="32a43-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="32a43-113">PARAMETERS</span></span>

### <span data-ttu-id="32a43-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="32a43-114">-AsJob</span></span>
<span data-ttu-id="32a43-115">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="32a43-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="32a43-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="32a43-116">-ClusterName</span></span>
<span data-ttu-id="32a43-117">O nome do recurso de cluster gerenciado.</span><span class="sxs-lookup"><span data-stu-id="32a43-117">The name of the managed cluster resource.</span></span>

```yaml
Type: System.String
Parameter Sets: defaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32a43-118">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="32a43-118">-ClusterObject</span></span>
<span data-ttu-id="32a43-119">O objeto cluster</span><span class="sxs-lookup"><span data-stu-id="32a43-119">The cluster object</span></span>

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

### <span data-ttu-id="32a43-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32a43-120">-DefaultProfile</span></span>
<span data-ttu-id="32a43-121">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="32a43-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="32a43-122">-EnableAutoScaling</span><span class="sxs-lookup"><span data-stu-id="32a43-122">-EnableAutoScaling</span></span>
<span data-ttu-id="32a43-123">Se deve habilitar o dimensionador automático</span><span class="sxs-lookup"><span data-stu-id="32a43-123">Whether to enable auto-scaler</span></span>

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

### <span data-ttu-id="32a43-124">-Force</span><span class="sxs-lookup"><span data-stu-id="32a43-124">-Force</span></span>
<span data-ttu-id="32a43-125">Atualizar pool de nós sem prompt</span><span class="sxs-lookup"><span data-stu-id="32a43-125">Update node pool without prompt</span></span>

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

### <span data-ttu-id="32a43-126">-Id</span><span class="sxs-lookup"><span data-stu-id="32a43-126">-Id</span></span>
<span data-ttu-id="32a43-127">ID de um pool de nós no cluster kubernetes gerenciado</span><span class="sxs-lookup"><span data-stu-id="32a43-127">Id of an node pool in managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32a43-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="32a43-128">-InputObject</span></span>
<span data-ttu-id="32a43-129">Um objeto PSAgentPool, normalmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="32a43-129">A PSAgentPool object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="32a43-130">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="32a43-130">-KubernetesVersion</span></span>
<span data-ttu-id="32a43-131">A versão do Kubernetes a ser usada para criar o cluster.</span><span class="sxs-lookup"><span data-stu-id="32a43-131">The version of Kubernetes to use for creating the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32a43-132">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="32a43-132">-MaxCount</span></span>
<span data-ttu-id="32a43-133">Número máximo de nós para dimensionamento automático</span><span class="sxs-lookup"><span data-stu-id="32a43-133">Maximum number of nodes for auto-scaling</span></span>

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

### <span data-ttu-id="32a43-134">-MinCount</span><span class="sxs-lookup"><span data-stu-id="32a43-134">-MinCount</span></span>
<span data-ttu-id="32a43-135">Número mínimo de nós para dimensionamento automático.</span><span class="sxs-lookup"><span data-stu-id="32a43-135">Minimum number of nodes for auto-scaling.</span></span>

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

### <span data-ttu-id="32a43-136">-Name</span><span class="sxs-lookup"><span data-stu-id="32a43-136">-Name</span></span>
<span data-ttu-id="32a43-137">O nome do pool de nós.</span><span class="sxs-lookup"><span data-stu-id="32a43-137">The name of the node pool.</span></span>

```yaml
Type: System.String
Parameter Sets: defaultParameterSet, ParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32a43-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32a43-138">-ResourceGroupName</span></span>
<span data-ttu-id="32a43-139">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="32a43-139">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: defaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32a43-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="32a43-140">-Confirm</span></span>
<span data-ttu-id="32a43-141">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="32a43-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32a43-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32a43-142">-WhatIf</span></span>
<span data-ttu-id="32a43-143">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="32a43-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32a43-144">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="32a43-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32a43-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32a43-145">CommonParameters</span></span>
<span data-ttu-id="32a43-146">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32a43-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32a43-147">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="32a43-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32a43-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="32a43-148">INPUTS</span></span>

### <span data-ttu-id="32a43-149">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span><span class="sxs-lookup"><span data-stu-id="32a43-149">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

### <span data-ttu-id="32a43-150">System.String</span><span class="sxs-lookup"><span data-stu-id="32a43-150">System.String</span></span>

## <span data-ttu-id="32a43-151">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="32a43-151">OUTPUTS</span></span>

### <span data-ttu-id="32a43-152">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span><span class="sxs-lookup"><span data-stu-id="32a43-152">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

## <span data-ttu-id="32a43-153">NOTES</span><span class="sxs-lookup"><span data-stu-id="32a43-153">NOTES</span></span>

## <span data-ttu-id="32a43-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="32a43-154">RELATED LINKS</span></span>
