---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerservicetopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerServiceTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerServiceTopology.md
ms.openlocfilehash: d3716d18bc883d5407ee4acf3fa43960b63e7cd6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888971"
---
# <span data-ttu-id="6a8f8-101">Remove-AzDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="6a8f8-101">Remove-AzDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="6a8f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a8f8-102">SYNOPSIS</span></span>
<span data-ttu-id="6a8f8-103">Exclui a topologia do serviço.</span><span class="sxs-lookup"><span data-stu-id="6a8f8-103">Deletes the service topology.</span></span> <span data-ttu-id="6a8f8-104">Todos os serviços criados sob uma topologia de serviço precisam ser excluídos antes de excluir a topologia do serviço.</span><span class="sxs-lookup"><span data-stu-id="6a8f8-104">All services created under a service topology need to be deleted before deleting the service topology.</span></span>

## <span data-ttu-id="6a8f8-105">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="6a8f8-105">SYNTAX</span></span>

### <span data-ttu-id="6a8f8-106">Interativo (Padrão)</span><span class="sxs-lookup"><span data-stu-id="6a8f8-106">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerServiceTopology [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a8f8-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="6a8f8-107">ResourceId</span></span>
```
Remove-AzDeploymentManagerServiceTopology [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a8f8-108">InputObject</span><span class="sxs-lookup"><span data-stu-id="6a8f8-108">InputObject</span></span>
```
Remove-AzDeploymentManagerServiceTopology [-InputObject] <PSServiceTopologyResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6a8f8-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="6a8f8-109">DESCRIPTION</span></span>
<span data-ttu-id="6a8f8-110">O cmdlet **Remove-AzDeploymentManagerServiceTopology** exclui uma topologia de serviço.</span><span class="sxs-lookup"><span data-stu-id="6a8f8-110">The **Remove-AzDeploymentManagerServiceTopology** cmdlet deletes a service topology.</span></span>

<span data-ttu-id="6a8f8-111">Especifique a topologia de serviço pelo nome e o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6a8f8-111">Specify the service topology by its name and the resource group name.</span></span> <span data-ttu-id="6a8f8-112">Como alternativa, você pode fornecer o objeto ServiceTopology ou ResourceId.</span><span class="sxs-lookup"><span data-stu-id="6a8f8-112">Alternately, you can provide the ServiceTopology object or the ResourceId.</span></span>

## <span data-ttu-id="6a8f8-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6a8f8-113">EXAMPLES</span></span>

### <span data-ttu-id="6a8f8-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6a8f8-114">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology
```

<span data-ttu-id="6a8f8-115">Este comando exclui uma topologia de serviço chamada ContosoServiceTopology no ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="6a8f8-115">This command deletes a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="6a8f8-116">Exemplo 2: excluir uma topologia de serviço usando o identificador de recurso.</span><span class="sxs-lookup"><span data-stu-id="6a8f8-116">Example 2: Delete a service topology using the resource identifier.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerServiceTopology -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology"
```

<span data-ttu-id="6a8f8-117">Este comando exclui uma topologia de serviço chamada ContosoServiceTopology no ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="6a8f8-117">This command deletes a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="6a8f8-118">Exemplo 3: Excluir uma topologia de serviço usando o objeto de topologia de serviço.</span><span class="sxs-lookup"><span data-stu-id="6a8f8-118">Example 3: Delete a service topology using the service topology object.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerService -InputObject $serviceTopologyObject
```

<span data-ttu-id="6a8f8-119">Este comando exclui uma topologia de serviço cujo nome e ResourceGroup corresponderem às propriedades Name e ResourceGroupName do $serviceTopologyObject, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="6a8f8-119">This command deletes a service topology whose name and ResourceGroup match the Name and ResourceGroupName properties of the $serviceTopologyObject, respectively.</span></span>

## <span data-ttu-id="6a8f8-120">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="6a8f8-120">PARAMETERS</span></span>

### <span data-ttu-id="6a8f8-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a8f8-121">-DefaultProfile</span></span>
<span data-ttu-id="6a8f8-122">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6a8f8-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a8f8-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6a8f8-123">-InputObject</span></span>
<span data-ttu-id="6a8f8-124">O recurso a ser removido.</span><span class="sxs-lookup"><span data-stu-id="6a8f8-124">The resource to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6a8f8-125">-Name</span><span class="sxs-lookup"><span data-stu-id="6a8f8-125">-Name</span></span>
<span data-ttu-id="6a8f8-126">O nome da topologia de serviço.</span><span class="sxs-lookup"><span data-stu-id="6a8f8-126">The name of the service topology.</span></span>

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

### <span data-ttu-id="6a8f8-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6a8f8-127">-PassThru</span></span>
<span data-ttu-id="6a8f8-128">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="6a8f8-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="6a8f8-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a8f8-129">-ResourceGroupName</span></span>
<span data-ttu-id="6a8f8-130">O grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6a8f8-130">The resource group.</span></span>

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

### <span data-ttu-id="6a8f8-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6a8f8-131">-ResourceId</span></span>
<span data-ttu-id="6a8f8-132">O identificador de recurso.</span><span class="sxs-lookup"><span data-stu-id="6a8f8-132">The resource identifier.</span></span>

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

### <span data-ttu-id="6a8f8-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6a8f8-133">-Confirm</span></span>
<span data-ttu-id="6a8f8-134">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6a8f8-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a8f8-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a8f8-135">-WhatIf</span></span>
<span data-ttu-id="6a8f8-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6a8f8-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a8f8-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6a8f8-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a8f8-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a8f8-138">CommonParameters</span></span>
<span data-ttu-id="6a8f8-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a8f8-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a8f8-140">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6a8f8-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a8f8-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6a8f8-141">INPUTS</span></span>

### <span data-ttu-id="6a8f8-142">System.String</span><span class="sxs-lookup"><span data-stu-id="6a8f8-142">System.String</span></span>

### <span data-ttu-id="6a8f8-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="6a8f8-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="6a8f8-144">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="6a8f8-144">OUTPUTS</span></span>

### <span data-ttu-id="6a8f8-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6a8f8-145">System.Boolean</span></span>

## <span data-ttu-id="6a8f8-146">NOTES</span><span class="sxs-lookup"><span data-stu-id="6a8f8-146">NOTES</span></span>

## <span data-ttu-id="6a8f8-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6a8f8-147">RELATED LINKS</span></span>
