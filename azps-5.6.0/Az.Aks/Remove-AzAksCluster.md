---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/powershell/module/az.aks/remove-azakscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Remove-AzAksCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Remove-AzAksCluster.md
ms.openlocfilehash: 0f0a1c530e4f02e031307006c0e6bf994f9a7c5f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886804"
---
# <span data-ttu-id="ee57c-101">Remove-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="ee57c-101">Remove-AzAksCluster</span></span>

## <span data-ttu-id="ee57c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee57c-102">SYNOPSIS</span></span>
<span data-ttu-id="ee57c-103">Exclua um cluster kubernetes gerenciado.</span><span class="sxs-lookup"><span data-stu-id="ee57c-103">Delete a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="ee57c-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ee57c-104">SYNTAX</span></span>

### <span data-ttu-id="ee57c-105">GroupNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="ee57c-105">GroupNameParameterSet (Default)</span></span>
```
Remove-AzAksCluster [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee57c-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee57c-106">InputObjectParameterSet</span></span>
```
Remove-AzAksCluster -InputObject <PSKubernetesCluster> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee57c-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee57c-107">IdParameterSet</span></span>
```
Remove-AzAksCluster [-Id] <String> [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee57c-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ee57c-108">DESCRIPTION</span></span>
<span data-ttu-id="ee57c-109">Exclua um cluster kubernetes gerenciado.</span><span class="sxs-lookup"><span data-stu-id="ee57c-109">Delete a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="ee57c-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ee57c-110">EXAMPLES</span></span>

### <span data-ttu-id="ee57c-111">Excluir um cluster kubernetes gerenciado existente</span><span class="sxs-lookup"><span data-stu-id="ee57c-111">Delete an existing managed Kubernetes cluster</span></span>
```powershell
PS C:\> Remove-AzAks -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="ee57c-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ee57c-112">PARAMETERS</span></span>

### <span data-ttu-id="ee57c-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ee57c-113">-AsJob</span></span>
<span data-ttu-id="ee57c-114">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="ee57c-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ee57c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee57c-115">-DefaultProfile</span></span>
<span data-ttu-id="ee57c-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ee57c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee57c-117">-Force</span><span class="sxs-lookup"><span data-stu-id="ee57c-117">-Force</span></span>
<span data-ttu-id="ee57c-118">Remover cluster do Kubernetes gerenciado sem prompt</span><span class="sxs-lookup"><span data-stu-id="ee57c-118">Remove managed Kubernetes cluster without prompt</span></span>

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

### <span data-ttu-id="ee57c-119">-Id</span><span class="sxs-lookup"><span data-stu-id="ee57c-119">-Id</span></span>
<span data-ttu-id="ee57c-120">ID de um cluster kubernetes gerenciado</span><span class="sxs-lookup"><span data-stu-id="ee57c-120">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="ee57c-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ee57c-121">-InputObject</span></span>
<span data-ttu-id="ee57c-122">Um objeto PSKubernetesCluster, normalmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="ee57c-122">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ee57c-123">-Name</span><span class="sxs-lookup"><span data-stu-id="ee57c-123">-Name</span></span>
<span data-ttu-id="ee57c-124">Nome do cluster kubernetes gerenciado</span><span class="sxs-lookup"><span data-stu-id="ee57c-124">Name of your managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="ee57c-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ee57c-125">-PassThru</span></span>
<span data-ttu-id="ee57c-126">Retorna true se a exclusão for bem-sucedida</span><span class="sxs-lookup"><span data-stu-id="ee57c-126">Returns true if deletion is successful</span></span>

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

### <span data-ttu-id="ee57c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee57c-127">-ResourceGroupName</span></span>
<span data-ttu-id="ee57c-128">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="ee57c-128">Resource group name</span></span>

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

### <span data-ttu-id="ee57c-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ee57c-129">-Confirm</span></span>
<span data-ttu-id="ee57c-130">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ee57c-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee57c-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee57c-131">-WhatIf</span></span>
<span data-ttu-id="ee57c-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ee57c-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee57c-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ee57c-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee57c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee57c-134">CommonParameters</span></span>
<span data-ttu-id="ee57c-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee57c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee57c-136">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ee57c-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee57c-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ee57c-137">INPUTS</span></span>

### <span data-ttu-id="ee57c-138">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="ee57c-138">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="ee57c-139">System.String</span><span class="sxs-lookup"><span data-stu-id="ee57c-139">System.String</span></span>

## <span data-ttu-id="ee57c-140">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ee57c-140">OUTPUTS</span></span>

### <span data-ttu-id="ee57c-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ee57c-141">System.Boolean</span></span>

## <span data-ttu-id="ee57c-142">NOTES</span><span class="sxs-lookup"><span data-stu-id="ee57c-142">NOTES</span></span>

## <span data-ttu-id="ee57c-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ee57c-143">RELATED LINKS</span></span>
