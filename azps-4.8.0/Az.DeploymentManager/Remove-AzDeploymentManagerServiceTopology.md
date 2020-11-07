---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerservicetopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerServiceTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerServiceTopology.md
ms.openlocfilehash: 7323883028d062cf11f4e1befe1ea42cb1f8bcb2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93948326"
---
# <span data-ttu-id="e4640-101">Remove-AzDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="e4640-101">Remove-AzDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="e4640-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e4640-102">SYNOPSIS</span></span>
<span data-ttu-id="e4640-103">Exclui a topologia de serviço.</span><span class="sxs-lookup"><span data-stu-id="e4640-103">Deletes the service topology.</span></span> <span data-ttu-id="e4640-104">Todos os serviços criados em uma topologia de serviço precisam ser excluídos antes de excluir a topologia de serviço.</span><span class="sxs-lookup"><span data-stu-id="e4640-104">All services created under a service topology need to be deleted before deleting the service topology.</span></span>

## <span data-ttu-id="e4640-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e4640-105">SYNTAX</span></span>

### <span data-ttu-id="e4640-106">Interativo (padrão)</span><span class="sxs-lookup"><span data-stu-id="e4640-106">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerServiceTopology [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4640-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="e4640-107">ResourceId</span></span>
```
Remove-AzDeploymentManagerServiceTopology [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4640-108">InputObject</span><span class="sxs-lookup"><span data-stu-id="e4640-108">InputObject</span></span>
```
Remove-AzDeploymentManagerServiceTopology [-InputObject] <PSServiceTopologyResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4640-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e4640-109">DESCRIPTION</span></span>
<span data-ttu-id="e4640-110">O cmdlet **Remove-AzDeploymentManagerServiceTopology** exclui uma topologia de serviço.</span><span class="sxs-lookup"><span data-stu-id="e4640-110">The **Remove-AzDeploymentManagerServiceTopology** cmdlet deletes a service topology.</span></span>

<span data-ttu-id="e4640-111">Especifique a topologia do serviço de acordo com o nome e o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e4640-111">Specify the service topology by its name and the resource group name.</span></span> <span data-ttu-id="e4640-112">Como alternativa, você pode fornecer o objeto imtopology ou o resourceId.</span><span class="sxs-lookup"><span data-stu-id="e4640-112">Alternately, you can provide the ServiceTopology object or the ResourceId.</span></span>

## <span data-ttu-id="e4640-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e4640-113">EXAMPLES</span></span>

### <span data-ttu-id="e4640-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e4640-114">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology
```

<span data-ttu-id="e4640-115">Esse comando exclui uma topologia de serviço chamada ContosoServiceTopology no ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="e4640-115">This command deletes a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="e4640-116">Exemplo 2: excluir uma topologia de serviço usando o identificador de recursos.</span><span class="sxs-lookup"><span data-stu-id="e4640-116">Example 2: Delete a service topology using the resource identifier.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerServiceTopology -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology"
```

<span data-ttu-id="e4640-117">Esse comando exclui uma topologia de serviço chamada ContosoServiceTopology no ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="e4640-117">This command deletes a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="e4640-118">Exemplo 3: excluir uma topologia de serviço usando o objeto de topologia de serviço.</span><span class="sxs-lookup"><span data-stu-id="e4640-118">Example 3: Delete a service topology using the service topology object.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerService -InputObject $serviceTopologyObject
```

<span data-ttu-id="e4640-119">Esse comando exclui uma topologia de serviço cujo nome e o meu nome do contato correspondam às propriedades Name e ResourceGroupName do $serviceTopologyObject, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="e4640-119">This command deletes a service topology whose name and ResourceGroup match the Name and ResourceGroupName properties of the $serviceTopologyObject, respectively.</span></span>

## <span data-ttu-id="e4640-120">OS</span><span class="sxs-lookup"><span data-stu-id="e4640-120">PARAMETERS</span></span>

### <span data-ttu-id="e4640-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4640-121">-DefaultProfile</span></span>
<span data-ttu-id="e4640-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e4640-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4640-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e4640-123">-InputObject</span></span>
<span data-ttu-id="e4640-124">O recurso a ser removido.</span><span class="sxs-lookup"><span data-stu-id="e4640-124">The resource to be removed.</span></span>

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

### <span data-ttu-id="e4640-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="e4640-125">-Name</span></span>
<span data-ttu-id="e4640-126">O nome da topologia de serviço.</span><span class="sxs-lookup"><span data-stu-id="e4640-126">The name of the service topology.</span></span>

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

### <span data-ttu-id="e4640-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e4640-127">-PassThru</span></span>
<span data-ttu-id="e4640-128">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="e4640-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="e4640-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4640-129">-ResourceGroupName</span></span>
<span data-ttu-id="e4640-130">O grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e4640-130">The resource group.</span></span>

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

### <span data-ttu-id="e4640-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e4640-131">-ResourceId</span></span>
<span data-ttu-id="e4640-132">O identificador do recurso.</span><span class="sxs-lookup"><span data-stu-id="e4640-132">The resource identifier.</span></span>

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

### <span data-ttu-id="e4640-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e4640-133">-Confirm</span></span>
<span data-ttu-id="e4640-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4640-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4640-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4640-135">-WhatIf</span></span>
<span data-ttu-id="e4640-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e4640-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4640-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e4640-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4640-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4640-138">CommonParameters</span></span>
<span data-ttu-id="e4640-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4640-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4640-140">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e4640-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4640-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e4640-141">INPUTS</span></span>

### <span data-ttu-id="e4640-142">System. String</span><span class="sxs-lookup"><span data-stu-id="e4640-142">System.String</span></span>

### <span data-ttu-id="e4640-143">Microsoft. Azure. Commands. DeploymentManager. Models. PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="e4640-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="e4640-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e4640-144">OUTPUTS</span></span>

### <span data-ttu-id="e4640-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e4640-145">System.Boolean</span></span>

## <span data-ttu-id="e4640-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e4640-146">NOTES</span></span>

## <span data-ttu-id="e4640-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e4640-147">RELATED LINKS</span></span>
