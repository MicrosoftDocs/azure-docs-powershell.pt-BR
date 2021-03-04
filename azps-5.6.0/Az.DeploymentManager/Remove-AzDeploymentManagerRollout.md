---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerrollout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerRollout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerRollout.md
ms.openlocfilehash: 3ade9bfd724a84e162c0cedd937f2255ebb5b6a4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888973"
---
# <span data-ttu-id="ee8d8-101">Remove-AzDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="ee8d8-101">Remove-AzDeploymentManagerRollout</span></span>

## <span data-ttu-id="ee8d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee8d8-102">SYNOPSIS</span></span>
<span data-ttu-id="ee8d8-103">Exclui a adoção.</span><span class="sxs-lookup"><span data-stu-id="ee8d8-103">Deletes the rollout.</span></span>

## <span data-ttu-id="ee8d8-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ee8d8-104">SYNTAX</span></span>

### <span data-ttu-id="ee8d8-105">Interativo (Padrão)</span><span class="sxs-lookup"><span data-stu-id="ee8d8-105">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee8d8-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="ee8d8-106">ResourceId</span></span>
```
Remove-AzDeploymentManagerRollout [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee8d8-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="ee8d8-107">InputObject</span></span>
```
Remove-AzDeploymentManagerRollout [-InputObject] <PSRollout> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee8d8-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ee8d8-108">DESCRIPTION</span></span>
<span data-ttu-id="ee8d8-109">O cmdlet **Remove-AzDeploymentManagerRollout** exclui uma rolagem em um estado de terminal.</span><span class="sxs-lookup"><span data-stu-id="ee8d8-109">The **Remove-AzDeploymentManagerRollout** cmdlet deletes a rollout in a terminal state.</span></span>
<span data-ttu-id="ee8d8-110">Especifique a distribuição pelo nome e o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ee8d8-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="ee8d8-111">Como alternativa, você pode fornecer o objeto Rollout ou ResourceId.</span><span class="sxs-lookup"><span data-stu-id="ee8d8-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>

## <span data-ttu-id="ee8d8-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ee8d8-112">EXAMPLES</span></span>

### <span data-ttu-id="ee8d8-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ee8d8-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout
```

<span data-ttu-id="ee8d8-114">Este comando exclui um lançamento chamado ContosoRollout no ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="ee8d8-114">This command deletes a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="ee8d8-115">Exemplo 2: Excluir uma distribuição usando o identificador de recurso</span><span class="sxs-lookup"><span data-stu-id="ee8d8-115">Example 2: Delete a rollout using the resource identifier</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="ee8d8-116">Este comando exclui um lançamento chamado ContosoRollout no ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="ee8d8-116">This command deletes a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="ee8d8-117">Exemplo 3: Excluir uma apostila usando o objeto de lançamento.</span><span class="sxs-lookup"><span data-stu-id="ee8d8-117">Example 3: Delete a rollout using the rollout object.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerRollout -InputObject $rolloutObject
```

<span data-ttu-id="ee8d8-118">Este comando exclui uma distribuição cujo nome e ResourceGroup corresponderem às propriedades Name e ResourceGroupName do $rolloutObject, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="ee8d8-118">This command deletes a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="ee8d8-119">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ee8d8-119">PARAMETERS</span></span>

### <span data-ttu-id="ee8d8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee8d8-120">-DefaultProfile</span></span>
<span data-ttu-id="ee8d8-121">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ee8d8-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee8d8-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ee8d8-122">-InputObject</span></span>
<span data-ttu-id="ee8d8-123">O recurso a ser removido.</span><span class="sxs-lookup"><span data-stu-id="ee8d8-123">The resource to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ee8d8-124">-Name</span><span class="sxs-lookup"><span data-stu-id="ee8d8-124">-Name</span></span>
<span data-ttu-id="ee8d8-125">O nome da apostila.</span><span class="sxs-lookup"><span data-stu-id="ee8d8-125">The name of the rollout.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee8d8-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ee8d8-126">-PassThru</span></span>
<span data-ttu-id="ee8d8-127">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="ee8d8-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="ee8d8-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee8d8-128">-ResourceGroupName</span></span>
<span data-ttu-id="ee8d8-129">O grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ee8d8-129">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee8d8-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ee8d8-130">-ResourceId</span></span>
<span data-ttu-id="ee8d8-131">O identificador de recurso.</span><span class="sxs-lookup"><span data-stu-id="ee8d8-131">The resource identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee8d8-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ee8d8-132">-Confirm</span></span>
<span data-ttu-id="ee8d8-133">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ee8d8-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee8d8-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee8d8-134">-WhatIf</span></span>
<span data-ttu-id="ee8d8-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ee8d8-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee8d8-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ee8d8-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee8d8-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee8d8-137">CommonParameters</span></span>
<span data-ttu-id="ee8d8-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee8d8-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee8d8-139">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ee8d8-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee8d8-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ee8d8-140">INPUTS</span></span>

### <span data-ttu-id="ee8d8-141">System.String</span><span class="sxs-lookup"><span data-stu-id="ee8d8-141">System.String</span></span>

### <span data-ttu-id="ee8d8-142">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span><span class="sxs-lookup"><span data-stu-id="ee8d8-142">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="ee8d8-143">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ee8d8-143">OUTPUTS</span></span>

### <span data-ttu-id="ee8d8-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ee8d8-144">System.Boolean</span></span>

## <span data-ttu-id="ee8d8-145">NOTES</span><span class="sxs-lookup"><span data-stu-id="ee8d8-145">NOTES</span></span>

## <span data-ttu-id="ee8d8-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ee8d8-146">RELATED LINKS</span></span>
