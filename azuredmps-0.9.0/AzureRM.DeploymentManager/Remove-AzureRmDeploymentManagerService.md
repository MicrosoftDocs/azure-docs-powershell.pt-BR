---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/remove-azurermdeploymentmanagerservice
schema: 2.0.0
ms.openlocfilehash: 4b2cd4ef2dde674b10d51dc378578acbd13c4a7b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93425680"
---
# <span data-ttu-id="a6889-101">Remove-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="a6889-101">Remove-AzureRmDeploymentManagerService</span></span>

## <span data-ttu-id="a6889-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a6889-102">SYNOPSIS</span></span>
<span data-ttu-id="a6889-103">Exclui um serviço em uma topologia de serviço.</span><span class="sxs-lookup"><span data-stu-id="a6889-103">Deletes a service in a service topology.</span></span>

## <span data-ttu-id="a6889-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a6889-104">SYNTAX</span></span>

### <span data-ttu-id="a6889-105">Interativo (padrão)</span><span class="sxs-lookup"><span data-stu-id="a6889-105">Interactive (Default)</span></span>
```
Remove-AzureRmDeploymentManagerService [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a6889-106">ByServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="a6889-106">ByServiceTopologyObject</span></span>
```
Remove-AzureRmDeploymentManagerService [-Name] <String> [-ServiceTopology] <PSServiceTopologyResource> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6889-107">ByServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="a6889-107">ByServiceTopologyResourceId</span></span>
```
Remove-AzureRmDeploymentManagerService [-Name] <String> [-ServiceTopologyResourceId] <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6889-108">Identificação</span><span class="sxs-lookup"><span data-stu-id="a6889-108">ResourceId</span></span>
```
Remove-AzureRmDeploymentManagerService [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6889-109">InputObject</span><span class="sxs-lookup"><span data-stu-id="a6889-109">InputObject</span></span>
```
Remove-AzureRmDeploymentManagerService [-Service] <PSServiceResource> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6889-110">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a6889-110">DESCRIPTION</span></span>
<span data-ttu-id="a6889-111">O cmdlet **Remove-AzureRmDeploymentManagerService** exclui um serviço em uma topologia de serviço.</span><span class="sxs-lookup"><span data-stu-id="a6889-111">The **Remove-AzureRmDeploymentManagerService** cmdlet deletes a service under a service topology.</span></span>
<span data-ttu-id="a6889-112">Especifique o serviço pelo nome, topologia de serviço em que ele se encontra e o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a6889-112">Specify the service by its name, service topology it is in and the resource group name.</span></span> <span data-ttu-id="a6889-113">Como alternativa, você pode fornecer o objeto de serviço ou a ResourceId.</span><span class="sxs-lookup"><span data-stu-id="a6889-113">Alternately, you can provide the Service object or the ResourceId.</span></span>

## <span data-ttu-id="a6889-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a6889-114">EXAMPLES</span></span>

### <span data-ttu-id="a6889-115">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a6889-115">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerService -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -Name ContosoService1
```

<span data-ttu-id="a6889-116">Esse comando exclui um serviço denominado ContosoService1 em uma topologia de serviço chamada ContosoServiceTopology no ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="a6889-116">This command deletes a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="a6889-117">Exemplo 2: excluir um serviço usando o identificador de recursos.</span><span class="sxs-lookup"><span data-stu-id="a6889-117">Example 2: Delete a service using the resource identifier.</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerService -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1"
```

<span data-ttu-id="a6889-118">Esse comando exclui um serviço denominado ContosoService1 em uma topologia de serviço chamada ContosoServiceTopology no ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="a6889-118">This command deletes a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="a6889-119">Exemplo 3: excluir um serviço usando o objeto de serviço.</span><span class="sxs-lookup"><span data-stu-id="a6889-119">Example 3: Delete a service using the service object.</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerService -Service $serviceObject
```

<span data-ttu-id="a6889-120">Esse comando exclui um serviço cujo nome, nome da topologia de serviço e o nome do contato correspondem às propriedades Name, imtopologyname e ResourceGroupName da $serviceObject, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="a6889-120">This command deletes a service whose name, service topology name and ResourceGroup match the Name, ServiceTopologyName and ResourceGroupName properties of the $serviceObject, respectively.</span></span>

## <span data-ttu-id="a6889-121">OS</span><span class="sxs-lookup"><span data-stu-id="a6889-121">PARAMETERS</span></span>

### <span data-ttu-id="a6889-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6889-122">-DefaultProfile</span></span>
<span data-ttu-id="a6889-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a6889-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6889-124">-Force</span><span class="sxs-lookup"><span data-stu-id="a6889-124">-Force</span></span>
<span data-ttu-id="a6889-125">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="a6889-125">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="a6889-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="a6889-126">-Name</span></span>
<span data-ttu-id="a6889-127">O nome do serviço.</span><span class="sxs-lookup"><span data-stu-id="a6889-127">The name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceTopologyObject, ByServiceTopologyResourceId
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6889-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a6889-128">-PassThru</span></span>
<span data-ttu-id="a6889-129">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="a6889-129">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="a6889-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6889-130">-ResourceGroupName</span></span>
<span data-ttu-id="a6889-131">O grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a6889-131">The resource group.</span></span>

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

### <span data-ttu-id="a6889-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a6889-132">-ResourceId</span></span>
<span data-ttu-id="a6889-133">O identificador do recurso.</span><span class="sxs-lookup"><span data-stu-id="a6889-133">The resource identifier.</span></span>

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

### <span data-ttu-id="a6889-134">-Serviço</span><span class="sxs-lookup"><span data-stu-id="a6889-134">-Service</span></span>
<span data-ttu-id="a6889-135">O recurso a ser removido.</span><span class="sxs-lookup"><span data-stu-id="a6889-135">The resource to be removed.</span></span>

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

### <span data-ttu-id="a6889-136">-Outtopology</span><span class="sxs-lookup"><span data-stu-id="a6889-136">-ServiceTopology</span></span>
<span data-ttu-id="a6889-137">O objeto de topologia de serviço no qual o serviço deve ser criado.</span><span class="sxs-lookup"><span data-stu-id="a6889-137">The service topology object in which the service should be created.</span></span>

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

### <span data-ttu-id="a6889-138">-Imtopologyname</span><span class="sxs-lookup"><span data-stu-id="a6889-138">-ServiceTopologyName</span></span>
<span data-ttu-id="a6889-139">O nome da topologia de serviço à qual o serviço pertence.</span><span class="sxs-lookup"><span data-stu-id="a6889-139">The name of the service topology the service belongs to.</span></span>

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

### <span data-ttu-id="a6889-140">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="a6889-140">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="a6889-141">O identificador de recursos de topologia de serviço no qual o serviço deve ser criado.</span><span class="sxs-lookup"><span data-stu-id="a6889-141">The service topology resource identifier in which the service should be created.</span></span>

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

### <span data-ttu-id="a6889-142">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a6889-142">-Confirm</span></span>
<span data-ttu-id="a6889-143">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6889-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6889-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6889-144">-WhatIf</span></span>
<span data-ttu-id="a6889-145">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a6889-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6889-146">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a6889-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6889-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6889-147">CommonParameters</span></span>
<span data-ttu-id="a6889-148">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6889-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6889-149">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6889-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6889-150">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a6889-150">INPUTS</span></span>

### <span data-ttu-id="a6889-151">Microsoft. Azure. Commands. DeploymentManager. Models. PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="a6889-151">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="a6889-152">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a6889-152">OUTPUTS</span></span>

### <span data-ttu-id="a6889-153">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a6889-153">System.Boolean</span></span>

## <span data-ttu-id="a6889-154">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a6889-154">NOTES</span></span>

## <span data-ttu-id="a6889-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a6889-155">RELATED LINKS</span></span>

[<span data-ttu-id="a6889-156">New-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="a6889-156">New-AzureRmDeploymentManagerService</span></span>](./New-AzureRmDeploymentManagerService.md)

[<span data-ttu-id="a6889-157">Get-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="a6889-157">Get-AzureRmDeploymentManagerService</span></span>](./Get-AzureRmDeploymentManagerService.md)

[<span data-ttu-id="a6889-158">Set-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="a6889-158">Set-AzureRmDeploymentManagerService</span></span>](./Set-AzureRmDeploymentManagerService.md)