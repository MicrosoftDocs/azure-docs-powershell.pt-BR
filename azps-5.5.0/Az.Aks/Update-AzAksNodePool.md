---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/update-azaksnodepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Update-AzAksNodePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Update-AzAksNodePool.md
ms.openlocfilehash: a3849a07f83cda8876acdf87015e8f2fc9fe81b5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114876"
---
# <span data-ttu-id="24763-101">Update-AzAksNodePool</span><span class="sxs-lookup"><span data-stu-id="24763-101">Update-AzAksNodePool</span></span>

## <span data-ttu-id="24763-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="24763-102">SYNOPSIS</span></span>
<span data-ttu-id="24763-103">Atualizar pool de nó em um cluster gerenciado.</span><span class="sxs-lookup"><span data-stu-id="24763-103">Update node pool in a managed cluster.</span></span>

## <span data-ttu-id="24763-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="24763-104">SYNTAX</span></span>

### <span data-ttu-id="24763-105">defaultParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="24763-105">defaultParameterSet (Default)</span></span>
```
Update-AzAksNodePool -ResourceGroupName <String> -ClusterName <String> -Name <String> [-AsJob] [-Force]
 [-KubernetesVersion <String>] [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24763-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="24763-106">ParentObjectParameterSet</span></span>
```
Update-AzAksNodePool -Name <String> -ClusterObject <PSKubernetesCluster> [-AsJob] [-Force]
 [-KubernetesVersion <String>] [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24763-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="24763-107">InputObjectParameterSet</span></span>
```
Update-AzAksNodePool -InputObject <PSNodePool> [-AsJob] [-Force] [-KubernetesVersion <String>]
 [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24763-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="24763-108">IdParameterSet</span></span>
```
Update-AzAksNodePool -Id <String> [-AsJob] [-Force] [-KubernetesVersion <String>] [-MinCount <Int32>]
 [-MaxCount <Int32>] [-EnableAutoScaling] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="24763-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="24763-109">DESCRIPTION</span></span>
<span data-ttu-id="24763-110">Atualizar pool de nó em um cluster gerenciado.</span><span class="sxs-lookup"><span data-stu-id="24763-110">Update node pool in a managed cluster.</span></span>

## <span data-ttu-id="24763-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="24763-111">EXAMPLES</span></span>

### <span data-ttu-id="24763-112">Alterar a contagem de mínimos para 5 para pool de nó especificado</span><span class="sxs-lookup"><span data-stu-id="24763-112">Change minimun count to 5 for specified node pool</span></span>
```powershell
PS C:\> Update-AzAksNodePool -ResourceGroupName myResourceGroup -ClusterName myCluster -Name linuxpool -MinCount 5
```

## <span data-ttu-id="24763-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="24763-113">PARAMETERS</span></span>

### <span data-ttu-id="24763-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="24763-114">-AsJob</span></span>
<span data-ttu-id="24763-115">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="24763-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="24763-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="24763-116">-ClusterName</span></span>
<span data-ttu-id="24763-117">O nome do recurso de cluster gerenciado.</span><span class="sxs-lookup"><span data-stu-id="24763-117">The name of the managed cluster resource.</span></span>

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

### <span data-ttu-id="24763-118">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="24763-118">-ClusterObject</span></span>
<span data-ttu-id="24763-119">O objeto de cluster</span><span class="sxs-lookup"><span data-stu-id="24763-119">The cluster object</span></span>

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

### <span data-ttu-id="24763-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24763-120">-DefaultProfile</span></span>
<span data-ttu-id="24763-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="24763-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24763-122">-EnableAutoScaling</span><span class="sxs-lookup"><span data-stu-id="24763-122">-EnableAutoScaling</span></span>
<span data-ttu-id="24763-123">Se você quer habilitar o dimensionador automático</span><span class="sxs-lookup"><span data-stu-id="24763-123">Whether to enable auto-scaler</span></span>

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

### <span data-ttu-id="24763-124">-Forçar</span><span class="sxs-lookup"><span data-stu-id="24763-124">-Force</span></span>
<span data-ttu-id="24763-125">Atualizar pool de nó sem aviso</span><span class="sxs-lookup"><span data-stu-id="24763-125">Update node pool without prompt</span></span>

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

### <span data-ttu-id="24763-126">-ID</span><span class="sxs-lookup"><span data-stu-id="24763-126">-Id</span></span>
<span data-ttu-id="24763-127">ID de um pool de nó no cluster Desernetes gerenciados</span><span class="sxs-lookup"><span data-stu-id="24763-127">Id of an node pool in managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="24763-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="24763-128">-InputObject</span></span>
<span data-ttu-id="24763-129">Um objeto PSAgentPool, normalmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="24763-129">A PSAgentPool object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="24763-130">-LtdernetesVersion</span><span class="sxs-lookup"><span data-stu-id="24763-130">-KubernetesVersion</span></span>
<span data-ttu-id="24763-131">A versão do Queernetes a ser usada para criar o cluster.</span><span class="sxs-lookup"><span data-stu-id="24763-131">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="24763-132">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="24763-132">-MaxCount</span></span>
<span data-ttu-id="24763-133">Número máximo de nós para dimensionamento automático</span><span class="sxs-lookup"><span data-stu-id="24763-133">Maximum number of nodes for auto-scaling</span></span>

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

### <span data-ttu-id="24763-134">-MinCount</span><span class="sxs-lookup"><span data-stu-id="24763-134">-MinCount</span></span>
<span data-ttu-id="24763-135">Número mínimo de nós para dimensionamento automático.</span><span class="sxs-lookup"><span data-stu-id="24763-135">Minimum number of nodes for auto-scaling.</span></span>

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

### <span data-ttu-id="24763-136">-Nome</span><span class="sxs-lookup"><span data-stu-id="24763-136">-Name</span></span>
<span data-ttu-id="24763-137">O nome do pool de nó.</span><span class="sxs-lookup"><span data-stu-id="24763-137">The name of the node pool.</span></span>

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

### <span data-ttu-id="24763-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24763-138">-ResourceGroupName</span></span>
<span data-ttu-id="24763-139">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="24763-139">The name of the resource group.</span></span>

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

### <span data-ttu-id="24763-140">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="24763-140">-Confirm</span></span>
<span data-ttu-id="24763-141">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24763-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24763-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24763-142">-WhatIf</span></span>
<span data-ttu-id="24763-143">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="24763-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24763-144">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="24763-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24763-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24763-145">CommonParameters</span></span>
<span data-ttu-id="24763-146">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24763-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24763-147">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="24763-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24763-148">Entradas</span><span class="sxs-lookup"><span data-stu-id="24763-148">INPUTS</span></span>

### <span data-ttu-id="24763-149">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span><span class="sxs-lookup"><span data-stu-id="24763-149">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

### <span data-ttu-id="24763-150">System.String</span><span class="sxs-lookup"><span data-stu-id="24763-150">System.String</span></span>

## <span data-ttu-id="24763-151">Saídas</span><span class="sxs-lookup"><span data-stu-id="24763-151">OUTPUTS</span></span>

### <span data-ttu-id="24763-152">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span><span class="sxs-lookup"><span data-stu-id="24763-152">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

## <span data-ttu-id="24763-153">Notas</span><span class="sxs-lookup"><span data-stu-id="24763-153">NOTES</span></span>

## <span data-ttu-id="24763-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="24763-154">RELATED LINKS</span></span>
