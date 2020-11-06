---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerserviceunit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerServiceUnit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerServiceUnit.md
ms.openlocfilehash: 607e094a03d43704057af80266a6f9f2b669d3b1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93601006"
---
# <span data-ttu-id="a8646-101">Get-AzDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="a8646-101">Get-AzDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="a8646-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a8646-102">SYNOPSIS</span></span>
<span data-ttu-id="a8646-103">Obtém a unidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="a8646-103">Gets the service unit.</span></span>

## <span data-ttu-id="a8646-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a8646-104">SYNTAX</span></span>

### <span data-ttu-id="a8646-105">Interativo (padrão)</span><span class="sxs-lookup"><span data-stu-id="a8646-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-ServiceName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a8646-106">ByServiceObject</span><span class="sxs-lookup"><span data-stu-id="a8646-106">ByServiceObject</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-Name] <String>
 [-ServiceObject] <PSServiceResource> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a8646-107">ByServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="a8646-107">ByServiceResourceId</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-Name] <String> [-ServiceResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a8646-108">ByTopologyObjectAndServiceName</span><span class="sxs-lookup"><span data-stu-id="a8646-108">ByTopologyObjectAndServiceName</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 [-ServiceTopologyObject] <PSServiceTopologyResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a8646-109">ByTopologyResourceAndServiceName</span><span class="sxs-lookup"><span data-stu-id="a8646-109">ByTopologyResourceAndServiceName</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 [-ServiceTopologyResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a8646-110">Identificação</span><span class="sxs-lookup"><span data-stu-id="a8646-110">ResourceId</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a8646-111">InputObject</span><span class="sxs-lookup"><span data-stu-id="a8646-111">InputObject</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ServiceUnitObject] <PSServiceUnitResource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a8646-112">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a8646-112">DESCRIPTION</span></span>
<span data-ttu-id="a8646-113">O cmdlet **Get-AzDeploymentManagerServiceUnit** Obtém uma unidade de serviço em um serviço.</span><span class="sxs-lookup"><span data-stu-id="a8646-113">The **Get-AzDeploymentManagerServiceUnit** cmdlet gets a service unit in a service.</span></span>

<span data-ttu-id="a8646-114">Especifique a unidade de serviço por nome, o serviço sob o qual ele foi definido, o nome da topologia do serviço e o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a8646-114">Specify the service unit by its name, the service under which it was defined, the service topology name and the resource group name.</span></span> <span data-ttu-id="a8646-115">Como alternativa, você pode fornecer o objeto onunit ou o resourceId.</span><span class="sxs-lookup"><span data-stu-id="a8646-115">Alternately, you can provide the ServiceUnit object or the ResourceId.</span></span>

<span data-ttu-id="a8646-116">Você pode modificar esse objeto localmente e, em seguida, aplicar as alterações à unidade de serviço usando o cmdlet Set-AzDeploymentManagerServiceUnit.</span><span class="sxs-lookup"><span data-stu-id="a8646-116">You can modify this object locally, and then apply changes to the service unit by using the Set-AzDeploymentManagerServiceUnit cmdlet.</span></span>

## <span data-ttu-id="a8646-117">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a8646-117">EXAMPLES</span></span>

### <span data-ttu-id="a8646-118">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a8646-118">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -ServiceName ContosoService1  -Name ContosoService1Storage
```

<span data-ttu-id="a8646-119">Esse comando obtém uma unidade de serviço chamada ContosoService1Storage em um ContosoService1 de serviço em uma topologia de serviço chamada ContosoServiceTopology no ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="a8646-119">This command gets a service unit named ContosoService1Storage under a service ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="a8646-120">Exemplo 2: obter uma unidade de serviço usando o identificador de recursos.</span><span class="sxs-lookup"><span data-stu-id="a8646-120">Example 2: Get a service unit using the resource identifier.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceUnit -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1/serviceUnits/ContosoService1Storage"
```

