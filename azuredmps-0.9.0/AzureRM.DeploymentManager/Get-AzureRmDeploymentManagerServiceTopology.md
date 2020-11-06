---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/get-azurermdeploymentmanagerservicetopology
schema: 2.0.0
ms.openlocfilehash: f5e0b1e0b2e85eb3c17a53b0108e853535712db1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93426190"
---
# <span data-ttu-id="934a3-101">Get-AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="934a3-101">Get-AzureRmDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="934a3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="934a3-102">SYNOPSIS</span></span>
<span data-ttu-id="934a3-103">Obtém uma topologia de serviço.</span><span class="sxs-lookup"><span data-stu-id="934a3-103">Gets a service topology.</span></span>

## <span data-ttu-id="934a3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="934a3-104">SYNTAX</span></span>

### <span data-ttu-id="934a3-105">Interativo (padrão)</span><span class="sxs-lookup"><span data-stu-id="934a3-105">Interactive (Default)</span></span>
```
Get-AzureRmDeploymentManagerServiceTopology [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="934a3-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="934a3-106">ResourceId</span></span>
```
Get-AzureRmDeploymentManagerServiceTopology [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="934a3-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="934a3-107">InputObject</span></span>
```
Get-AzureRmDeploymentManagerServiceTopology [-ServiceTopology] <PSServiceTopologyResource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="934a3-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="934a3-108">DESCRIPTION</span></span>
<span data-ttu-id="934a3-109">O cmdlet **Get-AzureRmDeploymentManagerServiceTopology** Obtém uma topologia de serviço.</span><span class="sxs-lookup"><span data-stu-id="934a3-109">The **Get-AzureRmDeploymentManagerServiceTopology** cmdlet gets a service topology.</span></span>

<span data-ttu-id="934a3-110">Você pode modificar esse objeto localmente e, em seguida, aplicar as alterações à topologia usando o cmdlet Set-AzureRmDeploymentManagerServiceTopology.</span><span class="sxs-lookup"><span data-stu-id="934a3-110">You can modify this object locally, and then apply changes to the topology by using the Set-AzureRmDeploymentManagerServiceTopology cmdlet.</span></span>
<span data-ttu-id="934a3-111">Especifique a topologia do serviço de acordo com o nome e o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="934a3-111">Specify the service topology by its name and the resource group name.</span></span> <span data-ttu-id="934a3-112">Como alternativa, você pode fornecer o objeto imtopology ou o resourceId.</span><span class="sxs-lookup"><span data-stu-id="934a3-112">Alternately, you can provide the ServiceTopology object or the ResourceId.</span></span>

## <span data-ttu-id="934a3-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="934a3-113">EXAMPLES</span></span>

### <span data-ttu-id="934a3-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="934a3-114">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology
```

<span data-ttu-id="934a3-115">Esse comando obtém uma topologia de serviço chamada ContosoServiceTopology no ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="934a3-115">This command gets a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="934a3-116">Exemplo 2: obter uma topologia de serviço usando o identificador de recursos.</span><span class="sxs-lookup"><span data-stu-id="934a3-116">Example 2: Get a service topology using the resource identifier.</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerServiceTopology -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology"
```

<span data-ttu-id="934a3-117">Esse comando obtém uma topologia de serviço chamada ContosoServiceTopology no ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="934a3-117">This command gets a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="934a3-118">Exemplo 3: obter uma topologia de serviço usando o objeto de topologia de serviço.</span><span class="sxs-lookup"><span data-stu-id="934a3-118">Example 3: Get a service topology using the service topology object.</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerService -ServiceTopology $serviceTopologyObject
```

<span data-ttu-id="934a3-119">Esse comando obtém uma topologia de serviço cujo nome e o meu nome de fonte correspondem às propriedades Name e ResourceGroupName do $serviceTopologyObject, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="934a3-119">This command gets a service topology whose name and ResourceGroup match the Name and ResourceGroupName properties of the $serviceTopologyObject, respectively.</span></span>

## <span data-ttu-id="934a3-120">OS</span><span class="sxs-lookup"><span data-stu-id="934a3-120">PARAMETERS</span></span>

### <span data-ttu-id="934a3-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="934a3-121">-DefaultProfile</span></span>
<span data-ttu-id="934a3-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="934a3-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="934a3-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="934a3-123">-Name</span></span>
<span data-ttu-id="934a3-124">O nome da topologia de serviço.</span><span class="sxs-lookup"><span data-stu-id="934a3-124">The name of the service topology.</span></span>

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

### <span data-ttu-id="934a3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="934a3-125">-ResourceGroupName</span></span>
<span data-ttu-id="934a3-126">O grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="934a3-126">The resource group.</span></span>

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

### <span data-ttu-id="934a3-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="934a3-127">-ResourceId</span></span>
<span data-ttu-id="934a3-128">O identificador do recurso.</span><span class="sxs-lookup"><span data-stu-id="934a3-128">The resource identifier.</span></span>

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

### <span data-ttu-id="934a3-129">-Outtopology</span><span class="sxs-lookup"><span data-stu-id="934a3-129">-ServiceTopology</span></span>
<span data-ttu-id="934a3-130">Objeto de recurso de topologia de serviço.</span><span class="sxs-lookup"><span data-stu-id="934a3-130">Service topology resource object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="934a3-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="934a3-131">CommonParameters</span></span>
<span data-ttu-id="934a3-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="934a3-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="934a3-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="934a3-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="934a3-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="934a3-134">INPUTS</span></span>

### <span data-ttu-id="934a3-135">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="934a3-135">None</span></span>

## <span data-ttu-id="934a3-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="934a3-136">OUTPUTS</span></span>

### <span data-ttu-id="934a3-137">Microsoft. Azure. Commands. DeploymentManager. Models. PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="934a3-137">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="934a3-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="934a3-138">NOTES</span></span>

## <span data-ttu-id="934a3-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="934a3-139">RELATED LINKS</span></span>

[<span data-ttu-id="934a3-140">New-AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="934a3-140">New-AzureRmDeploymentManagerServiceTopology</span></span>](./New-AzureRmDeploymentManagerServiceTopology.md)

[<span data-ttu-id="934a3-141">Remove-AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="934a3-141">Remove-AzureRmDeploymentManagerServiceTopology</span></span>](./Remove-AzureRmDeploymentManagerServiceTopology.md)

[<span data-ttu-id="934a3-142">Set-AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="934a3-142">Set-AzureRmDeploymentManagerServiceTopology</span></span>](./Set-AzureRmDeploymentManagerServiceTopology.md)