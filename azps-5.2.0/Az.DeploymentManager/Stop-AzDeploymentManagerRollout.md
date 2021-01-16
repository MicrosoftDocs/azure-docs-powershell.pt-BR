---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/stop-azdeploymentmanagerrollout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Stop-AzDeploymentManagerRollout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Stop-AzDeploymentManagerRollout.md
ms.openlocfilehash: cd59cd39fb2834bed2162a257905fea643c0a767
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98258302"
---
# <span data-ttu-id="219f1-101">Stop-AzDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="219f1-101">Stop-AzDeploymentManagerRollout</span></span>

## <span data-ttu-id="219f1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="219f1-102">SYNOPSIS</span></span>
<span data-ttu-id="219f1-103">Interrompe a distribuição.</span><span class="sxs-lookup"><span data-stu-id="219f1-103">Stops the rollout.</span></span>

## <span data-ttu-id="219f1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="219f1-104">SYNTAX</span></span>

### <span data-ttu-id="219f1-105">Interativo (padrão)</span><span class="sxs-lookup"><span data-stu-id="219f1-105">Interactive (Default)</span></span>
```
Stop-AzDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="219f1-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="219f1-106">ResourceId</span></span>
```
Stop-AzDeploymentManagerRollout [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="219f1-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="219f1-107">InputObject</span></span>
```
Stop-AzDeploymentManagerRollout [-InputObject] <PSRollout> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="219f1-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="219f1-108">DESCRIPTION</span></span>
<span data-ttu-id="219f1-109">O cmdlet **Stop-AzDeploymentManagerRollout** interrompe uma distribuição em andamento e retorna um objeto que representa o estado atual da distribuição.</span><span class="sxs-lookup"><span data-stu-id="219f1-109">The **Stop-AzDeploymentManagerRollout** cmdlet stops a rollout in progress and returns an object that represents the current state of the rollout.</span></span>
<span data-ttu-id="219f1-110">Especifique a distribuição por nome e nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="219f1-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="219f1-111">Como alternativa, você pode fornecer o objeto de distribuição ou a ResourceId.</span><span class="sxs-lookup"><span data-stu-id="219f1-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>

<span data-ttu-id="219f1-112">Observe que depois que uma distribuição é interrompida, ela não pode ser retomada ou reiniciada.</span><span class="sxs-lookup"><span data-stu-id="219f1-112">Note that once a rollout is stopped, it cannot be resumed or restarted.</span></span> <span data-ttu-id="219f1-113">Você só pode criar uma nova distribuição.</span><span class="sxs-lookup"><span data-stu-id="219f1-113">You can only create a new rollout.</span></span>

## <span data-ttu-id="219f1-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="219f1-114">EXAMPLES</span></span>

### <span data-ttu-id="219f1-115">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="219f1-115">Example 1</span></span>
```powershell
PS C:\> Stop-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout -SkipSucceeded
```

<span data-ttu-id="219f1-116">Esse comando interrompe uma distribuição chamada ContosoRollout no ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="219f1-116">This command stops a rollout named ContosoRollout in the ContosoResourceGroup.</span></span> 

### <span data-ttu-id="219f1-117">Exemplo 2: parar uma distribuição usando o identificador de recursos</span><span class="sxs-lookup"><span data-stu-id="219f1-117">Example 2: Stop a rollout using the resource identifier</span></span>
```powershell
PS C:\> Restart-AzDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="219f1-118">Esse comando interrompe uma distribuição chamada ContosoRollout no ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="219f1-118">This command stops a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="219f1-119">Exemplo 3: parar uma distribuição usando o objeto de distribuição.</span><span class="sxs-lookup"><span data-stu-id="219f1-119">Example 3: Stop a rollout using the rollout object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -InputObject $rolloutObject
```

<span data-ttu-id="219f1-120">Esse comando interrompe uma distribuição cujo nome e o meu nome do contato correspondem às propriedades Name e ResourceGroupName do $rolloutObject, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="219f1-120">This command stops a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="219f1-121">OS</span><span class="sxs-lookup"><span data-stu-id="219f1-121">PARAMETERS</span></span>

### <span data-ttu-id="219f1-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="219f1-122">-DefaultProfile</span></span>
<span data-ttu-id="219f1-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="219f1-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="219f1-124">-Force</span><span class="sxs-lookup"><span data-stu-id="219f1-124">-Force</span></span>
<span data-ttu-id="219f1-125">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="219f1-125">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="219f1-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="219f1-126">-InputObject</span></span>
<span data-ttu-id="219f1-127">A distribuição a ser removida.</span><span class="sxs-lookup"><span data-stu-id="219f1-127">The rollout to be removed.</span></span>

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

### <span data-ttu-id="219f1-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="219f1-128">-Name</span></span>
<span data-ttu-id="219f1-129">O nome da distribuição.</span><span class="sxs-lookup"><span data-stu-id="219f1-129">The name of the rollout.</span></span>

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

### <span data-ttu-id="219f1-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="219f1-130">-ResourceGroupName</span></span>
<span data-ttu-id="219f1-131">O grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="219f1-131">The resource group.</span></span>

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

### <span data-ttu-id="219f1-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="219f1-132">-ResourceId</span></span>
<span data-ttu-id="219f1-133">O identificador do recurso.</span><span class="sxs-lookup"><span data-stu-id="219f1-133">The resource identifier.</span></span>

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

### <span data-ttu-id="219f1-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="219f1-134">-Confirm</span></span>
<span data-ttu-id="219f1-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="219f1-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="219f1-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="219f1-136">-WhatIf</span></span>
<span data-ttu-id="219f1-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="219f1-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="219f1-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="219f1-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="219f1-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="219f1-139">CommonParameters</span></span>
<span data-ttu-id="219f1-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="219f1-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="219f1-141">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="219f1-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="219f1-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="219f1-142">INPUTS</span></span>

### <span data-ttu-id="219f1-143">System. String</span><span class="sxs-lookup"><span data-stu-id="219f1-143">System.String</span></span>

### <span data-ttu-id="219f1-144">Microsoft. Azure. Commands. DeploymentManager. Models. PSRollout</span><span class="sxs-lookup"><span data-stu-id="219f1-144">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="219f1-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="219f1-145">OUTPUTS</span></span>

### <span data-ttu-id="219f1-146">Microsoft. Azure. Commands. DeploymentManager. Models. PSRollout</span><span class="sxs-lookup"><span data-stu-id="219f1-146">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="219f1-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="219f1-147">NOTES</span></span>

## <span data-ttu-id="219f1-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="219f1-148">RELATED LINKS</span></span>
