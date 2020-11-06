---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/stop-azurermdeploymentmanagerrollout
schema: 2.0.0
ms.openlocfilehash: 3c4f221fc00187c4faea2dbcc1a5014822c476c8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93601704"
---
# <span data-ttu-id="65c73-101">Stop-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="65c73-101">Stop-AzureRmDeploymentManagerRollout</span></span>

## <span data-ttu-id="65c73-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="65c73-102">SYNOPSIS</span></span>
<span data-ttu-id="65c73-103">Interrompe uma distribuição em andamento.</span><span class="sxs-lookup"><span data-stu-id="65c73-103">Stops a rollout in progress.</span></span>

## <span data-ttu-id="65c73-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="65c73-104">SYNTAX</span></span>

### <span data-ttu-id="65c73-105">Interativo (padrão)</span><span class="sxs-lookup"><span data-stu-id="65c73-105">Interactive (Default)</span></span>
```
Stop-AzureRmDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65c73-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="65c73-106">ResourceId</span></span>
```
Stop-AzureRmDeploymentManagerRollout [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65c73-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="65c73-107">InputObject</span></span>
```
Stop-AzureRmDeploymentManagerRollout [-Rollout] <PSRollout> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65c73-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="65c73-108">DESCRIPTION</span></span>
<span data-ttu-id="65c73-109">O cmdlet **Stop-AzureRmDeploymentManagerRollout** interrompe uma distribuição em andamento e retorna um objeto que representa o estado atual da distribuição.</span><span class="sxs-lookup"><span data-stu-id="65c73-109">The **Stop-AzureRmDeploymentManagerRollout** cmdlet stops a rollout in progress and returns an object that represents the current state of the rollout.</span></span>
<span data-ttu-id="65c73-110">Especifique a distribuição por nome e nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="65c73-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="65c73-111">Como alternativa, você pode fornecer o objeto de distribuição ou a ResourceId.</span><span class="sxs-lookup"><span data-stu-id="65c73-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>

<span data-ttu-id="65c73-112">Observe que depois que uma distribuição é interrompida, ela não pode ser retomada ou reiniciada.</span><span class="sxs-lookup"><span data-stu-id="65c73-112">Note that once a rollout is stopped, it cannot be resumed or restarted.</span></span> <span data-ttu-id="65c73-113">Você só pode criar uma nova distribuição.</span><span class="sxs-lookup"><span data-stu-id="65c73-113">You can only create a new rollout.</span></span>

## <span data-ttu-id="65c73-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="65c73-114">EXAMPLES</span></span>

### <span data-ttu-id="65c73-115">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="65c73-115">Example 1</span></span>
```powershell
PS C:\> Stop-AzureRmDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout -SkipSucceeded
```

<span data-ttu-id="65c73-116">Esse comando interrompe uma distribuição chamada ContosoRollout no ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="65c73-116">This command stops a rollout named ContosoRollout in the ContosoResourceGroup.</span></span> 

### <span data-ttu-id="65c73-117">Exemplo 2: parar uma distribuição usando o identificador de recursos</span><span class="sxs-lookup"><span data-stu-id="65c73-117">Example 2: Stop a rollout using the resource identifier</span></span>
```powershell
PS C:\> Restart-AzureRmDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="65c73-118">Esse comando interrompe uma distribuição chamada ContosoRollout no ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="65c73-118">This command stops a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="65c73-119">Exemplo 3: parar uma distribuição usando o objeto de distribuição.</span><span class="sxs-lookup"><span data-stu-id="65c73-119">Example 3: Stop a rollout using the rollout object.</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerRollout -Rollout $rolloutObject
```

<span data-ttu-id="65c73-120">Esse comando interrompe uma distribuição cujo nome e o meu nome do contato correspondem às propriedades Name e ResourceGroupName do $rolloutObject, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="65c73-120">This command stops a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="65c73-121">OS</span><span class="sxs-lookup"><span data-stu-id="65c73-121">PARAMETERS</span></span>

### <span data-ttu-id="65c73-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65c73-122">-DefaultProfile</span></span>
<span data-ttu-id="65c73-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="65c73-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65c73-124">-Force</span><span class="sxs-lookup"><span data-stu-id="65c73-124">-Force</span></span>
<span data-ttu-id="65c73-125">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="65c73-125">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="65c73-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="65c73-126">-Name</span></span>
<span data-ttu-id="65c73-127">O nome da distribuição.</span><span class="sxs-lookup"><span data-stu-id="65c73-127">The name of the rollout.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65c73-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65c73-128">-ResourceGroupName</span></span>
<span data-ttu-id="65c73-129">O grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="65c73-129">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65c73-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="65c73-130">-ResourceId</span></span>
<span data-ttu-id="65c73-131">O identificador do recurso.</span><span class="sxs-lookup"><span data-stu-id="65c73-131">The resource identifier.</span></span>

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

### <span data-ttu-id="65c73-132">-Distribuição</span><span class="sxs-lookup"><span data-stu-id="65c73-132">-Rollout</span></span>
<span data-ttu-id="65c73-133">O recurso a ser removido.</span><span class="sxs-lookup"><span data-stu-id="65c73-133">The resource to be removed.</span></span>

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

### <span data-ttu-id="65c73-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="65c73-134">-Confirm</span></span>
<span data-ttu-id="65c73-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65c73-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65c73-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65c73-136">-WhatIf</span></span>
<span data-ttu-id="65c73-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="65c73-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="65c73-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="65c73-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65c73-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65c73-139">CommonParameters</span></span>
<span data-ttu-id="65c73-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65c73-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65c73-141">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65c73-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65c73-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="65c73-142">INPUTS</span></span>

### <span data-ttu-id="65c73-143">Microsoft. Azure. Commands. DeploymentManager. Models. PSRollout</span><span class="sxs-lookup"><span data-stu-id="65c73-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="65c73-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="65c73-144">OUTPUTS</span></span>

### <span data-ttu-id="65c73-145">Microsoft. Azure. Commands. DeploymentManager. Models. PSRollout</span><span class="sxs-lookup"><span data-stu-id="65c73-145">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="65c73-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="65c73-146">NOTES</span></span>

## <span data-ttu-id="65c73-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="65c73-147">RELATED LINKS</span></span>

[<span data-ttu-id="65c73-148">Get-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="65c73-148">Get-AzureRmDeploymentManagerRollout</span></span>](./Get-AzureRmDeploymentManagerRollout.md)

[<span data-ttu-id="65c73-149">Restart-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="65c73-149">Restart-AzureRmDeploymentManagerRollout</span></span>](./Restart-AzureRmDeploymentManagerRollout.md)

[<span data-ttu-id="65c73-150">Remove-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="65c73-150">Remove-AzureRmDeploymentManagerRollout</span></span>](./Remove-AzureRmDeploymentManagerRollout.md)