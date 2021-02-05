---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/get-azurermdeploymentmanagerservice
schema: 2.0.0
ms.openlocfilehash: 4a91c2f8fdda1d2cda7c75f0cf7cfab165701f3d
ms.sourcegitcommit: e57be0da5162efeb0a01f396e2343dd137920063
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/05/2021
ms.locfileid: "99572098"
---
# <span data-ttu-id="630a6-101">Get-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="630a6-101">Get-AzureRmDeploymentManagerService</span></span>

## <span data-ttu-id="630a6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="630a6-102">SYNOPSIS</span></span>
<span data-ttu-id="630a6-103">Obtém um serviço em uma topologia de serviço.</span><span class="sxs-lookup"><span data-stu-id="630a6-103">Gets a service in a service topology.</span></span>

## <span data-ttu-id="630a6-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="630a6-104">SYNTAX</span></span>

### <span data-ttu-id="630a6-105">Interativo (Padrão)</span><span class="sxs-lookup"><span data-stu-id="630a6-105">Interactive (Default)</span></span>
```
Get-AzureRmDeploymentManagerService [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="630a6-106">ByServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="630a6-106">ByServiceTopologyObject</span></span>
```
Get-AzureRmDeploymentManagerService [-ResourceGroupName] <String> [-Name] <String>
 [-ServiceTopology] <PSServiceTopologyResource> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="630a6-107">ByServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="630a6-107">ByServiceTopologyResourceId</span></span>
```
Get-AzureRmDeploymentManagerService [-ResourceGroupName] <String> [-Name] <String>
 [-ServiceTopologyResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="630a6-108">Resourceid</span><span class="sxs-lookup"><span data-stu-id="630a6-108">ResourceId</span></span>
```
Get-AzureRmDeploymentManagerService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="630a6-109">Inputobject</span><span class="sxs-lookup"><span data-stu-id="630a6-109">InputObject</span></span>
```
Get-AzureRmDeploymentManagerService [-Service] <PSServiceResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="630a6-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="630a6-110">DESCRIPTION</span></span>
<span data-ttu-id="630a6-111">O cmdlet **Get-AzureRmDeploymentManagerService** obtém um serviço em uma topologia de serviço e retorna um objeto que representa esse serviço.</span><span class="sxs-lookup"><span data-stu-id="630a6-111">The **Get-AzureRmDeploymentManagerService** cmdlet gets a service under a service topology, and returns an object that represents that service.</span></span>
<span data-ttu-id="630a6-112">Especifique o serviço pelo nome, topologia do serviço em que ele está e o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="630a6-112">Specify the service by its name, service topology it is in and the resource group name.</span></span> <span data-ttu-id="630a6-113">Como alternativa, você pode fornecer o objeto Serviço ou o ResourceId.</span><span class="sxs-lookup"><span data-stu-id="630a6-113">Alternately, you can provide the Service object or the ResourceId.</span></span>

<span data-ttu-id="630a6-114">Você pode modificar esse objeto localmente e aplicar alterações ao serviço usando o cmdlet Set-AzureRmDeploymentManagerService usuário.</span><span class="sxs-lookup"><span data-stu-id="630a6-114">You can modify this object locally, and then apply changes to the service by using the Set-AzureRmDeploymentManagerService cmdlet.</span></span>

## <span data-ttu-id="630a6-115">Exemplos</span><span class="sxs-lookup"><span data-stu-id="630a6-115">EXAMPLES</span></span>

### <span data-ttu-id="630a6-116">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="630a6-116">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerService -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -Name ContosoService1
```

<span data-ttu-id="630a6-117">Esse comando obtém um serviço chamado ContosoService1 em uma topologia de serviço chamada ContosoServiceTopology no Grupo ContosoResource.</span><span class="sxs-lookup"><span data-stu-id="630a6-117">This command gets a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="630a6-118">Exemplo 2: Obter um serviço usando o identificador de recurso.</span><span class="sxs-lookup"><span data-stu-id="630a6-118">Example 2: Get a service using the resource identifier.</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerService -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1"
```

<span data-ttu-id="630a6-119">Esse comando obtém um serviço chamado ContosoService1 em uma topologia de serviço chamada ContosoServiceTopology no Grupo ContosoResource.</span><span class="sxs-lookup"><span data-stu-id="630a6-119">This command gets a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="630a6-120">Exemplo 3: Obter um serviço usando o objeto de serviço.</span><span class="sxs-lookup"><span data-stu-id="630a6-120">Example 3: Get a service using the service object.</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerService -Service $serviceObject
```

