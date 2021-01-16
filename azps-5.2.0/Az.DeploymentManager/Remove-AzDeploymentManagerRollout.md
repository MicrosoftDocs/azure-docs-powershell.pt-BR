---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerrollout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerRollout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerRollout.md
ms.openlocfilehash: 8e5e2c25f69d6e61c21a0f616f49079710c2d5db
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98262027"
---
# <span data-ttu-id="889b1-101">Remove-AzDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="889b1-101">Remove-AzDeploymentManagerRollout</span></span>

## <span data-ttu-id="889b1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="889b1-102">SYNOPSIS</span></span>
<span data-ttu-id="889b1-103">Exclui a distribuição.</span><span class="sxs-lookup"><span data-stu-id="889b1-103">Deletes the rollout.</span></span>

## <span data-ttu-id="889b1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="889b1-104">SYNTAX</span></span>

### <span data-ttu-id="889b1-105">Interativo (padrão)</span><span class="sxs-lookup"><span data-stu-id="889b1-105">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="889b1-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="889b1-106">ResourceId</span></span>
```
Remove-AzDeploymentManagerRollout [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="889b1-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="889b1-107">InputObject</span></span>
```
Remove-AzDeploymentManagerRollout [-InputObject] <PSRollout> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="889b1-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="889b1-108">DESCRIPTION</span></span>
<span data-ttu-id="889b1-109">O cmdlet **Remove-AzDeploymentManagerRollout** exclui uma distribuição em um estado de terminal.</span><span class="sxs-lookup"><span data-stu-id="889b1-109">The **Remove-AzDeploymentManagerRollout** cmdlet deletes a rollout in a terminal state.</span></span>
<span data-ttu-id="889b1-110">Especifique a distribuição por nome e nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="889b1-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="889b1-111">Como alternativa, você pode fornecer o objeto de distribuição ou a ResourceId.</span><span class="sxs-lookup"><span data-stu-id="889b1-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>

## <span data-ttu-id="889b1-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="889b1-112">EXAMPLES</span></span>

### <span data-ttu-id="889b1-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="889b1-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout
```

<span data-ttu-id="889b1-114">Esse comando exclui uma distribuição chamada ContosoRollout no ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="889b1-114">This command deletes a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="889b1-115">Exemplo 2: excluir uma distribuição usando o identificador de recursos</span><span class="sxs-lookup"><span data-stu-id="889b1-115">Example 2: Delete a rollout using the resource identifier</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="889b1-116">Esse comando exclui uma distribuição chamada ContosoRollout no ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="889b1-116">This command deletes a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="889b1-117">Exemplo 3: excluir uma distribuição usando o objeto de distribuição.</span><span class="sxs-lookup"><span data-stu-id="889b1-117">Example 3: Delete a rollout using the rollout object.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerRollout -InputObject $rolloutObject
```

<span data-ttu-id="889b1-118">Este comando exclui uma distribuição cujo nome e o meu nome do contato correspondem às propriedades Name e ResourceGroupName do $rolloutObject, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="889b1-118">This command deletes a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="889b1-119">OS</span><span class="sxs-lookup"><span data-stu-id="889b1-119">PARAMETERS</span></span>

### <span data-ttu-id="889b1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="889b1-120">-DefaultProfile</span></span>
<span data-ttu-id="889b1-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="889b1-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="889b1-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="889b1-122">-InputObject</span></span>
<span data-ttu-id="889b1-123">O recurso a ser removido.</span><span class="sxs-lookup"><span data-stu-id="889b1-123">The resource to be removed.</span></span>

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

### <span data-ttu-id="889b1-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="889b1-124">-Name</span></span>
<span data-ttu-id="889b1-125">O nome da distribuição.</span><span class="sxs-lookup"><span data-stu-id="889b1-125">The name of the rollout.</span></span>

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

### <span data-ttu-id="889b1-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="889b1-126">-PassThru</span></span>
<span data-ttu-id="889b1-127">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="889b1-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="889b1-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="889b1-128">-ResourceGroupName</span></span>
<span data-ttu-id="889b1-129">O grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="889b1-129">The resource group.</span></span>

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

### <span data-ttu-id="889b1-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="889b1-130">-ResourceId</span></span>
<span data-ttu-id="889b1-131">O identificador do recurso.</span><span class="sxs-lookup"><span data-stu-id="889b1-131">The resource identifier.</span></span>

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

### <span data-ttu-id="889b1-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="889b1-132">-Confirm</span></span>
<span data-ttu-id="889b1-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="889b1-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="889b1-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="889b1-134">-WhatIf</span></span>
<span data-ttu-id="889b1-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="889b1-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="889b1-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="889b1-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="889b1-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="889b1-137">CommonParameters</span></span>
<span data-ttu-id="889b1-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="889b1-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="889b1-139">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="889b1-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="889b1-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="889b1-140">INPUTS</span></span>

### <span data-ttu-id="889b1-141">System. String</span><span class="sxs-lookup"><span data-stu-id="889b1-141">System.String</span></span>

### <span data-ttu-id="889b1-142">Microsoft. Azure. Commands. DeploymentManager. Models. PSRollout</span><span class="sxs-lookup"><span data-stu-id="889b1-142">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="889b1-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="889b1-143">OUTPUTS</span></span>

### <span data-ttu-id="889b1-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="889b1-144">System.Boolean</span></span>

## <span data-ttu-id="889b1-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="889b1-145">NOTES</span></span>

## <span data-ttu-id="889b1-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="889b1-146">RELATED LINKS</span></span>
