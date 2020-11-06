---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/get-azurermdeploymentmanagerserviceunit
schema: 2.0.0
ms.openlocfilehash: e83f619bd14a2e0ba2012a206d0c3dffd5204863
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93601705"
---
# <span data-ttu-id="8fc25-101">Get-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="8fc25-101">Get-AzureRmDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="8fc25-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8fc25-102">SYNOPSIS</span></span>
<span data-ttu-id="8fc25-103">Obtém uma unidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="8fc25-103">Gets a service unit.</span></span>

## <span data-ttu-id="8fc25-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8fc25-104">SYNTAX</span></span>

### <span data-ttu-id="8fc25-105">Interativo (padrão)</span><span class="sxs-lookup"><span data-stu-id="8fc25-105">Interactive (Default)</span></span>
```
Get-AzureRmDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-ServiceName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8fc25-106">ByServiceObject</span><span class="sxs-lookup"><span data-stu-id="8fc25-106">ByServiceObject</span></span>
```
Get-AzureRmDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-Name] <String>
 [-Service] <PSServiceResource> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8fc25-107">ByServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="8fc25-107">ByServiceResourceId</span></span>
```
Get-AzureRmDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-Name] <String>
 [-ServiceResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8fc25-108">ByTopologyObjectAndServiceName</span><span class="sxs-lookup"><span data-stu-id="8fc25-108">ByTopologyObjectAndServiceName</span></span>
```
Get-AzureRmDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 [-ServiceTopology] <PSServiceTopologyResource> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8fc25-109">ByTopologyResourceAndServiceName</span><span class="sxs-lookup"><span data-stu-id="8fc25-109">ByTopologyResourceAndServiceName</span></span>
```
Get-AzureRmDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 [-ServiceTopologyResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8fc25-110">Identificação</span><span class="sxs-lookup"><span data-stu-id="8fc25-110">ResourceId</span></span>
```
Get-AzureRmDeploymentManagerServiceUnit [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8fc25-111">InputObject</span><span class="sxs-lookup"><span data-stu-id="8fc25-111">InputObject</span></span>
```
Get-AzureRmDeploymentManagerServiceUnit [-ServiceUnit] <PSServiceUnitResource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8fc25-112">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8fc25-112">DESCRIPTION</span></span>
<span data-ttu-id="8fc25-113">O cmdlet **Get-AzureRmDeploymentManagerServiceUnit** Obtém uma unidade de serviço em um serviço.</span><span class="sxs-lookup"><span data-stu-id="8fc25-113">The **Get-AzureRmDeploymentManagerServiceUnit** cmdlet gets a service unit in a service.</span></span>

<span data-ttu-id="8fc25-114">Especifique a unidade de serviço por nome, o serviço sob o qual ele foi definido, o nome da topologia do serviço e o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8fc25-114">Specify the service unit by its name, the service under which it was defined, the service topology name and the resource group name.</span></span> <span data-ttu-id="8fc25-115">Como alternativa, você pode fornecer o objeto onunit ou o resourceId.</span><span class="sxs-lookup"><span data-stu-id="8fc25-115">Alternately, you can provide the ServiceUnit object or the ResourceId.</span></span>

<span data-ttu-id="8fc25-116">Você pode modificar esse objeto localmente e, em seguida, aplicar as alterações à unidade de serviço usando o cmdlet Set-AzureRmDeploymentManagerServiceUnit.</span><span class="sxs-lookup"><span data-stu-id="8fc25-116">You can modify this object locally, and then apply changes to the service unit by using the Set-AzureRmDeploymentManagerServiceUnit cmdlet.</span></span>

## <span data-ttu-id="8fc25-117">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8fc25-117">EXAMPLES</span></span>

### <span data-ttu-id="8fc25-118">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8fc25-118">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -ServiceName ContosoService1  -Name ContosoService1Storage
```

<span data-ttu-id="8fc25-119">Esse comando obtém uma unidade de serviço chamada ContosoService1Storage em um ContosoService1 de serviço em uma topologia de serviço chamada ContosoServiceTopology no ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="8fc25-119">This command gets a service unit named ContosoService1Storage under a service ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="8fc25-120">Exemplo 2: obter uma unidade de serviço usando o identificador de recursos.</span><span class="sxs-lookup"><span data-stu-id="8fc25-120">Example 2: Get a service unit using the resource identifier.</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerServiceUnit -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1/serviceUnits/ContosoService1Storage"
```

<span data-ttu-id="8fc25-121">Esse comando obtém uma unidade de serviço chamada ContosoService1Storage em um ContosoService1 de serviço em uma topologia de serviço chamada ContosoServiceTopology no ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="8fc25-121">This command gets a service unit named ContosoService1Storage under a service ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="8fc25-122">Exemplo 3: obter uma unidade de serviço usando o objeto de unidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="8fc25-122">Example 3: Get a service unit using the service unit object.</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerServiceUnit -ServiceUnit $serviceUnitObject
```

<span data-ttu-id="8fc25-123">Esse comando obtém uma unidade de serviço cujo nome, nome do serviço, nome da topologia do serviço e o nome da sua topologia correspondem às propriedades Name, ServiceName, Service Topologyname e ResourceGroupName da $serviceUnitObject, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="8fc25-123">This command gets a service unit whose name, service name, service topology name and ResourceGroup match the Name, ServiceName, ServiceTopologyName and ResourceGroupName properties of the $serviceUnitObject, respectively.</span></span>

## <span data-ttu-id="8fc25-124">OS</span><span class="sxs-lookup"><span data-stu-id="8fc25-124">PARAMETERS</span></span>

### <span data-ttu-id="8fc25-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fc25-125">-DefaultProfile</span></span>
<span data-ttu-id="8fc25-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8fc25-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8fc25-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="8fc25-127">-Name</span></span>
<span data-ttu-id="8fc25-128">O nome da unidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="8fc25-128">The name of the service unit.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceObject, ByServiceResourceId, ByTopologyObjectAndServiceName, ByTopologyResourceAndServiceName
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fc25-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8fc25-129">-ResourceGroupName</span></span>
<span data-ttu-id="8fc25-130">O grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8fc25-130">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceObject, ByServiceResourceId, ByTopologyObjectAndServiceName, ByTopologyResourceAndServiceName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fc25-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8fc25-131">-ResourceId</span></span>
<span data-ttu-id="8fc25-132">O identificador do recurso.</span><span class="sxs-lookup"><span data-stu-id="8fc25-132">The resource identifier.</span></span>

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

### <span data-ttu-id="8fc25-133">-Serviço</span><span class="sxs-lookup"><span data-stu-id="8fc25-133">-Service</span></span>
<span data-ttu-id="8fc25-134">O objeto de serviço no qual a unidade de serviço deve ser criada.</span><span class="sxs-lookup"><span data-stu-id="8fc25-134">The service object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="8fc25-135">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="8fc25-135">-ServiceName</span></span>
<span data-ttu-id="8fc25-136">O nome do serviço do qual a unidade de serviço faz parte.</span><span class="sxs-lookup"><span data-stu-id="8fc25-136">The name of the service the service unit is part of.</span></span>

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

### <span data-ttu-id="8fc25-137">-Objectresourceid</span><span class="sxs-lookup"><span data-stu-id="8fc25-137">-ServiceResourceId</span></span>
<span data-ttu-id="8fc25-138">O identificador do recurso de serviço no qual a unidade de serviço deve ser criada.</span><span class="sxs-lookup"><span data-stu-id="8fc25-138">The service resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="8fc25-139">-Outtopology</span><span class="sxs-lookup"><span data-stu-id="8fc25-139">-ServiceTopology</span></span>
<span data-ttu-id="8fc25-140">O objeto de topologia de serviço no qual a unidade de serviço deve ser criada.</span><span class="sxs-lookup"><span data-stu-id="8fc25-140">The service topology object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="8fc25-141">-Imtopologyname</span><span class="sxs-lookup"><span data-stu-id="8fc25-141">-ServiceTopologyName</span></span>
<span data-ttu-id="8fc25-142">O nome da topologia de serviço da qual a unidade de serviço faz parte.</span><span class="sxs-lookup"><span data-stu-id="8fc25-142">The name of the service topology the service unit is part of.</span></span>

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

### <span data-ttu-id="8fc25-143">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="8fc25-143">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="8fc25-144">O identificador de recursos de topologia de serviço no qual a unidade de serviço deve ser criada.</span><span class="sxs-lookup"><span data-stu-id="8fc25-144">The service topology resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="8fc25-145">-Enunidade</span><span class="sxs-lookup"><span data-stu-id="8fc25-145">-ServiceUnit</span></span>
<span data-ttu-id="8fc25-146">Objeto de recurso de unidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="8fc25-146">Service unit resource object.</span></span>

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

### <span data-ttu-id="8fc25-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fc25-147">CommonParameters</span></span>
<span data-ttu-id="8fc25-148">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8fc25-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fc25-149">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8fc25-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fc25-150">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8fc25-150">INPUTS</span></span>

### <span data-ttu-id="8fc25-151">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="8fc25-151">None</span></span>

## <span data-ttu-id="8fc25-152">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8fc25-152">OUTPUTS</span></span>

### <span data-ttu-id="8fc25-153">Microsoft. Azure. Commands. DeploymentManager. Models. PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="8fc25-153">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="8fc25-154">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8fc25-154">NOTES</span></span>

## <span data-ttu-id="8fc25-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8fc25-155">RELATED LINKS</span></span>

[<span data-ttu-id="8fc25-156">New-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="8fc25-156">New-AzureRmDeploymentManagerServiceUnit</span></span>](./New-AzureRmDeploymentManagerServiceUnit.md)

[<span data-ttu-id="8fc25-157">Remove-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="8fc25-157">Remove-AzureRmDeploymentManagerServiceUnit</span></span>](./Remove-AzureRmDeploymentManagerServiceUnit.md)

[<span data-ttu-id="8fc25-158">Set-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="8fc25-158">Set-AzureRmDeploymentManagerServiceUnit</span></span>](./Set-AzureRmDeploymentManagerServiceUnit.md)