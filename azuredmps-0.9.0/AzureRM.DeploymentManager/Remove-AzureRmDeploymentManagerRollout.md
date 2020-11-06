---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/remove-azurermdeploymentmanagerrollout
schema: 2.0.0
ms.openlocfilehash: f329468dce9c520eb647bb0d927ba91de64a5c33
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93425681"
---
# <span data-ttu-id="45ae6-101">Remove-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="45ae6-101">Remove-AzureRmDeploymentManagerRollout</span></span>

## <span data-ttu-id="45ae6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="45ae6-102">SYNOPSIS</span></span>
<span data-ttu-id="45ae6-103">Exclui uma distribuição.</span><span class="sxs-lookup"><span data-stu-id="45ae6-103">Deletes a rollout.</span></span>

## <span data-ttu-id="45ae6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="45ae6-104">SYNTAX</span></span>

### <span data-ttu-id="45ae6-105">Interativo (padrão)</span><span class="sxs-lookup"><span data-stu-id="45ae6-105">Interactive (Default)</span></span>
```
Remove-AzureRmDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45ae6-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="45ae6-106">ResourceId</span></span>
```
Remove-AzureRmDeploymentManagerRollout [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45ae6-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="45ae6-107">InputObject</span></span>
```
Remove-AzureRmDeploymentManagerRollout [-Rollout] <PSRollout> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45ae6-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="45ae6-108">DESCRIPTION</span></span>
<span data-ttu-id="45ae6-109">O cmdlet **Remove-AzureRmDeploymentManagerRollout** exclui uma distribuição em um estado de terminal.</span><span class="sxs-lookup"><span data-stu-id="45ae6-109">The **Remove-AzureRmDeploymentManagerRollout** cmdlet deletes a rollout in a terminal state.</span></span>
<span data-ttu-id="45ae6-110">Especifique a distribuição por nome e nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="45ae6-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="45ae6-111">Como alternativa, você pode fornecer o objeto de distribuição ou a ResourceId.</span><span class="sxs-lookup"><span data-stu-id="45ae6-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>

## <span data-ttu-id="45ae6-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="45ae6-112">EXAMPLES</span></span>

### <span data-ttu-id="45ae6-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="45ae6-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout
```

<span data-ttu-id="45ae6-114">Esse comando exclui uma distribuição chamada ContosoRollout no ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="45ae6-114">This command deletes a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="45ae6-115">Exemplo 2: excluir uma distribuição usando o identificador de recursos</span><span class="sxs-lookup"><span data-stu-id="45ae6-115">Example 2: Delete a rollout using the resource identifier</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="45ae6-116">Esse comando exclui uma distribuição chamada ContosoRollout no ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="45ae6-116">This command deletes a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="45ae6-117">Exemplo 3: excluir uma distribuição usando o objeto de distribuição.</span><span class="sxs-lookup"><span data-stu-id="45ae6-117">Example 3: Delete a rollout using the rollout object.</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerRollout -Rollout $rolloutObject
```

<span data-ttu-id="45ae6-118">Este comando exclui uma distribuição cujo nome e o meu nome do contato correspondem às propriedades Name e ResourceGroupName do $rolloutObject, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="45ae6-118">This command deletes a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="45ae6-119">OS</span><span class="sxs-lookup"><span data-stu-id="45ae6-119">PARAMETERS</span></span>

### <span data-ttu-id="45ae6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45ae6-120">-DefaultProfile</span></span>
<span data-ttu-id="45ae6-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="45ae6-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="45ae6-122">-Force</span><span class="sxs-lookup"><span data-stu-id="45ae6-122">-Force</span></span>
<span data-ttu-id="45ae6-123">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="45ae6-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="45ae6-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="45ae6-124">-Name</span></span>
<span data-ttu-id="45ae6-125">O nome da distribuição.</span><span class="sxs-lookup"><span data-stu-id="45ae6-125">The name of the rollout.</span></span>

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

### <span data-ttu-id="45ae6-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="45ae6-126">-PassThru</span></span>
<span data-ttu-id="45ae6-127">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="45ae6-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="45ae6-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45ae6-128">-ResourceGroupName</span></span>
<span data-ttu-id="45ae6-129">O grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="45ae6-129">The resource group.</span></span>

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

### <span data-ttu-id="45ae6-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="45ae6-130">-ResourceId</span></span>
<span data-ttu-id="45ae6-131">O identificador do recurso.</span><span class="sxs-lookup"><span data-stu-id="45ae6-131">The resource identifier.</span></span>

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

### <span data-ttu-id="45ae6-132">-Distribuição</span><span class="sxs-lookup"><span data-stu-id="45ae6-132">-Rollout</span></span>
<span data-ttu-id="45ae6-133">O recurso a ser removido.</span><span class="sxs-lookup"><span data-stu-id="45ae6-133">The resource to be removed.</span></span>

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

### <span data-ttu-id="45ae6-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="45ae6-134">-Confirm</span></span>
<span data-ttu-id="45ae6-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45ae6-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45ae6-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45ae6-136">-WhatIf</span></span>
<span data-ttu-id="45ae6-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="45ae6-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45ae6-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="45ae6-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45ae6-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45ae6-139">CommonParameters</span></span>
<span data-ttu-id="45ae6-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45ae6-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45ae6-141">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45ae6-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45ae6-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="45ae6-142">INPUTS</span></span>

### <span data-ttu-id="45ae6-143">Microsoft. Azure. Commands. DeploymentManager. Models. PSRollout</span><span class="sxs-lookup"><span data-stu-id="45ae6-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="45ae6-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="45ae6-144">OUTPUTS</span></span>

### <span data-ttu-id="45ae6-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="45ae6-145">System.Boolean</span></span>

## <span data-ttu-id="45ae6-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="45ae6-146">NOTES</span></span>

## <span data-ttu-id="45ae6-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="45ae6-147">RELATED LINKS</span></span>

[<span data-ttu-id="45ae6-148">Get-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="45ae6-148">Get-AzureRmDeploymentManagerRollout</span></span>](./Get-AzureRmDeploymentManagerRollout.md)

[<span data-ttu-id="45ae6-149">Parar-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="45ae6-149">Stop-AzureRmDeploymentManagerRollout</span></span>](./Stop-AzureRmDeploymentManagerRollout.md)

[<span data-ttu-id="45ae6-150">Restart-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="45ae6-150">Restart-AzureRmDeploymentManagerRollout</span></span>](./Restart-AzureRmDeploymentManagerRollout.md)