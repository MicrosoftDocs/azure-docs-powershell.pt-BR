---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/stop-azdeploymentmanagerrollout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Stop-AzDeploymentManagerRollout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Stop-AzDeploymentManagerRollout.md
ms.openlocfilehash: cd59cd39fb2834bed2162a257905fea643c0a767
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115838"
---
# <span data-ttu-id="56d34-101">Stop-AzDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="56d34-101">Stop-AzDeploymentManagerRollout</span></span>

## <span data-ttu-id="56d34-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="56d34-102">SYNOPSIS</span></span>
<span data-ttu-id="56d34-103">Interrompe a adoção.</span><span class="sxs-lookup"><span data-stu-id="56d34-103">Stops the rollout.</span></span>

## <span data-ttu-id="56d34-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="56d34-104">SYNTAX</span></span>

### <span data-ttu-id="56d34-105">Interativo (Padrão)</span><span class="sxs-lookup"><span data-stu-id="56d34-105">Interactive (Default)</span></span>
```
Stop-AzDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56d34-106">Resourceid</span><span class="sxs-lookup"><span data-stu-id="56d34-106">ResourceId</span></span>
```
Stop-AzDeploymentManagerRollout [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56d34-107">Inputobject</span><span class="sxs-lookup"><span data-stu-id="56d34-107">InputObject</span></span>
```
Stop-AzDeploymentManagerRollout [-InputObject] <PSRollout> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56d34-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="56d34-108">DESCRIPTION</span></span>
<span data-ttu-id="56d34-109">O cmdlet **Stop-AzDeploymentManagerRollout** interrompe uma versão em andamento e retorna um objeto que representa o estado atual da versão.</span><span class="sxs-lookup"><span data-stu-id="56d34-109">The **Stop-AzDeploymentManagerRollout** cmdlet stops a rollout in progress and returns an object that represents the current state of the rollout.</span></span>
<span data-ttu-id="56d34-110">Especifique a distribuição pelo nome e nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="56d34-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="56d34-111">Como alternativa, você pode fornecer o objeto Distribuição ou o ResourceId.</span><span class="sxs-lookup"><span data-stu-id="56d34-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>

<span data-ttu-id="56d34-112">Observe que depois que uma adoção é interrompida, ela não pode ser retomada ou reiniciada.</span><span class="sxs-lookup"><span data-stu-id="56d34-112">Note that once a rollout is stopped, it cannot be resumed or restarted.</span></span> <span data-ttu-id="56d34-113">Você só pode criar uma nova versão.</span><span class="sxs-lookup"><span data-stu-id="56d34-113">You can only create a new rollout.</span></span>

## <span data-ttu-id="56d34-114">Exemplos</span><span class="sxs-lookup"><span data-stu-id="56d34-114">EXAMPLES</span></span>

### <span data-ttu-id="56d34-115">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="56d34-115">Example 1</span></span>
```powershell
PS C:\> Stop-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout -SkipSucceeded
```

<span data-ttu-id="56d34-116">Esse comando interrompe uma adoção chamada ContosoRollout no Grupo ContosoResource.</span><span class="sxs-lookup"><span data-stu-id="56d34-116">This command stops a rollout named ContosoRollout in the ContosoResourceGroup.</span></span> 

### <span data-ttu-id="56d34-117">Exemplo 2: Parar uma distribuição usando o identificador de recurso</span><span class="sxs-lookup"><span data-stu-id="56d34-117">Example 2: Stop a rollout using the resource identifier</span></span>
```powershell
PS C:\> Restart-AzDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="56d34-118">Esse comando interrompe uma adoção chamada ContosoRollout no Grupo ContosoResource.</span><span class="sxs-lookup"><span data-stu-id="56d34-118">This command stops a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="56d34-119">Exemplo 3: Interromper uma adoção usando o objeto de adoção.</span><span class="sxs-lookup"><span data-stu-id="56d34-119">Example 3: Stop a rollout using the rollout object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -InputObject $rolloutObject
```

<span data-ttu-id="56d34-120">Esse comando interrompe uma distribuição cujo nome e Grupo de Recursos corresponderem às propriedades Nome e NomeDoGrupo de Recursos do $rolloutObject, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="56d34-120">This command stops a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="56d34-121">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="56d34-121">PARAMETERS</span></span>

### <span data-ttu-id="56d34-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56d34-122">-DefaultProfile</span></span>
<span data-ttu-id="56d34-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="56d34-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56d34-124">-Forçar</span><span class="sxs-lookup"><span data-stu-id="56d34-124">-Force</span></span>
<span data-ttu-id="56d34-125">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="56d34-125">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="56d34-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="56d34-126">-InputObject</span></span>
<span data-ttu-id="56d34-127">A adoção a ser removida.</span><span class="sxs-lookup"><span data-stu-id="56d34-127">The rollout to be removed.</span></span>

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

### <span data-ttu-id="56d34-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="56d34-128">-Name</span></span>
<span data-ttu-id="56d34-129">O nome da apostila.</span><span class="sxs-lookup"><span data-stu-id="56d34-129">The name of the rollout.</span></span>

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

### <span data-ttu-id="56d34-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56d34-130">-ResourceGroupName</span></span>
<span data-ttu-id="56d34-131">O grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="56d34-131">The resource group.</span></span>

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

### <span data-ttu-id="56d34-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="56d34-132">-ResourceId</span></span>
<span data-ttu-id="56d34-133">O identificador de recurso.</span><span class="sxs-lookup"><span data-stu-id="56d34-133">The resource identifier.</span></span>

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

### <span data-ttu-id="56d34-134">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="56d34-134">-Confirm</span></span>
<span data-ttu-id="56d34-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56d34-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56d34-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56d34-136">-WhatIf</span></span>
<span data-ttu-id="56d34-137">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="56d34-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56d34-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="56d34-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56d34-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56d34-139">CommonParameters</span></span>
<span data-ttu-id="56d34-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56d34-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56d34-141">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="56d34-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56d34-142">Entradas</span><span class="sxs-lookup"><span data-stu-id="56d34-142">INPUTS</span></span>

### <span data-ttu-id="56d34-143">System.String</span><span class="sxs-lookup"><span data-stu-id="56d34-143">System.String</span></span>

### <span data-ttu-id="56d34-144">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span><span class="sxs-lookup"><span data-stu-id="56d34-144">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="56d34-145">Saídas</span><span class="sxs-lookup"><span data-stu-id="56d34-145">OUTPUTS</span></span>

### <span data-ttu-id="56d34-146">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span><span class="sxs-lookup"><span data-stu-id="56d34-146">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="56d34-147">Notas</span><span class="sxs-lookup"><span data-stu-id="56d34-147">NOTES</span></span>

## <span data-ttu-id="56d34-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="56d34-148">RELATED LINKS</span></span>
