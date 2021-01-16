---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerService.md
ms.openlocfilehash: 4828471d684e82d67a10bed7340cc560e843210a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98272915"
---
# <span data-ttu-id="9ad5b-101">Remove-AzDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="9ad5b-101">Remove-AzDeploymentManagerService</span></span>

## <span data-ttu-id="9ad5b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9ad5b-102">SYNOPSIS</span></span>
<span data-ttu-id="9ad5b-103">Exclui o serviço..</span><span class="sxs-lookup"><span data-stu-id="9ad5b-103">Deletes the service..</span></span> <span data-ttu-id="9ad5b-104">Todas as unidades de serviço criadas em um serviço precisam ser excluídas antes de excluir o serviço.</span><span class="sxs-lookup"><span data-stu-id="9ad5b-104">All service units created under a service need to be deleted before deleting the service.</span></span>

## <span data-ttu-id="9ad5b-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9ad5b-105">SYNTAX</span></span>

### <span data-ttu-id="9ad5b-106">Interativo (padrão)</span><span class="sxs-lookup"><span data-stu-id="9ad5b-106">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerService [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-Name] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9ad5b-107">ByServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="9ad5b-107">ByServiceTopologyObject</span></span>
```
Remove-AzDeploymentManagerService [-Name] <String> [-ServiceTopologyObject] <PSServiceTopologyResource>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ad5b-108">ByServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="9ad5b-108">ByServiceTopologyResourceId</span></span>
```
Remove-AzDeploymentManagerService [-Name] <String> [-ServiceTopologyResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ad5b-109">Identificação</span><span class="sxs-lookup"><span data-stu-id="9ad5b-109">ResourceId</span></span>
```
Remove-AzDeploymentManagerService [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ad5b-110">InputObject</span><span class="sxs-lookup"><span data-stu-id="9ad5b-110">InputObject</span></span>
```
Remove-AzDeploymentManagerService [-InputObject] <PSServiceResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ad5b-111">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9ad5b-111">DESCRIPTION</span></span>
<span data-ttu-id="9ad5b-112">O cmdlet **Remove-AzDeploymentManagerService** exclui um serviço em uma topologia de serviço.</span><span class="sxs-lookup"><span data-stu-id="9ad5b-112">The **Remove-AzDeploymentManagerService** cmdlet deletes a service under a service topology.</span></span>
<span data-ttu-id="9ad5b-113">Especifique o serviço pelo nome, topologia de serviço em que ele se encontra e o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9ad5b-113">Specify the service by its name, service topology it is in and the resource group name.</span></span> <span data-ttu-id="9ad5b-114">Como alternativa, você pode fornecer o objeto de serviço ou a ResourceId.</span><span class="sxs-lookup"><span data-stu-id="9ad5b-114">Alternately, you can provide the Service object or the ResourceId.</span></span>

## <span data-ttu-id="9ad5b-115">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9ad5b-115">EXAMPLES</span></span>

### <span data-ttu-id="9ad5b-116">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9ad5b-116">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerService -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -Name ContosoService1
```

<span data-ttu-id="9ad5b-117">Esse comando exclui um serviço denominado ContosoService1 em uma topologia de serviço chamada ContosoServiceTopology no ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="9ad5b-117">This command deletes a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="9ad5b-118">Exemplo 2: excluir um serviço usando o identificador de recursos.</span><span class="sxs-lookup"><span data-stu-id="9ad5b-118">Example 2: Delete a service using the resource identifier.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerService -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1"
```

<span data-ttu-id="9ad5b-119">Esse comando exclui um serviço denominado ContosoService1 em uma topologia de serviço chamada ContosoServiceTopology no ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="9ad5b-119">This command deletes a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="9ad5b-120">Exemplo 3: excluir um serviço usando o objeto de serviço.</span><span class="sxs-lookup"><span data-stu-id="9ad5b-120">Example 3: Delete a service using the service object.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerService -InputObject $serviceObject
```

<span data-ttu-id="9ad5b-121">Esse comando exclui um serviço cujo nome, nome da topologia de serviço e o nome do contato correspondem às propriedades Name, imtopologyname e ResourceGroupName da $serviceObject, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="9ad5b-121">This command deletes a service whose name, service topology name and ResourceGroup match the Name, ServiceTopologyName and ResourceGroupName properties of the $serviceObject, respectively.</span></span>

## <span data-ttu-id="9ad5b-122">OS</span><span class="sxs-lookup"><span data-stu-id="9ad5b-122">PARAMETERS</span></span>

### <span data-ttu-id="9ad5b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ad5b-123">-DefaultProfile</span></span>
<span data-ttu-id="9ad5b-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9ad5b-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ad5b-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9ad5b-125">-InputObject</span></span>
<span data-ttu-id="9ad5b-126">Objeto de serviço.</span><span class="sxs-lookup"><span data-stu-id="9ad5b-126">Service object.</span></span>

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

### <span data-ttu-id="9ad5b-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="9ad5b-127">-Name</span></span>
<span data-ttu-id="9ad5b-128">O nome do serviço.</span><span class="sxs-lookup"><span data-stu-id="9ad5b-128">The name of the service.</span></span>

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

### <span data-ttu-id="9ad5b-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9ad5b-129">-PassThru</span></span>
<span data-ttu-id="9ad5b-130">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="9ad5b-130">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="9ad5b-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ad5b-131">-ResourceGroupName</span></span>
<span data-ttu-id="9ad5b-132">O grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9ad5b-132">The resource group.</span></span>

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

### <span data-ttu-id="9ad5b-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9ad5b-133">-ResourceId</span></span>
<span data-ttu-id="9ad5b-134">O identificador do recurso.</span><span class="sxs-lookup"><span data-stu-id="9ad5b-134">The resource identifier.</span></span>

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

### <span data-ttu-id="9ad5b-135">-Imtopologyname</span><span class="sxs-lookup"><span data-stu-id="9ad5b-135">-ServiceTopologyName</span></span>
<span data-ttu-id="9ad5b-136">O nome da topologia de serviço.</span><span class="sxs-lookup"><span data-stu-id="9ad5b-136">The name of the service topology.</span></span>

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

### <span data-ttu-id="9ad5b-137">-Imtopologyobject</span><span class="sxs-lookup"><span data-stu-id="9ad5b-137">-ServiceTopologyObject</span></span>
<span data-ttu-id="9ad5b-138">O objeto de topologia de serviço no qual o serviço deve ser criado.</span><span class="sxs-lookup"><span data-stu-id="9ad5b-138">The service topology object in which the service should be created.</span></span>

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

### <span data-ttu-id="9ad5b-139">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="9ad5b-139">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="9ad5b-140">O identificador de recursos de topologia de serviço no qual o serviço deve ser criado.</span><span class="sxs-lookup"><span data-stu-id="9ad5b-140">The service topology resource identifier in which the service should be created.</span></span>

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

### <span data-ttu-id="9ad5b-141">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9ad5b-141">-Confirm</span></span>
<span data-ttu-id="9ad5b-142">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9ad5b-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ad5b-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ad5b-143">-WhatIf</span></span>
<span data-ttu-id="9ad5b-144">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9ad5b-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ad5b-145">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9ad5b-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ad5b-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ad5b-146">CommonParameters</span></span>
<span data-ttu-id="9ad5b-147">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ad5b-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ad5b-148">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9ad5b-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ad5b-149">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9ad5b-149">INPUTS</span></span>

### <span data-ttu-id="9ad5b-150">System. String</span><span class="sxs-lookup"><span data-stu-id="9ad5b-150">System.String</span></span>

### <span data-ttu-id="9ad5b-151">Microsoft. Azure. Commands. DeploymentManager. Models. PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="9ad5b-151">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="9ad5b-152">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9ad5b-152">OUTPUTS</span></span>

### <span data-ttu-id="9ad5b-153">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9ad5b-153">System.Boolean</span></span>

## <span data-ttu-id="9ad5b-154">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9ad5b-154">NOTES</span></span>

## <span data-ttu-id="9ad5b-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9ad5b-155">RELATED LINKS</span></span>
