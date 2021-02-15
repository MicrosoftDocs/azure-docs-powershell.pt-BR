---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/remove-azaksnodepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Remove-AzAksNodePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Remove-AzAksNodePool.md
ms.openlocfilehash: 13bc647a0b2cbbc415c12aabb9e14016e3d34149
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114880"
---
# <span data-ttu-id="ed2cd-101">Remove-AzAksNodePool</span><span class="sxs-lookup"><span data-stu-id="ed2cd-101">Remove-AzAksNodePool</span></span>

## <span data-ttu-id="ed2cd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ed2cd-102">SYNOPSIS</span></span>
<span data-ttu-id="ed2cd-103">Excluir pool de nó do cluster gerenciado.</span><span class="sxs-lookup"><span data-stu-id="ed2cd-103">Delete node pool from managed cluster.</span></span>

## <span data-ttu-id="ed2cd-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ed2cd-104">SYNTAX</span></span>

### <span data-ttu-id="ed2cd-105">GroupNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="ed2cd-105">GroupNameParameterSet (Default)</span></span>
```
Remove-AzAksNodePool [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String> [-PassThru]
 [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed2cd-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ed2cd-106">InputObjectParameterSet</span></span>
```
Remove-AzAksNodePool -InputObject <PSNodePool> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed2cd-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ed2cd-107">IdParameterSet</span></span>
```
Remove-AzAksNodePool [-Id] <String> [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed2cd-108">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ed2cd-108">ParentObjectParameterSet</span></span>
```
Remove-AzAksNodePool [-Name] <String> -ClusterObject <PSKubernetesCluster> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed2cd-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="ed2cd-109">DESCRIPTION</span></span>
<span data-ttu-id="ed2cd-110">Excluir pool de nó do cluster gerenciado.</span><span class="sxs-lookup"><span data-stu-id="ed2cd-110">Delete node pool from managed cluster.</span></span>

## <span data-ttu-id="ed2cd-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ed2cd-111">EXAMPLES</span></span>

### <span data-ttu-id="ed2cd-112">Excluir pool de nó especificado</span><span class="sxs-lookup"><span data-stu-id="ed2cd-112">Delete specified node pool</span></span>
```powershell
PS C:\> Remove-AzAksNodePool -ResourceGroupName myResourceGroup -CulsterName myCluster -Name winpool
```

## <span data-ttu-id="ed2cd-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ed2cd-113">PARAMETERS</span></span>

### <span data-ttu-id="ed2cd-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ed2cd-114">-AsJob</span></span>
<span data-ttu-id="ed2cd-115">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="ed2cd-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ed2cd-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="ed2cd-116">-ClusterName</span></span>
<span data-ttu-id="ed2cd-117">Nome do cluster Desarnetes gerenciados</span><span class="sxs-lookup"><span data-stu-id="ed2cd-117">Name of your managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="ed2cd-118">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="ed2cd-118">-ClusterObject</span></span>
<span data-ttu-id="ed2cd-119">O objeto de cluster.</span><span class="sxs-lookup"><span data-stu-id="ed2cd-119">The cluster object.</span></span>

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

### <span data-ttu-id="ed2cd-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed2cd-120">-DefaultProfile</span></span>
<span data-ttu-id="ed2cd-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ed2cd-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed2cd-122">-Forçar</span><span class="sxs-lookup"><span data-stu-id="ed2cd-122">-Force</span></span>
<span data-ttu-id="ed2cd-123">Remover pool de nó sem aviso</span><span class="sxs-lookup"><span data-stu-id="ed2cd-123">Remove node pool without prompt</span></span>

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

### <span data-ttu-id="ed2cd-124">-ID</span><span class="sxs-lookup"><span data-stu-id="ed2cd-124">-Id</span></span>
<span data-ttu-id="ed2cd-125">ID de um pool de nó no cluster Desernetes gerenciados</span><span class="sxs-lookup"><span data-stu-id="ed2cd-125">Id of an node pool in managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="ed2cd-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ed2cd-126">-InputObject</span></span>
<span data-ttu-id="ed2cd-127">Um objeto PSAgentPool, normalmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="ed2cd-127">A PSAgentPool object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="ed2cd-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="ed2cd-128">-Name</span></span>
<span data-ttu-id="ed2cd-129">Nome do pool de nó</span><span class="sxs-lookup"><span data-stu-id="ed2cd-129">Name of your node pool</span></span>

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

### <span data-ttu-id="ed2cd-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ed2cd-130">-PassThru</span></span>
<span data-ttu-id="ed2cd-131">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="ed2cd-131">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="ed2cd-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed2cd-132">-ResourceGroupName</span></span>
<span data-ttu-id="ed2cd-133">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="ed2cd-133">Resource group name</span></span>

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

### <span data-ttu-id="ed2cd-134">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="ed2cd-134">-Confirm</span></span>
<span data-ttu-id="ed2cd-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ed2cd-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed2cd-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed2cd-136">-WhatIf</span></span>
<span data-ttu-id="ed2cd-137">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="ed2cd-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed2cd-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ed2cd-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed2cd-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed2cd-139">CommonParameters</span></span>
<span data-ttu-id="ed2cd-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed2cd-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed2cd-141">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ed2cd-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed2cd-142">Entradas</span><span class="sxs-lookup"><span data-stu-id="ed2cd-142">INPUTS</span></span>

### <span data-ttu-id="ed2cd-143">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span><span class="sxs-lookup"><span data-stu-id="ed2cd-143">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

### <span data-ttu-id="ed2cd-144">System.String</span><span class="sxs-lookup"><span data-stu-id="ed2cd-144">System.String</span></span>

## <span data-ttu-id="ed2cd-145">Saídas</span><span class="sxs-lookup"><span data-stu-id="ed2cd-145">OUTPUTS</span></span>

### <span data-ttu-id="ed2cd-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ed2cd-146">System.Boolean</span></span>

## <span data-ttu-id="ed2cd-147">Notas</span><span class="sxs-lookup"><span data-stu-id="ed2cd-147">NOTES</span></span>

## <span data-ttu-id="ed2cd-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ed2cd-148">RELATED LINKS</span></span>
