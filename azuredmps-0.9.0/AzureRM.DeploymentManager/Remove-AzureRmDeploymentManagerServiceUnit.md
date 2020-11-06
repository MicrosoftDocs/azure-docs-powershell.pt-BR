---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/remove-azurermdeploymentmanagerserviceunit
schema: 2.0.0
ms.openlocfilehash: 993b250b0c49efc448c0198c4e9a3aea29f77714
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93426069"
---
# <span data-ttu-id="2efda-101">Remove-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="2efda-101">Remove-AzureRmDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="2efda-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2efda-102">SYNOPSIS</span></span>
<span data-ttu-id="2efda-103">Exclui a unidade de serviço de um serviço em uma topologia de serviço.</span><span class="sxs-lookup"><span data-stu-id="2efda-103">Deletes the service unit of a service in a service topology.</span></span>

## <span data-ttu-id="2efda-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2efda-104">SYNTAX</span></span>

### <span data-ttu-id="2efda-105">Interativo (padrão)</span><span class="sxs-lookup"><span data-stu-id="2efda-105">Interactive (Default)</span></span>
```
Remove-AzureRmDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-ServiceName] <String> [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2efda-106">ByTopologyObjectAndServiceName</span><span class="sxs-lookup"><span data-stu-id="2efda-106">ByTopologyObjectAndServiceName</span></span>
```
Remove-AzureRmDeploymentManagerServiceUnit [-ServiceName] <String> [-Name] <String>
 [-ServiceTopology] <PSServiceTopologyResource> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2efda-107">ByTopologyResourceAndServiceName</span><span class="sxs-lookup"><span data-stu-id="2efda-107">ByTopologyResourceAndServiceName</span></span>
