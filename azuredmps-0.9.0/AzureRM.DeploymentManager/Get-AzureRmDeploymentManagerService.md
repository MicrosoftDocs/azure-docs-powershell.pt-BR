---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/get-azurermdeploymentmanagerservice
schema: 2.0.0
content_git_url: ''
ms.openlocfilehash: 655cfeeae35d1b48bbfe2149fd4262dffe72ae09
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93426188"
---
# <span data-ttu-id="39271-101">Get-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="39271-101">Get-AzureRmDeploymentManagerService</span></span>

## <span data-ttu-id="39271-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="39271-102">SYNOPSIS</span></span>
<span data-ttu-id="39271-103">Obtém um serviço em uma topologia de serviço.</span><span class="sxs-lookup"><span data-stu-id="39271-103">Gets a service in a service topology.</span></span>

## <span data-ttu-id="39271-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="39271-104">SYNTAX</span></span>

### <span data-ttu-id="39271-105">Interativo (padrão)</span><span class="sxs-lookup"><span data-stu-id="39271-105">Interactive (Default)</span></span>
```
Get-AzureRmDeploymentManagerService [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="39271-106">ByServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="39271-106">ByServiceTopologyObject</span></span>
```
Get-AzureRmDeploymentManagerService [-ResourceGroupName] <String> [-Name] <String>
 [-ServiceTopology] <PSServiceTopologyResource> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="39271-107">ByServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="39271-107">ByServiceTopologyResourceId</span></span>
```
Get-AzureRmDeploymentManagerService [-ResourceGroupName] <String> [-Name] <String>
 [-ServiceTopologyResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="39271-108">Identificação</span><span class="sxs-lookup"><span data-stu-id="39271-108">ResourceId</span></span>
```
Get-AzureRmDeploymentManagerService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="39271-109">InputObject</span><span class="sxs-lookup"><span data-stu-id="39271-109">InputObject</span></span>
```
Get-AzureRmDeploymentManagerService [-Service] <PSServiceResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="39271-110">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="39271-110">DESCRIPTION</span></span>
<span data-ttu-id="39271-111">O cmdlet **Get-AzureRmDeploymentManagerService** Obtém um serviço em uma topologia de serviço e retorna um objeto que representa esse serviço.</span><span class="sxs-lookup"><span data-stu-id="39271-111">The **Get-AzureRmDeploymentManagerService** cmdlet gets a service under a service topology, and returns an object that represents that service.</span></span>
<span data-ttu-id="39271-112">Especifique o serviço pelo nome, topologia de serviço em que ele se encontra e o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="39271-112">Specify the service by its name, service topology it is in and the resource group name.</span></span> <span data-ttu-id="39271-113">Como alternativa, você pode fornecer o objeto de serviço ou a ResourceId.</span><span class="sxs-lookup"><span data-stu-id="39271-113">Alternately, you can provide the Service object or the ResourceId.</span></span>

<span data-ttu-id="39271-114">Você pode modificar esse objeto localmente e, em seguida, aplicar as alterações ao serviço usando o cmdlet Set-AzureRmDeploymentManagerService.</span><span class="sxs-lookup"><span data-stu-id="39271-114">You can modify this object locally, and then apply changes to the service by using the Set-AzureRmDeploymentManagerService cmdlet.</span></span>

## <span data-ttu-id="39271-115">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="39271-115">EXAMPLES</span></span>

### <span data-ttu-id="39271-116">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="39271-116">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerService -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -Name ContosoService1
```

<span data-ttu-id="39271-117">Esse comando obtém um serviço denominado ContosoService1 em uma topologia de serviço chamada ContosoServiceTopology no ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="39271-117">This command gets a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="39271-118">Exemplo 2: obter um serviço usando o identificador de recursos.</span><span class="sxs-lookup"><span data-stu-id="39271-118">Example 2: Get a service using the resource identifier.</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerService -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1"
```

<span data-ttu-id="39271-119">Esse comando obtém um serviço denominado ContosoService1 em uma topologia de serviço chamada ContosoServiceTopology no ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="39271-119">This command gets a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="39271-120">Exemplo 3: obter um serviço usando o objeto de serviço.</span><span class="sxs-lookup"><span data-stu-id="39271-120">Example 3: Get a service using the service object.</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerService -Service $serviceObject
```

