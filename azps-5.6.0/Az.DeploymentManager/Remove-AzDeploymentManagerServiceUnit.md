---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerserviceunit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerServiceUnit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerServiceUnit.md
ms.openlocfilehash: db7291f143abc5305f79f6b41310a5526c9fbb3e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887175"
---
# <span data-ttu-id="d241a-101">Remove-AzDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="d241a-101">Remove-AzDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="d241a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d241a-102">SYNOPSIS</span></span>
<span data-ttu-id="d241a-103">Exclui a unidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="d241a-103">Deletes the service unit.</span></span>

## <span data-ttu-id="d241a-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d241a-104">SYNTAX</span></span>

### <span data-ttu-id="d241a-105">Interativo (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d241a-105">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-ServiceName] <String> [-Name] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d241a-106">ByTopologyObjectAndServiceName</span><span class="sxs-lookup"><span data-stu-id="d241a-106">ByTopologyObjectAndServiceName</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-ServiceName] <String> [-Name] <String>
 [-ServiceTopologyObject] <PSServiceTopologyResource> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d241a-107">ByTopologyResourceAndServiceName</span><span class="sxs-lookup"><span data-stu-id="d241a-107">ByTopologyResourceAndServiceName</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-ServiceName] <String> [-Name] <String>
 [-ServiceTopologyResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d241a-108">ByServiceObject</span><span class="sxs-lookup"><span data-stu-id="d241a-108">ByServiceObject</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-Name] <String> [-ServiceObject] <PSServiceResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d241a-109">ByServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="d241a-109">ByServiceResourceId</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-Name] <String> [-ServiceResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d241a-110">ResourceId</span><span class="sxs-lookup"><span data-stu-id="d241a-110">ResourceId</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d241a-111">InputObject</span><span class="sxs-lookup"><span data-stu-id="d241a-111">InputObject</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-InputObject] <PSServiceUnitResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d241a-112">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d241a-112">DESCRIPTION</span></span>
<span data-ttu-id="d241a-113">O cmdlet **Remove-AzDeploymentManagerServiceUnit** exclui uma unidade de serviço em um serviço.</span><span class="sxs-lookup"><span data-stu-id="d241a-113">The **Remove-AzDeploymentManagerServiceUnit** cmdlet deletes a service unit in a service.</span></span>

<span data-ttu-id="d241a-114">Especifique a unidade de serviço pelo nome, o serviço no qual foi definida, o nome da topologia do serviço e o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d241a-114">Specify the service unit by its name, the service under which it was defined, the service topology name and the resource group name.</span></span> <span data-ttu-id="d241a-115">Como alternativa, você pode fornecer o objeto ServiceUnit ou ResourceId.</span><span class="sxs-lookup"><span data-stu-id="d241a-115">Alternately, you can provide the ServiceUnit object or the ResourceId.</span></span>

## <span data-ttu-id="d241a-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d241a-116">EXAMPLES</span></span>

### <span data-ttu-id="d241a-117">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d241a-117">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -ServiceName ContosoService1  -Name ContosoService1Storage
```

<span data-ttu-id="d241a-118">Este comando exclui uma unidade de serviço chamada ContosoService1Storage em um serviço ContosoService1 em uma topologia de serviço chamada ContosoServiceTopology no ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="d241a-118">This command deletes a service unit named ContosoService1Storage under a service ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="d241a-119">Exemplo 2: Excluir uma unidade de serviço usando o identificador de recurso.</span><span class="sxs-lookup"><span data-stu-id="d241a-119">Example 2: Delete a service unit using the resource identifier.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerServiceUnit -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1/serviceUnits/ContosoService1Storage"
```