<span data-ttu-id="630a6-121">Esse comando obtém um serviço cujo nome, nome de topologia de serviço e Grupo de Recursos corresponderem às propriedades Nome, ServiceTopologyName e ResourceGroupName do $serviceObject, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="630a6-121">This command gets a service whose name, service topology name and ResourceGroup match the Name, ServiceTopologyName and ResourceGroupName properties of the $serviceObject, respectively.</span></span>

## <span data-ttu-id="630a6-122">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="630a6-122">PARAMETERS</span></span>

### <span data-ttu-id="630a6-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="630a6-123">-DefaultProfile</span></span>
<span data-ttu-id="630a6-124">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="630a6-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="630a6-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="630a6-125">-Name</span></span>
<span data-ttu-id="630a6-126">O nome do serviço.</span><span class="sxs-lookup"><span data-stu-id="630a6-126">The name of the service.</span></span>

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

### <span data-ttu-id="630a6-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="630a6-127">-ResourceGroupName</span></span>
<span data-ttu-id="630a6-128">O grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="630a6-128">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceTopologyObject, ByServiceTopologyResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="630a6-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="630a6-129">-ResourceId</span></span>
<span data-ttu-id="630a6-130">O identificador de recurso.</span><span class="sxs-lookup"><span data-stu-id="630a6-130">The resource identifier.</span></span>

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

### <span data-ttu-id="630a6-131">-Serviço</span><span class="sxs-lookup"><span data-stu-id="630a6-131">-Service</span></span>
<span data-ttu-id="630a6-132">Objeto de serviço.</span><span class="sxs-lookup"><span data-stu-id="630a6-132">Service object.</span></span>

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

### <span data-ttu-id="630a6-133">-ServiceTopology</span><span class="sxs-lookup"><span data-stu-id="630a6-133">-ServiceTopology</span></span>
<span data-ttu-id="630a6-134">O objeto de topologia de serviço no qual o serviço deve ser criado.</span><span class="sxs-lookup"><span data-stu-id="630a6-134">The service topology object in which the service should be created.</span></span>

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

### <span data-ttu-id="630a6-135">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="630a6-135">-ServiceTopologyName</span></span>
<span data-ttu-id="630a6-136">O nome da topologia do serviço.</span><span class="sxs-lookup"><span data-stu-id="630a6-136">The name of the service topology.</span></span>

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

### <span data-ttu-id="630a6-137">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="630a6-137">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="630a6-138">O identificador de recurso de topologia de serviço no qual o serviço deve ser criado.</span><span class="sxs-lookup"><span data-stu-id="630a6-138">The service topology resource identifier in which the service should be created.</span></span>

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

### <span data-ttu-id="630a6-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="630a6-139">CommonParameters</span></span>
<span data-ttu-id="630a6-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="630a6-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="630a6-141">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="630a6-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="630a6-142">Entradas</span><span class="sxs-lookup"><span data-stu-id="630a6-142">INPUTS</span></span>

### <span data-ttu-id="630a6-143">Nenhum</span><span class="sxs-lookup"><span data-stu-id="630a6-143">None</span></span>

## <span data-ttu-id="630a6-144">Saídas</span><span class="sxs-lookup"><span data-stu-id="630a6-144">OUTPUTS</span></span>

### <span data-ttu-id="630a6-145">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="630a6-145">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="630a6-146">Notas</span><span class="sxs-lookup"><span data-stu-id="630a6-146">NOTES</span></span>

## <span data-ttu-id="630a6-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="630a6-147">RELATED LINKS</span></span>

[<span data-ttu-id="630a6-148">New-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="630a6-148">New-AzureRmDeploymentManagerService</span></span>](./New-AzureRmDeploymentManagerService.md)

[<span data-ttu-id="630a6-149">Remove-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="630a6-149">Remove-AzureRmDeploymentManagerService</span></span>](./Remove-AzureRmDeploymentManagerService.md)

[<span data-ttu-id="630a6-150">Set-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="630a6-150">Set-AzureRmDeploymentManagerService</span></span>](./Set-AzureRmDeploymentManagerService.md)