<span data-ttu-id="39271-121">Esse comando obtém um serviço cujo nome, o nome da topologia de serviço e o nome do contato correspondem às propriedades Name, imtopologyname e ResourceGroupName da $serviceObject, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="39271-121">This command gets a service whose name, service topology name and ResourceGroup match the Name, ServiceTopologyName and ResourceGroupName properties of the $serviceObject, respectively.</span></span>

## <span data-ttu-id="39271-122">OS</span><span class="sxs-lookup"><span data-stu-id="39271-122">PARAMETERS</span></span>

### <span data-ttu-id="39271-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39271-123">-DefaultProfile</span></span>
<span data-ttu-id="39271-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="39271-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39271-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="39271-125">-Name</span></span>
<span data-ttu-id="39271-126">O nome do serviço.</span><span class="sxs-lookup"><span data-stu-id="39271-126">The name of the service.</span></span>

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

### <span data-ttu-id="39271-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39271-127">-ResourceGroupName</span></span>
<span data-ttu-id="39271-128">O grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="39271-128">The resource group.</span></span>

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

### <span data-ttu-id="39271-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="39271-129">-ResourceId</span></span>
<span data-ttu-id="39271-130">O identificador do recurso.</span><span class="sxs-lookup"><span data-stu-id="39271-130">The resource identifier.</span></span>

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

### <span data-ttu-id="39271-131">-Serviço</span><span class="sxs-lookup"><span data-stu-id="39271-131">-Service</span></span>
<span data-ttu-id="39271-132">Objeto de serviço.</span><span class="sxs-lookup"><span data-stu-id="39271-132">Service object.</span></span>

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

### <span data-ttu-id="39271-133">-Outtopology</span><span class="sxs-lookup"><span data-stu-id="39271-133">-ServiceTopology</span></span>
<span data-ttu-id="39271-134">O objeto de topologia de serviço no qual o serviço deve ser criado.</span><span class="sxs-lookup"><span data-stu-id="39271-134">The service topology object in which the service should be created.</span></span>

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

### <span data-ttu-id="39271-135">-Imtopologyname</span><span class="sxs-lookup"><span data-stu-id="39271-135">-ServiceTopologyName</span></span>
<span data-ttu-id="39271-136">O nome da topologia de serviço.</span><span class="sxs-lookup"><span data-stu-id="39271-136">The name of the service topology.</span></span>

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

### <span data-ttu-id="39271-137">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="39271-137">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="39271-138">O identificador de recursos de topologia de serviço no qual o serviço deve ser criado.</span><span class="sxs-lookup"><span data-stu-id="39271-138">The service topology resource identifier in which the service should be created.</span></span>

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

### <span data-ttu-id="39271-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39271-139">CommonParameters</span></span>
<span data-ttu-id="39271-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39271-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39271-141">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39271-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39271-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="39271-142">INPUTS</span></span>

### <span data-ttu-id="39271-143">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="39271-143">None</span></span>

## <span data-ttu-id="39271-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="39271-144">OUTPUTS</span></span>

### <span data-ttu-id="39271-145">Microsoft. Azure. Commands. DeploymentManager. Models. PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="39271-145">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="39271-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="39271-146">NOTES</span></span>

## <span data-ttu-id="39271-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="39271-147">RELATED LINKS</span></span>

[<span data-ttu-id="39271-148">New-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="39271-148">New-AzureRmDeploymentManagerService</span></span>](./New-AzureRmDeploymentManagerService.md)

[<span data-ttu-id="39271-149">Remove-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="39271-149">Remove-AzureRmDeploymentManagerService</span></span>](./Remove-AzureRmDeploymentManagerService.md)

[<span data-ttu-id="39271-150">Set-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="39271-150">Set-AzureRmDeploymentManagerService</span></span>](./Set-AzureRmDeploymentManagerService.md)