---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/get-azdeploymentmanagerserviceunit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerServiceUnit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerServiceUnit.md
ms.openlocfilehash: 2910afe209a83e07e65cc04b9ffa371fe4ed72d5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887180"
---
# <span data-ttu-id="f7d95-101">Get-AzDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="f7d95-101">Get-AzDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="f7d95-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7d95-102">SYNOPSIS</span></span>
<span data-ttu-id="f7d95-103">Obtém a unidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="f7d95-103">Gets the service unit.</span></span>

## <span data-ttu-id="f7d95-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="f7d95-104">SYNTAX</span></span>

### <span data-ttu-id="f7d95-105">Interativo (Padrão)</span><span class="sxs-lookup"><span data-stu-id="f7d95-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-ServiceName] <String> [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f7d95-106">ByServiceObject</span><span class="sxs-lookup"><span data-stu-id="f7d95-106">ByServiceObject</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [[-Name] <String>]
 [-ServiceObject] <PSServiceResource> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f7d95-107">ByServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="f7d95-107">ByServiceResourceId</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [[-Name] <String>]
 [-ServiceResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f7d95-108">ByTopologyObjectAndServiceName</span><span class="sxs-lookup"><span data-stu-id="f7d95-108">ByTopologyObjectAndServiceName</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [[-Name] <String>]
 [-ServiceTopologyObject] <PSServiceTopologyResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f7d95-109">ByTopologyResourceAndServiceName</span><span class="sxs-lookup"><span data-stu-id="f7d95-109">ByTopologyResourceAndServiceName</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [[-Name] <String>]
 [-ServiceTopologyResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f7d95-110">ResourceId</span><span class="sxs-lookup"><span data-stu-id="f7d95-110">ResourceId</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f7d95-111">InputObject</span><span class="sxs-lookup"><span data-stu-id="f7d95-111">InputObject</span></span>
```
Get-AzDeploymentManagerServiceUnit [-InputObject] <PSServiceUnitResource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f7d95-112">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="f7d95-112">DESCRIPTION</span></span>
<span data-ttu-id="f7d95-113">O cmdlet **Get-AzDeploymentManagerServiceUnit** obtém uma unidade de serviço em um serviço.</span><span class="sxs-lookup"><span data-stu-id="f7d95-113">The **Get-AzDeploymentManagerServiceUnit** cmdlet gets a service unit in a service.</span></span>

<span data-ttu-id="f7d95-114">Especifique a unidade de serviço pelo nome, o serviço no qual foi definida, o nome da topologia do serviço e o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f7d95-114">Specify the service unit by its name, the service under which it was defined, the service topology name and the resource group name.</span></span> <span data-ttu-id="f7d95-115">Como alternativa, você pode fornecer o objeto ServiceUnit ou ResourceId.</span><span class="sxs-lookup"><span data-stu-id="f7d95-115">Alternately, you can provide the ServiceUnit object or the ResourceId.</span></span>

<span data-ttu-id="f7d95-116">Você pode modificar esse objeto localmente e aplicar alterações à unidade de serviço usando o cmdlet Set-AzDeploymentManagerServiceUnit.</span><span class="sxs-lookup"><span data-stu-id="f7d95-116">You can modify this object locally, and then apply changes to the service unit by using the Set-AzDeploymentManagerServiceUnit cmdlet.</span></span>

## <span data-ttu-id="f7d95-117">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f7d95-117">EXAMPLES</span></span>

### <span data-ttu-id="f7d95-118">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f7d95-118">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -ServiceName ContosoService1  -Name ContosoService1Storage
```

<span data-ttu-id="f7d95-119">Este comando obtém uma unidade de serviço chamada ContosoService1Storage em um serviço ContosoService1 em uma topologia de serviço chamada ContosoServiceTopology no ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="f7d95-119">This command gets a service unit named ContosoService1Storage under a service ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="f7d95-120">Exemplo 2: Obter uma unidade de serviço usando o identificador de recurso.</span><span class="sxs-lookup"><span data-stu-id="f7d95-120">Example 2: Get a service unit using the resource identifier.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceUnit -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1/serviceUnits/ContosoService1Storage"
```

<span data-ttu-id="f7d95-121">Este comando obtém uma unidade de serviço chamada ContosoService1Storage em um serviço ContosoService1 em uma topologia de serviço chamada ContosoServiceTopology no ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="f7d95-121">This command gets a service unit named ContosoService1Storage under a service ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="f7d95-122">Exemplo 3: Obter uma unidade de serviço usando o objeto da unidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="f7d95-122">Example 3: Get a service unit using the service unit object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceUnit -InputObject $serviceUnitObject
```

<span data-ttu-id="f7d95-123">Este comando obtém uma unidade de serviço cujo nome, nome do serviço, nome da topologia de serviço e ResourceGroup corresponder às propriedades Name, ServiceName, ServiceTopologyName e ResourceGroupName do $serviceUnitObject, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="f7d95-123">This command gets a service unit whose name, service name, service topology name and ResourceGroup match the Name, ServiceName, ServiceTopologyName and ResourceGroupName properties of the $serviceUnitObject, respectively.</span></span>

## <span data-ttu-id="f7d95-124">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="f7d95-124">PARAMETERS</span></span>

### <span data-ttu-id="f7d95-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7d95-125">-DefaultProfile</span></span>
<span data-ttu-id="f7d95-126">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f7d95-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7d95-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f7d95-127">-InputObject</span></span>
<span data-ttu-id="f7d95-128">Objeto de recurso da unidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="f7d95-128">Service unit resource object.</span></span>

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

### <span data-ttu-id="f7d95-129">-Name</span><span class="sxs-lookup"><span data-stu-id="f7d95-129">-Name</span></span>
<span data-ttu-id="f7d95-130">O nome da unidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="f7d95-130">The name of the service unit.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceObject, ByServiceResourceId, ByTopologyObjectAndServiceName, ByTopologyResourceAndServiceName
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7d95-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7d95-131">-ResourceGroupName</span></span>
<span data-ttu-id="f7d95-132">O grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f7d95-132">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceObject, ByServiceResourceId, ByTopologyObjectAndServiceName, ByTopologyResourceAndServiceName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7d95-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f7d95-133">-ResourceId</span></span>
<span data-ttu-id="f7d95-134">O identificador de recurso.</span><span class="sxs-lookup"><span data-stu-id="f7d95-134">The resource identifier.</span></span>

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

### <span data-ttu-id="f7d95-135">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="f7d95-135">-ServiceName</span></span>
<span data-ttu-id="f7d95-136">O nome do serviço do que a unidade de serviço faz parte.</span><span class="sxs-lookup"><span data-stu-id="f7d95-136">The name of the service the service unit is part of.</span></span>

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

### <span data-ttu-id="f7d95-137">-ServiceObject</span><span class="sxs-lookup"><span data-stu-id="f7d95-137">-ServiceObject</span></span>
<span data-ttu-id="f7d95-138">O objeto de serviço no qual a unidade de serviço deve ser criada.</span><span class="sxs-lookup"><span data-stu-id="f7d95-138">The service object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="f7d95-139">-ServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="f7d95-139">-ServiceResourceId</span></span>
<span data-ttu-id="f7d95-140">O identificador de recurso de serviço no qual a unidade de serviço deve ser criada.</span><span class="sxs-lookup"><span data-stu-id="f7d95-140">The service resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="f7d95-141">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="f7d95-141">-ServiceTopologyName</span></span>
<span data-ttu-id="f7d95-142">O nome da topologia de serviço da unidade de serviço faz parte.</span><span class="sxs-lookup"><span data-stu-id="f7d95-142">The name of the service topology the service unit is part of.</span></span>

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

### <span data-ttu-id="f7d95-143">-ServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="f7d95-143">-ServiceTopologyObject</span></span>
<span data-ttu-id="f7d95-144">O objeto de topologia de serviço no qual a unidade de serviço deve ser criada.</span><span class="sxs-lookup"><span data-stu-id="f7d95-144">The service topology object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="f7d95-145">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="f7d95-145">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="f7d95-146">O identificador de recurso de topologia de serviço no qual a unidade de serviço deve ser criada.</span><span class="sxs-lookup"><span data-stu-id="f7d95-146">The service topology resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="f7d95-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7d95-147">CommonParameters</span></span>
<span data-ttu-id="f7d95-148">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7d95-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7d95-149">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f7d95-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7d95-150">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f7d95-150">INPUTS</span></span>

### <span data-ttu-id="f7d95-151">System.String</span><span class="sxs-lookup"><span data-stu-id="f7d95-151">System.String</span></span>

### <span data-ttu-id="f7d95-152">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="f7d95-152">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="f7d95-153">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="f7d95-153">OUTPUTS</span></span>

### <span data-ttu-id="f7d95-154">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="f7d95-154">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="f7d95-155">NOTES</span><span class="sxs-lookup"><span data-stu-id="f7d95-155">NOTES</span></span>

## <span data-ttu-id="f7d95-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f7d95-156">RELATED LINKS</span></span>
