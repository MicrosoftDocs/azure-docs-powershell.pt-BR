---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerrollout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerRollout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerRollout.md
ms.openlocfilehash: 066026331fa43af06fc2e3314ccb97d06a0f9b50
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93600985"
---
# <span data-ttu-id="ee4a4-101">Remove-AzDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="ee4a4-101">Remove-AzDeploymentManagerRollout</span></span>

## <span data-ttu-id="ee4a4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ee4a4-102">SYNOPSIS</span></span>
<span data-ttu-id="ee4a4-103">Exclui a distribuição.</span><span class="sxs-lookup"><span data-stu-id="ee4a4-103">Deletes the rollout.</span></span>

## <span data-ttu-id="ee4a4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ee4a4-104">SYNTAX</span></span>

### <span data-ttu-id="ee4a4-105">Interativo (padrão)</span><span class="sxs-lookup"><span data-stu-id="ee4a4-105">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee4a4-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="ee4a4-106">ResourceId</span></span>
```
Remove-AzDeploymentManagerRollout [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee4a4-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="ee4a4-107">InputObject</span></span>
```
Remove-AzDeploymentManagerRollout [-InputObject] <PSRollout> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee4a4-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ee4a4-108">DESCRIPTION</span></span>
<span data-ttu-id="ee4a4-109">O cmdlet **Remove-AzDeploymentManagerRollout** exclui uma distribuição em um estado de terminal.</span><span class="sxs-lookup"><span data-stu-id="ee4a4-109">The **Remove-AzDeploymentManagerRollout** cmdlet deletes a rollout in a terminal state.</span></span>
<span data-ttu-id="ee4a4-110">Especifique a distribuição por nome e nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ee4a4-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="ee4a4-111">Como alternativa, você pode fornecer o objeto de distribuição ou a ResourceId.</span><span class="sxs-lookup"><span data-stu-id="ee4a4-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>

## <span data-ttu-id="ee4a4-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ee4a4-112">EXAMPLES</span></span>

### <span data-ttu-id="ee4a4-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ee4a4-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout
```

<span data-ttu-id="ee4a4-114">Esse comando exclui uma distribuição chamada ContosoRollout no ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="ee4a4-114">This command deletes a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="ee4a4-115">Exemplo 2: excluir uma distribuição usando o identificador de recursos</span><span class="sxs-lookup"><span data-stu-id="ee4a4-115">Example 2: Delete a rollout using the resource identifier</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="ee4a4-116">Esse comando exclui uma distribuição chamada ContosoRollout no ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="ee4a4-116">This command deletes a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="ee4a4-117">Exemplo 3: excluir uma distribuição usando o objeto de distribuição.</span><span class="sxs-lookup"><span data-stu-id="ee4a4-117">Example 3: Delete a rollout using the rollout object.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerRollout -InputObject $rolloutObject
```

<span data-ttu-id="ee4a4-118">Este comando exclui uma distribuição cujo nome e o meu nome do contato correspondem às propriedades Name e ResourceGroupName do $rolloutObject, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="ee4a4-118">This command deletes a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="ee4a4-119">OS</span><span class="sxs-lookup"><span data-stu-id="ee4a4-119">PARAMETERS</span></span>

### <span data-ttu-id="ee4a4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee4a4-120">-DefaultProfile</span></span>
<span data-ttu-id="ee4a4-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ee4a4-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee4a4-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ee4a4-122">-InputObject</span></span>
<span data-ttu-id="ee4a4-123">O recurso a ser removido.</span><span class="sxs-lookup"><span data-stu-id="ee4a4-123">The resource to be removed.</span></span>

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

### <span data-ttu-id="ee4a4-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="ee4a4-124">-Name</span></span>
<span data-ttu-id="ee4a4-125">O nome da distribuição.</span><span class="sxs-lookup"><span data-stu-id="ee4a4-125">The name of the rollout.</span></span>

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

### <span data-ttu-id="ee4a4-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ee4a4-126">-PassThru</span></span>
<span data-ttu-id="ee4a4-127">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="ee4a4-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="ee4a4-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee4a4-128">-ResourceGroupName</span></span>
<span data-ttu-id="ee4a4-129">O grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ee4a4-129">The resource group.</span></span>

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

### <span data-ttu-id="ee4a4-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ee4a4-130">-ResourceId</span></span>
<span data-ttu-id="ee4a4-131">O identificador do recurso.</span><span class="sxs-lookup"><span data-stu-id="ee4a4-131">The resource identifier.</span></span>

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

### <span data-ttu-id="ee4a4-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ee4a4-132">-Confirm</span></span>
<span data-ttu-id="ee4a4-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ee4a4-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee4a4-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee4a4-134">-WhatIf</span></span>
<span data-ttu-id="ee4a4-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ee4a4-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee4a4-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ee4a4-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee4a4-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee4a4-137">CommonParameters</span></span>
<span data-ttu-id="ee4a4-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee4a4-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee4a4-139">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee4a4-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee4a4-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ee4a4-140">INPUTS</span></span>

### <span data-ttu-id="ee4a4-141">System. String</span><span class="sxs-lookup"><span data-stu-id="ee4a4-141">System.String</span></span>

### <span data-ttu-id="ee4a4-142">Microsoft. Azure. Commands. DeploymentManager. Models. PSRollout</span><span class="sxs-lookup"><span data-stu-id="ee4a4-142">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="ee4a4-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ee4a4-143">OUTPUTS</span></span>

### <span data-ttu-id="ee4a4-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ee4a4-144">System.Boolean</span></span>

## <span data-ttu-id="ee4a4-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ee4a4-145">NOTES</span></span>

## <span data-ttu-id="ee4a4-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ee4a4-146">RELATED LINKS</span></span>
