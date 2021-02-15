---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerrollout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerRollout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerRollout.md
ms.openlocfilehash: 8e5e2c25f69d6e61c21a0f616f49079710c2d5db
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118787"
---
# <span data-ttu-id="29979-101">Remove-AzDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="29979-101">Remove-AzDeploymentManagerRollout</span></span>

## <span data-ttu-id="29979-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="29979-102">SYNOPSIS</span></span>
<span data-ttu-id="29979-103">Exclui a adoção.</span><span class="sxs-lookup"><span data-stu-id="29979-103">Deletes the rollout.</span></span>

## <span data-ttu-id="29979-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="29979-104">SYNTAX</span></span>

### <span data-ttu-id="29979-105">Interativo (Padrão)</span><span class="sxs-lookup"><span data-stu-id="29979-105">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29979-106">Resourceid</span><span class="sxs-lookup"><span data-stu-id="29979-106">ResourceId</span></span>
```
Remove-AzDeploymentManagerRollout [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29979-107">Inputobject</span><span class="sxs-lookup"><span data-stu-id="29979-107">InputObject</span></span>
```
Remove-AzDeploymentManagerRollout [-InputObject] <PSRollout> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29979-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="29979-108">DESCRIPTION</span></span>
<span data-ttu-id="29979-109">O cmdlet **Remove-AzDeploymentManagerRollout** exclui uma rollout em um estado de terminal.</span><span class="sxs-lookup"><span data-stu-id="29979-109">The **Remove-AzDeploymentManagerRollout** cmdlet deletes a rollout in a terminal state.</span></span>
<span data-ttu-id="29979-110">Especifique a distribuição pelo nome e nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="29979-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="29979-111">Como alternativa, você pode fornecer o objeto Distribuição ou o ResourceId.</span><span class="sxs-lookup"><span data-stu-id="29979-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>

## <span data-ttu-id="29979-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="29979-112">EXAMPLES</span></span>

### <span data-ttu-id="29979-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="29979-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout
```

<span data-ttu-id="29979-114">Esse comando exclui uma apostila chamada ContosoRollout no Grupo ContosoResource.</span><span class="sxs-lookup"><span data-stu-id="29979-114">This command deletes a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="29979-115">Exemplo 2: Excluir uma distribuição usando o identificador de recurso</span><span class="sxs-lookup"><span data-stu-id="29979-115">Example 2: Delete a rollout using the resource identifier</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="29979-116">Esse comando exclui uma apostila chamada ContosoRollout no Grupo ContosoResource.</span><span class="sxs-lookup"><span data-stu-id="29979-116">This command deletes a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="29979-117">Exemplo 3: Excluir uma apostila usando o objeto de adoção.</span><span class="sxs-lookup"><span data-stu-id="29979-117">Example 3: Delete a rollout using the rollout object.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerRollout -InputObject $rolloutObject
```

<span data-ttu-id="29979-118">Esse comando exclui uma distribuição cujo nome e Grupo de Recursos corresponderem às propriedades Nome e NomeDoGrupo de Recursos da $rolloutObject, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="29979-118">This command deletes a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="29979-119">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="29979-119">PARAMETERS</span></span>

### <span data-ttu-id="29979-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29979-120">-DefaultProfile</span></span>
<span data-ttu-id="29979-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="29979-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29979-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="29979-122">-InputObject</span></span>
<span data-ttu-id="29979-123">O recurso a ser removido.</span><span class="sxs-lookup"><span data-stu-id="29979-123">The resource to be removed.</span></span>

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

### <span data-ttu-id="29979-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="29979-124">-Name</span></span>
<span data-ttu-id="29979-125">O nome da apostila.</span><span class="sxs-lookup"><span data-stu-id="29979-125">The name of the rollout.</span></span>

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

### <span data-ttu-id="29979-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="29979-126">-PassThru</span></span>
<span data-ttu-id="29979-127">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="29979-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="29979-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29979-128">-ResourceGroupName</span></span>
<span data-ttu-id="29979-129">O grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="29979-129">The resource group.</span></span>

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

### <span data-ttu-id="29979-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="29979-130">-ResourceId</span></span>
<span data-ttu-id="29979-131">O identificador de recurso.</span><span class="sxs-lookup"><span data-stu-id="29979-131">The resource identifier.</span></span>

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

### <span data-ttu-id="29979-132">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="29979-132">-Confirm</span></span>
<span data-ttu-id="29979-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="29979-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29979-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29979-134">-WhatIf</span></span>
<span data-ttu-id="29979-135">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="29979-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29979-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="29979-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29979-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29979-137">CommonParameters</span></span>
<span data-ttu-id="29979-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29979-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29979-139">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="29979-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29979-140">Entradas</span><span class="sxs-lookup"><span data-stu-id="29979-140">INPUTS</span></span>

### <span data-ttu-id="29979-141">System.String</span><span class="sxs-lookup"><span data-stu-id="29979-141">System.String</span></span>

### <span data-ttu-id="29979-142">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span><span class="sxs-lookup"><span data-stu-id="29979-142">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="29979-143">Saídas</span><span class="sxs-lookup"><span data-stu-id="29979-143">OUTPUTS</span></span>

### <span data-ttu-id="29979-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="29979-144">System.Boolean</span></span>

## <span data-ttu-id="29979-145">Notas</span><span class="sxs-lookup"><span data-stu-id="29979-145">NOTES</span></span>

## <span data-ttu-id="29979-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="29979-146">RELATED LINKS</span></span>
