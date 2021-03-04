---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/get-azdeploymentmanagerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerService.md
ms.openlocfilehash: 12a2e8b27697436a38753c054f178878b9ed3bd1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888978"
---
# <span data-ttu-id="2c385-101">Get-AzDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="2c385-101">Get-AzDeploymentManagerService</span></span>

## <span data-ttu-id="2c385-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2c385-102">SYNOPSIS</span></span>
<span data-ttu-id="2c385-103">Obtém o serviço.</span><span class="sxs-lookup"><span data-stu-id="2c385-103">Gets the service.</span></span>

## <span data-ttu-id="2c385-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="2c385-104">SYNTAX</span></span>

### <span data-ttu-id="2c385-105">Interativo (Padrão)</span><span class="sxs-lookup"><span data-stu-id="2c385-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerService [-ResourceGroupName] <String> [-ServiceTopologyName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2c385-106">ByServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="2c385-106">ByServiceTopologyObject</span></span>
```
Get-AzDeploymentManagerService [-ResourceGroupName] <String> [[-Name] <String>]
 [-ServiceTopologyObject] <PSServiceTopologyResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2c385-107">ByServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="2c385-107">ByServiceTopologyResourceId</span></span>
```
Get-AzDeploymentManagerService [-ResourceGroupName] <String> [[-Name] <String>]
 [-ServiceTopologyResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2c385-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="2c385-108">ResourceId</span></span>
```
Get-AzDeploymentManagerService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2c385-109">InputObject</span><span class="sxs-lookup"><span data-stu-id="2c385-109">InputObject</span></span>
```
Get-AzDeploymentManagerService [-InputObject] <PSServiceResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2c385-110">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="2c385-110">DESCRIPTION</span></span>
<span data-ttu-id="2c385-111">O cmdlet **Get-AzDeploymentManagerService** obtém um serviço em uma topologia de serviço e retorna um objeto que representa esse serviço.</span><span class="sxs-lookup"><span data-stu-id="2c385-111">The **Get-AzDeploymentManagerService** cmdlet gets a service under a service topology, and returns an object that represents that service.</span></span>
<span data-ttu-id="2c385-112">Especifique o serviço pelo nome, topologia de serviço em que ele está e o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2c385-112">Specify the service by its name, service topology it is in and the resource group name.</span></span> <span data-ttu-id="2c385-113">Como alternativa, você pode fornecer o objeto Service ou ResourceId.</span><span class="sxs-lookup"><span data-stu-id="2c385-113">Alternately, you can provide the Service object or the ResourceId.</span></span>

<span data-ttu-id="2c385-114">Você pode modificar esse objeto localmente e aplicar alterações ao serviço usando o cmdlet Set-AzDeploymentManagerService.</span><span class="sxs-lookup"><span data-stu-id="2c385-114">You can modify this object locally, and then apply changes to the service by using the Set-AzDeploymentManagerService cmdlet.</span></span>

## <span data-ttu-id="2c385-115">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2c385-115">EXAMPLES</span></span>

### <span data-ttu-id="2c385-116">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2c385-116">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerService -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -Name ContosoService1
```

<span data-ttu-id="2c385-117">Este comando obtém um serviço chamado ContosoService1 em uma topologia de serviço chamada ContosoServiceTopology no ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="2c385-117">This command gets a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="2c385-118">Exemplo 2: Obter um serviço usando o identificador de recurso.</span><span class="sxs-lookup"><span data-stu-id="2c385-118">Example 2: Get a service using the resource identifier.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerService -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1"
```

<span data-ttu-id="2c385-119">Este comando obtém um serviço chamado ContosoService1 em uma topologia de serviço chamada ContosoServiceTopology no ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="2c385-119">This command gets a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="2c385-120">Exemplo 3: Obter um serviço usando o objeto de serviço.</span><span class="sxs-lookup"><span data-stu-id="2c385-120">Example 3: Get a service using the service object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerService -InputObject $serviceObject
```

<span data-ttu-id="2c385-121">Este comando obtém um serviço cujo nome, nome da topologia de serviço e ResourceGroup corresponderem às propriedades Name, ServiceTopologyName e ResourceGroupName do $serviceObject, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="2c385-121">This command gets a service whose name, service topology name and ResourceGroup match the Name, ServiceTopologyName and ResourceGroupName properties of the $serviceObject, respectively.</span></span>
 

## <span data-ttu-id="2c385-122">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="2c385-122">PARAMETERS</span></span>

### <span data-ttu-id="2c385-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c385-123">-DefaultProfile</span></span>
<span data-ttu-id="2c385-124">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2c385-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c385-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2c385-125">-InputObject</span></span>
<span data-ttu-id="2c385-126">Objeto Service.</span><span class="sxs-lookup"><span data-stu-id="2c385-126">Service object.</span></span>

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

### <span data-ttu-id="2c385-127">-Name</span><span class="sxs-lookup"><span data-stu-id="2c385-127">-Name</span></span>
<span data-ttu-id="2c385-128">O nome do serviço.</span><span class="sxs-lookup"><span data-stu-id="2c385-128">The name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceTopologyObject, ByServiceTopologyResourceId
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c385-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c385-129">-ResourceGroupName</span></span>
<span data-ttu-id="2c385-130">O grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2c385-130">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceTopologyObject, ByServiceTopologyResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c385-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2c385-131">-ResourceId</span></span>
<span data-ttu-id="2c385-132">O identificador de recurso.</span><span class="sxs-lookup"><span data-stu-id="2c385-132">The resource identifier.</span></span>

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

### <span data-ttu-id="2c385-133">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="2c385-133">-ServiceTopologyName</span></span>
<span data-ttu-id="2c385-134">O nome da topologia de serviço.</span><span class="sxs-lookup"><span data-stu-id="2c385-134">The name of the service topology.</span></span>

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

### <span data-ttu-id="2c385-135">-ServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="2c385-135">-ServiceTopologyObject</span></span>
<span data-ttu-id="2c385-136">O objeto de topologia de serviço no qual o serviço deve ser criado.</span><span class="sxs-lookup"><span data-stu-id="2c385-136">The service topology object in which the service should be created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource
Parameter Sets: ByServiceTopologyObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c385-137">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="2c385-137">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="2c385-138">O identificador de recurso de topologia de serviço no qual o serviço deve ser criado.</span><span class="sxs-lookup"><span data-stu-id="2c385-138">The service topology resource identifier in which the service should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: ByServiceTopologyResourceId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c385-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c385-139">CommonParameters</span></span>
<span data-ttu-id="2c385-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c385-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c385-141">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2c385-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c385-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2c385-142">INPUTS</span></span>

### <span data-ttu-id="2c385-143">System.String</span><span class="sxs-lookup"><span data-stu-id="2c385-143">System.String</span></span>

### <span data-ttu-id="2c385-144">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="2c385-144">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="2c385-145">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="2c385-145">OUTPUTS</span></span>

### <span data-ttu-id="2c385-146">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="2c385-146">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="2c385-147">NOTES</span><span class="sxs-lookup"><span data-stu-id="2c385-147">NOTES</span></span>

## <span data-ttu-id="2c385-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2c385-148">RELATED LINKS</span></span>