<span data-ttu-id="a8646-121">Esse comando obtém uma unidade de serviço chamada ContosoService1Storage em um ContosoService1 de serviço em uma topologia de serviço chamada ContosoServiceTopology no ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="a8646-121">This command gets a service unit named ContosoService1Storage under a service ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="a8646-122">Exemplo 3: obter uma unidade de serviço usando o objeto de unidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="a8646-122">Example 3: Get a service unit using the service unit object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceUnit -InputObject $serviceUnitObject
```

<span data-ttu-id="a8646-123">Esse comando obtém uma unidade de serviço cujo nome, nome do serviço, nome da topologia do serviço e o nome da sua topologia correspondem às propriedades Name, ServiceName, Service Topologyname e ResourceGroupName da $serviceUnitObject, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="a8646-123">This command gets a service unit whose name, service name, service topology name and ResourceGroup match the Name, ServiceName, ServiceTopologyName and ResourceGroupName properties of the $serviceUnitObject, respectively.</span></span>

## <span data-ttu-id="a8646-124">OS</span><span class="sxs-lookup"><span data-stu-id="a8646-124">PARAMETERS</span></span>

### <span data-ttu-id="a8646-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8646-125">-DefaultProfile</span></span>
<span data-ttu-id="a8646-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a8646-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a8646-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="a8646-127">-Name</span></span>
<span data-ttu-id="a8646-128">O nome da unidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="a8646-128">The name of the service unit.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceObject, ByServiceResourceId, ByTopologyObjectAndServiceName, ByTopologyResourceAndServiceName
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8646-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8646-129">-ResourceGroupName</span></span>
<span data-ttu-id="a8646-130">O grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a8646-130">The resource group.</span></span>

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

### <span data-ttu-id="a8646-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a8646-131">-ResourceId</span></span>
<span data-ttu-id="a8646-132">O identificador do recurso.</span><span class="sxs-lookup"><span data-stu-id="a8646-132">The resource identifier.</span></span>

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

### <span data-ttu-id="a8646-133">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="a8646-133">-ServiceName</span></span>
<span data-ttu-id="a8646-134">O nome do serviço do qual a unidade de serviço faz parte.</span><span class="sxs-lookup"><span data-stu-id="a8646-134">The name of the service the service unit is part of.</span></span>

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

### <span data-ttu-id="a8646-135">-ServiceObject</span><span class="sxs-lookup"><span data-stu-id="a8646-135">-ServiceObject</span></span>
<span data-ttu-id="a8646-136">O objeto de serviço no qual a unidade de serviço deve ser criada.</span><span class="sxs-lookup"><span data-stu-id="a8646-136">The service object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="a8646-137">-Objectresourceid</span><span class="sxs-lookup"><span data-stu-id="a8646-137">-ServiceResourceId</span></span>
<span data-ttu-id="a8646-138">O identificador do recurso de serviço no qual a unidade de serviço deve ser criada.</span><span class="sxs-lookup"><span data-stu-id="a8646-138">The service resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="a8646-139">-Imtopologyname</span><span class="sxs-lookup"><span data-stu-id="a8646-139">-ServiceTopologyName</span></span>
<span data-ttu-id="a8646-140">O nome da topologia de serviço da qual a unidade de serviço faz parte.</span><span class="sxs-lookup"><span data-stu-id="a8646-140">The name of the service topology the service unit is part of.</span></span>

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

### <span data-ttu-id="a8646-141">-Imtopologyobject</span><span class="sxs-lookup"><span data-stu-id="a8646-141">-ServiceTopologyObject</span></span>
<span data-ttu-id="a8646-142">O objeto de topologia de serviço no qual a unidade de serviço deve ser criada.</span><span class="sxs-lookup"><span data-stu-id="a8646-142">The service topology object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="a8646-143">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="a8646-143">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="a8646-144">O identificador de recursos de topologia de serviço no qual a unidade de serviço deve ser criada.</span><span class="sxs-lookup"><span data-stu-id="a8646-144">The service topology resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="a8646-145">-Reunitobject</span><span class="sxs-lookup"><span data-stu-id="a8646-145">-ServiceUnitObject</span></span>
<span data-ttu-id="a8646-146">Objeto de recurso de unidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="a8646-146">Service unit resource object.</span></span>

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

### <span data-ttu-id="a8646-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8646-147">CommonParameters</span></span>
<span data-ttu-id="a8646-148">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8646-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8646-149">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8646-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8646-150">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a8646-150">INPUTS</span></span>

### <span data-ttu-id="a8646-151">System. String</span><span class="sxs-lookup"><span data-stu-id="a8646-151">System.String</span></span>

### <span data-ttu-id="a8646-152">Microsoft. Azure. Commands. DeploymentManager. Models. PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="a8646-152">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="a8646-153">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a8646-153">OUTPUTS</span></span>

### <span data-ttu-id="a8646-154">Microsoft. Azure. Commands. DeploymentManager. Models. PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="a8646-154">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="a8646-155">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a8646-155">NOTES</span></span>

## <span data-ttu-id="a8646-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a8646-156">RELATED LINKS</span></span>
