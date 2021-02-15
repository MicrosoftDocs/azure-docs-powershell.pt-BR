---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerserviceunit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerServiceUnit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerServiceUnit.md
ms.openlocfilehash: f80f67270652d9c9edef38c9eb793074acd95a27
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115353"
---
# <span data-ttu-id="51ab9-101">Get-AzDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="51ab9-101">Get-AzDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="51ab9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="51ab9-102">SYNOPSIS</span></span>
<span data-ttu-id="51ab9-103">Obtém a unidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="51ab9-103">Gets the service unit.</span></span>

## <span data-ttu-id="51ab9-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="51ab9-104">SYNTAX</span></span>

### <span data-ttu-id="51ab9-105">Interativo (Padrão)</span><span class="sxs-lookup"><span data-stu-id="51ab9-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-ServiceName] <String> [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="51ab9-106">ByServiceObject</span><span class="sxs-lookup"><span data-stu-id="51ab9-106">ByServiceObject</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [[-Name] <String>]
 [-ServiceObject] <PSServiceResource> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="51ab9-107">ByServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="51ab9-107">ByServiceResourceId</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [[-Name] <String>]
 [-ServiceResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="51ab9-108">ByTopologyObjectAndServiceName</span><span class="sxs-lookup"><span data-stu-id="51ab9-108">ByTopologyObjectAndServiceName</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [[-Name] <String>]
 [-ServiceTopologyObject] <PSServiceTopologyResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="51ab9-109">ByTopologyResourceAndServiceName</span><span class="sxs-lookup"><span data-stu-id="51ab9-109">ByTopologyResourceAndServiceName</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [[-Name] <String>]
 [-ServiceTopologyResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="51ab9-110">Resourceid</span><span class="sxs-lookup"><span data-stu-id="51ab9-110">ResourceId</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="51ab9-111">Inputobject</span><span class="sxs-lookup"><span data-stu-id="51ab9-111">InputObject</span></span>
```
Get-AzDeploymentManagerServiceUnit [-InputObject] <PSServiceUnitResource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="51ab9-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="51ab9-112">DESCRIPTION</span></span>
<span data-ttu-id="51ab9-113">O cmdlet **Get-AzDeploymentManagerServiceUnit obtém** uma unidade de serviço em um serviço.</span><span class="sxs-lookup"><span data-stu-id="51ab9-113">The **Get-AzDeploymentManagerServiceUnit** cmdlet gets a service unit in a service.</span></span>

<span data-ttu-id="51ab9-114">Especifique a unidade de serviço pelo nome, o serviço no qual ela foi definida, o nome da topologia do serviço e o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="51ab9-114">Specify the service unit by its name, the service under which it was defined, the service topology name and the resource group name.</span></span> <span data-ttu-id="51ab9-115">Como alternativa, você pode fornecer o objeto ServiceUnit ou o ResourceId.</span><span class="sxs-lookup"><span data-stu-id="51ab9-115">Alternately, you can provide the ServiceUnit object or the ResourceId.</span></span>

<span data-ttu-id="51ab9-116">Você pode modificar esse objeto localmente e aplicar alterações à unidade de serviço usando o cmdlet Set-AzDeploymentManagerServiceUnit usuário.</span><span class="sxs-lookup"><span data-stu-id="51ab9-116">You can modify this object locally, and then apply changes to the service unit by using the Set-AzDeploymentManagerServiceUnit cmdlet.</span></span>

## <span data-ttu-id="51ab9-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="51ab9-117">EXAMPLES</span></span>

### <span data-ttu-id="51ab9-118">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="51ab9-118">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -ServiceName ContosoService1  -Name ContosoService1Storage
```

<span data-ttu-id="51ab9-119">Esse comando obtém uma unidade de serviço chamada ContosoService1Storage sob um serviço ContosoService1 em uma topologia de serviço chamada ContosoServiceTopology no Grupo ContosoResource.</span><span class="sxs-lookup"><span data-stu-id="51ab9-119">This command gets a service unit named ContosoService1Storage under a service ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="51ab9-120">Exemplo 2: Obter uma unidade de serviço usando o identificador de recurso.</span><span class="sxs-lookup"><span data-stu-id="51ab9-120">Example 2: Get a service unit using the resource identifier.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceUnit -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1/serviceUnits/ContosoService1Storage"
```

<span data-ttu-id="51ab9-121">Esse comando obtém uma unidade de serviço chamada ContosoService1Storage sob um serviço ContosoService1 em uma topologia de serviço chamada ContosoServiceTopology no Grupo ContosoResource.</span><span class="sxs-lookup"><span data-stu-id="51ab9-121">This command gets a service unit named ContosoService1Storage under a service ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="51ab9-122">Exemplo 3: Obter uma unidade de serviço usando o objeto da unidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="51ab9-122">Example 3: Get a service unit using the service unit object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceUnit -InputObject $serviceUnitObject
```

<span data-ttu-id="51ab9-123">Esse comando obtém uma unidade de serviço cujo nome, nome do serviço, nome da topologia do serviço e Grupo de Recursos corresponderem às propriedades Nome, NomedoAtendado, ServiceTopologyName e ResourceGroupName do $serviceUnitObject, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="51ab9-123">This command gets a service unit whose name, service name, service topology name and ResourceGroup match the Name, ServiceName, ServiceTopologyName and ResourceGroupName properties of the $serviceUnitObject, respectively.</span></span>

## <span data-ttu-id="51ab9-124">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="51ab9-124">PARAMETERS</span></span>

### <span data-ttu-id="51ab9-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51ab9-125">-DefaultProfile</span></span>
<span data-ttu-id="51ab9-126">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="51ab9-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="51ab9-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="51ab9-127">-InputObject</span></span>
<span data-ttu-id="51ab9-128">Objeto de recurso da unidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="51ab9-128">Service unit resource object.</span></span>

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

### <span data-ttu-id="51ab9-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="51ab9-129">-Name</span></span>
<span data-ttu-id="51ab9-130">O nome da unidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="51ab9-130">The name of the service unit.</span></span>

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

### <span data-ttu-id="51ab9-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51ab9-131">-ResourceGroupName</span></span>
<span data-ttu-id="51ab9-132">O grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="51ab9-132">The resource group.</span></span>

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

### <span data-ttu-id="51ab9-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="51ab9-133">-ResourceId</span></span>
<span data-ttu-id="51ab9-134">O identificador de recurso.</span><span class="sxs-lookup"><span data-stu-id="51ab9-134">The resource identifier.</span></span>

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

### <span data-ttu-id="51ab9-135">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="51ab9-135">-ServiceName</span></span>
<span data-ttu-id="51ab9-136">O nome do serviço do serviço do que a unidade de serviço faz parte.</span><span class="sxs-lookup"><span data-stu-id="51ab9-136">The name of the service the service unit is part of.</span></span>

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

### <span data-ttu-id="51ab9-137">-ServiceObject</span><span class="sxs-lookup"><span data-stu-id="51ab9-137">-ServiceObject</span></span>
<span data-ttu-id="51ab9-138">O objeto de serviço no qual a unidade de serviço deve ser criada.</span><span class="sxs-lookup"><span data-stu-id="51ab9-138">The service object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="51ab9-139">-ServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="51ab9-139">-ServiceResourceId</span></span>
<span data-ttu-id="51ab9-140">O identificador de recurso de serviço no qual a unidade de serviço deve ser criada.</span><span class="sxs-lookup"><span data-stu-id="51ab9-140">The service resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="51ab9-141">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="51ab9-141">-ServiceTopologyName</span></span>
<span data-ttu-id="51ab9-142">O nome da topologia de serviço da unidade de serviço faz parte.</span><span class="sxs-lookup"><span data-stu-id="51ab9-142">The name of the service topology the service unit is part of.</span></span>

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

### <span data-ttu-id="51ab9-143">-ServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="51ab9-143">-ServiceTopologyObject</span></span>
<span data-ttu-id="51ab9-144">O objeto de topologia de serviço no qual a unidade de serviço deve ser criada.</span><span class="sxs-lookup"><span data-stu-id="51ab9-144">The service topology object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="51ab9-145">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="51ab9-145">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="51ab9-146">O identificador de recurso de topologia de serviço no qual a unidade de serviço deve ser criada.</span><span class="sxs-lookup"><span data-stu-id="51ab9-146">The service topology resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="51ab9-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51ab9-147">CommonParameters</span></span>
<span data-ttu-id="51ab9-148">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51ab9-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51ab9-149">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="51ab9-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51ab9-150">Entradas</span><span class="sxs-lookup"><span data-stu-id="51ab9-150">INPUTS</span></span>

### <span data-ttu-id="51ab9-151">System.String</span><span class="sxs-lookup"><span data-stu-id="51ab9-151">System.String</span></span>

### <span data-ttu-id="51ab9-152">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceunitResource</span><span class="sxs-lookup"><span data-stu-id="51ab9-152">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="51ab9-153">Saídas</span><span class="sxs-lookup"><span data-stu-id="51ab9-153">OUTPUTS</span></span>

### <span data-ttu-id="51ab9-154">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceunitResource</span><span class="sxs-lookup"><span data-stu-id="51ab9-154">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="51ab9-155">Notas</span><span class="sxs-lookup"><span data-stu-id="51ab9-155">NOTES</span></span>

## <span data-ttu-id="51ab9-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="51ab9-156">RELATED LINKS</span></span>
