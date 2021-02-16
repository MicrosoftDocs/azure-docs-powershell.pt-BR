---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerservicetopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerServiceTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerServiceTopology.md
ms.openlocfilehash: 7323883028d062cf11f4e1befe1ea42cb1f8bcb2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117706"
---
# <span data-ttu-id="4b3be-101">Remove-AzDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="4b3be-101">Remove-AzDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="4b3be-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4b3be-102">SYNOPSIS</span></span>
<span data-ttu-id="4b3be-103">Exclui a topologia do serviço.</span><span class="sxs-lookup"><span data-stu-id="4b3be-103">Deletes the service topology.</span></span> <span data-ttu-id="4b3be-104">Todos os serviços criados em uma topologia de serviço precisam ser excluídos antes de excluir a topologia do serviço.</span><span class="sxs-lookup"><span data-stu-id="4b3be-104">All services created under a service topology need to be deleted before deleting the service topology.</span></span>

## <span data-ttu-id="4b3be-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4b3be-105">SYNTAX</span></span>

### <span data-ttu-id="4b3be-106">Interativo (Padrão)</span><span class="sxs-lookup"><span data-stu-id="4b3be-106">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerServiceTopology [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b3be-107">Resourceid</span><span class="sxs-lookup"><span data-stu-id="4b3be-107">ResourceId</span></span>
```
Remove-AzDeploymentManagerServiceTopology [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b3be-108">Inputobject</span><span class="sxs-lookup"><span data-stu-id="4b3be-108">InputObject</span></span>
```
Remove-AzDeploymentManagerServiceTopology [-InputObject] <PSServiceTopologyResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b3be-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="4b3be-109">DESCRIPTION</span></span>
<span data-ttu-id="4b3be-110">O cmdlet **Remove-AzDeploymentManagerServiceTopology** exclui uma topologia de serviço.</span><span class="sxs-lookup"><span data-stu-id="4b3be-110">The **Remove-AzDeploymentManagerServiceTopology** cmdlet deletes a service topology.</span></span>

<span data-ttu-id="4b3be-111">Especifique a topologia do serviço pelo nome e pelo nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4b3be-111">Specify the service topology by its name and the resource group name.</span></span> <span data-ttu-id="4b3be-112">Como alternativa, você pode fornecer o objeto ServiceTopology ou o ResourceId.</span><span class="sxs-lookup"><span data-stu-id="4b3be-112">Alternately, you can provide the ServiceTopology object or the ResourceId.</span></span>

## <span data-ttu-id="4b3be-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4b3be-113">EXAMPLES</span></span>

### <span data-ttu-id="4b3be-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4b3be-114">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology
```

<span data-ttu-id="4b3be-115">Esse comando exclui uma topologia de serviço chamada ContosoServiceTopology no Grupo ContosoResource.</span><span class="sxs-lookup"><span data-stu-id="4b3be-115">This command deletes a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="4b3be-116">Exemplo 2: Excluir uma topologia de serviço usando o identificador de recurso.</span><span class="sxs-lookup"><span data-stu-id="4b3be-116">Example 2: Delete a service topology using the resource identifier.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerServiceTopology -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology"
```

<span data-ttu-id="4b3be-117">Esse comando exclui uma topologia de serviço chamada ContosoServiceTopology no Grupo ContosoResource.</span><span class="sxs-lookup"><span data-stu-id="4b3be-117">This command deletes a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="4b3be-118">Exemplo 3: Excluir uma topologia de serviço usando o objeto de topologia de serviço.</span><span class="sxs-lookup"><span data-stu-id="4b3be-118">Example 3: Delete a service topology using the service topology object.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerService -InputObject $serviceTopologyObject
```

<span data-ttu-id="4b3be-119">Esse comando exclui uma topologia de serviço cujo nome e Grupo de Recursos corresponderem às propriedades Nome e NomeDoGrupo de Recursos do $serviceTopologyObject, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="4b3be-119">This command deletes a service topology whose name and ResourceGroup match the Name and ResourceGroupName properties of the $serviceTopologyObject, respectively.</span></span>

## <span data-ttu-id="4b3be-120">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4b3be-120">PARAMETERS</span></span>

### <span data-ttu-id="4b3be-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b3be-121">-DefaultProfile</span></span>
<span data-ttu-id="4b3be-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4b3be-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b3be-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4b3be-123">-InputObject</span></span>
<span data-ttu-id="4b3be-124">O recurso a ser removido.</span><span class="sxs-lookup"><span data-stu-id="4b3be-124">The resource to be removed.</span></span>

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

### <span data-ttu-id="4b3be-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="4b3be-125">-Name</span></span>
<span data-ttu-id="4b3be-126">O nome da topologia do serviço.</span><span class="sxs-lookup"><span data-stu-id="4b3be-126">The name of the service topology.</span></span>

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

### <span data-ttu-id="4b3be-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4b3be-127">-PassThru</span></span>
<span data-ttu-id="4b3be-128">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="4b3be-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="4b3be-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b3be-129">-ResourceGroupName</span></span>
<span data-ttu-id="4b3be-130">O grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4b3be-130">The resource group.</span></span>

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

### <span data-ttu-id="4b3be-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4b3be-131">-ResourceId</span></span>
<span data-ttu-id="4b3be-132">O identificador de recurso.</span><span class="sxs-lookup"><span data-stu-id="4b3be-132">The resource identifier.</span></span>

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

### <span data-ttu-id="4b3be-133">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="4b3be-133">-Confirm</span></span>
<span data-ttu-id="4b3be-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4b3be-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b3be-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b3be-135">-WhatIf</span></span>
<span data-ttu-id="4b3be-136">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="4b3be-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b3be-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4b3be-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b3be-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b3be-138">CommonParameters</span></span>
<span data-ttu-id="4b3be-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b3be-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b3be-140">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4b3be-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b3be-141">Entradas</span><span class="sxs-lookup"><span data-stu-id="4b3be-141">INPUTS</span></span>

### <span data-ttu-id="4b3be-142">System.String</span><span class="sxs-lookup"><span data-stu-id="4b3be-142">System.String</span></span>

### <span data-ttu-id="4b3be-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="4b3be-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="4b3be-144">Saídas</span><span class="sxs-lookup"><span data-stu-id="4b3be-144">OUTPUTS</span></span>

### <span data-ttu-id="4b3be-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4b3be-145">System.Boolean</span></span>

## <span data-ttu-id="4b3be-146">Notas</span><span class="sxs-lookup"><span data-stu-id="4b3be-146">NOTES</span></span>

## <span data-ttu-id="4b3be-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4b3be-147">RELATED LINKS</span></span>
