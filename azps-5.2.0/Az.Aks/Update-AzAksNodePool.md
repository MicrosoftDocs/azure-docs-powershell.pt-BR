---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/update-azaksnodepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Update-AzAksNodePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Update-AzAksNodePool.md
ms.openlocfilehash: a3849a07f83cda8876acdf87015e8f2fc9fe81b5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98260853"
---
# <span data-ttu-id="a8115-101">Update-AzAksNodePool</span><span class="sxs-lookup"><span data-stu-id="a8115-101">Update-AzAksNodePool</span></span>

## <span data-ttu-id="a8115-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a8115-102">SYNOPSIS</span></span>
<span data-ttu-id="a8115-103">Atualize o pool de nós em um cluster gerenciado.</span><span class="sxs-lookup"><span data-stu-id="a8115-103">Update node pool in a managed cluster.</span></span>

## <span data-ttu-id="a8115-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a8115-104">SYNTAX</span></span>

### <span data-ttu-id="a8115-105">DefaultParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="a8115-105">defaultParameterSet (Default)</span></span>
```
Update-AzAksNodePool -ResourceGroupName <String> -ClusterName <String> -Name <String> [-AsJob] [-Force]
 [-KubernetesVersion <String>] [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8115-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a8115-106">ParentObjectParameterSet</span></span>
```
Update-AzAksNodePool -Name <String> -ClusterObject <PSKubernetesCluster> [-AsJob] [-Force]
 [-KubernetesVersion <String>] [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8115-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a8115-107">InputObjectParameterSet</span></span>
```
Update-AzAksNodePool -InputObject <PSNodePool> [-AsJob] [-Force] [-KubernetesVersion <String>]
 [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8115-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a8115-108">IdParameterSet</span></span>
```
Update-AzAksNodePool -Id <String> [-AsJob] [-Force] [-KubernetesVersion <String>] [-MinCount <Int32>]
 [-MaxCount <Int32>] [-EnableAutoScaling] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a8115-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a8115-109">DESCRIPTION</span></span>
<span data-ttu-id="a8115-110">Atualize o pool de nós em um cluster gerenciado.</span><span class="sxs-lookup"><span data-stu-id="a8115-110">Update node pool in a managed cluster.</span></span>

## <span data-ttu-id="a8115-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a8115-111">EXAMPLES</span></span>

### <span data-ttu-id="a8115-112">Alterar a contagem de Minimun para 5 para o pool de nós especificado</span><span class="sxs-lookup"><span data-stu-id="a8115-112">Change minimun count to 5 for specified node pool</span></span>
```powershell
PS C:\> Update-AzAksNodePool -ResourceGroupName myResourceGroup -ClusterName myCluster -Name linuxpool -MinCount 5
```

## <span data-ttu-id="a8115-113">OS</span><span class="sxs-lookup"><span data-stu-id="a8115-113">PARAMETERS</span></span>

### <span data-ttu-id="a8115-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a8115-114">-AsJob</span></span>
<span data-ttu-id="a8115-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="a8115-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a8115-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="a8115-116">-ClusterName</span></span>
<span data-ttu-id="a8115-117">O nome do recurso de cluster gerenciado.</span><span class="sxs-lookup"><span data-stu-id="a8115-117">The name of the managed cluster resource.</span></span>

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

### <span data-ttu-id="a8115-118">-Clusterobject</span><span class="sxs-lookup"><span data-stu-id="a8115-118">-ClusterObject</span></span>
<span data-ttu-id="a8115-119">O objeto de cluster</span><span class="sxs-lookup"><span data-stu-id="a8115-119">The cluster object</span></span>

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

### <span data-ttu-id="a8115-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8115-120">-DefaultProfile</span></span>
<span data-ttu-id="a8115-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a8115-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a8115-122">-EnableAutoScaling</span><span class="sxs-lookup"><span data-stu-id="a8115-122">-EnableAutoScaling</span></span>
<span data-ttu-id="a8115-123">Se o dimensionador automático deve ser habilitado</span><span class="sxs-lookup"><span data-stu-id="a8115-123">Whether to enable auto-scaler</span></span>

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

### <span data-ttu-id="a8115-124">-Force</span><span class="sxs-lookup"><span data-stu-id="a8115-124">-Force</span></span>
<span data-ttu-id="a8115-125">Atualizar o pool de nós sem avisar</span><span class="sxs-lookup"><span data-stu-id="a8115-125">Update node pool without prompt</span></span>

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

### <span data-ttu-id="a8115-126">-ID</span><span class="sxs-lookup"><span data-stu-id="a8115-126">-Id</span></span>
<span data-ttu-id="a8115-127">ID de um pool de nós no cluster de kubernetes gerenciados</span><span class="sxs-lookup"><span data-stu-id="a8115-127">Id of an node pool in managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="a8115-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a8115-128">-InputObject</span></span>
<span data-ttu-id="a8115-129">Um objeto PSAgentPool, normalmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="a8115-129">A PSAgentPool object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="a8115-130">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="a8115-130">-KubernetesVersion</span></span>
<span data-ttu-id="a8115-131">A versão do kubernetes a ser usada para criar o cluster.</span><span class="sxs-lookup"><span data-stu-id="a8115-131">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="a8115-132">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="a8115-132">-MaxCount</span></span>
<span data-ttu-id="a8115-133">Número máximo de nós para dimensionamento automático</span><span class="sxs-lookup"><span data-stu-id="a8115-133">Maximum number of nodes for auto-scaling</span></span>

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

### <span data-ttu-id="a8115-134">-MinCount</span><span class="sxs-lookup"><span data-stu-id="a8115-134">-MinCount</span></span>
<span data-ttu-id="a8115-135">Número mínimo de nós para dimensionamento automático.</span><span class="sxs-lookup"><span data-stu-id="a8115-135">Minimum number of nodes for auto-scaling.</span></span>

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

### <span data-ttu-id="a8115-136">-Nome</span><span class="sxs-lookup"><span data-stu-id="a8115-136">-Name</span></span>
<span data-ttu-id="a8115-137">O nome do pool de nós.</span><span class="sxs-lookup"><span data-stu-id="a8115-137">The name of the node pool.</span></span>

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

### <span data-ttu-id="a8115-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8115-138">-ResourceGroupName</span></span>
<span data-ttu-id="a8115-139">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a8115-139">The name of the resource group.</span></span>

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

### <span data-ttu-id="a8115-140">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a8115-140">-Confirm</span></span>
<span data-ttu-id="a8115-141">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8115-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8115-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8115-142">-WhatIf</span></span>
<span data-ttu-id="a8115-143">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a8115-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8115-144">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a8115-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8115-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8115-145">CommonParameters</span></span>
<span data-ttu-id="a8115-146">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8115-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8115-147">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a8115-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8115-148">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a8115-148">INPUTS</span></span>

### <span data-ttu-id="a8115-149">Microsoft. Azure. Commands. AKs. Models. PSNodePool</span><span class="sxs-lookup"><span data-stu-id="a8115-149">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

### <span data-ttu-id="a8115-150">System. String</span><span class="sxs-lookup"><span data-stu-id="a8115-150">System.String</span></span>

## <span data-ttu-id="a8115-151">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a8115-151">OUTPUTS</span></span>

### <span data-ttu-id="a8115-152">Microsoft. Azure. Commands. AKs. Models. PSNodePool</span><span class="sxs-lookup"><span data-stu-id="a8115-152">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

## <span data-ttu-id="a8115-153">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a8115-153">NOTES</span></span>

## <span data-ttu-id="a8115-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a8115-154">RELATED LINKS</span></span>
