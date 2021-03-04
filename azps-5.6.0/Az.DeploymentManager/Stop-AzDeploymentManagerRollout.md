---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/stop-azdeploymentmanagerrollout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Stop-AzDeploymentManagerRollout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Stop-AzDeploymentManagerRollout.md
ms.openlocfilehash: f053adcd90b013df6f1678ed6468b2efa26d3ff4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886646"
---
# <span data-ttu-id="1481c-101">Stop-AzDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="1481c-101">Stop-AzDeploymentManagerRollout</span></span>

## <span data-ttu-id="1481c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1481c-102">SYNOPSIS</span></span>
<span data-ttu-id="1481c-103">Interrompe a rolagem.</span><span class="sxs-lookup"><span data-stu-id="1481c-103">Stops the rollout.</span></span>

## <span data-ttu-id="1481c-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="1481c-104">SYNTAX</span></span>

### <span data-ttu-id="1481c-105">Interativo (Padrão)</span><span class="sxs-lookup"><span data-stu-id="1481c-105">Interactive (Default)</span></span>
```
Stop-AzDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1481c-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="1481c-106">ResourceId</span></span>
```
Stop-AzDeploymentManagerRollout [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1481c-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="1481c-107">InputObject</span></span>
```
Stop-AzDeploymentManagerRollout [-InputObject] <PSRollout> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1481c-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="1481c-108">DESCRIPTION</span></span>
<span data-ttu-id="1481c-109">O cmdlet **Stop-AzDeploymentManagerRollout** interrompe uma versão em andamento e retorna um objeto que representa o estado atual da rollout.</span><span class="sxs-lookup"><span data-stu-id="1481c-109">The **Stop-AzDeploymentManagerRollout** cmdlet stops a rollout in progress and returns an object that represents the current state of the rollout.</span></span>
<span data-ttu-id="1481c-110">Especifique a distribuição pelo nome e o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1481c-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="1481c-111">Como alternativa, você pode fornecer o objeto Rollout ou ResourceId.</span><span class="sxs-lookup"><span data-stu-id="1481c-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>

<span data-ttu-id="1481c-112">Observe que, depois que uma adoção é interrompida, ela não pode ser retomada ou reiniciada.</span><span class="sxs-lookup"><span data-stu-id="1481c-112">Note that once a rollout is stopped, it cannot be resumed or restarted.</span></span> <span data-ttu-id="1481c-113">Você só pode criar uma nova versão.</span><span class="sxs-lookup"><span data-stu-id="1481c-113">You can only create a new rollout.</span></span>

## <span data-ttu-id="1481c-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1481c-114">EXAMPLES</span></span>

### <span data-ttu-id="1481c-115">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1481c-115">Example 1</span></span>
```powershell
PS C:\> Stop-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout -SkipSucceeded
```

<span data-ttu-id="1481c-116">Este comando interrompe um lançamento chamado ContosoRollout no ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="1481c-116">This command stops a rollout named ContosoRollout in the ContosoResourceGroup.</span></span> 

### <span data-ttu-id="1481c-117">Exemplo 2: Interromper uma distribuição usando o identificador de recurso</span><span class="sxs-lookup"><span data-stu-id="1481c-117">Example 2: Stop a rollout using the resource identifier</span></span>
```powershell
PS C:\> Restart-AzDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="1481c-118">Este comando interrompe um lançamento chamado ContosoRollout no ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="1481c-118">This command stops a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="1481c-119">Exemplo 3: Pare uma rolagem usando o objeto de lançamento.</span><span class="sxs-lookup"><span data-stu-id="1481c-119">Example 3: Stop a rollout using the rollout object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -InputObject $rolloutObject
```

<span data-ttu-id="1481c-120">Este comando interrompe uma distribuição cujo nome e ResourceGroup corresponderem às propriedades Name e ResourceGroupName do $rolloutObject, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="1481c-120">This command stops a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="1481c-121">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="1481c-121">PARAMETERS</span></span>

### <span data-ttu-id="1481c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1481c-122">-DefaultProfile</span></span>
<span data-ttu-id="1481c-123">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1481c-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1481c-124">-Force</span><span class="sxs-lookup"><span data-stu-id="1481c-124">-Force</span></span>
<span data-ttu-id="1481c-125">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="1481c-125">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="1481c-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1481c-126">-InputObject</span></span>
<span data-ttu-id="1481c-127">A adoção a ser removida.</span><span class="sxs-lookup"><span data-stu-id="1481c-127">The rollout to be removed.</span></span>

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

### <span data-ttu-id="1481c-128">-Name</span><span class="sxs-lookup"><span data-stu-id="1481c-128">-Name</span></span>
<span data-ttu-id="1481c-129">O nome da apostila.</span><span class="sxs-lookup"><span data-stu-id="1481c-129">The name of the rollout.</span></span>

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

### <span data-ttu-id="1481c-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1481c-130">-ResourceGroupName</span></span>
<span data-ttu-id="1481c-131">O grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1481c-131">The resource group.</span></span>

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

### <span data-ttu-id="1481c-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1481c-132">-ResourceId</span></span>
<span data-ttu-id="1481c-133">O identificador de recurso.</span><span class="sxs-lookup"><span data-stu-id="1481c-133">The resource identifier.</span></span>

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

### <span data-ttu-id="1481c-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1481c-134">-Confirm</span></span>
<span data-ttu-id="1481c-135">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1481c-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1481c-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1481c-136">-WhatIf</span></span>
<span data-ttu-id="1481c-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1481c-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1481c-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1481c-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1481c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1481c-139">CommonParameters</span></span>
<span data-ttu-id="1481c-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1481c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1481c-141">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1481c-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1481c-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1481c-142">INPUTS</span></span>

### <span data-ttu-id="1481c-143">System.String</span><span class="sxs-lookup"><span data-stu-id="1481c-143">System.String</span></span>

### <span data-ttu-id="1481c-144">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span><span class="sxs-lookup"><span data-stu-id="1481c-144">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="1481c-145">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="1481c-145">OUTPUTS</span></span>

### <span data-ttu-id="1481c-146">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span><span class="sxs-lookup"><span data-stu-id="1481c-146">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="1481c-147">NOTES</span><span class="sxs-lookup"><span data-stu-id="1481c-147">NOTES</span></span>

## <span data-ttu-id="1481c-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1481c-148">RELATED LINKS</span></span>
