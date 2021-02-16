---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerService.md
ms.openlocfilehash: 4828471d684e82d67a10bed7340cc560e843210a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117705"
---
# <span data-ttu-id="884bd-101">Remove-AzDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="884bd-101">Remove-AzDeploymentManagerService</span></span>

## <span data-ttu-id="884bd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="884bd-102">SYNOPSIS</span></span>
<span data-ttu-id="884bd-103">Exclui o serviço..</span><span class="sxs-lookup"><span data-stu-id="884bd-103">Deletes the service..</span></span> <span data-ttu-id="884bd-104">Todas as unidades de serviço criadas em um serviço precisam ser excluídas antes de excluir o serviço.</span><span class="sxs-lookup"><span data-stu-id="884bd-104">All service units created under a service need to be deleted before deleting the service.</span></span>

## <span data-ttu-id="884bd-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="884bd-105">SYNTAX</span></span>

### <span data-ttu-id="884bd-106">Interativo (Padrão)</span><span class="sxs-lookup"><span data-stu-id="884bd-106">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerService [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-Name] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="884bd-107">ByServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="884bd-107">ByServiceTopologyObject</span></span>
```
Remove-AzDeploymentManagerService [-Name] <String> [-ServiceTopologyObject] <PSServiceTopologyResource>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="884bd-108">ByServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="884bd-108">ByServiceTopologyResourceId</span></span>
```
Remove-AzDeploymentManagerService [-Name] <String> [-ServiceTopologyResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="884bd-109">Resourceid</span><span class="sxs-lookup"><span data-stu-id="884bd-109">ResourceId</span></span>
```
Remove-AzDeploymentManagerService [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="884bd-110">Inputobject</span><span class="sxs-lookup"><span data-stu-id="884bd-110">InputObject</span></span>
```
Remove-AzDeploymentManagerService [-InputObject] <PSServiceResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="884bd-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="884bd-111">DESCRIPTION</span></span>
<span data-ttu-id="884bd-112">O cmdlet **Remove-AzDeploymentManagerService** exclui um serviço em uma topologia de serviço.</span><span class="sxs-lookup"><span data-stu-id="884bd-112">The **Remove-AzDeploymentManagerService** cmdlet deletes a service under a service topology.</span></span>
<span data-ttu-id="884bd-113">Especifique o serviço pelo nome, topologia do serviço em que ele está e o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="884bd-113">Specify the service by its name, service topology it is in and the resource group name.</span></span> <span data-ttu-id="884bd-114">Como alternativa, você pode fornecer o objeto Serviço ou o ResourceId.</span><span class="sxs-lookup"><span data-stu-id="884bd-114">Alternately, you can provide the Service object or the ResourceId.</span></span>

## <span data-ttu-id="884bd-115">Exemplos</span><span class="sxs-lookup"><span data-stu-id="884bd-115">EXAMPLES</span></span>

### <span data-ttu-id="884bd-116">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="884bd-116">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerService -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -Name ContosoService1
```

<span data-ttu-id="884bd-117">Esse comando exclui um serviço chamado ContosoService1 em uma topologia de serviço chamada ContosoServiceTopology no Grupo ContosoResource.</span><span class="sxs-lookup"><span data-stu-id="884bd-117">This command deletes a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="884bd-118">Exemplo 2: Excluir um serviço usando o identificador de recurso.</span><span class="sxs-lookup"><span data-stu-id="884bd-118">Example 2: Delete a service using the resource identifier.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerService -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1"
```

<span data-ttu-id="884bd-119">Esse comando exclui um serviço chamado ContosoService1 em uma topologia de serviço chamada ContosoServiceTopology no Grupo ContosoResource.</span><span class="sxs-lookup"><span data-stu-id="884bd-119">This command deletes a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="884bd-120">Exemplo 3: Excluir um serviço usando o objeto de serviço.</span><span class="sxs-lookup"><span data-stu-id="884bd-120">Example 3: Delete a service using the service object.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerService -InputObject $serviceObject
```

<span data-ttu-id="884bd-121">Esse comando exclui um serviço cujo nome, nome de topologia de serviço e Grupo de Recursos corresponderem às propriedades Nome, ServiceTopologyName e ResourceGroupName do $serviceObject, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="884bd-121">This command deletes a service whose name, service topology name and ResourceGroup match the Name, ServiceTopologyName and ResourceGroupName properties of the $serviceObject, respectively.</span></span>

## <span data-ttu-id="884bd-122">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="884bd-122">PARAMETERS</span></span>

### <span data-ttu-id="884bd-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="884bd-123">-DefaultProfile</span></span>
<span data-ttu-id="884bd-124">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="884bd-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="884bd-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="884bd-125">-InputObject</span></span>
<span data-ttu-id="884bd-126">Objeto de serviço.</span><span class="sxs-lookup"><span data-stu-id="884bd-126">Service object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="884bd-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="884bd-127">-Name</span></span>
<span data-ttu-id="884bd-128">O nome do serviço.</span><span class="sxs-lookup"><span data-stu-id="884bd-128">The name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceTopologyObject, ByServiceTopologyResourceId
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="884bd-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="884bd-129">-PassThru</span></span>
<span data-ttu-id="884bd-130">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="884bd-130">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="884bd-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="884bd-131">-ResourceGroupName</span></span>
<span data-ttu-id="884bd-132">O grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="884bd-132">The resource group.</span></span>

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

### <span data-ttu-id="884bd-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="884bd-133">-ResourceId</span></span>
<span data-ttu-id="884bd-134">O identificador de recurso.</span><span class="sxs-lookup"><span data-stu-id="884bd-134">The resource identifier.</span></span>

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

### <span data-ttu-id="884bd-135">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="884bd-135">-ServiceTopologyName</span></span>
<span data-ttu-id="884bd-136">O nome da topologia do serviço.</span><span class="sxs-lookup"><span data-stu-id="884bd-136">The name of the service topology.</span></span>

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

### <span data-ttu-id="884bd-137">-ServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="884bd-137">-ServiceTopologyObject</span></span>
<span data-ttu-id="884bd-138">O objeto de topologia de serviço no qual o serviço deve ser criado.</span><span class="sxs-lookup"><span data-stu-id="884bd-138">The service topology object in which the service should be created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource
Parameter Sets: ByServiceTopologyObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="884bd-139">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="884bd-139">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="884bd-140">O identificador de recurso de topologia de serviço no qual o serviço deve ser criado.</span><span class="sxs-lookup"><span data-stu-id="884bd-140">The service topology resource identifier in which the service should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: ByServiceTopologyResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="884bd-141">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="884bd-141">-Confirm</span></span>
<span data-ttu-id="884bd-142">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="884bd-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="884bd-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="884bd-143">-WhatIf</span></span>
<span data-ttu-id="884bd-144">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="884bd-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="884bd-145">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="884bd-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="884bd-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="884bd-146">CommonParameters</span></span>
<span data-ttu-id="884bd-147">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="884bd-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="884bd-148">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="884bd-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="884bd-149">Entradas</span><span class="sxs-lookup"><span data-stu-id="884bd-149">INPUTS</span></span>

### <span data-ttu-id="884bd-150">System.String</span><span class="sxs-lookup"><span data-stu-id="884bd-150">System.String</span></span>

### <span data-ttu-id="884bd-151">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="884bd-151">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="884bd-152">Saídas</span><span class="sxs-lookup"><span data-stu-id="884bd-152">OUTPUTS</span></span>

### <span data-ttu-id="884bd-153">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="884bd-153">System.Boolean</span></span>

## <span data-ttu-id="884bd-154">Notas</span><span class="sxs-lookup"><span data-stu-id="884bd-154">NOTES</span></span>

## <span data-ttu-id="884bd-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="884bd-155">RELATED LINKS</span></span>
