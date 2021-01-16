---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/remove-azaksnodepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Remove-AzAksNodePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Remove-AzAksNodePool.md
ms.openlocfilehash: 13bc647a0b2cbbc415c12aabb9e14016e3d34149
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98261097"
---
# <span data-ttu-id="5fd9f-101">Remove-AzAksNodePool</span><span class="sxs-lookup"><span data-stu-id="5fd9f-101">Remove-AzAksNodePool</span></span>

## <span data-ttu-id="5fd9f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5fd9f-102">SYNOPSIS</span></span>
<span data-ttu-id="5fd9f-103">Exclua o pool de nós do cluster gerenciado.</span><span class="sxs-lookup"><span data-stu-id="5fd9f-103">Delete node pool from managed cluster.</span></span>

## <span data-ttu-id="5fd9f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5fd9f-104">SYNTAX</span></span>

### <span data-ttu-id="5fd9f-105">GroupNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="5fd9f-105">GroupNameParameterSet (Default)</span></span>
```
Remove-AzAksNodePool [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String> [-PassThru]
 [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5fd9f-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5fd9f-106">InputObjectParameterSet</span></span>
```
Remove-AzAksNodePool -InputObject <PSNodePool> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5fd9f-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5fd9f-107">IdParameterSet</span></span>
```
Remove-AzAksNodePool [-Id] <String> [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5fd9f-108">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5fd9f-108">ParentObjectParameterSet</span></span>
```
Remove-AzAksNodePool [-Name] <String> -ClusterObject <PSKubernetesCluster> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5fd9f-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5fd9f-109">DESCRIPTION</span></span>
<span data-ttu-id="5fd9f-110">Exclua o pool de nós do cluster gerenciado.</span><span class="sxs-lookup"><span data-stu-id="5fd9f-110">Delete node pool from managed cluster.</span></span>

## <span data-ttu-id="5fd9f-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5fd9f-111">EXAMPLES</span></span>

### <span data-ttu-id="5fd9f-112">Excluir o pool de nós especificado</span><span class="sxs-lookup"><span data-stu-id="5fd9f-112">Delete specified node pool</span></span>
```powershell
PS C:\> Remove-AzAksNodePool -ResourceGroupName myResourceGroup -CulsterName myCluster -Name winpool
```

## <span data-ttu-id="5fd9f-113">OS</span><span class="sxs-lookup"><span data-stu-id="5fd9f-113">PARAMETERS</span></span>

### <span data-ttu-id="5fd9f-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5fd9f-114">-AsJob</span></span>
<span data-ttu-id="5fd9f-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="5fd9f-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5fd9f-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="5fd9f-116">-ClusterName</span></span>
<span data-ttu-id="5fd9f-117">Nome do seu cluster gerenciado do kubernetes</span><span class="sxs-lookup"><span data-stu-id="5fd9f-117">Name of your managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="5fd9f-118">-Clusterobject</span><span class="sxs-lookup"><span data-stu-id="5fd9f-118">-ClusterObject</span></span>
<span data-ttu-id="5fd9f-119">O objeto de cluster.</span><span class="sxs-lookup"><span data-stu-id="5fd9f-119">The cluster object.</span></span>

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

### <span data-ttu-id="5fd9f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fd9f-120">-DefaultProfile</span></span>
<span data-ttu-id="5fd9f-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5fd9f-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5fd9f-122">-Force</span><span class="sxs-lookup"><span data-stu-id="5fd9f-122">-Force</span></span>
<span data-ttu-id="5fd9f-123">Remover pool de nós sem solicitação</span><span class="sxs-lookup"><span data-stu-id="5fd9f-123">Remove node pool without prompt</span></span>

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

### <span data-ttu-id="5fd9f-124">-ID</span><span class="sxs-lookup"><span data-stu-id="5fd9f-124">-Id</span></span>
<span data-ttu-id="5fd9f-125">ID de um pool de nós no cluster de kubernetes gerenciados</span><span class="sxs-lookup"><span data-stu-id="5fd9f-125">Id of an node pool in managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="5fd9f-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5fd9f-126">-InputObject</span></span>
<span data-ttu-id="5fd9f-127">Um objeto PSAgentPool, normalmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="5fd9f-127">A PSAgentPool object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="5fd9f-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="5fd9f-128">-Name</span></span>
<span data-ttu-id="5fd9f-129">Nome do pool de nós</span><span class="sxs-lookup"><span data-stu-id="5fd9f-129">Name of your node pool</span></span>

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

### <span data-ttu-id="5fd9f-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5fd9f-130">-PassThru</span></span>
<span data-ttu-id="5fd9f-131">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="5fd9f-131">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="5fd9f-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5fd9f-132">-ResourceGroupName</span></span>
<span data-ttu-id="5fd9f-133">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="5fd9f-133">Resource group name</span></span>

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

### <span data-ttu-id="5fd9f-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5fd9f-134">-Confirm</span></span>
<span data-ttu-id="5fd9f-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5fd9f-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5fd9f-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5fd9f-136">-WhatIf</span></span>
<span data-ttu-id="5fd9f-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5fd9f-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5fd9f-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5fd9f-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5fd9f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fd9f-139">CommonParameters</span></span>
<span data-ttu-id="5fd9f-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5fd9f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fd9f-141">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5fd9f-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fd9f-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5fd9f-142">INPUTS</span></span>

### <span data-ttu-id="5fd9f-143">Microsoft. Azure. Commands. AKs. Models. PSNodePool</span><span class="sxs-lookup"><span data-stu-id="5fd9f-143">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

### <span data-ttu-id="5fd9f-144">System. String</span><span class="sxs-lookup"><span data-stu-id="5fd9f-144">System.String</span></span>

## <span data-ttu-id="5fd9f-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5fd9f-145">OUTPUTS</span></span>

### <span data-ttu-id="5fd9f-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5fd9f-146">System.Boolean</span></span>

## <span data-ttu-id="5fd9f-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5fd9f-147">NOTES</span></span>

## <span data-ttu-id="5fd9f-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5fd9f-148">RELATED LINKS</span></span>
