---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerService.md
ms.openlocfilehash: 3dda11ec4fddde67a3ae4300f884290831ac28ae
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93601007"
---
# <span data-ttu-id="08cfb-101">Get-AzDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="08cfb-101">Get-AzDeploymentManagerService</span></span>

## <span data-ttu-id="08cfb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="08cfb-102">SYNOPSIS</span></span>
<span data-ttu-id="08cfb-103">Obtém o serviço.</span><span class="sxs-lookup"><span data-stu-id="08cfb-103">Gets the service.</span></span>

## <span data-ttu-id="08cfb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="08cfb-104">SYNTAX</span></span>

### <span data-ttu-id="08cfb-105">Interativo (padrão)</span><span class="sxs-lookup"><span data-stu-id="08cfb-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerService [-ResourceGroupName] <String> [-ServiceTopologyName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="08cfb-106">ByServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="08cfb-106">ByServiceTopologyObject</span></span>
```
Get-AzDeploymentManagerService [-ResourceGroupName] <String> [-Name] <String>
 [-ServiceTopologyObject] <PSServiceTopologyResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="08cfb-107">ByServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="08cfb-107">ByServiceTopologyResourceId</span></span>
```
Get-AzDeploymentManagerService [-ResourceGroupName] <String> [-Name] <String>
 [-ServiceTopologyResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="08cfb-108">Identificação</span><span class="sxs-lookup"><span data-stu-id="08cfb-108">ResourceId</span></span>
```
Get-AzDeploymentManagerService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="08cfb-109">InputObject</span><span class="sxs-lookup"><span data-stu-id="08cfb-109">InputObject</span></span>
```
Get-AzDeploymentManagerService [-InputObject] <PSServiceResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="08cfb-110">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="08cfb-110">DESCRIPTION</span></span>
<span data-ttu-id="08cfb-111">O cmdlet **Get-AzDeploymentManagerService** Obtém um serviço em uma topologia de serviço e retorna um objeto que representa esse serviço.</span><span class="sxs-lookup"><span data-stu-id="08cfb-111">The **Get-AzDeploymentManagerService** cmdlet gets a service under a service topology, and returns an object that represents that service.</span></span>
<span data-ttu-id="08cfb-112">Especifique o serviço pelo nome, topologia de serviço em que ele se encontra e o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="08cfb-112">Specify the service by its name, service topology it is in and the resource group name.</span></span> <span data-ttu-id="08cfb-113">Como alternativa, você pode fornecer o objeto de serviço ou a ResourceId.</span><span class="sxs-lookup"><span data-stu-id="08cfb-113">Alternately, you can provide the Service object or the ResourceId.</span></span>

<span data-ttu-id="08cfb-114">Você pode modificar esse objeto localmente e, em seguida, aplicar as alterações ao serviço usando o cmdlet Set-AzDeploymentManagerService.</span><span class="sxs-lookup"><span data-stu-id="08cfb-114">You can modify this object locally, and then apply changes to the service by using the Set-AzDeploymentManagerService cmdlet.</span></span>

## <span data-ttu-id="08cfb-115">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="08cfb-115">EXAMPLES</span></span>

### <span data-ttu-id="08cfb-116">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="08cfb-116">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerService -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -Name ContosoService1
```

<span data-ttu-id="08cfb-117">Esse comando obtém um serviço denominado ContosoService1 em uma topologia de serviço chamada ContosoServiceTopology no ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="08cfb-117">This command gets a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="08cfb-118">Exemplo 2: obter um serviço usando o identificador de recursos.</span><span class="sxs-lookup"><span data-stu-id="08cfb-118">Example 2: Get a service using the resource identifier.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerService -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1"
```

<span data-ttu-id="08cfb-119">Esse comando obtém um serviço denominado ContosoService1 em uma topologia de serviço chamada ContosoServiceTopology no ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="08cfb-119">This command gets a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="08cfb-120">Exemplo 3: obter um serviço usando o objeto de serviço.</span><span class="sxs-lookup"><span data-stu-id="08cfb-120">Example 3: Get a service using the service object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerService -InputObject $serviceObject
```

<span data-ttu-id="08cfb-121">Esse comando obtém um serviço cujo nome, o nome da topologia de serviço e o nome do contato correspondem às propriedades Name, imtopologyname e ResourceGroupName da $serviceObject, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="08cfb-121">This command gets a service whose name, service topology name and ResourceGroup match the Name, ServiceTopologyName and ResourceGroupName properties of the $serviceObject, respectively.</span></span>
 

## <span data-ttu-id="08cfb-122">OS</span><span class="sxs-lookup"><span data-stu-id="08cfb-122">PARAMETERS</span></span>

### <span data-ttu-id="08cfb-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08cfb-123">-DefaultProfile</span></span>
<span data-ttu-id="08cfb-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="08cfb-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="08cfb-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="08cfb-125">-InputObject</span></span>
<span data-ttu-id="08cfb-126">Objeto de serviço.</span><span class="sxs-lookup"><span data-stu-id="08cfb-126">Service object.</span></span>

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

### <span data-ttu-id="08cfb-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="08cfb-127">-Name</span></span>
<span data-ttu-id="08cfb-128">O nome do serviço.</span><span class="sxs-lookup"><span data-stu-id="08cfb-128">The name of the service.</span></span>

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

### <span data-ttu-id="08cfb-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08cfb-129">-ResourceGroupName</span></span>
<span data-ttu-id="08cfb-130">O grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="08cfb-130">The resource group.</span></span>

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

### <span data-ttu-id="08cfb-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="08cfb-131">-ResourceId</span></span>
<span data-ttu-id="08cfb-132">O identificador do recurso.</span><span class="sxs-lookup"><span data-stu-id="08cfb-132">The resource identifier.</span></span>

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

### <span data-ttu-id="08cfb-133">-Imtopologyname</span><span class="sxs-lookup"><span data-stu-id="08cfb-133">-ServiceTopologyName</span></span>
<span data-ttu-id="08cfb-134">O nome da topologia de serviço.</span><span class="sxs-lookup"><span data-stu-id="08cfb-134">The name of the service topology.</span></span>

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

### <span data-ttu-id="08cfb-135">-Imtopologyobject</span><span class="sxs-lookup"><span data-stu-id="08cfb-135">-ServiceTopologyObject</span></span>
<span data-ttu-id="08cfb-136">O objeto de topologia de serviço no qual o serviço deve ser criado.</span><span class="sxs-lookup"><span data-stu-id="08cfb-136">The service topology object in which the service should be created.</span></span>

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

### <span data-ttu-id="08cfb-137">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="08cfb-137">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="08cfb-138">O identificador de recursos de topologia de serviço no qual o serviço deve ser criado.</span><span class="sxs-lookup"><span data-stu-id="08cfb-138">The service topology resource identifier in which the service should be created.</span></span>

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

### <span data-ttu-id="08cfb-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08cfb-139">CommonParameters</span></span>
<span data-ttu-id="08cfb-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08cfb-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08cfb-141">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08cfb-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08cfb-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="08cfb-142">INPUTS</span></span>

### <span data-ttu-id="08cfb-143">System. String</span><span class="sxs-lookup"><span data-stu-id="08cfb-143">System.String</span></span>

### <span data-ttu-id="08cfb-144">Microsoft. Azure. Commands. DeploymentManager. Models. PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="08cfb-144">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="08cfb-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="08cfb-145">OUTPUTS</span></span>

### <span data-ttu-id="08cfb-146">Microsoft. Azure. Commands. DeploymentManager. Models. PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="08cfb-146">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="08cfb-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="08cfb-147">NOTES</span></span>

## <span data-ttu-id="08cfb-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="08cfb-148">RELATED LINKS</span></span>