<span data-ttu-id="d241a-120">Este comando obtém uma unidade de serviço chamada ContosoService1Storage em um serviço ContosoService1 em uma topologia de serviço chamada ContosoServiceTopology no ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="d241a-120">This command gets a service unit named ContosoService1Storage under a service ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="d241a-121">Exemplo 3: Excluir uma unidade de serviço usando o objeto da unidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="d241a-121">Example 3: Delete a service unit using the service unit object.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerServiceUnit -InputObject $serviceUnitObject
```

<span data-ttu-id="d241a-122">Este comando exclui uma unidade de serviço cujo nome, nome do serviço, nome da topologia de serviço e ResourceGroup corresponderão às propriedades Name, ServiceName, ServiceTopologyName e ResourceGroupName do $serviceUnitObject, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="d241a-122">This command deletes a service unit whose name, service name, service topology name and ResourceGroup match the Name, ServiceName, ServiceTopologyName and ResourceGroupName properties of the $serviceUnitObject, respectively.</span></span>

## <span data-ttu-id="d241a-123">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d241a-123">PARAMETERS</span></span>

### <span data-ttu-id="d241a-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d241a-124">-DefaultProfile</span></span>
<span data-ttu-id="d241a-125">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d241a-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d241a-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d241a-126">-InputObject</span></span>
<span data-ttu-id="d241a-127">Objeto de recurso da unidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="d241a-127">Service unit resource object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d241a-128">-Name</span><span class="sxs-lookup"><span data-stu-id="d241a-128">-Name</span></span>
<span data-ttu-id="d241a-129">O nome da unidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="d241a-129">The name of the service unit.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByTopologyObjectAndServiceName, ByTopologyResourceAndServiceName, ByServiceObject, ByServiceResourceId
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d241a-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d241a-130">-PassThru</span></span>
<span data-ttu-id="d241a-131">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="d241a-131">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="d241a-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d241a-132">-ResourceGroupName</span></span>
<span data-ttu-id="d241a-133">O grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d241a-133">The resource group.</span></span>

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

### <span data-ttu-id="d241a-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d241a-134">-ResourceId</span></span>
<span data-ttu-id="d241a-135">O identificador de recurso.</span><span class="sxs-lookup"><span data-stu-id="d241a-135">The resource identifier.</span></span>

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

### <span data-ttu-id="d241a-136">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="d241a-136">-ServiceName</span></span>
<span data-ttu-id="d241a-137">O nome do serviço do que a unidade de serviço faz parte.</span><span class="sxs-lookup"><span data-stu-id="d241a-137">The name of the service the service unit is part of.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByTopologyObjectAndServiceName, ByTopologyResourceAndServiceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d241a-138">-ServiceObject</span><span class="sxs-lookup"><span data-stu-id="d241a-138">-ServiceObject</span></span>
<span data-ttu-id="d241a-139">O objeto de serviço no qual a unidade de serviço deve ser criada.</span><span class="sxs-lookup"><span data-stu-id="d241a-139">The service object in which the service unit should be created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource
Parameter Sets: ByServiceObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d241a-140">-ServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="d241a-140">-ServiceResourceId</span></span>
<span data-ttu-id="d241a-141">O identificador de recurso de serviço no qual a unidade de serviço deve ser criada.</span><span class="sxs-lookup"><span data-stu-id="d241a-141">The service resource identifier in which the service unit should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: ByServiceResourceId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d241a-142">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="d241a-142">-ServiceTopologyName</span></span>
<span data-ttu-id="d241a-143">O nome da topologia de serviço da unidade de serviço faz parte.</span><span class="sxs-lookup"><span data-stu-id="d241a-143">The name of the service topology the service unit is part of.</span></span>

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

### <span data-ttu-id="d241a-144">-ServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="d241a-144">-ServiceTopologyObject</span></span>
<span data-ttu-id="d241a-145">O objeto de topologia de serviço no qual a unidade de serviço deve ser criada.</span><span class="sxs-lookup"><span data-stu-id="d241a-145">The service topology object in which the service unit should be created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource
Parameter Sets: ByTopologyObjectAndServiceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d241a-146">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="d241a-146">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="d241a-147">O identificador de recurso de topologia de serviço no qual a unidade de serviço deve ser criada.</span><span class="sxs-lookup"><span data-stu-id="d241a-147">The service topology resource identifier in which the service unit should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTopologyResourceAndServiceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d241a-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d241a-148">-Confirm</span></span>
<span data-ttu-id="d241a-149">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d241a-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d241a-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d241a-150">-WhatIf</span></span>
<span data-ttu-id="d241a-151">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d241a-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d241a-152">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d241a-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d241a-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d241a-153">CommonParameters</span></span>
<span data-ttu-id="d241a-154">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d241a-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d241a-155">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d241a-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d241a-156">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d241a-156">INPUTS</span></span>

### <span data-ttu-id="d241a-157">System.String</span><span class="sxs-lookup"><span data-stu-id="d241a-157">System.String</span></span>

### <span data-ttu-id="d241a-158">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="d241a-158">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="d241a-159">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d241a-159">OUTPUTS</span></span>

### <span data-ttu-id="d241a-160">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d241a-160">System.Boolean</span></span>

## <span data-ttu-id="d241a-161">NOTES</span><span class="sxs-lookup"><span data-stu-id="d241a-161">NOTES</span></span>

## <span data-ttu-id="d241a-162">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d241a-162">RELATED LINKS</span></span>