```
Remove-AzureRmDeploymentManagerServiceUnit [-ServiceName] <String> [-Name] <String>
 [-ServiceTopologyResourceId] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2efda-108">ByServiceObject</span><span class="sxs-lookup"><span data-stu-id="2efda-108">ByServiceObject</span></span>
```
Remove-AzureRmDeploymentManagerServiceUnit [-Name] <String> [-Service] <PSServiceResource> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2efda-109">ByServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="2efda-109">ByServiceResourceId</span></span>
```
Remove-AzureRmDeploymentManagerServiceUnit [-Name] <String> [-ServiceResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2efda-110">Identificação</span><span class="sxs-lookup"><span data-stu-id="2efda-110">ResourceId</span></span>
```
Remove-AzureRmDeploymentManagerServiceUnit [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2efda-111">InputObject</span><span class="sxs-lookup"><span data-stu-id="2efda-111">InputObject</span></span>
```
Remove-AzureRmDeploymentManagerServiceUnit [-ServiceUnit] <PSServiceUnitResource> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2efda-112">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2efda-112">DESCRIPTION</span></span>
<span data-ttu-id="2efda-113">O cmdlet **Remove-AzureRmDeploymentManagerServiceUnit** exclui uma unidade de serviço em um serviço.</span><span class="sxs-lookup"><span data-stu-id="2efda-113">The **Remove-AzureRmDeploymentManagerServiceUnit** cmdlet deletes a service unit in a service.</span></span>

<span data-ttu-id="2efda-114">Especifique a unidade de serviço por nome, o serviço sob o qual ele foi definido, o nome da topologia do serviço e o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2efda-114">Specify the service unit by its name, the service under which it was defined, the service topology name and the resource group name.</span></span> <span data-ttu-id="2efda-115">Como alternativa, você pode fornecer o objeto onunit ou o resourceId.</span><span class="sxs-lookup"><span data-stu-id="2efda-115">Alternately, you can provide the ServiceUnit object or the ResourceId.</span></span>

## <span data-ttu-id="2efda-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2efda-116">EXAMPLES</span></span>

### <span data-ttu-id="2efda-117">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2efda-117">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -ServiceName ContosoService1  -Name ContosoService1Storage
```

<span data-ttu-id="2efda-118">Esse comando exclui uma unidade de serviço chamada ContosoService1Storage em um ContosoService1 de serviço em uma topologia de serviço chamada ContosoServiceTopology no ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="2efda-118">This command deletes a service unit named ContosoService1Storage under a service ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="2efda-119">Exemplo 2: excluir uma unidade de serviço usando o identificador de recursos.</span><span class="sxs-lookup"><span data-stu-id="2efda-119">Example 2: Delete a service unit using the resource identifier.</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerServiceUnit -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1/serviceUnits/ContosoService1Storage"
```

<span data-ttu-id="2efda-120">Esse comando obtém uma unidade de serviço chamada ContosoService1Storage em um ContosoService1 de serviço em uma topologia de serviço chamada ContosoServiceTopology no ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="2efda-120">This command gets a service unit named ContosoService1Storage under a service ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="2efda-121">Exemplo 3: excluir uma unidade de serviço usando o objeto de unidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="2efda-121">Example 3: Delete a service unit using the service unit object.</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerServiceUnit -ServiceUnit $serviceUnitObject
```

<span data-ttu-id="2efda-122">Esse comando exclui uma unidade de serviço cujo nome, nome do serviço, nome da topologia do serviço e o nome da sua subfonte corresponde às propriedades Name, ServiceName, Service Topologyname e ResourceGroupName da $serviceUnitObject, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="2efda-122">This command deletes a service unit whose name, service name, service topology name and ResourceGroup match the Name, ServiceName, ServiceTopologyName and ResourceGroupName properties of the $serviceUnitObject, respectively.</span></span>

## <span data-ttu-id="2efda-123">OS</span><span class="sxs-lookup"><span data-stu-id="2efda-123">PARAMETERS</span></span>

### <span data-ttu-id="2efda-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2efda-124">-DefaultProfile</span></span>
<span data-ttu-id="2efda-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2efda-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2efda-126">-Force</span><span class="sxs-lookup"><span data-stu-id="2efda-126">-Force</span></span>
<span data-ttu-id="2efda-127">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="2efda-127">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="2efda-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="2efda-128">-Name</span></span>
<span data-ttu-id="2efda-129">O nome da unidade de serviço a ser excluída.</span><span class="sxs-lookup"><span data-stu-id="2efda-129">The name of the service unit to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByTopologyObjectAndServiceName, ByTopologyResourceAndServiceName, ByServiceObject, ByServiceResourceId
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2efda-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2efda-130">-PassThru</span></span>
<span data-ttu-id="2efda-131">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="2efda-131">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="2efda-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2efda-132">-ResourceGroupName</span></span>
<span data-ttu-id="2efda-133">O grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2efda-133">The resource group.</span></span>

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

### <span data-ttu-id="2efda-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2efda-134">-ResourceId</span></span>
<span data-ttu-id="2efda-135">O identificador do recurso.</span><span class="sxs-lookup"><span data-stu-id="2efda-135">The resource identifier.</span></span>

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

### <span data-ttu-id="2efda-136">-Serviço</span><span class="sxs-lookup"><span data-stu-id="2efda-136">-Service</span></span>
<span data-ttu-id="2efda-137">O objeto de serviço no qual a unidade de serviço deve ser criada.</span><span class="sxs-lookup"><span data-stu-id="2efda-137">The service object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="2efda-138">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="2efda-138">-ServiceName</span></span>
<span data-ttu-id="2efda-139">O nome do serviço ao qual a unidade de serviço pertence.</span><span class="sxs-lookup"><span data-stu-id="2efda-139">The name of the service the service unit belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByTopologyObjectAndServiceName, ByTopologyResourceAndServiceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2efda-140">-Objectresourceid</span><span class="sxs-lookup"><span data-stu-id="2efda-140">-ServiceResourceId</span></span>
<span data-ttu-id="2efda-141">O identificador do recurso de serviço no qual a unidade de serviço deve ser criada.</span><span class="sxs-lookup"><span data-stu-id="2efda-141">The service resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="2efda-142">-Outtopology</span><span class="sxs-lookup"><span data-stu-id="2efda-142">-ServiceTopology</span></span>
<span data-ttu-id="2efda-143">O objeto de topologia de serviço no qual a unidade de serviço deve ser criada.</span><span class="sxs-lookup"><span data-stu-id="2efda-143">The service topology object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="2efda-144">-Imtopologyname</span><span class="sxs-lookup"><span data-stu-id="2efda-144">-ServiceTopologyName</span></span>
<span data-ttu-id="2efda-145">O nome da topologia do serviço à qual a unidade de serviço pertence.</span><span class="sxs-lookup"><span data-stu-id="2efda-145">The name of the service topology the service unit belongs to.</span></span>

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

### <span data-ttu-id="2efda-146">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="2efda-146">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="2efda-147">O identificador de recursos de topologia de serviço no qual a unidade de serviço deve ser criada.</span><span class="sxs-lookup"><span data-stu-id="2efda-147">The service topology resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="2efda-148">-Enunidade</span><span class="sxs-lookup"><span data-stu-id="2efda-148">-ServiceUnit</span></span>
<span data-ttu-id="2efda-149">O recurso a ser removido.</span><span class="sxs-lookup"><span data-stu-id="2efda-149">The resource to be removed.</span></span>

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

### <span data-ttu-id="2efda-150">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2efda-150">-Confirm</span></span>
<span data-ttu-id="2efda-151">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2efda-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2efda-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2efda-152">-WhatIf</span></span>
<span data-ttu-id="2efda-153">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2efda-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2efda-154">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2efda-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2efda-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2efda-155">CommonParameters</span></span>
<span data-ttu-id="2efda-156">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2efda-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2efda-157">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2efda-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2efda-158">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2efda-158">INPUTS</span></span>

### <span data-ttu-id="2efda-159">Microsoft. Azure. Commands. DeploymentManager. Models. PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="2efda-159">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="2efda-160">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2efda-160">OUTPUTS</span></span>

### <span data-ttu-id="2efda-161">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2efda-161">System.Boolean</span></span>

## <span data-ttu-id="2efda-162">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2efda-162">NOTES</span></span>

## <span data-ttu-id="2efda-163">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2efda-163">RELATED LINKS</span></span>

[<span data-ttu-id="2efda-164">New-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="2efda-164">New-AzureRmDeploymentManagerServiceUnit</span></span>](./New-AzureRmDeploymentManagerServiceUnit.md)

[<span data-ttu-id="2efda-165">Get-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="2efda-165">Get-AzureRmDeploymentManagerServiceUnit</span></span>](./Get-AzureRmDeploymentManagerServiceUnit.md)

[<span data-ttu-id="2efda-166">Set-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="2efda-166">Set-AzureRmDeploymentManagerServiceUnit</span></span>](./Set-AzureRmDeploymentManagerServiceUnit.md)