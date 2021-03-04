---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/restart-azdeploymentmanagerrollout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Restart-AzDeploymentManagerRollout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Restart-AzDeploymentManagerRollout.md
ms.openlocfilehash: d11a19ed5189220c8f6c327c9483e0e11e671ed8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888965"
---
# <span data-ttu-id="eb49c-101">Restart-AzDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="eb49c-101">Restart-AzDeploymentManagerRollout</span></span>

## <span data-ttu-id="eb49c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eb49c-102">SYNOPSIS</span></span>
<span data-ttu-id="eb49c-103">Reinicia uma rollout com falha.</span><span class="sxs-lookup"><span data-stu-id="eb49c-103">Restarts a failed rollout.</span></span>

## <span data-ttu-id="eb49c-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="eb49c-104">SYNTAX</span></span>

### <span data-ttu-id="eb49c-105">Interativo (Padrão)</span><span class="sxs-lookup"><span data-stu-id="eb49c-105">Interactive (Default)</span></span>
```
Restart-AzDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [-SkipSucceeded]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb49c-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="eb49c-106">ResourceId</span></span>
```
Restart-AzDeploymentManagerRollout [-ResourceId] <String> [-SkipSucceeded]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb49c-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="eb49c-107">InputObject</span></span>
```
Restart-AzDeploymentManagerRollout [-InputObject] <PSRollout> [-SkipSucceeded]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eb49c-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="eb49c-108">DESCRIPTION</span></span>
<span data-ttu-id="eb49c-109">O cmdlet **Restart-AzDeploymentManagerRollout** reinicia uma rollout com falha e retorna um objeto que representa essa rolagem com todas as informações detalhadas sobre o andamento da lançamento.</span><span class="sxs-lookup"><span data-stu-id="eb49c-109">The **Restart-AzDeploymentManagerRollout** cmdlet restarts a failed rollout, and returns an object that represents that rollout with all the detailed information on the progress of the rollout.</span></span>
<span data-ttu-id="eb49c-110">Especifique a distribuição pelo nome e o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="eb49c-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="eb49c-111">Como alternativa, você pode fornecer o objeto Rollout ou ResourceId.</span><span class="sxs-lookup"><span data-stu-id="eb49c-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>
<span data-ttu-id="eb49c-112">O parâmetro opcional SkipSucceeded permite ignorar todas as etapas bem-sucedidas na versão anterior da versão.</span><span class="sxs-lookup"><span data-stu-id="eb49c-112">Optional parameter SkipSucceeded allows you to skip all the succeeded steps in the previous run of the rollout.</span></span>

## <span data-ttu-id="eb49c-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="eb49c-113">EXAMPLES</span></span>

### <span data-ttu-id="eb49c-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="eb49c-114">Example 1</span></span>
```powershell
PS C:\> Restart-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout -SkipSucceeded
```

<span data-ttu-id="eb49c-115">Este comando reinicia um lançamento chamado ContosoRollout no ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="eb49c-115">This command restarts a rollout named ContosoRollout in the ContosoResourceGroup.</span></span> <span data-ttu-id="eb49c-116">O sinalizador SkipSucceeded indica que todas as etapas que já foram realizadas com êxito devem ser ignoradas e a adoção deve continuar a execução de onde falhou pela última vez.</span><span class="sxs-lookup"><span data-stu-id="eb49c-116">The SkipSucceeded flag indicates that all the steps that already ran successfully should be skipped and the rollout should continue execution from where it last failed.</span></span>

### <span data-ttu-id="eb49c-117">Exemplo 2: Reiniciar uma distribuição usando o identificador de recurso</span><span class="sxs-lookup"><span data-stu-id="eb49c-117">Example 2: Restart a rollout using the resource identifier</span></span>
```powershell
PS C:\> Restart-AzDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="eb49c-118">Este comando reinicia um lançamento chamado ContosoRollout no ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="eb49c-118">This command restarts a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="eb49c-119">Exemplo 3: Reinicie uma rolagem usando o objeto de lançamento.</span><span class="sxs-lookup"><span data-stu-id="eb49c-119">Example 3: Restart a rollout using the rollout object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -InputObject $rolloutObject
```

<span data-ttu-id="eb49c-120">Este comando reinicia uma distribuição cujo nome e ResourceGroup corresponderem às propriedades Name e ResourceGroupName do $rolloutObject, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="eb49c-120">This command restarts a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="eb49c-121">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="eb49c-121">PARAMETERS</span></span>

### <span data-ttu-id="eb49c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb49c-122">-DefaultProfile</span></span>
<span data-ttu-id="eb49c-123">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="eb49c-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eb49c-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eb49c-124">-InputObject</span></span>
<span data-ttu-id="eb49c-125">O recurso a ser removido.</span><span class="sxs-lookup"><span data-stu-id="eb49c-125">The resource to be removed.</span></span>

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

### <span data-ttu-id="eb49c-126">-Name</span><span class="sxs-lookup"><span data-stu-id="eb49c-126">-Name</span></span>
<span data-ttu-id="eb49c-127">O nome da apostila.</span><span class="sxs-lookup"><span data-stu-id="eb49c-127">The name of the rollout.</span></span>

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

### <span data-ttu-id="eb49c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb49c-128">-ResourceGroupName</span></span>
<span data-ttu-id="eb49c-129">O grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="eb49c-129">The resource group.</span></span>

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

### <span data-ttu-id="eb49c-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eb49c-130">-ResourceId</span></span>
<span data-ttu-id="eb49c-131">O identificador de recurso.</span><span class="sxs-lookup"><span data-stu-id="eb49c-131">The resource identifier.</span></span>

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

### <span data-ttu-id="eb49c-132">-SkipSucceededed</span><span class="sxs-lookup"><span data-stu-id="eb49c-132">-SkipSucceeded</span></span>
<span data-ttu-id="eb49c-133">Ignore as etapas que foram bem-sucedidas na versão anterior da versão.</span><span class="sxs-lookup"><span data-stu-id="eb49c-133">Skip steps that succeeded in the previous run of the rollout.</span></span>

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

### <span data-ttu-id="eb49c-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eb49c-134">-Confirm</span></span>
<span data-ttu-id="eb49c-135">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eb49c-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb49c-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb49c-136">-WhatIf</span></span>
<span data-ttu-id="eb49c-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="eb49c-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb49c-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="eb49c-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb49c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb49c-139">CommonParameters</span></span>
<span data-ttu-id="eb49c-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb49c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb49c-141">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eb49c-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb49c-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="eb49c-142">INPUTS</span></span>

### <span data-ttu-id="eb49c-143">System.String</span><span class="sxs-lookup"><span data-stu-id="eb49c-143">System.String</span></span>

### <span data-ttu-id="eb49c-144">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span><span class="sxs-lookup"><span data-stu-id="eb49c-144">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="eb49c-145">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="eb49c-145">OUTPUTS</span></span>

### <span data-ttu-id="eb49c-146">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span><span class="sxs-lookup"><span data-stu-id="eb49c-146">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="eb49c-147">NOTES</span><span class="sxs-lookup"><span data-stu-id="eb49c-147">NOTES</span></span>

## <span data-ttu-id="eb49c-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="eb49c-148">RELATED LINKS</span></span>
